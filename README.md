# Placed Skills

> AI assistant skills for the [Placed](https://placed.exidian.tech) career platform — works with OpenClaw, Claude Code, Cursor, and any AgentSkills-compatible tool.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![MCP Powered](https://img.shields.io/badge/MCP-Powered-blue)](https://modelcontextprotocol.io)
[![Platform](https://img.shields.io/badge/Platform-Placed-success)](https://placed.exidian.tech)
[![ClawHub](https://img.shields.io/badge/ClawHub-Published-purple)](https://clawhub.io)

## What are Placed Skills?

Placed Skills are reusable AI assistant skill files that give your AI assistant higher-level workflows on top of the 47 tools exposed by the Placed MCP server. Instead of calling raw tools one by one, invoke specialized skills for resume building, resume optimization, interview prep, job tracking, and career decision support.

## Prerequisites

1. Create an account at https://placed.exidian.tech
2. Get your API key from Settings → API Keys
3. Install the Placed MCP server — see [placed-mcp](https://github.com/Exidian-Tech/placed-mcp)

## Available Skills

| Skill | Description |
|-------|-------------|
| `placed-resume-builder` | Create, update, template-switch, and export resumes |
| `placed-interview-coach` | Mock interviews, system design, behavioral prep, STAR stories |
| `placed-career-tools` | Job tracking, cover letters, LinkedIn optimizer, salary tools, company research |
| `placed-resume-optimizer` | ATS scoring, keyword gap analysis, bullet point improvement |

---

## Installation

### OpenClaw (via ClawHub)

```bash
clawhub install placed-resume-builder
clawhub install placed-interview-coach
clawhub install placed-career-tools
clawhub install placed-resume-optimizer
```

Or install all at once:

```bash
clawhub install placed-resume-builder placed-interview-coach placed-career-tools placed-resume-optimizer
```

Skills are installed to `~/.agents/skills/` and auto-discovered by OpenClaw.

### Claude Code

**Option A — via ClawHub (recommended):**
```bash
clawhub install placed-resume-builder
```

**Option B — manual copy:**
```bash
mkdir -p ~/.claude/skills/placed-resume-builder
cp -R placed-resume-builder/ ~/.claude/skills/placed-resume-builder/

mkdir -p ~/.claude/skills/placed-interview-coach
cp -R placed-interview-coach/ ~/.claude/skills/placed-interview-coach/

mkdir -p ~/.claude/skills/placed-career-tools
cp -R placed-career-tools/ ~/.claude/skills/placed-career-tools/

mkdir -p ~/.claude/skills/placed-resume-optimizer
cp -R placed-resume-optimizer/ ~/.claude/skills/placed-resume-optimizer/
```

Restart your Claude Code session after copying.

### Cursor

Copy the combined Cursor skill to your project:

```bash
mkdir -p .cursor/skills/placed
cp .cursor/skills/placed/SKILL.md .cursor/skills/placed/SKILL.md
```

Or for global Cursor skills:

```bash
mkdir -p ~/.cursor/skills/placed
cp .cursor/skills/placed/SKILL.md ~/.cursor/skills/placed/SKILL.md
```

The combined skill covers all Placed tools in a single file optimized for Cursor's skill format.

### Manual (any AgentSkills-compatible tool)

Copy any skill folder to your tool's skills directory:

```bash
cp -R placed-resume-builder/ /path/to/your/tool/skills/
```

Each skill folder contains a `SKILL.md` with proper frontmatter and a `references/api-guide.md` with full API documentation.

---

## MCP Server Configuration

Add to your AI tool's MCP config:

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

- **OpenClaw / Claude Code:** `~/.claude/mcp.json` or project `.mcp.json`
- **Cursor:** `~/.cursor/mcp.json` or project `.cursor/mcp.json`

---

## Example Prompts

**Resume:**
- "Create a new resume for Senior Backend Engineer roles"
- "Update my resume skills section with Go, Kubernetes, and Kafka"
- "Give me a PDF download link for my resume"
- "Switch my resume to the Modern template"

**Interview:**
- "Start a mock interview for Staff Engineer at Google"
- "Practice system design for Twitter"
- "Give me behavioral questions for engineering manager roles"
- "Save this STAR story about leading a team through a production incident"

**Career Tools:**
- "Track my application to Stripe for Senior Engineer"
- "Generate a cover letter for my Airbnb application"
- "What's the market salary for Staff Engineer in Amsterdam?"
- "Generate a salary negotiation script for a $200K offer"
- "Research Databricks — culture, interview style, recent news"

**Optimization:**
- "Check my resume ATS score"
- "Optimize my resume for this job description: [paste JD]"
- "Improve the bullet points in my experience section"
- "Find keyword gaps between my resume and this job posting"

---

## Skill Structure

Each skill follows the AgentSkills spec:

```
placed-resume-builder/
├── SKILL.md              # Skill definition with frontmatter + instructions
└── references/
    └── api-guide.md      # Full API reference and examples
```

**SKILL.md frontmatter:**
```yaml
---
name: placed-resume-builder
description: Trigger phrases for auto-selection
version: 1.0.0
homepage: https://placed.exidian.tech
---
```

---

## Links

- **Placed platform:** https://placed.exidian.tech
- **Official MCP server:** https://github.com/Exidian-Tech/placed-mcp
- **Skills repo:** https://github.com/Exidian-Tech/placed-skills
- **ClawHub:** https://clawhub.io/skills/placed-resume-builder

## License

MIT © Exidian Technologies Pvt Ltd
