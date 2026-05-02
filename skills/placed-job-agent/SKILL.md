---
name: placed-job-agent
description: >
  Autonomous job search, ranking, application, and tracking using Placed MCP tools.
  Orchestrates the full job search lifecycle: profile fetch → search → rank → shortlist → apply (with confirmation) → track.
triggers:
  - find me jobs
  - job search
  - apply to jobs
  - track my applications
  - what jobs match my profile
  - apply to top N jobs
  - autonomous job search
  - manage my job search
allowed-tools:
  - mcp__placed-mcp__*
  - Bash
---

# placed-job-agent

Autonomous job search agent for Placed. Runs the full lifecycle end-to-end.
Never skip the confirmation gate before applying — that's non-negotiable.

---

## Step 1: Get Candidate Profile

Call `get_candidate_profile('me')` first. Always. Even if the user just told you their background.
The profile is the source of truth for match scoring and application data.

Extract from the response:
- Target roles / job titles
- Preferred locations (and remote preference)
- Tech stack / skills
- Compensation expectations (if present)
- Years of experience / seniority level

If the profile is empty or incomplete, tell the user and offer to run placed-resume-sync first.

---

## Step 2: Search Jobs

Call `search_jobs()` with parameters derived from the candidate profile.
Use the user's stated criteria if they gave any in the trigger message — those override profile defaults.

Parameters to pass (use what's available):
- `role` — job title / function
- `location` — city or country; pass `remote=true` if user wants remote
- `stack` — key technologies from profile
- `salary_min` — from compensation expectations if present

Fetch at least 20 results to have enough to rank meaningfully.

---

## Step 3: Rank by Match Score

For the top 10 results by raw relevance, call `get_match_score('me', job_id)` for each.
Do these calls in parallel where the MCP server allows it.

Build a ranked list sorted by match score descending.
Attach to each entry: job_id, company, role title, location, match score, and a one-line reason for the score.

---

## Step 4: Present Shortlist

Show the user the top 5 matches in a clean table:

  Rank | Company | Role | Location | Match Score | Why
  -----|---------|------|----------|-------------|----
  1    | ...     | ...  | ...      | 94%         | Strong Python + SRE overlap, remote-friendly

After the table, ask: "Which of these would you like to apply to? (list numbers, or 'all top 3', or 'none')"

Do not proceed to Step 5 until the user responds.

---

## Step 5: Apply — WITH EXPLICIT CONFIRMATION

For each job the user selected, show a confirmation prompt before calling apply_to_job:

  Apply to [Company] for [Role]? ([Match Score] match)
  Location: [location] | [job URL or ID]
  (yes / no / skip)

Only call `apply_to_job('me', job_id)` after receiving an explicit "yes" for that specific job.
Never batch-apply without per-job confirmation.
If the user says "apply to all" — still confirm each one individually. No exceptions.

---

## Step 6: Track Applications

After each successful apply_to_job call, immediately call `track_application()` with the job_id and status.

At the end, print a summary:

  Applied: N jobs
  Tracked: N applications
  Pending review: [any that were skipped]

If the user asks "track my applications" without applying first, call `track_application()` with no job_id
(or list mode if the API supports it) to fetch current application statuses and display them.

---

## Pitfalls

- Empty profile: if get_candidate_profile returns nothing useful, stop and run placed-resume-sync first.
- Match score API rate limits: if parallel calls fail, fall back to sequential.
- apply_to_job failure: log the error, skip that job, continue with the rest. Report failures at the end.
- Never invent job_ids. Only use IDs returned by search_jobs or get_match_score.
- If the user says "just apply to everything" — still confirm each job. The confirmation gate is a product requirement, not a suggestion.

---

## Verification

After the full run, confirm:
- [ ] Profile was fetched (not assumed)
- [ ] At least 10 jobs were scored
- [ ] Top 5 were shown before any apply call
- [ ] Every apply had explicit per-job confirmation
- [ ] Every applied job was tracked
