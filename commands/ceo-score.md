# Score Idea Viability

Quick viability scoring using a weighted 15-criteria rubric. For full validation with live research, use /ceo-validate instead.

## Input
Ask: "Describe your idea and target market in 2-3 sentences."

## Process
Load scoring rubric from @ceo-assistant/docs/validation-scoring-rubric.md

Score each criterion 1-10 using the explicit guidelines in the rubric. Show your reasoning for each score.

## The 15 Criteria

| # | Criterion | Weight |
|---|-----------|--------|
| 1 | Market Timing | 12% |
| 2 | Market Size (TAM) | 10% |
| 3 | Market Growth Rate | 8% |
| 4 | Problem Severity | 8% |
| 5 | Willingness to Pay | 8% |
| 6 | Competition Intensity | 7% |
| 7 | Differentiation Strength | 7% |
| 8 | Business Model Clarity | 6% |
| 9 | Unit Economics Feasibility | 6% |
| 10 | Founder-Market Fit | 6% |
| 11 | Technical Feasibility | 5% |
| 12 | Regulatory Risk | 5% |
| 13 | Scalability | 4% |
| 14 | Distribution Advantage | 4% |
| 15 | Defensibility/Moat | 4% |

## Scoring
For each: Score (1-10) x Weight x 10 = weighted points. Sum all = final score out of 100.

## Output

### [Idea] - Viability Score: [X]/100 ([Rating])

| # | Criterion | Weight | Score | Points | Rationale |
|---|-----------|--------|-------|--------|-----------|
| 1 | Market Timing | 12% | X/10 | X.X | [1-line reason] |
| ... | | | | | |
| **TOTAL** | | **100%** | | **X/100** | |

**Top 3 Strengths:** [highest scoring criteria]
**Top 3 Risks:** [lowest scoring criteria]

**Interpretation:**
- 85-100: Exceptional (89% historical success) - proceed with confidence
- 75-84: Strong (75%) - address flagged weaknesses
- 65-74: Moderate (52%) - validate further before committing
- 50-64: Weak (28%) - major pivots needed
- 0-49: Very Weak (8%) - explore different ideas

**To improve score:** [specific actions to raise the lowest-scoring criteria]

### Additional Checks

**Tar Pit Detection (YC/Dalton Caldwell):**
Before finalizing score, check: Has this been attempted many times before with zero large companies built? If yes, the critical question is "what's fundamentally different NOW?" (technology shift, regulation change, behavior change - not just "better execution").

Known tar pits: discovery/recommendation apps, todo/habit trackers, social media "with a twist", restaurant platforms, standalone AI wrappers.

**YC's 10-5-20 Pricing Sanity Check (Kevin Hale):**
- Price at 1/10th of value delivered
- Increase by 5% iteratively
- Keep increasing until you lose 20% of deals
- 80% of YC companies are charging too little

**Weekly Growth Benchmark:**
- 5-7% week-over-week = good
- 10% WoW = exceptional
- Below 1% WoW = red flag

If score >= 65: "Run /ceo-validate for full validation with live market research."
