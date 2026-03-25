# Validate a Startup Idea

Validate the user's startup idea using a structured scoring framework with live research.

## Input
Ask the user to describe their idea in 1-2 paragraphs. If they already provided it, proceed.

## Step 1: Classify Industry
Match to one of 13 verticals: SaaS B2B, E-commerce, Mobile App, FinTech, HealthTech, EdTech, Marketplace, FoodTech, PropTech, TravelTech, GameTech, AI/ML, Other. Load benchmarks from @ceo-assistant/docs/industry-benchmarks.md.

## Step 2: Live Market Research (Parallel Agents)
Launch 3 agents in parallel:

**Agent 1 - Market Size:** WebSearch for TAM/SAM data for this specific market. Search for "[industry] market size 2025 2026", "[specific niche] TAM". Extract numbers.

**Agent 2 - Competition:** WebSearch for direct competitors. Search for "[idea keywords] competitors", "[idea keywords] alternatives". Find top 5-10 players, their funding, pricing, positioning.

**Agent 3 - Trends & Timing:** WebSearch for market trends. Search for "[industry] trends 2026", "[technology] adoption rate". Check Google Trends signals.

## Step 2.5: Tar Pit Check (YC/Dalton Caldwell Framework)
Before scoring, check if this idea is a known "tar pit" - concepts that look promising but historically trap founders.

**Known tar pits:** Discovery/recommendation apps, todo/habit trackers, social media "with a twist", restaurant platforms, dating apps (except rare breakouts), standalone AI wrappers around foundation model APIs.

**Tar pit detection criteria:**
- Problem remains unsolved despite many attempts
- Buyers enthusiastically say they'd love a solution
- No large company has been built around this specific problem
- If all 3 are true, likely a tar pit

**The critical question:** "If this has been attempted before, what is fundamentally different NOW?"
- Valid answers: new enabling technology just matured, regulatory change, behavior shift, infrastructure that didn't exist before
- Invalid answers: "better execution", "we're using AI", "mobile-first" (these are not context changes)

**Context changes that untar tarpits:** DSL enabled YouTube, GPU compute enabled AI, smartphones enabled Uber, batteries enabled Tesla. Look for equivalent shifts.

If the idea appears to be a tar pit, flag it prominently in the report with specific evidence and ask: "What has fundamentally changed that makes this work now when it didn't before?"

## Step 3: Score Using Rubric
Apply the weighted scoring rubric from @ceo-assistant/docs/validation-scoring-rubric.md. Score each of 15 criteria 1-10. Calculate weighted total.

## Step 4: Generate Report
Output a structured validation report:

### [Idea Name] - Validation Report

**Viability Score: [X]/100 - [Rating]**

| Category | Weight | Score | Weighted |
|----------|--------|-------|----------|
| Market Timing | 12% | X/10 | X.X |
| Market Size | 10% | X/10 | X.X |
| ... (all 15 criteria) |
| **TOTAL** | **100%** | | **X/100** |

**Industry Benchmarks ([vertical]):**
- Success Rate: X%
- Typical CAC: $X-Y
- Typical LTV: $X-Y
- Time to PMF: X-Y months

**Competitors Found:**
[Table of competitors with funding, pricing, positioning]

**Market Data:**
- Estimated TAM: $X
- Growth Rate: X% CAGR
- Key Trends: [from research]

**GO/NO-GO: [RECOMMENDATION]**

**Next Steps:**
1. [Specific action with cost and timeline]
2. [Specific action]
3. [Specific action]

## Step 5: Offer Follow-ups
Ask: "Want me to: (a) generate a lean canvas, (b) create a competitive analysis deep-dive, (c) build financial projections, or (d) create a pitch deck?"
