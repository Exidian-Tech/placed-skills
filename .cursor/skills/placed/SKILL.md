---
name: placed
description: This skill should be used when the user wants to "build a resume", "create a resume", "track job applications", "practice interview", "mock interview", "optimize resume for job", "generate cover letter", "check ATS score", "improve resume bullets", "get salary insights", "negotiate salary", "research company", "generate LinkedIn profile", "STAR stories", "system design interview", or wants to use any AI career tool from the Placed platform at placed.exidian.tech.
version: 1.0.0
homepage: https://placed.exidian.tech
---

# Placed — AI Career Platform

Full integration with the Placed career platform (https://placed.exidian.tech). Covers resume management, interview coaching, job tracking, ATS optimization, cover letters, LinkedIn optimization, salary tools, and company research.

## Overview

Placed is an AI career platform with 47+ tools covering the full job search lifecycle. This skill provides access to all tools via the Placed MCP server.

## Prerequisites

1. Create an account at https://placed.exidian.tech
2. Get your API key from Settings → API Keys
3. Add the Placed MCP server to your Cursor MCP config (`~/.cursor/mcp.json` or project `.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "placed": {
      "command": "npx",
      "args": ["-y", "@exidian/placed-mcp"],
      "env": {
        "PLACED_API_KEY": "your-api-key-here",
        "PLACED_BASE_URL": "https://placed.exidian.tech"
      }
    }
  }
}
```

## Resume Builder Tools

| Tool | Description |
|------|-------------|
| `create_resume` | Create a new resume from profile or scratch |
| `get_resume` | Retrieve a resume by ID |
| `update_resume` | Update any section (experience, skills, education, etc.) |
| `list_resumes` | List all resumes |
| `get_resume_schema` | Get full schema of available resume fields |
| `list_resume_templates` | Browse 37 professional templates |
| `get_template_preview` | Preview a template |
| `change_resume_template` | Switch resume template (non-destructive) |
| `get_resume_pdf_url` | Get PDF download URL (15 min expiry) |
| `get_resume_docx_url` | Get DOCX download URL |
| `export_resume_json` | Export as JSON |
| `export_resume_markdown` | Export as Markdown |

## Interview Coach Tools

| Tool | Description |
|------|-------------|
| `start_interview_session` | Begin mock interview for a role and company |
| `continue_interview_session` | Submit answer, get next question + feedback |
| `get_interview_feedback` | Full performance analysis for a session |
| `list_interview_cases` | Browse system design cases |
| `start_system_design` | Start a system design interview |
| `get_behavioral_questions` | Get behavioral questions by category |
| `save_story_to_bank` | Save a STAR story for reuse |

## Career Tools

| Tool | Description |
|------|-------------|
| `match_job` | Score resume-job fit (0-100) |
| `analyze_resume_gaps` | Find missing keywords and skills |
| `generate_cover_letter` | Generate tailored cover letter |
| `optimize_resume_for_job` | Tailor resume to a job description |
| `generate_interview_questions` | Get likely questions for a company/role |
| `generate_linkedin_profile` | AI-optimized LinkedIn headline + About |
| `add_job_application` | Track a new job application |
| `list_job_applications` | View application pipeline |
| `update_job_status` | Move application to new stage |
| `get_application_analytics` | Pipeline analytics and conversion rates |
| `get_salary_insights` | Market salary data by role/location |
| `generate_negotiation_script` | Personalized negotiation script |
| `research_company` | Company overview, culture, interview tips |

## Resume Optimizer Tools

| Tool | Description |
|------|-------------|
| `optimize_resume_for_job` | Full resume optimization for a job |
| `analyze_resume_gaps` | Keyword and skills gap analysis |
| `match_job` | Resume-job match score |
| `get_ats_score` | ATS compatibility check |
| `improve_resume_bullets` | Rewrite bullets with stronger impact |

## Common Workflows

### Apply to a job
1. `research_company` — understand culture and interview style
2. `match_job` — check resume-job fit score
3. `analyze_resume_gaps` — find missing keywords
4. `optimize_resume_for_job` — tailor resume
5. `generate_cover_letter` — create tailored cover letter
6. `add_job_application` — track the application

### Interview prep
1. `research_company` — recent news, culture, interview style
2. `generate_interview_questions` — likely questions
3. `start_interview_session` — mock interview
4. `get_interview_feedback` — review performance
5. `save_story_to_bank` — bank STAR stories

### Salary negotiation
1. `get_salary_insights` — benchmark the offer
2. `generate_negotiation_script` — get scripts (conservative/balanced/aggressive)

### Resume optimization
1. `get_ats_score` — check formatting issues
2. `analyze_resume_gaps` — find keyword gaps
3. `improve_resume_bullets` — strengthen bullet points
4. `optimize_resume_for_job` — full tailoring

## Tips

- Always have a `resume_id` ready — run `list_resumes` to find yours
- `optimize_resume_for_job` with `apply_changes=false` lets you review before committing
- PDF URLs expire in 15 minutes — generate fresh when needed
- Build a STAR story bank with `save_story_to_bank` — reuse across interviews
- Run `match_job` before applying to prioritize high-fit opportunities (aim for 80+)

## Platform Links

- **Dashboard** — https://placed.exidian.tech
- **Resumes** — https://placed.exidian.tech/resumes
- **Job Tracker** — https://placed.exidian.tech/jobs
- **Interview Hub** — https://placed.exidian.tech/interview
- **Settings / API Key** — https://placed.exidian.tech/settings
