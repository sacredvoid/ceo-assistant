# Track Startup Metrics

Record, track, and visualize startup metrics over time with trend analysis.

## Commands
- "Record this month's metrics" - saves a snapshot
- "Show my dashboard" - displays current metrics with trends
- "Compare to last month" - shows deltas and health

## First Time Setup
If no metrics file exists at ~/.claude/ceo-metrics.json:
1. Ask: "What's your company name and industry?"
2. Ask for current metrics (offer defaults based on industry)
3. Create initial snapshot

## Recording Metrics
1. Load last snapshot from ~/.claude/ceo-metrics.json
2. Ask for updated values (pre-fill with last known)
3. Calculate derived metrics automatically:
   - LTV = ARPU x Gross Margin x (1 / Churn Rate)
   - LTV:CAC = LTV / CAC
   - Runway = Cash / Net Burn
   - Burn Multiple = Net Burn / Net New ARR
4. Save new snapshot with today's date

## Dashboard Display

### [Company] - Metrics Dashboard ([date])

| Metric | Current | Last Month | Change | Benchmark | Health |
|--------|---------|-----------|--------|-----------|--------|
| MRR | | | | | |
| Customers | | | | | |
| Churn Rate | | | | <5% | |
| CAC | | | | [industry] | |
| LTV | | | | [industry] | |
| LTV:CAC | | | | >3:1 | |
| Burn Rate | | | | | |
| Cash | | | | | |
| Runway | | | | >18mo | |

Health: use benchmarks from @ceo-assistant/docs/industry-benchmarks.md
- Green: meeting or exceeding benchmark
- Yellow: within 20% of benchmark
- Red: significantly below

## Alerts
- Runway < 6 months: "CRITICAL: Start fundraising immediately"
- Churn > 5% monthly: "WARNING: Churn is unsustainable. Address retention."
- LTV:CAC < 2:1: "WARNING: Unit economics need work before scaling."
- No MRR growth for 2+ months: "STALL: Growth has plateaued."
- Burn Multiple > 3x: "WARNING: Spending efficiency is poor."

## Trend Analysis (3+ snapshots)
Show MoM growth rate, churn direction, runway trajectory, and whether metrics are improving or declining.

## Storage Format
File: ~/.claude/ceo-metrics.json
```json
{
  "company": "Name",
  "industry": "SaaS B2B",
  "snapshots": [
    {
      "date": "2026-03-25",
      "metrics": { "mrr": 15000, "customers": 150, ... }
    }
  ]
}
```
