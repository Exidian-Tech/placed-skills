---
name: placed
description: Complete Placed career platform integration — resume builder, interview coach, job tracker, ATS checker, cover letter generator, LinkedIn optimizer, and salary tools. Use when the user wants to build or manage resumes, practice interviews, track job applications, optimize resumes for ATS, generate cover letters, research companies, or get salary insights via placed.exidian.tech.
metadata:
  { "openclaw": { "emoji": "💼", "homepage": "https://placed.exidian.tech" } }
---

# Placed — AI Career Platform

Full integration with the Placed career platform (https://placed.exidian.tech). All tools call the Placed API directly — no MCP server required.

## API Key

Before making any call, obtain the API key:

1. Check if `PLACED_API_KEY` is already set in the environment
2. If not set, ask the user: "Please provide your Placed API key (get it from https://placed.exidian.tech/settings/api)"
3. Use the provided key for all API calls in this session

```bash
# Check if key is available
echo "${PLACED_API_KEY:-not_set}"
```

If not set, prompt the user, then use it as:

```bash
PLACED_API_KEY="<user_provided_key>"
```

## How to Call the API

Every Placed action is a POST to the same endpoint:

```bash
curl -s -X POST https://placed.exidian.tech/api/mcp \
  -H "Authorization: Bearer $PLACED_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"<tool_name>","arguments":{<args>}}}'
```

Parse the result:

```bash
# The response is: {"result":{"content":[{"type":"text","text":"<json_string>"}]}}
# Extract the text field and parse it
```

## Available Skills

- `placed-resume-builder` — Resume management + 37 templates
- `placed-interview-coach` — Mock interviews + STAR coaching
- `placed-career-tools` — Job tracker, cover letters, salary tools, company research
- `placed-resume-optimizer` — AI resume optimization for specific jobs
- `placed-job-tracker` — Application pipeline tracking

## What You Can Do

- Build and manage resumes with professional templates
- Track job applications with pipeline analytics
- Practice mock interviews (technical, system design, behavioral)
- Optimize resumes for specific job descriptions
- Check ATS compatibility scores
- Generate tailored cover letters
- Get LinkedIn headline + About section
- Research companies and salary ranges
- Save STAR stories for behavioral interviews

## Sign Up

Create an account at https://placed.exidian.tech, then get your API key from Settings → API Keys.
