---
name: placed-resume-sync
description: >
  Upload an existing resume file to Placed, or build a resume from a LinkedIn URL.
  Run this before placed-job-agent if the candidate profile is empty or stale.
triggers:
  - sync my resume to placed
  - upload resume to placed
  - build resume in placed
  - my resume to placed
  - import resume
allowed-tools:
  - mcp__placed-mcp__*
  - Bash
---

# placed-resume-sync

Gets the user's resume into Placed so the job agent has a real profile to work with.
Two paths: file upload or LinkedIn import. Ask the user which they want if not specified.

---

## Path A: Upload Resume File

Use when the user has a local resume file (PDF, DOCX, or plain text).

1. Ask for the file path if not provided: "What's the path to your resume file?"
2. Verify the file exists: `ls -lh <path>` — if missing, tell the user and stop.
3. Call `upload_resume(candidate_id='me', file_path=<path>)`
4. On success, call `get_candidate_profile('me')` to confirm the profile was populated.
5. Show a summary of what was extracted: name, skills, experience, target roles.

Supported formats: PDF, DOCX, TXT. If the user gives something else, warn them it may not parse correctly.

---

## Path B: Build from LinkedIn URL

Use when the user provides a LinkedIn profile URL.

1. Confirm the URL looks valid: starts with `https://linkedin.com/in/` or `https://www.linkedin.com/in/`
2. Call `import_from_linkedin(candidate_id='me', linkedin_url=<url>)`
3. LinkedIn import can be slow — tell the user "Importing from LinkedIn, this may take 15-30 seconds..."
4. On success, call `get_candidate_profile('me')` to confirm the profile was populated.
5. Show a summary of what was extracted.

Note: LinkedIn import depends on the user's profile being public, or Placed having OAuth access.
If the import fails with an auth error, suggest Path A (file upload) as fallback.

---

## After Sync

Once the profile is populated, always offer to run the job agent:
"Profile synced. Want me to search for matching jobs now?"

If yes, hand off to placed-job-agent (Step 2 onwards — skip Step 1 since profile was just fetched).

---

## Pitfalls

- Stale profile: if the user says "my resume is outdated in Placed", run this skill to overwrite it.
- Large PDF files (>5MB): warn the user the upload may be slow.
- LinkedIn rate limiting: if import fails with 429 or similar, wait 60 seconds and retry once.
- Never assume the profile is correct after upload — always verify with get_candidate_profile.

---

## Verification

After sync:
- [ ] File exists / LinkedIn URL is valid
- [ ] Upload or import call succeeded (no error)
- [ ] get_candidate_profile returned non-empty data
- [ ] Summary shown to user
