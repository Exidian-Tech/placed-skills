# placed-interview-coach

Master technical, system design, and behavioral interviews with AI coaching, real-time feedback, and STAR story banking.

## Tools

- `start_interview_session` - Begin mock interview for a specific role
- `continue_interview_session` - Answer questions and get feedback
- `get_interview_feedback` - Get detailed performance analysis
- `list_interview_cases` - Browse system design cases
- `start_system_design` - Start system design interview
- `get_behavioral_questions` - Get behavioral questions
- `save_story_to_bank` - Save STAR stories for reuse

## Interview Types

### 1. Technical Interviews (Coding)

Start a mock interview for a specific job role:

```
start_interview_session(
  resume_id="your-resume-id",
  job_title="Senior Software Engineer",
  difficulty="hard",
  company="Google"
)
```

Then answer each question:

```
continue_interview_session(
  session_id="session-123",
  user_answer="I would use a hash map to store key-value pairs for O(1) lookup..."
)
```

Get feedback on your performance:

```
get_interview_feedback(session_id="session-123")
```

**Tips:**
- Explain your approach before coding
- Discuss time and space complexity
- Consider edge cases
- Ask clarifying questions
- Walk through examples

### 2. System Design Interviews

List available cases:

```
list_interview_cases()
# Returns: Design Twitter, Design URL Shortener, Design Netflix, Design Uber, etc.
```

Start a system design session:

```
start_system_design(
  case_id="design-twitter",
  difficulty="senior"
)
```

**Common Cases:**
- **URL Shortener** — Hash functions, collision handling, database design, scalability
- **Twitter** — Feed generation, real-time updates, distributed systems, caching
- **Netflix** — Video streaming, CDN, recommendation engine, fault tolerance
- **Uber** — Geolocation, real-time matching, scalability, consistency
- **Instagram** — Photo storage, feed ranking, notifications, sharding

**System Design Framework:**
1. **Requirements Clarification** — Functional and non-functional requirements
2. **High-Level Architecture** — Components, data flow, APIs
3. **Database Design** — Schema, indexing, replication, sharding
4. **Scalability** — Load balancing, caching, CDN, horizontal scaling
5. **Fault Tolerance** — Redundancy, failover, monitoring
6. **Trade-offs** — CAP theorem, consistency vs. availability, latency vs. throughput

**Reference Material:**
Use `qmd search` to research system design patterns:
```bash
qmd search "system design interview URL shortener Twitter distributed"
qmd search "system design scalability load balancing database"
```

Best resources:
- **Grokking the System Design Interview** — Step-by-step methodology, real examples
- **System Design Interview by Alex Xu** — Deep dives on distributed systems, CAP theorem, Merkle trees
- **Educative System Design** — Comprehensive coverage of scalability, load balancing, caching

### 3. Behavioral Interviews

Get behavioral questions for your target role:

```
get_behavioral_questions(
  target_role="Engineering Manager",
  focus_categories=["leadership", "conflict-resolution", "failure"]
)
```

**STAR Method** — Structure every answer:
- **Situation** — Context and background
- **Task** — Your responsibility and challenge
- **Action** — What you did specifically
- **Result** — Outcome with metrics

**Common Categories:**
- **Leadership** — Led a team, mentored someone, made a difficult decision
- **Conflict Resolution** — Disagreed with a colleague, handled a difficult person
- **Failure** — Project that failed, mistake you made, lesson learned
- **Teamwork** — Collaborated across teams, helped someone succeed
- **Initiative** — Took ownership, improved a process, solved a problem
- **Pressure** — Tight deadline, high stakes, competing priorities

**Example STAR Story:**

```
Situation: "Our team was shipping a critical feature but discovered a major performance issue 2 days before launch."

Task: "As tech lead, I needed to decide whether to delay launch or ship with degraded performance."

Action: "I analyzed the issue, found it was in a specific component. I created a phased rollout plan: ship to 10% of users first, monitor metrics, then gradually increase. I also assigned a junior engineer to optimize the component in parallel."

Result: "We shipped on time, caught the issue early with minimal user impact, and the optimization was ready within a week. The junior engineer gained valuable experience. This became our standard approach for risky launches."
```

### 4. Story Banking

Save STAR stories for reuse across interviews:

```
save_story_to_bank(
  situation="Led team through major refactor",
  task="Reduce technical debt while shipping features",
  action="Created phased plan, mentored junior devs, set clear milestones",
  result="30% faster deployments, improved morale, reduced bugs by 25%",
  category="leadership"
)
```

**Build Your Story Bank:**
- 3-5 stories per category
- Include specific metrics and outcomes
- Mix technical and people-focused stories
- Update stories as you gain new experiences

## Interview Flow

1. **Prepare** — Research company, review resume, practice with qmd resources
2. **Start Session** — Begin mock interview with your resume and target role
3. **Answer Questions** — Think out loud, explain your reasoning
4. **Get Feedback** — Review performance after each question
5. **Iterate** — Practice multiple times, improve weak areas
6. **Save Stories** — Bank STAR stories for behavioral interviews
7. **Review** — Study system design patterns and common questions

## Interview Tips

**Technical Interviews:**
- Clarify requirements before diving into code
- Discuss trade-offs (time vs. space, simplicity vs. optimization)
- Test your solution with examples
- Explain your thought process
- Ask for hints if stuck

**System Design:**
- Start with requirements and constraints
- Draw diagrams and explain components
- Discuss scalability bottlenecks
- Consider failure scenarios
- Mention monitoring and alerting

**Behavioral:**
- Use STAR method consistently
- Include specific metrics and outcomes
- Show growth and learning
- Be authentic and honest
- Ask thoughtful questions about the role

**General:**
- Research the company and role thoroughly
- Practice explaining technical concepts simply
- Get good sleep before the interview
- Dress professionally
- Arrive early (or log in early for virtual)
- Ask thoughtful questions at the end
- Send a thank-you note after

## Resources

**System Design Books (via qmd):**
- Grokking the System Design Interview — Best for interview prep
- System Design Interview by Alex Xu — Deep technical content
- Educative System Design — Comprehensive coverage

**Behavioral Interview:**
- Engineering Managers Handbook — Leadership and people skills
- Leading Effective Engineering Teams — Team dynamics and conflict resolution

Search with qmd:
```bash
qmd search "system design interview URL shortener Twitter distributed"
qmd search "behavioral interview STAR method engineering manager"
qmd search "system design scalability load balancing database"
```
