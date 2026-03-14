# placed-career-tools

Research companies, benchmark salaries, negotiate offers, and make data-driven career decisions.

## Tools

- `research_company` - Get company info, culture, news, ratings, funding
- `get_company_salary_data` - Benchmark salaries by role and location
- `generate_salary_negotiation_script` - Prepare negotiation talking points
- `analyze_offer` - Evaluate job offers against market rates
- `get_subscription_status` - Check subscription tier and limits
- `get_usage_stats` - View usage breakdown by feature
- `get_usage_limits` - Check remaining quota

## Company Research

Get comprehensive company information:

```
research_company(company_name="Google")
# Returns: culture, recent news, ratings, funding, growth trajectory, employee reviews
```

**What You Get:**
- Company culture and values
- Recent news and announcements
- Employee ratings and reviews
- Funding and growth stage
- Company size and locations
- Industry and market position

**Use Cases:**
- Prepare for interviews (understand company mission and values)
- Evaluate cultural fit
- Understand company stability and growth
- Research leadership and recent changes
- Identify potential red flags

## Salary Benchmarking

Get market data for your target role:

```
get_company_salary_data(
  company_name="Google",
  position="Senior Software Engineer",
  location="San Francisco"
)
# Returns: salary ranges, percentiles, bonus %, equity, market trends
```

**What You Get:**
- Base salary range (10th, 25th, 50th, 75th, 90th percentile)
- Bonus percentage and range
- Equity grants (stock options or RSUs)
- Total compensation range
- Market trends and historical data
- Comparison to industry averages

**How to Use:**
1. Research 3-5 similar roles at different companies
2. Identify your target salary range (aim for 60-75th percentile)
3. Factor in location, experience, and specialization
4. Consider total compensation (salary + bonus + equity)
5. Use this data in negotiations

**Salary Factors:**
- **Experience** — Years in role, seniority level
- **Location** — SF Bay Area, NYC, Seattle, remote
- **Company Stage** — Startup, scale-up, public company
- **Industry** — Tech, finance, healthcare, etc.
- **Specialization** — ML, DevOps, full-stack, etc.
- **Negotiation Skill** — Your ability to negotiate

## Salary Negotiation

Generate negotiation scripts and talking points:

```
generate_salary_negotiation_script(
  current_offer=200000,
  target_salary=250000,
  justification=[
    "5+ years experience in distributed systems",
    "Led 3 major projects with 10M+ user impact",
    "Market rate for Senior Engineer in SF is $240-280K",
    "Proven track record of mentoring junior engineers"
  ]
)
# Returns: conservative, balanced, aggressive scripts with email templates
```

**Negotiation Strategies:**

**1. Conservative Approach**
- Polite, collaborative tone
- Focus on market data
- Ask for modest increase
- Good for: Risk-averse candidates, early-career

**2. Balanced Approach**
- Professional, confident tone
- Combine market data with accomplishments
- Ask for reasonable increase
- Good for: Most candidates, mid-career

**3. Aggressive Approach**
- Assertive, data-driven tone
- Emphasize unique value and accomplishments
- Ask for significant increase
- Good for: High-demand skills, senior roles, multiple offers

**Negotiation Tips:**

1. **Research First**
   - Get market data from Placed, Levels.fyi, Blind, Glassdoor
   - Know your target range (not a single number)
   - Understand company's budget and constraints

2. **Know Your Value**
   - Document accomplishments with metrics
   - Highlight unique skills and experience
   - Prepare examples of impact

3. **Timing**
   - Negotiate after offer, not before
   - Don't accept immediately
   - Give yourself 24-48 hours to think

4. **Approach**
   - Be professional and collaborative
   - Focus on market data, not personal needs
   - Emphasize mutual benefit
   - Ask questions about flexibility

5. **Negotiation Points**
   - Base salary (most important)
   - Sign-on bonus (especially for equity vesting)
   - Annual bonus percentage
   - Equity grants and vesting schedule
   - Remote work flexibility
   - Professional development budget
   - Vacation days
   - Start date flexibility

6. **What NOT to Do**
   - Don't be aggressive or demanding
   - Don't mention personal financial needs
   - Don't accept the first offer
   - Don't negotiate via email if possible (phone is better)
   - Don't burn bridges

7. **If They Say No**
   - Ask what would make it possible
   - Propose alternative benefits
   - Negotiate start date or sign-on bonus
   - Accept gracefully and revisit in 6-12 months

**Example Email:**

```
Hi [Hiring Manager],

Thank you for the offer for Senior Software Engineer at [Company]. I'm excited about the opportunity and the team.

I've researched market rates for this role in [Location], and the typical range is $240-280K base salary. Given my 5+ years of experience in distributed systems and track record of leading high-impact projects, I'd like to request a base salary of $260K.

I'm also open to discussing other components of the package, such as sign-on bonus or equity, if that works better for the budget.

I'm very interested in joining the team and believe this adjustment reflects fair market value for the role.

Looking forward to discussing this further.

Best regards,
[Your Name]
```

## Offer Analysis

Evaluate job offers comprehensively:

```
analyze_offer(
  company="Google",
  position="Senior Engineer",
  base_salary=250000,
  location="San Francisco",
  bonus=50000,
  equity="0.5% over 4 years"
)
# Returns: market comparison, total comp, recommendations, trade-offs
```

**What You Get:**
- Market comparison (how offer compares to similar roles)
- Total compensation breakdown
- Equity value and vesting schedule
- Bonus structure and likelihood
- Benefits comparison
- Recommendations and trade-offs

**How to Compare Offers:**

1. **Calculate Total Compensation**
   - Base salary
   - Bonus (use realistic percentage, not max)
   - Equity value (annualized over vesting period)
   - Benefits (health insurance, 401k match, etc.)

2. **Consider Non-Monetary Factors**
   - Career growth and learning opportunities
   - Team quality and culture
   - Work-life balance and flexibility
   - Location and commute
   - Job security and company stability
   - Mission and impact

3. **Evaluate Equity**
   - Vesting schedule (typically 4 years with 1-year cliff)
   - Strike price (for options) or grant price (for RSUs)
   - Company stage and exit potential
   - Dilution risk (for startups)

4. **Compare Multiple Offers**
   - Use spreadsheet to compare side-by-side
   - Weight factors by importance to you
   - Consider long-term career impact
   - Don't just optimize for highest salary

## Subscription Management

Check your Placed subscription and usage:

```
get_subscription_status()
# Returns: current tier, limits, features, renewal date

get_usage_stats(date_range="30d")
# Returns: usage breakdown by feature (job matches, cover letters, AI optimizations, etc.)

get_usage_limits()
# Returns: remaining quota for each feature
```

**Subscription Tiers:**
- **Free** — Limited features, basic tools
- **Pro** — Full access to all tools, higher limits
- **Premium** — Unlimited usage, priority support

## Career Decision Framework

Use this framework to make career decisions:

1. **Gather Data**
   - Research companies (culture, stability, growth)
   - Benchmark salaries (market rates, percentiles)
   - Analyze offers (total comp, benefits, equity)

2. **Evaluate Factors**
   - Compensation (salary, bonus, equity)
   - Career growth (learning, opportunities, mentorship)
   - Work environment (team, culture, flexibility)
   - Impact (mission, scale, influence)
   - Stability (company health, job security)

3. **Weight by Importance**
   - What matters most to you right now?
   - Short-term vs. long-term goals
   - Risk tolerance and preferences

4. **Make Decision**
   - Compare options side-by-side
   - Trust your gut feeling
   - Negotiate if needed
   - Commit fully to your choice

## Resources

**Salary Research:**
- Levels.fyi — Crowdsourced salary data by company and level
- Blind — Anonymous employee discussions and salary sharing
- Glassdoor — Company reviews and salary reports
- PayScale — Salary calculator and market data

**Company Research:**
- Company websites and investor relations
- LinkedIn company pages
- Crunchbase — Funding and company info
- News sources — Recent announcements and changes

**Negotiation:**
- "Never Split the Difference" by Chris Voss — Negotiation tactics
- "Salary Negotiation" guides on Blind and Reddit
- Placed's salary negotiation scripts and templates
