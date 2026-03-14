---
name: placed
description: Complete Placed career platform integration — resume builder, interview coach, job tracker, ATS checker, cover letter generator, LinkedIn optimizer, and salary tools. Install individual skills or this bundle for full access.
metadata: {"openclaw":{"emoji":"💼","homepage":"https://placed.exidian.tech","requires":{"env":["PLACED_API_KEY"]},"primaryEnv":"PLACED_API_KEY"}}
---

# Placed — AI Career Platform

Full integration with the Placed career platform (https://placed.exidian.tech).

## Setup

1. Sign up at https://placed.exidian.tech
2. Get your API key from Settings
3. Install the MCP server:

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

## Included Skills

Install individually via ClawHub:
- `clawhub install placed-resume-builder` — Resume management + 37 templates
- `clawhub install placed-interview-coach` — Mock interviews + STAR coaching
- `clawhub install placed-career-tools` — Job tracker, ATS, cover letters, salary tools
- `clawhub install placed-resume-optimizer` — AI resume optimization for specific jobs

## What You Can Do

- Build and manage resumes with 37 professional templates
- Track job applications with pipeline analytics
- Practice mock interviews (technical, system design, behavioral)
- Optimize resumes for specific job descriptions
- Check ATS compatibility scores
- Generate tailored cover letters
- Get LinkedIn headline + About section
- Research companies and salary ranges
- Save STAR stories for behavioral interviews
