# Generate Financial Spreadsheet

Create an Excel spreadsheet with startup financial calculations.

## Input
Ask: "What do you need in the spreadsheet?"
Options:
1. Financial projections (3-year P&L, MRR waterfall, cash flow)
2. Unit economics dashboard (CAC, LTV, payback, margins)
3. Fundraising model (round sizing, dilution, cap table)
4. Runway calculator (burn rate, cash position, zero-cash date)
5. All of the above (full financial model)

## Process
1. Collect the user's actual numbers (or help them estimate)
2. Load formulas from @ceo-assistant/docs/financial-calculators.md
3. Use the xlsx skill to generate an actual .xlsx file with:
   - Formatted headers and sections
   - Formulas in cells (not just values)
   - Conditional formatting for health indicators (green/yellow/red)
   - Charts where appropriate (MRR growth, runway burn-down)
   - Multiple sheets if needed (P&L, Cash Flow, Unit Economics, Cap Table)
4. Save to current directory or user-specified location

## Sheet Templates

### P&L Sheet:
Rows: Revenue, COGS, Gross Profit, S&M, R&D, G&A, EBITDA, Net Income
Columns: Monthly for Year 1, Quarterly for Years 2-3

### Unit Economics Sheet:
Rows: ARPU, CAC, LTV, LTV:CAC, Payback Period, Gross Margin, Churn Rate, NRR
Include: industry benchmark column for comparison

### Cap Table Sheet:
Rows: Founders (each), Option Pool, Seed Investors, Series A
Columns: Shares, %, Pre-money value
Model multiple round scenarios

### Runway Sheet:
Monthly: Cash balance, Revenue, Expenses, Net burn, Remaining months
Chart: Cash burn-down projection with zero-cash date marked

## Output
Actual .xlsx file saved to disk. Tell the user where it is.
