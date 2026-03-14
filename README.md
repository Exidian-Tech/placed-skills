# Placed Skills

> OpenClaw / Claude Code skills for the [Placed](https://placed.exidian.tech) career platform, powered by the official [placed-mcp](https://github.com/Exidian-Tech/placed-mcp) server.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![MCP Powered](https://img.shields.io/badge/MCP-Powered-blue)](https://modelcontextprotocol.io)
[![Platform](https://img.shields.io/badge/Platform-Placed-success)](https://placed.exidian.tech)

## What are Placed Skills?

Placed Skills are reusable OpenClaw / Claude Code skill files that give your AI assistant higher-level workflows on top of the 47 tools exposed by the Placed MCP server. Instead of calling raw tools one by one, you can invoke specialized skills for resume building, resume optimization, interview prep, job tracking, and career decision support.

These skills are ideal if you want a faster, more guided experience for common career tasks like tailoring a resume to a job, practicing interviews, tracking applications, researching companies, or analyzing compensation.

## Prerequisites

Before using these skills, install and configure the official MCP server:

- **MCP server repo:** https://github.com/Exidian-Tech/placed-mcp
- **Platform:** https://placed.exidian.tech

## Installation

### Option 1: OpenClaw skills directory

Copy the skill files into:

```bash
~/.agents/skills/
```

### Option 2: Claude Code local skills directory

Copy the skill files into:

```bash
~/.claude/skills/
```

### Example install

```bash
mkdir -p ~/.agents/skills/placed
cp -R . ~/.agents/skills/placed/
```

After copying, restart your assistant session so the new skills are discovered.

## Available Skills

### 1. `placed-resume-builder`

**What it does:**
Builds and manages resumes using Placed templates and profile data.

**Primary capabilities:**
- Create resumes
- Update resume sections
- Browse 37 templates
- Switch templates
- Export resume formats

**Example prompts:**
- `Build me a new resume for Senior Backend Engineer roles`
- `Create a resume from my profile and use the most modern template`
- `Update my resume summary and skills section`
- `Show me resume templates suitable for product roles`

---

### 2. `placed-resume-optimizer`

**What it does:**
Improves resumes for ATS performance, clarity, and job-specific relevance.

**Primary capabilities:**
- ATS compatibility checks
- Resume quality scoring
- Bullet point improvement
- Section optimization
- Job-specific tailoring

**Example prompts:**
- `Optimize my resume for this Staff Engineer job description`
- `Check my resume ATS compatibility`
- `Improve these experience bullet points`
- `Give me a quality score breakdown for my resume`

---

### 3. `placed-interview-coach`

**What it does:**
Runs mock interview workflows across technical, behavioral, and system design interviews.

**Primary capabilities:**
- Mock interview sessions
- Feedback on answers
- Behavioral question prep
- System design case practice
- STAR story banking

**Example prompts:**
- `Start a mock interview for a senior frontend engineer role`
- `Practice system design for Twitter or Uber Eats`
- `Give me behavioral questions for engineering manager interviews`
- `Save this STAR story for leadership and conflict resolution`

---

### 4. `placed-career-tools`

**What it does:**
Supports company research, salary benchmarking, offer analysis, and negotiation prep.

**Primary capabilities:**
- Research companies
- Fetch salary data
- Analyze offers
- Generate salary negotiation scripts
- View subscription and usage data

**Example prompts:**
- `Research Stripe for a senior PM interview`
- `What salary range should I expect for Staff Engineer at Datadog in Amsterdam?`
- `Analyze this offer package and tell me if it's competitive`
- `Write a salary negotiation script for this offer`

---

### 5. `placed-job-tracker`

**What it does:**
Helps manage and analyze the full job application pipeline.

**Primary capabilities:**
- Add job applications
- Update status
- List tracked roles
- Delete stale entries
- Review application analytics

**Example prompts:**
- `Add my application to Notion for Senior Product Engineer`
- `Show all roles currently in interview stage`
- `Update my Google application to rejected`
- `Give me analytics on my job search pipeline`

---

### 6. `SKILL.md` umbrella overview

**What it does:**
Provides a top-level overview of the Placed skill suite, tool groupings, workflows, and recommended usage patterns.

**Example prompts:**
- `What Placed skills are available?`
- `Which skill should I use for interview prep?`
- `Show me the Placed workflow for optimizing a resume and preparing for interviews`

## Included Files

- `SKILL.md` — master overview of the Placed skills ecosystem
- `placed-resume-builder.md`
- `placed-resume-optimizer.md`
- `placed-interview-coach.md`
- `placed-career-tools.md`

## Recommended Workflow

1. Install `placed-mcp`
2. Configure your `PLACED_API_KEY`
3. Copy these skills into your skills directory
4. Restart your assistant
5. Use skill-style prompts for guided workflows

## Links

- **Placed platform:** https://placed.exidian.tech
- **Official MCP server:** https://github.com/Exidian-Tech/placed-mcp
- **Skills repo:** https://github.com/Exidian-Tech/placed-skills

## License

MIT © Exidian Technologies Pvt Ltd
