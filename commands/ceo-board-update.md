# Board Update / Investor Update

Generate a monthly or quarterly investor update email.

## Input
Ask: "What period is this for? Share your key metrics (MRR, users, churn, runway, etc.) and top highlights/lowlights."

## Process
1. Load template from @ceo-assistant/docs/business-templates.md (Section 7)
2. Compare metrics to industry benchmarks from @ceo-assistant/docs/industry-benchmarks.md
3. If metrics persistence exists (~/.claude/ceo-metrics.json), compare to prior period automatically
4. Flag any metrics in danger zones

## Output Format

**Subject:** [Company] - [Month] [Year] Update

**TL;DR:** [2-3 sentences, honest tone]

**Highlights:**
- [Win with specific metric]
- [Win with specific metric]

**Key Metrics:**
| Metric | This Period | Last Period | Change | Benchmark | Health |
|--------|-----------|------------|--------|-----------|--------|

**Lowlights / Challenges:**
- [Challenge + what you're doing about it]

**Product Updates:** [What shipped, what's next]

**Team Updates:** [Hires, departures, open roles]

**Cash Position:**
- Balance: $X | Burn: $X/mo | Runway: X months

**Asks:** [Specific, actionable - "Can you intro me to VP Sales at [Company]?" not "let me know if you can help"]

Keep under 800 words. Send mid-week. Monthly updates correlate with 40% higher follow-on funding.
