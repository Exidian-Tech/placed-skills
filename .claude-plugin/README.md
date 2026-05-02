<div align="center">

# Placed Skills for Claude Code & Cursor

### Your AI job search co-pilot — built into the IDE you already use

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Works With Claude Code](https://img.shields.io/badge/Works%20With-Claude%20Code-8A2BE2)](https://claude.ai/code)
[![Works With Cursor](https://img.shields.io/badge/Works%20With-Cursor-000000)](https://cursor.sh)
[![MCP Powered](https://img.shields.io/badge/MCP-Powered-0080FF)](https://modelcontextprotocol.io)
[![Platform](https://img.shields.io/badge/Platform-Placed-10B981)](https://placed.exidian.tech)
[![ClawHub](https://img.shields.io/badge/ClawHub-Published-7C3AED)](https://clawhub.io)
[![26 AI Tools](https://img.shields.io/badge/Tools-26%20AI%20Tools-FF6B6B)](https://placed.exidian.tech)

**Stop copy-pasting your resume into ChatGPT.<br>
Start landing interviews without leaving your terminal.**

[Get Started](#-quickstart) · [See All Tools](#-tools-at-a-glance) · [Example Prompts](#-what-you-can-say) · [Platform](https://placed.exidian.tech)

</div>

---

> **Keywords:** AI resume builder · ATS checker · ATS optimizer · Claude Code skills · ClawHub skills · Cursor MCP · job search AI · AI interview coach · cover letter AI generator · salary negotiation AI · job application tracker · resume AI · MCP tools · career AI · Claude MCP · AI job hunting · AI career coach · resume keyword optimizer · AI mock interview · job pipeline tracker

---

## The Problem With Job Searching in 2025

> **75% of resumes never reach a human.** ATS systems reject them automatically before anyone reads a single word.

Job hunting is broken:

- You spend 2 hours tailoring your resume for one role — then do it 50 more times.
- You fail interviews because you prepped for the wrong questions.
- You accept an underpaid offer because you had no idea what the market rate was.
- You lose track of 20 open applications across spreadsheets and sticky notes.

**Placed Skills gives you a full AI career team inside Claude Code or Cursor** — resume writer, ATS checker, interview coach, salary advisor, job tracker, cover letter generator, LinkedIn optimizer, and more. 26 tools. Zero tab-switching.

---

## What You Get

```
"Optimize my resume for this Staff Engineer role at Stripe"
```

Claude reads the job description, finds keyword gaps, rewrites your bullets, and returns a match score — in under 10 seconds.

```
"Start a mock interview for Senior SWE at Google, hard difficulty"
```

Company-specific questions. Scored answers after every response. A model answer showing exactly what "great" looks like.

```
"I got an offer for $180K. My target is $210K. Write me a negotiation script."
```

Full script with email template, talking points, and line-by-line guidance — ready to copy and send.

**This is what having an expert AI career coach in your terminal looks like.**

---

## Quickstart

**Step 1** — Sign up at [placed.exidian.tech](https://placed.exidian.tech) and grab your API key from **Settings → API Keys**.

**Step 2** — Save your key:

```bash
mkdir -p ~/.config/placed
echo "export PLACED_API_KEY=your-api-key-here" > ~/.config/placed/credentials
```

**Step 3** — Install:

```bash
# Claude Code plugin marketplace (recommended)
/plugin marketplace add Exidian-Tech/placed-skills
/plugin install placed@placed-skills
```

Or via ClawHub (Claude Code, Cursor, Cline, Continue.dev):

```bash
npm i -g clawhub
clawhub install placed-resume-builder
clawhub install placed-interview-coach
clawhub install placed-career-tools
clawhub install placed-resume-optimizer
clawhub install placed-job-tracker
```

Or manual:

```bash
git clone https://github.com/Exidian-Tech/placed-skills
cp -R placed-skills/skills/placed-resume-builder ~/.claude/skills/
cp -R placed-skills/skills/placed-interview-coach ~/.claude/skills/
cp -R placed-skills/skills/placed-career-tools ~/.claude/skills/
cp -R placed-skills/skills/placed-resume-optimizer ~/.claude/skills/
cp -R placed-skills/skills/placed-job-tracker ~/.claude/skills/
```

**Step 4** — Start:

```
"Create a resume targeting Senior Backend Engineer roles"
```

---

## Tools at a Glance

### Resume Builder — 12 AI Tools

Build, edit, template-switch, and export professional resumes without leaving your terminal.

| What you say | What happens |
|---|---|
| "Create a resume for Staff Engineer roles" | New AI resume from your profile, optimized for the target role |
| "Switch to a modern ATS-friendly template" | Browse 37 templates, apply instantly — content preserved |
| "Export my resume as PDF" | Shareable download link in 5 seconds |
| "Add my new job at Acme Corp to my resume" | Experience section updated |
| "Export my resume as Markdown" | Clean output for portfolios or GitHub |

**All 12 tools:** `create_resume` · `get_resume` · `update_resume` · `list_resumes` · `get_resume_schema` · `list_resume_templates` · `get_template_preview` · `change_resume_template` · `get_resume_pdf_url` · `get_resume_docx_url` · `export_resume_json` · `export_resume_markdown`

---

### ATS Resume Optimizer — 7 AI Tools

> The average job posting gets **250+ applications.** ATS filters 75% before a human ever reads one. These tools help you be in the 25%.

| What you say | What happens |
|---|---|
| "Check my ATS score" | Instant ATS compatibility score + every issue flagged with fixes |
| "How well does my resume match this job description?" | Match score, matched keywords, missing keywords, apply recommendation |
| "Optimize my resume for this role" | AI rewrites bullets, adds missing keywords, improves structure |
| "Improve this bullet: 'Led team to improve performance'" | Impact-driven version with metrics, action verbs, scale |
| "What keywords am I missing for this JD?" | Critical gaps vs. nice-to-have, with priority ranking |

**All 7 tools:** `check_ats_compatibility` · `get_resume_quality_score` · `match_job` · `analyze_resume_gaps` · `optimize_resume_for_job` · `optimize_resume_section` · `improve_bullet_point`

---

### AI Interview Coach — 8 Tools

> Most candidates prep for generic questions. The ones who get offers prep for *company-specific* ones.

| What you say | What happens |
|---|---|
| "Start a mock interview for Senior SWE at Stripe, hard mode" | Tailored questions, scored responses, model answers |
| "Give me system design practice — design Twitter's feed" | Full case prompts across 13 real-world system design scenarios |
| "What behavioral questions should I prep for a leadership role?" | STAR-format questions with what interviewers actually look for |
| "Save my leadership story to my answer bank" | STAR story stored, reusable across all future interviews |

**13 system design cases:** URL shortener · Real-time chat · News feed · Video streaming · Ride-sharing · Photo sharing · Search autocomplete · Distributed cache · Rate limiter · E-commerce · Payment processing · Notification system · File storage

**All 8 tools:** `start_interview_session` · `continue_interview_session` · `get_interview_feedback` · `list_interview_cases` · `start_system_design` · `get_behavioral_questions` · `save_story_to_bank` · `get_interview_questions`

---

### Career Tools — Cover Letters, Salary, LinkedIn — 12 Tools

Everything else you need to run a modern, AI-powered job search.

| What you say | What happens |
|---|---|
| "Generate a cover letter for my Airbnb application" | Tailored cover letter from your resume + the job description |
| "What does Stripe pay Staff Engineers in Amsterdam?" | Salary range with real market data |
| "Research Stripe's interview process" | Company overview, culture signals, interview patterns |
| "Optimize my LinkedIn headline and About section" | AI-written LinkedIn profile from your resume |
| "I got $180K, I want $210K — write my negotiation script" | Script with email template + talking points |

**All 12 tools:** `generate_cover_letter` · `generate_linkedin_profile` · `research_company` · `get_company_salary_data` · `get_interview_questions` · `generate_salary_negotiation_script` · `analyze_offer` · `match_job` · `analyze_resume_gaps` · `optimize_resume_for_job` · `add_job_application` · `list_job_applications`

---

### Job Tracker — 5 Tools

Your full application pipeline in plain English. No spreadsheets. No Notion boards.

| What you say | What happens |
|---|---|
| "I just applied to Stripe for Senior Engineer" | Application added with status `APPLIED` |
| "Move my Stripe application to INTERVIEWING" | Status updated instantly |
| "Show me all my INTERVIEWING applications" | Filtered pipeline view |
| "Give me my job search analytics for the last 30 days" | Conversion rates, response rates, pipeline health |

**Pipeline stages:** `WISHLIST` → `APPLIED` → `INTERVIEWING` → `OFFER` → `REJECTED` / `WITHDRAWN`

**All 5 tools:** `add_job_application` · `list_job_applications` · `update_job_status` · `delete_job_application` · `get_application_analytics`

---

## What You Can Say

No commands to memorize. Just talk to Claude:

```
"Create a resume targeting Staff Engineer roles at Series B startups"

"Check my ATS score and tell me exactly what to fix"

"My match score for this role is 62%. What keywords am I missing?"

"Start a hard system design mock interview — design Netflix's recommendation engine"

"I have a Google interview next week. Top behavioral questions they ask?"

"I just applied to Shopify for Product Engineer — add it to my tracker."

"What's competitive pay for a Staff Engineer in London with 8 years experience?"

"Generate a cover letter for Airbnb. Tone: enthusiastic."

"Export my resume as a Word document to share with a recruiter."

"How many applications do I have in the INTERVIEWING stage?"
```

---

## Why This Beats Generic AI for Job Hunting

| | ChatGPT / Claude.ai | Placed Skills (Claude Code + Cursor) |
|---|---|---|
| Resume editing | Copy-paste every session | Direct API — edits persist across sessions |
| ATS scoring | Generic tips | Real score with specific formatting fixes |
| Interview prep | Generic questions | Company-specific, scored, with model answers |
| Job tracking | None | Full pipeline with conversion analytics |
| Cover letters | Generic | Tailored to your resume + specific JD |
| Salary data | Often hallucinated | Real market data by role + location |
| LinkedIn optimizer | Manual copy-paste | Writes directly from your resume |
| Works in your IDE | No (browser only) | Yes — no context switching |
| Resume templates | No | 37 professional templates with ATS scores |

---

## IDE & Client Support

### Claude Code

Skills activate **automatically** when you describe career tasks — no slash commands needed.

```bash
/plugin install placed@placed-skills
```

### Cursor

Add to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "placed": {
      "command": "npx",
      "args": ["-y", "@exidian/placed-mcp"],
      "env": {
        "PLACED_API_KEY": "your-api-key-here"
      }
    }
  }
}
```

### Other MCP Clients

Works with any MCP-compatible client: **Claude Desktop** · **Cline** · **Continue.dev** · **Zed** · **Windsurf** · **Goose** · **ClawBot**

---

## Architecture

Built on the [ClawHub](https://clawhub.io) progressive disclosure skill format:

```
skills/
├── placed-resume-builder/      # 12 resume management tools
│   ├── SKILL.md                # Activates on resume conversations
│   └── references/api-guide.md # Full API reference, loaded only when needed
├── placed-resume-optimizer/    # 7 ATS + keyword optimization tools
├── placed-interview-coach/     # 8 interview prep + system design tools
├── placed-career-tools/        # Cover letters, salary, LinkedIn, research
└── placed-job-tracker/         # Application pipeline (no MCP needed — curl-based)
```

Skills load **only when relevant** — zero overhead when you're coding.

---

## Privacy & Security

- API key stored locally at `~/.config/placed/credentials` — never in code or git
- All API calls go directly to `placed.exidian.tech` — no intermediary servers
- No resume data stored by this skills package
- Privacy policy: [placed.exidian.tech/privacy](https://placed.exidian.tech/privacy)

---

## Contributing

Found a bug, wrong parameter, or want to add a tool? Open an issue or PR.

```bash
git clone https://github.com/Exidian-Tech/placed-skills
# Skills live in skills/<skill-name>/SKILL.md + references/api-guide.md
```

Follow the [ClawHub skill format](https://clawhub.io/docs/skills). PRs welcome.

---

## Links

- **Placed platform:** [placed.exidian.tech](https://placed.exidian.tech)
- **MCP npm package:** [@exidian/placed-mcp](https://www.npmjs.com/package/@exidian/placed-mcp)
- **MCP server source:** [github.com/Exidian-Tech/placed-mcp](https://github.com/Exidian-Tech/placed-mcp)
- **ClawHub listing:** [clawhub.io/skills/placed-resume-builder](https://clawhub.io/skills/placed-resume-builder)
- **API docs:** [placed.exidian.tech/docs](https://placed.exidian.tech/docs)

---

<div align="center">

**Built by [Exidian Technologies](https://exidian.tech) · MIT License**

*If Placed Skills helped your job search, give it a ⭐ — it helps other developers find it.*

**Share this:**
[Twitter/X](https://twitter.com/intent/tweet?text=Just%20added%20an%20AI%20career%20coach%20to%20Claude%20Code%20%F0%9F%A4%AF%0A%0AResume%20ATS%20optimization%2C%20mock%20interviews%2C%20salary%20negotiation%2C%20cover%20letters%20%E2%80%94%20all%20in%20the%20terminal.%0A%0A26%20AI%20tools%20via%20%40ExidianTech%27s%20Placed%20Skills%3A%20https%3A%2F%2Fgithub.com%2FExidian-Tech%2Fplaced-skills) ·
[LinkedIn](https://www.linkedin.com/sharing/share-offsite/?url=https%3A%2F%2Fgithub.com%2FExidian-Tech%2Fplaced-skills)

</div>
