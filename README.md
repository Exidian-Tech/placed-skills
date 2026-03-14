# Placed Skills

> AI assistant skills for the [Placed](https://placed.exidian.tech) career platform — resume builder, interview coach, job tracker, ATS optimizer, cover letters, LinkedIn optimizer, and salary tools.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![MCP Powered](https://img.shields.io/badge/MCP-Powered-blue)](https://modelcontextprotocol.io)
[![Platform](https://img.shields.io/badge/Platform-Placed-success)](https://placed.exidian.tech)
[![ClawHub](https://img.shields.io/badge/ClawHub-Published-purple)](https://clawhub.io)

## Prerequisites

1. Sign up at [placed.exidian.tech](https://placed.exidian.tech)
2. Get your API key from **Settings → API Keys**

---

## Install in Claude Code

**Option A — Plugin marketplace (recommended):**

```shell
/plugin marketplace add Exidian-Tech/placed-skills
/plugin install placed@placed-skills
```

Then add your API key to your environment:

```bash
export PLACED_API_KEY=your-api-key-here
```

**Option B — ClawHub CLI:**

```bash
npm i -g clawhub
clawhub install placed-resume-builder
clawhub install placed-interview-coach
clawhub install placed-career-tools
clawhub install placed-resume-optimizer
```

**Option C — Manual:**

```bash
mkdir -p ~/.claude/skills/placed-resume-builder
cp -R skills/placed-resume-builder/ ~/.claude/skills/placed-resume-builder/
# repeat for each skill
```

---

## Install in Cursor

Copy the combined skill to your project or globally:

```bash
# Project-level
mkdir -p .cursor/skills/placed
cp .cursor/skills/placed/SKILL.md .cursor/skills/placed/SKILL.md

# Global
mkdir -p ~/.cursor/skills/placed
cp .cursor/skills/placed/SKILL.md ~/.cursor/skills/placed/SKILL.md
```

Then add the MCP server to `~/.cursor/mcp.json` or `.cursor/mcp.json`:

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

---

## MCP Server (all tools)

Add to your MCP config (`~/.claude/mcp.json` for Claude Code, `~/.cursor/mcp.json` for Cursor):

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

---

## Skills

| Skill                     | What it does                                                                    |
| ------------------------- | ------------------------------------------------------------------------------- |
| `placed-resume-builder`   | Create, update, template-switch, and export resumes                             |
| `placed-interview-coach`  | Mock interviews, system design, behavioral prep, STAR stories                   |
| `placed-career-tools`     | Job tracking, cover letters, LinkedIn optimizer, salary tools, company research |
| `placed-resume-optimizer` | ATS scoring, keyword gap analysis, bullet point improvement                     |
| `placed-job-tracker`      | Application pipeline tracking and analytics                                     |

---

## Example Prompts

```
"Create a new resume for Senior Backend Engineer roles"
"Start a mock interview for Staff Engineer at Google"
"Track my application to Stripe for Senior Engineer"
"Check my resume ATS score"
"What's the market salary for Staff Engineer in Amsterdam?"
"Generate a cover letter for my Airbnb application"
"Optimize my resume for this job description: [paste JD]"
```

---

## Links

- **Placed platform:** https://placed.exidian.tech
- **MCP server:** https://github.com/Exidian-Tech/placed-mcp
- **Skills repo:** https://github.com/Exidian-Tech/placed-skills
- **ClawHub:** https://clawhub.io/skills/placed-resume-builder

## License

MIT © Exidian Technologies Pvt Ltd
