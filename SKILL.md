# Placed Skills

Skills for working with the Placed MCP server and its 47 tools.

## Overview

The Placed platform provides comprehensive career tools including resume management, job tracking, AI-powered optimization, interview coaching, and career research.

## Available Skills

### 1. placed-resume-builder
**Tools:** create_resume, get_resume, update_resume, list_resumes, get_resume_schema, list_resume_templates, get_template_preview, change_resume_template

Build and manage resumes with AI assistance. Create new resumes from scratch or from your profile, update any section, export in multiple formats, and choose from 37 professional templates.

### 2. placed-job-tracker
**Tools:** add_job_application, list_job_applications, update_job_status, delete_job_application, get_application_analytics

Track your job search journey. Add applications, monitor status changes, and get analytics on your application pipeline.

### 3. placed-ai-coach
**Tools:** optimize_resume_for_job, analyze_resume_gaps, match_job, generate_cover_letter, get_interview_questions, generate_linkedin_profile

AI-powered career coaching. Get resume optimization suggestions, analyze skill gaps, generate cover letters, and prepare for interviews.

### 4. placed-interview-coach
**Tools:** start_interview_session, continue_interview_session, get_interview_feedback, list_interview_cases, start_system_design, get_behavioral_questions, save_story_to_bank

Master technical, system design, and behavioral interviews with AI coaching, real-time feedback, and STAR story banking. Practice mock interviews, system design cases (URL Shortener, Twitter, Netflix, Uber), behavioral questions with STAR method, and save stories for reuse.

### 5. placed-career-tools
**Tools:** research_company, get_company_salary_data, generate_salary_negotiation_script, analyze_offer, get_subscription_status, get_usage_stats, get_usage_limits

Research companies, benchmark salaries, negotiate offers, and make data-driven career decisions. Get company culture and funding info, salary ranges by role and location, negotiation scripts, and offer analysis.

### 6. placed-resume-optimizer
**Tools:** check_ats_compatibility, get_resume_quality_score, improve_bullet_point, optimize_resume_section, optimize_resume_for_job

Optimize your resume for ATS systems, improve quality scores, and enhance bullet points for maximum impact. Check ATS compatibility, get quality scores, improve individual bullets, optimize sections, and tailor to job descriptions.

## Tool Categories

**Profile Tools (2):** get_profile, update_profile
**Resume Tools (8):** create_resume, get_resume, update_resume, list_resumes, get_resume_pdf_url, get_resume_docx_url, export_resume_json, export_resume_markdown
**Job Matching (2):** match_job, analyze_resume_gaps
**Cover Letter (1):** generate_cover_letter
**Job Tracker (4):** add_job_application, list_job_applications, update_job_status, delete_job_application
**Quick Apply (3):** get_quick_apply_profile, update_quick_apply_profile, clear_quick_apply_profile
**AI Tools (5):** optimize_resume_for_job, get_interview_questions, generate_linkedin_profile, get_application_analytics, get_resume_schema
**AI Wizard (3):** generate_resume_from_prompt, optimize_resume_section, improve_bullet_point
**Templates (3):** list_resume_templates, get_template_preview, change_resume_template
**ATS & Quality (2):** check_ats_compatibility, get_resume_quality_score
**Interview Coach (7):** start_interview_session, continue_interview_session, get_interview_feedback, list_interview_cases, start_system_design, get_behavioral_questions, save_story_to_bank
**Subscription (3):** get_subscription_status, get_usage_stats, get_usage_limits
**Company Research (2):** research_company, get_company_salary_data
**Salary Negotiation (2):** generate_salary_negotiation_script, analyze_offer

## Total Tools: 47

All tools are user-facing only. No admin endpoints are exposed.

## Quick Start

**1. Build Your Resume**
```
/placed-resume-builder
```

**2. Optimize for Jobs**
```
/placed-resume-optimizer
```

**3. Practice Interviews**
```
/placed-interview-coach
```

**4. Research & Negotiate**
```
/placed-career-tools
```

**5. Track Applications**
```
/placed-job-tracker
```

## Interview Preparation Workflow

1. **Research Company** — Use `/placed-career-tools` to research company culture and salary
2. **Practice Technical** — Use `/placed-interview-coach` for coding interviews
3. **Practice System Design** — Use `/placed-interview-coach` for system design cases
4. **Practice Behavioral** — Use `/placed-interview-coach` with STAR method
5. **Save Stories** — Bank STAR stories for reuse across interviews
6. **Get Feedback** — Review performance and iterate

## Resume Optimization Workflow

1. **Check ATS** — Use `/placed-resume-optimizer` to check ATS compatibility
2. **Get Quality Score** — Identify weak areas
3. **Improve Bullets** — Enhance individual achievements
4. **Optimize Sections** — Improve overall structure
5. **Tailor to Job** — Customize for specific opportunities
6. **Export** — Download as PDF or DOCX

## Career Decision Framework

1. **Gather Data** — Research companies, benchmark salaries, analyze offers
2. **Evaluate Factors** — Compensation, growth, culture, impact, stability
3. **Weight by Importance** — What matters most to you?
4. **Make Decision** — Compare options, negotiate if needed, commit fully

## Resources

**System Design Interview Prep:**
- Use `qmd search "system design interview URL shortener Twitter distributed"`
- Best books: Grokking the System Design Interview, System Design Interview by Alex Xu, Educative System Design

**Behavioral Interview Prep:**
- Use `qmd search "behavioral interview STAR method engineering manager"`
- Best books: Engineering Managers Handbook, Leading Effective Engineering Teams

**Salary Research:**
- Levels.fyi, Blind, Glassdoor, PayScale

**Company Research:**
- LinkedIn, Crunchbase, company websites, news sources
