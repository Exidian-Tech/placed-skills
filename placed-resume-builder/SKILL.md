---
name: placed-resume-builder
description: This skill should be used when the user wants to "build a resume", "create a resume", "update my resume", "export resume as PDF", "change resume template", "list my resumes", or wants to manage resumes using the Placed career platform at placed.exidian.tech.
version: 1.0.0
metadata: {"openclaw":{"emoji":"📄","homepage":"https://placed.exidian.tech","requires":{"env":["PLACED_API_KEY"]},"primaryEnv":"PLACED_API_KEY"}}
---

# Placed Resume Builder

Build and manage professional resumes with AI assistance via the Placed MCP server.

## Prerequisites

Requires the Placed MCP server. Install via:
```json
{
  "mcpServers": {
    "placed": {
      "command": "npx",
      "args": ["-y", "@exidian/placed-mcp"],
      "env": {
        "PLACED_API_KEY": "your-api-key",
        "PLACED_BASE_URL": "https://placed.exidian.tech"
      }
    }
  }
}
```
Get your API key at https://placed.exidian.tech/settings/api

## Available Tools

- `create_resume` — Create a new resume from your profile or scratch
- `get_resume` — Retrieve a resume by ID
- `update_resume` — Update any resume section (experience, education, skills, etc.)
- `list_resumes` — List all your resumes
- `get_resume_schema` — Understand available resume sections
- `list_resume_templates` — Browse 37 professional templates
- `get_template_preview` — Preview a template
- `change_resume_template` — Switch your resume template
- `get_resume_pdf_url` — Download as PDF (expires in 15 min)
- `get_resume_docx_url` — Download as Word document
- `export_resume_json` — Export as JSON
- `export_resume_markdown` — Export as Markdown

## Resume Sections

All sections are optional and can be updated independently:
- `basics` — name, email, phone, headline, location
- `summary` — professional overview
- `experience` — work history
- `education` — degrees and certifications
- `skills` — technical and soft skills
- `languages` — language proficiencies
- `certifications` — professional certs
- `awards` — honors and recognition
- `projects` — personal/professional projects
- `publications` — articles, papers, books
- `references` — professional references
- `volunteer` — volunteer experience
- `interests` — hobbies and interests
- `profiles` — LinkedIn, GitHub, etc.

## Usage

**To create a resume:**
Call `create_resume(title="Senior Engineer Resume", target_role="Staff Engineer")`

**To update sections:**
Call `update_resume(resume_id="...", experience=[...], skills=[...])`

**To choose a template:**
1. Call `list_resume_templates()` to browse options
2. Call `change_resume_template(resume_id="...", template_id="modern")` to apply

**To export:**
- PDF: Call `get_resume_pdf_url(resume_id="...")`
- Markdown: Call `export_resume_markdown(resume_id="...")`
- Word: Call `get_resume_docx_url(resume_id="...")`

**To understand available fields:**
Call `get_resume_schema()` to see all available fields and their formats.

## Tips

- Quantify achievements with metrics (numbers, percentages, dollars)
- Use action verbs at the start of bullet points
- Mirror job description language for better ATS matching
- Test ATS compatibility with `check_ats_compatibility()` from the placed-resume-optimizer skill
