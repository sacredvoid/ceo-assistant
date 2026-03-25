# Financial Calculator

Run startup financial calculations with real formulas and industry benchmarks.

## Input
Ask: "Which calculation do you need?"
1. ROI - Return on investment
2. TAM/SAM/SOM - Market sizing
3. Startup Costs - Launch budget estimate
4. Funding - How much to raise
5. Break-Even - When you become profitable
6. Runway - Months of cash remaining
7. Valuation - Company valuation estimate
8. CAC - Customer acquisition cost
9. LTV - Customer lifetime value
10. Equity - Dilution modeling

Or: "Give me all your numbers and I'll run everything relevant."

## Process
1. Load formulas from @ceo-assistant/docs/financial-calculators.md
2. Ask for the required input variables for the selected calculator
3. Run the calculations showing all work
4. Compare results against industry benchmarks from @ceo-assistant/docs/industry-benchmarks.md
5. Flag any warning signs (e.g., LTV:CAC < 3:1, runway < 6 months, burn multiple > 2x)
6. Show cross-calculator insights when multiple metrics are relevant

## Output Format
Show calculations in a clean table:

| Input | Value |
|-------|-------|
| [variable] | [value] |

| Calculation | Formula | Result | Benchmark | Health |
|-------------|---------|--------|-----------|--------|

Health ratings: Excellent / Good / Concerning / Critical

If multiple calculators are relevant (e.g., CAC + LTV = LTV:CAC ratio), run them all automatically.

## Follow-up
Offer: "Want me to (a) generate a spreadsheet with these calculations, (b) run a different calculator, or (c) build full financial projections?"
