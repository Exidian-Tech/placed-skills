# placed-resume-optimizer

Optimize your resume for ATS systems, improve quality scores, and enhance bullet points for maximum impact.

## Tools

- `check_ats_compatibility` - Scan resume for ATS compatibility issues
- `get_resume_quality_score` - Get overall quality score with section breakdown
- `improve_bullet_point` - Enhance a single bullet point with AI
- `optimize_resume_section` - Optimize experience, skills, or summary section
- `optimize_resume_for_job` - Tailor resume to a specific job description

## ATS Compatibility Check

Ensure your resume passes Applicant Tracking Systems:

```
check_ats_compatibility(resume_id="your-resume-id")
# Returns: compatibility score, issues found, recommendations
```

**What ATS Systems Check:**
- **Formatting** — Simple, clean layout (no tables, columns, graphics)
- **Keywords** — Job description keywords present in resume
- **Structure** — Standard sections (experience, skills, education)
- **Parsing** — Can the system read and extract your information?
- **Fonts** — Standard fonts (Arial, Calibri, Times New Roman)
- **File Format** — PDF or DOCX (not images or fancy formats)

**Common ATS Issues:**
- ❌ Fancy formatting, graphics, or images
- ❌ Tables, columns, or text boxes
- ❌ Unusual fonts or colors
- ❌ Headers/footers with important info
- ❌ Inconsistent date formats
- ❌ Missing keywords from job description
- ❌ Vague job titles or descriptions
- ❌ Gaps in employment without explanation

**How to Fix:**
1. Use simple, clean formatting
2. Use standard fonts (11-12pt)
3. Use bullet points, not paragraphs
4. Include keywords from job description
5. Use consistent date formats (MM/YYYY)
6. Avoid graphics, tables, and columns
7. Save as PDF or DOCX
8. Test with ATS parser tools

## Resume Quality Score

Get a comprehensive quality assessment:

```
get_resume_quality_score(resume_id="your-resume-id")
# Returns: overall score (0-100), section scores, improvement suggestions
```

**Quality Metrics:**
- **Summary/Objective** — Clear, compelling, tailored
- **Experience** — Specific achievements, metrics, impact
- **Skills** — Relevant, organized, specific
- **Education** — Degrees, certifications, relevant coursework
- **Projects** — Impactful, well-described, quantified
- **Overall** — Completeness, clarity, professionalism

**Scoring Breakdown:**
- 90-100: Excellent (ready to submit)
- 80-89: Good (minor improvements needed)
- 70-79: Fair (several improvements recommended)
- 60-69: Poor (significant improvements needed)
- <60: Very Poor (major overhaul required)

**How to Improve Score:**
1. Add specific metrics and outcomes
2. Use action verbs (led, built, improved, optimized)
3. Quantify impact (% improvement, users affected, revenue)
4. Tailor to job description
5. Remove vague or generic statements
6. Ensure consistent formatting
7. Proofread for grammar and spelling

## Improve Bullet Points

Enhance individual bullet points with AI:

```
improve_bullet_point(
  current_bullet="Worked on backend systems",
  context="Senior Software Engineer at Google",
  job_description="Design and optimize distributed systems"
)
# Returns: improved bullet point with metrics and impact
```

**Before & After Examples:**

**Before:** "Worked on database optimization"
**After:** "Optimized database query performance by 40%, reducing latency from 500ms to 300ms and improving user experience for 10M+ daily active users"

**Before:** "Led a team of engineers"
**After:** "Led cross-functional team of 8 engineers to redesign payment processing system, reducing transaction failures by 35% and increasing throughput by 2x"

**Before:** "Improved code quality"
**After:** "Implemented automated testing framework covering 85% of codebase, reducing production bugs by 60% and improving deployment confidence"

**Bullet Point Formula:**
```
[Action Verb] + [What You Did] + [How You Did It] + [Quantified Result] + [Business Impact]
```

**Examples:**
- "Led migration of 500K users to new platform, reducing infrastructure costs by $2M annually while improving system reliability to 99.99% uptime"
- "Built real-time analytics dashboard processing 1B+ events daily, enabling data-driven decisions that increased conversion by 15%"
- "Mentored 5 junior engineers, with 3 promoted to senior roles within 18 months, improving team retention by 40%"

**Action Verbs to Use:**
- Technical: Built, Designed, Optimized, Implemented, Architected, Engineered
- Leadership: Led, Managed, Mentored, Coached, Directed, Spearheaded
- Impact: Improved, Increased, Reduced, Accelerated, Transformed, Scaled
- Analysis: Analyzed, Identified, Discovered, Investigated, Evaluated, Assessed

## Optimize Resume Section

Improve an entire section of your resume:

```
optimize_resume_section(
  resume_id="your-resume-id",
  section="experience",
  job_description="Senior Software Engineer at distributed systems company"
)
# Returns: optimized section with improved bullet points and structure
```

**Section Optimization:**

**1. Professional Summary**
- 2-3 lines maximum
- Highlight key achievements and skills
- Tailor to target role
- Include years of experience and specialization

**Example:**
```
Senior Software Engineer with 7+ years building scalable distributed systems at Google and Uber. 
Expertise in system design, microservices, and cloud infrastructure. 
Led teams of 5-10 engineers, mentored 8+ junior developers, and shipped features impacting 100M+ users.
```

**2. Experience Section**
- Use reverse chronological order (most recent first)
- Include company, title, dates, location
- 4-6 bullet points per role (more for recent roles)
- Focus on impact and metrics
- Tailor to job description

**Example:**
```
Senior Software Engineer | Google | Jan 2020 - Present | Mountain View, CA
- Led redesign of payment processing system, reducing transaction failures by 35% and increasing throughput by 2x
- Architected microservices migration for 500K users, improving system reliability to 99.99% uptime
- Mentored 5 junior engineers, with 3 promoted to senior roles within 18 months
- Reduced infrastructure costs by $2M annually through optimization and consolidation
```

**3. Skills Section**
- Organize by category (Languages, Frameworks, Tools, Databases, etc.)
- List skills in order of proficiency
- Include 15-20 relevant skills
- Match job description keywords
- Be honest about proficiency level

**Example:**
```
Languages: Python, Go, Java, SQL, JavaScript
Frameworks: Django, FastAPI, Spring Boot, React
Databases: PostgreSQL, MongoDB, Redis, Cassandra
Cloud: AWS (EC2, S3, Lambda), GCP, Kubernetes
Tools: Git, Docker, Jenkins, Terraform, Datadog
```

**4. Education Section**
- Include degree, school, graduation date
- Add relevant coursework or honors if recent graduate
- Include certifications or relevant courses
- Keep it concise

**Example:**
```
B.S. Computer Science | Stanford University | May 2017
Relevant Coursework: Distributed Systems, Machine Learning, Algorithms
```

## Tailor Resume to Job Description

Optimize your entire resume for a specific job:

```
optimize_resume_for_job(
  resume_id="your-resume-id",
  job_description="Senior Software Engineer - Distributed Systems at Uber"
)
# Returns: tailored resume with optimized sections and keyword matching
```

**Tailoring Strategy:**

1. **Extract Keywords** — Identify key skills, technologies, and requirements from job description
2. **Match Skills** — Highlight relevant skills and experience
3. **Reorder Bullets** — Put most relevant achievements first
4. **Add Keywords** — Incorporate job description language naturally
5. **Emphasize Impact** — Focus on metrics and outcomes that matter to the company
6. **Remove Irrelevant** — De-emphasize or remove less relevant experience

**Example Tailoring:**

**Job Description Keywords:**
- Distributed systems, microservices, scalability
- Python, Go, Kubernetes
- System design, architecture
- Team leadership, mentoring

**Tailored Resume Bullets:**
- ✅ "Architected microservices platform handling 1M+ requests/sec using Go and Kubernetes"
- ✅ "Led system design for distributed cache layer, improving latency by 60%"
- ✅ "Mentored 5 engineers on distributed systems best practices"
- ❌ "Worked on various projects" (too vague)
- ❌ "Used JavaScript for frontend development" (not relevant)

## Resume Optimization Workflow

1. **Check ATS Compatibility** — Ensure your resume passes ATS systems
2. **Get Quality Score** — Identify weak areas
3. **Improve Bullet Points** — Enhance individual achievements
4. **Optimize Sections** — Improve overall structure and content
5. **Tailor to Job** — Customize for specific opportunities
6. **Final Review** — Proofread and verify formatting
7. **Export** — Download as PDF or DOCX

## Best Practices

**Do:**
- ✅ Use specific metrics and numbers
- ✅ Focus on impact and outcomes
- ✅ Tailor to each job description
- ✅ Use action verbs
- ✅ Keep it to 1-2 pages
- ✅ Use consistent formatting
- ✅ Proofread carefully
- ✅ Update regularly with new achievements

**Don't:**
- ❌ Use generic or vague language
- ❌ Include irrelevant experience
- ❌ Use fancy formatting or graphics
- ❌ Lie or exaggerate
- ❌ Include personal information (age, photo, marital status)
- ❌ Use unprofessional email or phone number
- ❌ Have spelling or grammar errors
- ❌ Make it longer than 2 pages

## Resume Templates

Placed offers 37 professional resume templates:

```
list_resume_templates()  # See all available templates
get_template_preview(template_id="modern-blue")  # Preview a template
change_resume_template(resume_id="...", template_id="modern-blue")  # Apply template
```

**Template Categories:**
- **Modern** — Clean, contemporary design
- **Professional** — Traditional, corporate style
- **Creative** — Unique, eye-catching design
- **Minimal** — Simple, ATS-friendly format
- **Academic** — For students and recent graduates

**Choosing a Template:**
- Consider industry (tech, finance, creative, etc.)
- Ensure ATS compatibility
- Match company culture
- Keep it professional
- Test with ATS parser

## Resources

**Resume Writing:**
- "Cracking the Coding Interview" — Resume tips for tech
- "The Muse" — Resume guides and examples
- "Indeed" — Resume builder and tips

**ATS Optimization:**
- Jobscan — ATS compatibility checker
- ResumeWorded — AI resume optimizer
- Placed — Built-in ATS checker and optimizer

**Inspiration:**
- GitHub profiles — Show your work
- Portfolio website — Demonstrate projects
- LinkedIn — Professional presence
- Blind — Salary and resume discussions
