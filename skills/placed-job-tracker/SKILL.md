---
name: placed-job-tracker
description: This skill should be used when the user wants to "track job applications", "add a job application", "update application status", "view my job pipeline", "get application analytics", or wants to manage their job search using the Placed career platform at placed.exidian.tech.
version: 1.0.0
metadata: {"openclaw":{"emoji":"📋","homepage":"https://placed.exidian.tech","requires":{"env":["PLACED_API_KEY"]},"primaryEnv":"PLACED_API_KEY"}}
---

# Placed Job Tracker

Track and manage your job applications with AI-powered pipeline analytics via the Placed platform.

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

- `add_job_application` — Track a new job application
- `list_job_applications` — View your application pipeline
- `update_job_status` — Update application status (Applied, Phone Screen, Interview, Offer, Rejected)
- `get_application_analytics` — Get pipeline analytics and conversion rates
- `match_job` — Score how well your resume matches a job (0-100)
- `analyze_resume_gaps` — Find missing keywords and skills for a specific role

## Usage

**To add a job application:**
Call `add_job_application(company="Stripe", role="Senior Engineer", status="Applied", url="https://stripe.com/jobs/123", notes="Referral from John")`

**To view your pipeline:**
Call `list_job_applications(status="all")` to see all applications
Call `list_job_applications(status="Interview")` to filter by stage

**To update application status:**
Call `update_job_status(application_id="...", status="Phone Screen", notes="Scheduled for next Tuesday")`

**To get pipeline analytics:**
Call `get_application_analytics(date_range="30d")`
Returns: conversion rates by stage, response rates, time-to-offer, top companies

**To score resume-job fit before applying:**
Call `match_job(resume_id="...", job_description="...")`
Returns: match score (0-100), missing keywords, strengths

## Application Statuses

- `Saved` — Job saved for later
- `Applied` — Application submitted
- `Phone Screen` — Initial phone/recruiter screen
- `Interview` — Technical or onsite interview
- `Offer` — Offer received
- `Accepted` — Offer accepted
- `Rejected` — Application rejected
- `Withdrawn` — Withdrew application

## Job Search Tips

1. Apply to 5-10 roles per week for best results
2. Customize your resume for each application using `optimize_resume_for_job`
3. Track all applications — even informal ones
4. Follow up after 1-2 weeks if no response
5. Use analytics to identify which stages need improvement
6. Aim for a 20%+ phone screen rate; if lower, improve your resume
