# Placed Resume Optimizer — API Reference

Full reference for all resume optimization tools available via the Placed MCP server.

## Authentication

All tools require `PLACED_API_KEY` set in the MCP server environment.

---

## optimize_resume_for_job

Tailor resume content to a specific job description.

**Parameters:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `resume_id` | string | yes | Resume ID to optimize |
| `job_description` | string | yes | Full job description text |
| `apply_changes` | boolean | no | Apply changes to resume (default: false) |
| `create_copy` | boolean | no | Create a new copy instead of modifying original (default: true when apply_changes=true) |
| `sections` | array | no | Sections to optimize (default: all) |

**Returns:**
```json
{
  "suggested_changes": {
    "summary": "Updated summary text...",
    "experience": [{ "bullet_index": 2, "original": "...", "improved": "..." }],
    "skills": { "add": ["Kafka", "gRPC"], "reorder": ["Go", "Python", "Java"] }
  },
  "keyword_additions": ["distributed systems", "service mesh"],
  "match_score_before": 65,
  "match_score_after": 84,
  "new_resume_id": "res_xyz789"
}
```

---

## analyze_resume_gaps

Find missing keywords and skills vs. a job description.

**Parameters:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `resume_id` | string | yes | Resume ID |
| `job_description` | string | yes | Job description text |
| `include_suggestions` | boolean | no | Include how to address each gap (default: true) |

**Returns:**
```json
{
  "critical_gaps": [
    {
      "keyword": "Kafka",
      "frequency_in_jd": 4,
      "suggestion": "Add to skills section if you have experience; mention in relevant bullet points"
    }
  ],
  "nice_to_have_gaps": ["gRPC", "Istio", "Prometheus"],
  "keyword_gaps": ["distributed tracing", "observability", "SLO"],
  "matched_keywords": ["Go", "Kubernetes", "microservices", "distributed systems"],
  "gap_score": 72
}
```

---

## match_job

Score resume-job fit with keyword breakdown.

**Parameters:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `resume_id` | string | yes | Resume ID |
| `job_description` | string | yes | Job description text |
| `job_title` | string | no | Job title for context |
| `company` | string | no | Company name for context |

**Returns:**
```json
{
  "match_score": 78,
  "grade": "B+",
  "matched_keywords": ["distributed systems", "Go", "Kubernetes", "microservices"],
  "missing_keywords": ["Kafka", "gRPC", "service mesh"],
  "matched_requirements": ["5+ years experience", "system design", "team leadership"],
  "missing_requirements": ["ML experience"],
  "recommendation": "Strong match. Add Kafka and gRPC to skills section to reach 85+.",
  "apply_recommendation": "yes"
}
```

**Score interpretation:**
- 90-100: Excellent match — apply immediately
- 80-89: Strong match — minor tweaks recommended
- 70-79: Good match — optimize before applying
- 60-69: Moderate match — significant gaps to address
- <60: Weak match — consider if role is right fit

---

## get_ats_score

Check ATS compatibility and formatting issues.

**Parameters:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `resume_id` | string | yes | Resume ID |
| `job_description` | string | no | Job description for keyword density check |

**Returns:**
```json
{
  "ats_score": 82,
  "formatting_issues": [
    { "issue": "Table detected in skills section", "severity": "high", "fix": "Convert to bullet list" },
    { "issue": "Inconsistent date format", "severity": "medium", "fix": "Use MM/YYYY throughout" }
  ],
  "keyword_density": {
    "score": 75,
    "top_missing": ["Kafka", "distributed tracing"]
  },
  "parsing_test": {
    "name_extracted": true,
    "email_extracted": true,
    "experience_extracted": true,
    "skills_extracted": true
  },
  "recommendations": [
    "Remove table from skills section",
    "Standardize date formats to MM/YYYY",
    "Add 'Kafka' to skills — appears 4x in job description"
  ]
}
```

---

## improve_resume_bullets

Rewrite bullet points with stronger impact and metrics.

**Parameters:**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `resume_id` | string | yes | Resume ID |
| `section` | string | no | Section to improve: `experience`, `projects` (default: `experience`) |
| `job_description` | string | no | Job description for context-aware improvements |
| `apply_changes` | boolean | no | Apply improved bullets to resume (default: false) |
| `bullet_indices` | array | no | Specific bullet indices to improve (default: all) |

**Returns:**
```json
{
  "improvements": [
    {
      "experience_index": 0,
      "bullet_index": 1,
      "original": "Worked on database optimization",
      "improved": "Optimized PostgreSQL query performance by 40%, reducing p99 latency from 500ms to 300ms for 10M+ daily active users",
      "improvement_score": 85,
      "changes_made": ["Added metrics", "Stronger action verb", "Added scale/impact"]
    }
  ],
  "overall_improvement": "+23 points",
  "bullets_improved": 8,
  "bullets_unchanged": 2
}
```

---

## Scoring Rubrics

### ATS Score Components
| Component | Weight | Description |
|-----------|--------|-------------|
| Formatting | 30% | No tables, graphics, unusual fonts |
| Keyword density | 30% | Job description keywords present |
| Parsing accuracy | 25% | Can ATS extract all key fields |
| Structure | 15% | Standard sections in expected order |

### Match Score Components
| Component | Weight | Description |
|-----------|--------|-------------|
| Required skills | 40% | Must-have skills from job description |
| Experience level | 25% | Years and seniority match |
| Nice-to-have skills | 20% | Preferred but not required skills |
| Title/role alignment | 15% | Job title similarity |

### Bullet Quality Score
| Score | Description |
|-------|-------------|
| 90-100 | Strong action verb + specific metric + business impact |
| 70-89 | Good action verb + some metrics |
| 50-69 | Weak verb or missing metrics |
| <50 | Vague, passive, or no impact stated |

---

## Error Codes

| Code | Meaning |
|------|---------|
| `RESUME_NOT_FOUND` | Resume ID invalid |
| `JOB_DESCRIPTION_TOO_SHORT` | Job description must be at least 100 characters |
| `NO_EXPERIENCE_SECTION` | Resume has no experience section to optimize |
| `OPTIMIZATION_FAILED` | AI optimization failed — retry |
| `COPY_LIMIT_REACHED` | Too many resume copies — delete unused resumes |
