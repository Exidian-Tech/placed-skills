---
name: placed-resume-optimizer
description: This skill should be used when the user wants to "optimize resume for job", "check ATS score", "improve resume bullets", "analyze resume gaps", "tailor resume to job description", "get ATS compatibility score", "improve bullet points", "match resume to job posting", "fix resume for ATS", or wants to maximize their resume's impact and ATS compatibility using the Placed platform at placed.exidian.tech.
version: 1.0.0
homepage: https://placed.exidian.tech
metadata: {"openclaw":{"emoji":"🎯","homepage":"https://placed.exidian.tech","requires":{"env":["PLACED_API_KEY"]},"primaryEnv":"PLACED_API_KEY"}}
---

# Placed Resume Optimizer

AI-powered resume optimization for ATS compatibility, keyword matching, and bullet point quality. Maximize your resume's impact for specific job descriptions using the Placed MCP server.

## Overview

The Placed Resume Optimizer analyzes your resume against job descriptions, scores ATS compatibility, identifies keyword gaps, and rewrites bullet points for maximum impact. Use it before every application to tailor your resume and improve your chances of passing automated screening.

## Prerequisites

1. Create an account at https://placed.exidian.tech
2. Get your API key from Settings → API Keys
3. Install the Placed MCP server:

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

## Available Tools

| Tool | Description |
|------|-------------|
| `optimize_resume_for_job` | Tailor resume to a specific job description |
| `analyze_resume_gaps` | Find missing keywords and skills vs. a job description |
| `match_job` | Score resume-job fit (0-100) with keyword breakdown |
| `get_ats_score` | Check ATS compatibility and formatting issues |
| `improve_resume_bullets` | Rewrite bullet points with stronger impact and metrics |

## Quick Start

### Check ATS compatibility

```
get_ats_score(resume_id="res_abc123")
# Returns: ATS score, formatting issues, keyword density, recommendations
```

### Analyze gaps vs. a job description

```
analyze_resume_gaps(
  resume_id="res_abc123",
  job_description="Senior Software Engineer at Stripe — Go, distributed systems, Kafka..."
)
# Returns: critical gaps, nice-to-have gaps, keyword gaps, suggestions
```

### Improve bullet points

```
improve_resume_bullets(
  resume_id="res_abc123",
  section="experience",
  job_description="..."
)
# Returns: rewritten bullets with stronger verbs, metrics, and impact
```

### Full optimization for a job

```
optimize_resume_for_job(
  resume_id="res_abc123",
  job_description="Senior Software Engineer at Airbnb...",
  apply_changes=false
)
# Returns: suggested changes — review before applying
```

## Optimization Workflow

Run this sequence before every application:

1. **Score the match** — `match_job` to see current fit score
2. **Find gaps** — `analyze_resume_gaps` to identify missing keywords
3. **Check ATS** — `get_ats_score` to catch formatting issues
4. **Improve bullets** — `improve_resume_bullets` for weak experience entries
5. **Full optimize** — `optimize_resume_for_job` with `apply_changes=false` to review
6. **Apply changes** — Re-run with `apply_changes=true` if satisfied
7. **Verify** — `match_job` again to confirm score improved

## Bullet Point Formula

Strong bullets follow this pattern:

```
[Action Verb] + [What You Did] + [How/Scale] + [Quantified Result]
```

**Before:** "Worked on database optimization"
**After:** "Optimized PostgreSQL query performance by 40%, reducing p99 latency from 500ms to 300ms for 10M+ daily active users"

**Before:** "Led a team"
**After:** "Led cross-functional team of 8 engineers to redesign payment processing pipeline, reducing transaction failures by 35% and increasing throughput 2x"

**Strong action verbs:**
- Technical: Architected, Built, Designed, Optimized, Implemented, Engineered, Migrated
- Leadership: Led, Managed, Mentored, Spearheaded, Directed, Coached
- Impact: Improved, Reduced, Increased, Accelerated, Scaled, Transformed

## ATS Compatibility Rules

Common ATS failures and fixes:

| Issue | Fix |
|-------|-----|
| Tables or columns | Use single-column layout |
| Graphics or images | Remove all non-text elements |
| Unusual fonts | Use Arial, Calibri, or Times New Roman |
| Headers/footers with key info | Move to main body |
| Inconsistent date formats | Use MM/YYYY throughout |
| Missing job description keywords | Add naturally to skills and bullets |
| Vague job titles | Use standard industry titles |

## Tips

- Run `match_job` first — if score is above 80, minimal optimization needed
- `improve_resume_bullets` works best when you provide the job description for context
- Always review `optimize_resume_for_job` suggestions before applying — don't auto-apply blindly
- Keep a "master resume" and create tailored copies per application using `optimize_resume_for_job` with `apply_changes=true` (creates a copy, doesn't modify original)
- ATS score below 70 means formatting issues — fix those before keyword optimization

## Additional Resources

- **`references/api-guide.md`** — Full API reference with scoring rubrics and response schemas
- **Placed Optimizer** — https://placed.exidian.tech/optimize
- **ATS Guide** — https://placed.exidian.tech/ats-guide
