# Financial Calculators Reference

Complete formulas, benchmarks, and interpretation guidelines for startup financial analysis. 14 calculators covering unit economics, efficiency, valuation, and growth health.

---

## Table of Contents

1. [ROI Calculator](#1-roi-calculator)
2. [Market Size (TAM/SAM/SOM)](#2-market-size-tamsamsom)
3. [Startup Cost Calculator](#3-startup-cost-calculator)
4. [Funding Calculator](#4-funding-calculator)
5. [Break-Even Calculator](#5-break-even-calculator)
6. [Runway Calculator](#6-runway-calculator)
7. [Valuation Calculator](#7-valuation-calculator)
8. [CAC Calculator](#8-cac-calculator)
9. [LTV Calculator](#9-ltv-calculator)
10. [Equity Dilution Calculator](#10-equity-dilution-calculator)
11. [Cross-Calculator Relationships](#cross-calculator-relationships)
12. [SaaS Magic Number](#11-saas-magic-number)
13. [Burn Multiple](#12-burn-multiple)
14. [SaaS Quick Ratio](#13-saas-quick-ratio)
15. [Rule of X Calculator](#14-rule-of-x-calculator)

---

## 1. ROI Calculator

Measures the efficiency and profitability of an investment relative to its cost.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Initial Investment | Currency | Total capital deployed upfront |
| Total Returns | Currency | Cumulative value received back (including principal) |
| Time Period | Years | Duration of the investment |
| Discount Rate | Percentage | Required rate of return (for NPV) |

### Formulas

```
Basic ROI = ((Total Returns - Initial Investment) / Initial Investment) x 100

Annualized ROI = ((1 + ROI)^(1/years) - 1) x 100

Net Present Value (NPV) = -Investment + Sum of [Returns_n / (1 + r)^n]
  where r = discount rate, n = year number

Return Multiple = Total Returns / Initial Investment
```

### Benchmarks

| Investment Type | Typical ROI Range |
|----------------|-------------------|
| S&P 500 (annual, historical) | 7-12% |
| VC Returns (5-10 year horizon) | 500-1000%+ |
| SaaS Marketing ROI | 200-500% |
| Real Estate (annual) | 8-20% |
| Angel Investing (portfolio) | 20-30% annualized |

### Interpretation

| ROI | Assessment |
|-----|-----------|
| Negative | Loss on investment |
| 0-10% | Low, comparable to passive index investing |
| 10-50% | Moderate, healthy for established businesses |
| 50-200% | Strong, good for growth-stage investments |
| 200%+ | Exceptional, typical of successful venture bets |

**Key notes:**
- Always compare ROI to opportunity cost (what else could the capital do).
- Annualized ROI is the proper comparison metric across investments with different time horizons.
- NPV accounts for the time value of money; a positive NPV means the investment exceeds the required return rate.
- Return Multiple of 1.0x = break-even, 3x+ = strong venture outcome, 10x+ = home run.

---

## 2. Market Size (TAM/SAM/SOM)

Quantifies the revenue opportunity at three levels of scope.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Total Potential Customers | Number | Everyone who could theoretically buy |
| Annual Spending per Customer | Currency | Average yearly spend in the category |
| Targetable Segment % | Percentage | Portion reachable by your business model |
| Realistic Capture % | Percentage | Market share you can win in 1-3 years |
| Annual Growth Rate | Percentage | Expected market growth rate |

### Formulas

```
TAM (Total Addressable Market) = Total Potential Customers x Annual Spending per Customer

SAM (Serviceable Addressable Market) = TAM x Targetable Segment %
  (filtered by geography, channel, product fit, business model constraints)

SOM (Serviceable Obtainable Market) = SAM x Realistic Capture %
  (what you can actually win given competition, resources, time)

Projected TAM (Year N) = Current TAM x (1 + Growth Rate)^N
```

### Benchmarks

| Metric | Threshold |
|--------|-----------|
| VC-investable TAM | $1B+ |
| Attractive TAM growth | 15%+ annually |
| Realistic SOM (years 1-3) | 1-5% of SAM |
| Mature company market share | 10-30% of SAM |
| Market leader share | 30%+ of SAM |

### Interpretation

| TAM Size | Assessment |
|----------|-----------|
| < $100M | Niche, likely not VC-fundable |
| $100M-$1B | Mid-size, suitable for bootstrapped or seed-stage |
| $1B-$10B | Attractive for Series A+ venture funding |
| $10B+ | Large market, strong VC interest if team is credible |

**Key notes:**
- Top-down TAM (industry reports) tends to be inflated. Bottom-up TAM (counting actual customers x price) is more credible.
- Investors focus on SAM for near-term revenue potential and TAM for long-term ceiling.
- SOM above 10% in year 1 is unrealistic for most startups and signals weak analysis.

---

## 3. Startup Cost Calculator

Estimates total capital needed to launch and sustain operations through initial months.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Legal & Incorporation | Currency | Entity formation, IP filings, contracts |
| Technology & Development | Currency | Software, hosting, tools, dev costs |
| Marketing & Branding | Currency | Launch campaigns, website, content |
| Office & Equipment | Currency | Space, furniture, hardware |
| Salaries & Contractors | Currency | Team compensation |
| Inventory & COGS | Currency | Physical goods (if applicable) |
| Other / Miscellaneous | Currency | Insurance, travel, subscriptions |
| Monthly Burn Rate | Currency | Ongoing monthly operating cost |
| Months of Runway | Number | How many months to fund beyond launch |

### Formulas

```
Total Launch Cost = Legal + Technology + Marketing + Office + Salaries + Inventory + Other

Buffer (20% contingency) = Total Launch Cost x 0.20

Total with Buffer = Total Launch Cost + Buffer

Extended Runway Cost = Total with Buffer + (Monthly Burn x Months of Runway)
```

### Benchmarks by Business Type

| Business Type | Typical Range |
|--------------|---------------|
| Solo SaaS (bootstrapped) | $5K-$20K |
| Small Team SaaS (2-5 people) | $50K-$150K |
| E-commerce | $10K-$50K |
| Mobile App | $25K-$100K |
| Hardware / Physical Product | $100K-$500K |
| Marketplace / Platform | $50K-$200K |
| Consulting / Services | $2K-$15K |

### Interpretation

- Always add the 20% buffer. Startups consistently underestimate costs.
- If Extended Runway Cost exceeds available capital, either reduce scope, extend timeline, or raise funding.
- Technology is typically the largest cost center for software startups (40-60% of total).
- Plan for at least 12-18 months of runway from day one.

---

## 4. Funding Calculator

Determines how much capital to raise based on burn rate, runway needs, and expected dilution.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Monthly Burn Rate | Currency | Net cash outflow per month |
| Target Runway | Months | How many months the raise should fund |
| Buffer Percentage | Percentage | Safety margin above minimum (typically 20-30%) |
| Pre-Money Valuation | Currency | Company value before investment |
| Expected Dilution | Percentage | Ownership given up per round |

### Formulas

```
Minimum Raise = Monthly Burn x Target Runway

Total Raise = Minimum Raise x (1 + Buffer %)

Implied Post-Money = Total Raise / Expected Dilution %

Implied Pre-Money = Implied Post-Money - Total Raise
```

### Benchmarks by Stage

| Stage | Typical Raise | Typical Dilution | Typical Valuation |
|-------|--------------|-------------------|-------------------|
| Pre-Seed | $50K-$500K | 10-15% | $500K-$3M |
| Seed | $500K-$3M | 15-25% | $3M-$15M |
| Series A | $5M-$20M | 20-30% | $20M-$80M |
| Series B | $15M-$50M | 15-25% | $80M-$250M |
| Series C+ | $50M-$200M+ | 10-20% | $250M-$1B+ |

### Interpretation

| Months Until Cash-Out | Action |
|-----------------------|--------|
| 12+ months | No urgency, plan strategically |
| 9-12 months | Begin fundraising process now |
| 6-9 months | Actively fundraise, high priority |
| < 6 months | Emergency mode, consider bridge rounds or cost cuts |

**Key notes:**
- Fundraising typically takes 3-6 months from first meeting to wire.
- Begin fundraising when you have 9+ months of runway remaining.
- Raising too little creates constant fundraising pressure. Raising too much increases dilution unnecessarily.
- Target 18-24 months of runway per round.
- Total founder dilution across all rounds typically lands at 50-70% by Series C.

---

## 5. Break-Even Calculator

Identifies the point at which revenue covers all costs, producing zero profit or loss.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Fixed Costs | Currency | Rent, salaries, software, insurance (monthly or annual) |
| Price per Unit | Currency | Revenue per unit sold or per subscription |
| Variable Cost per Unit | Currency | Cost directly tied to each unit (COGS, support) |
| Actual Sales Volume | Units | Current or projected sales |

### Formulas

```
Contribution Margin = Price per Unit - Variable Cost per Unit

Contribution Margin Ratio = Contribution Margin / Price per Unit

Break-Even Units = Fixed Costs / Contribution Margin

Break-Even Revenue = Fixed Costs / Contribution Margin Ratio

Margin of Safety = (Actual Sales - Break-Even Sales) / Actual Sales x 100

Operating Leverage = Contribution Margin / Net Income
```

### Benchmarks by Industry

| Business Type | Typical Gross Margin | Break-Even Timeline |
|--------------|---------------------|---------------------|
| SaaS | 70-90% | 12-24 months |
| E-commerce | 30-50% | 6-18 months |
| Services / Consulting | 50-70% | 3-12 months |
| Marketplace | 60-80% | 18-36 months |
| Hardware | 30-50% | 12-30 months |

### Interpretation

| Margin of Safety | Assessment |
|-----------------|-----------|
| Negative | Operating below break-even, losing money |
| 0-10% | Barely profitable, vulnerable to any downturn |
| 10-25% | Adequate buffer |
| 25-50% | Healthy, resilient to moderate revenue drops |
| 50%+ | Strong position, significant cushion |

**Key notes:**
- Higher contribution margins mean fewer units needed to break even.
- SaaS break-even analysis should use monthly recurring costs vs. MRR.
- For multi-product businesses, use weighted average contribution margin.
- Operating leverage amplifies both gains and losses past break-even.

---

## 6. Runway Calculator

Calculates how many months a startup can operate before running out of cash.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Cash on Hand | Currency | Current bank balance |
| Monthly Expenses | Currency | Total monthly operating costs |
| Monthly Revenue | Currency | Current monthly income |
| Monthly Revenue Growth | Percentage | Expected month-over-month revenue increase |
| Monthly Expense Growth | Percentage | Expected month-over-month cost increase |

### Formulas

```
Gross Burn Rate = Monthly Expenses

Net Burn Rate = Monthly Expenses - Monthly Revenue

Runway (months) = Cash on Hand / Net Burn Rate

Zero-Revenue Runway = Cash on Hand / Gross Burn Rate
```

**Default Alive / Default Dead determination:**

```
For each future month (iterative projection):
  Revenue_n = Revenue_(n-1) x (1 + Revenue Growth Rate)
  Expenses_n = Expenses_(n-1) x (1 + Expense Growth Rate)
  Net Burn_n = Expenses_n - Revenue_n
  Cash_n = Cash_(n-1) - Net Burn_n

Default Alive = Revenue exceeds Expenses before Cash hits zero
Default Dead = Cash hits zero before Revenue exceeds Expenses
```

### Benchmarks

| Runway Remaining | Health Status | Action |
|-----------------|---------------|--------|
| 0-6 months | CRITICAL | Immediate cost cuts, emergency fundraise, or pivot |
| 6-12 months | CONCERNING | Begin fundraising, reduce non-essential spend |
| 12-18 months | ADEQUATE | Plan next round, optimize growth spend |
| 18-24 months | HEALTHY | Focus on growth and hitting milestones |
| 24+ months | STRONG | Invest aggressively in growth |

### Interpretation

- "Default alive" (Paul Graham's framework): at current growth rate, the company reaches profitability before cash runs out, even without raising.
- "Default dead": cash runs out before profitability, meaning the company must raise or die.
- Zero-revenue runway is the worst-case scenario (all revenue disappears overnight).
- Revenue growth projections should be conservative. Use 50-75% of current growth rate for planning.
- Monitor runway monthly. Any month where runway decreases by more than 1 month signals accelerating burn.

---

## 7. Valuation Calculator

Estimates company value using standard startup and small business methodologies.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Annual Revenue | Currency | Trailing 12-month revenue |
| Revenue Growth Rate | Percentage | Year-over-year growth |
| Profit Margin | Percentage | Net income / Revenue |
| Seller's Discretionary Earnings (SDE) | Currency | Net income + owner comp + add-backs |
| Investment Amount | Currency | Capital being invested (for post-money) |
| Pre-Money Valuation | Currency | Value before investment |

### Formulas

```
Revenue Multiple Method:
  Valuation = Annual Revenue x Revenue Multiple

SDE Multiple Method:
  Valuation = SDE x SDE Multiple

Post-Money Valuation = Pre-Money Valuation + Investment Amount

Investor Ownership % = Investment Amount / Post-Money Valuation x 100

Rule of 40 Score = Revenue Growth Rate % + Profit Margin %
  (score >= 40 indicates a healthy, well-balanced SaaS business)

ARR Multiple = Valuation / Annual Recurring Revenue
```

### Revenue Multiple Benchmarks

| Business Type | Revenue Multiple Range |
|--------------|----------------------|
| Public SaaS (median) | 4-6x |
| Private SaaS (median) | ~4.7x |
| SaaS (high growth, >50% YoY) | 8-15x |
| SaaS (moderate growth, 20-50% YoY) | 5-8x |
| SaaS (low growth, <20% YoY) | 3-5x |
| AI startups | 25-30x |
| E-commerce | 1-3x |
| Marketplace | 3-8x |
| Traditional / Services | 1-3x |
| Hardware | 1-2x |

> AI companies valued at 24x ARR vs 19x for non-AI peers (Bessemer Cloud 100 2025).

### SDE Multiple Benchmarks

| Business Profile | SDE Multiple |
|-----------------|-------------|
| Small business (<$500K SDE) | 2-3x |
| Mid-size ($500K-$2M SDE) | 3-4x |
| Larger ($2M+ SDE, strong moat) | 4-6x |

### Rule of 40 Interpretation

| Score | Assessment |
|-------|-----------|
| < 20 | Underperforming, needs improvement in growth or profitability |
| 20-30 | Below average, one metric is weak |
| 30-40 | Acceptable, approaching healthy balance |
| 40-60 | Strong, well-balanced growth and profitability |
| 60+ | Elite, exceptional performance |

**Key notes:**
- Revenue multiples are the most common method for venture-backed startups.
- SDE multiples are standard for small business acquisitions and bootstrapped companies.
- Multiples are heavily influenced by growth rate, retention, and market conditions.
- Public SaaS median multiples compressed to 4-6x in 2024-2025, down from 10-15x in 2021.
- Rule of 40 is primarily used for SaaS businesses at scale ($10M+ ARR). See also Rule of X (Section 14) for a growth-weighted alternative.
- Pre-revenue startups are valued on team, TAM, traction signals, and comparable deals.

---

## 8. CAC Calculator

Measures the cost to acquire a single new customer across channels.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Total Marketing Spend | Currency | All marketing and sales costs in period |
| Total Sales Spend | Currency | Sales team compensation, tools, travel |
| New Customers Acquired | Number | Customers gained in the same period |
| Monthly ARPU | Currency | Average revenue per user per month |
| Gross Margin | Percentage | Revenue minus COGS as a percentage |

### Formulas

```
CAC = (Total Marketing Spend + Total Sales Spend) / New Customers Acquired

Blended CAC = Total Acquisition Spend / Total New Customers (all channels)

Paid CAC = Paid Channel Spend / Paid Channel Customers

Organic CAC = Organic Channel Spend / Organic Channel Customers

CAC Payback Period (months) = CAC / (Monthly ARPU x Gross Margin %)
```

### Benchmarks by Segment

| Customer Segment | Typical CAC Range |
|-----------------|-------------------|
| Consumer / Self-Serve | $10-$100 |
| SMB SaaS | $100-$400 |
| Mid-Market SaaS | $500-$2,000 |
| Enterprise SaaS | $2,000-$20,000+ |

### Benchmarks by Channel

| Channel | Typical CAC |
|---------|-------------|
| Referrals / Word of Mouth | ~$141-$200 |
| Content Marketing / SEO | ~$290-$500 (B2B) |
| Social Media (Organic) | ~$150 |
| Meta Ads (Facebook/Instagram) | ~$230 |
| Google Ads (Search) | ~$802 (B2B) |
| LinkedIn Ads | ~$982 |
| Outbound Sales (SDR) | ~$1,980 |
| Trade Shows / Events | ~$1,000-$5,000 |

> CAC benchmarks updated March 2026 from First Page Sage and Phoenix Strategy Group data. CAC has increased 40-60% across most channels since 2023.

### CAC Payback Interpretation

| Payback Period | Assessment |
|---------------|-----------|
| < 3 months | Excellent, very efficient acquisition |
| 3-6 months | Good, healthy unit economics |
| 6-12 months | Acceptable, typical for mid-market |
| 12-18 months | Concerning, acceptable only for enterprise |
| > 18 months | Poor, unsustainable unless LTV is very high |

**Key notes:**
- Always include fully-loaded costs (salaries, tools, agency fees) in CAC, not just ad spend.
- Track CAC by channel to identify most efficient acquisition paths.
- CAC tends to increase over time as you exhaust the easiest-to-reach customers.
- Paid CAC vs. Organic CAC should be tracked separately. Blended CAC can mask inefficient paid spend.

---

## 9. LTV Calculator

Estimates the total revenue a customer generates over their entire relationship.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Monthly ARPU | Currency | Average revenue per user per month |
| Gross Margin | Percentage | Revenue minus COGS as a percentage |
| Monthly Churn Rate | Percentage | % of customers lost per month |
| Expansion Revenue Rate | Percentage | Monthly upsell/cross-sell rate (optional) |

### Formulas

```
Average Customer Lifespan (months) = 1 / Monthly Churn Rate

LTV (simple) = Monthly ARPU x Average Customer Lifespan

LTV (gross margin adjusted) = Monthly ARPU x Gross Margin % x Average Customer Lifespan

LTV (with expansion) = (Monthly ARPU x (1 + Expansion Rate - Churn Rate) / Churn Rate) x Gross Margin %

LTV:CAC Ratio = LTV / CAC

Annual LTV = LTV / (Average Customer Lifespan / 12)
```

### LTV Benchmarks by Segment

| Customer Segment | Typical LTV Range |
|-----------------|-------------------|
| Consumer / Free-to-Paid | $100-$500 |
| SMB SaaS | $1,000-$5,000 |
| Mid-Market SaaS | $10,000-$50,000 |
| Enterprise SaaS | $50,000-$500,000 |

### LTV:CAC Ratio Interpretation

| Ratio | Assessment |
|-------|-----------|
| < 1:1 | Losing money on every customer. Unsustainable. |
| 1:1 - 2:1 | Critical. Barely breaking even after acquisition costs. |
| 3:1 | Target. The standard benchmark for healthy unit economics. |
| 3:1 - 5:1 | Strong. Efficient acquisition and good retention. |
| 5:1+ | Excellent, but may indicate under-investment in growth. |

### Churn Rate Benchmarks

| Segment | Acceptable Monthly Churn | Acceptable Annual Churn |
|---------|-------------------------|------------------------|
| Enterprise SaaS | < 0.5% | < 5% |
| Mid-Market SaaS | 0.5-1.0% | 5-10% |
| SMB SaaS | 1-3% | 10-30% |
| Consumer Subscription | 3-7% | 30-60% |

### CAC Payback Cross-Reference

| Payback Period | Assessment |
|---------------|-----------|
| < 3 months | Excellent |
| 3-12 months | Good |
| 12-18 months | Acceptable for enterprise only |
| > 18 months | Poor, review acquisition strategy |

**Key notes:**
- LTV should always use gross margin, not raw revenue. Gross-margin-adjusted LTV reflects actual profit from the customer.
- Net revenue retention > 100% means expansion revenue exceeds churn, making LTV theoretically infinite (cap at a reasonable horizon like 5-7 years).
- LTV:CAC of 3:1 is the gold standard, but context matters. Enterprise deals with 5:1 may signal under-spending on sales.
- LTV projections based on early cohorts are unreliable. Use 12+ months of data when possible.

---

## 10. Equity Dilution Calculator

Models how founder ownership changes through fundraising rounds.

### Inputs

| Field | Type | Description |
|-------|------|-------------|
| Pre-Money Valuation | Currency | Company value before investment |
| Investment Amount | Currency | Capital being invested |
| Current Founder Ownership | Percentage | Founder's ownership before this round |
| Option Pool | Percentage | Employee equity pool (created pre-money) |
| Exit Valuation | Currency | Projected acquisition or IPO valuation |

### Formulas

```
Post-Money Valuation = Pre-Money Valuation + Investment Amount

Investor Ownership % = (Investment Amount / Post-Money Valuation) x 100

New Founder Ownership % = Previous Founder % x (Pre-Money Valuation / Post-Money Valuation)

Effective Pre-Money (with option pool) = Pre-Money Valuation - (Option Pool % x Post-Money Valuation)

Price Per Percentage Point = Investment Amount / Investor Ownership %

Founder Exit Payout = Exit Valuation x Final Founder Ownership %

Total Dilution After N Rounds:
  Remaining Ownership = Initial % x Product of [(Pre-Money_n / Post-Money_n) for each round n]
```

### Dilution Benchmarks by Stage

| Stage | Typical Dilution per Round | Cumulative Founder Ownership After |
|-------|---------------------------|-----------------------------------|
| Founding | 0% | 100% (split among co-founders) |
| Option Pool (initial) | 10-15% | 85-90% |
| Pre-Seed | 10-15% | 72-81% |
| Seed | 15-25% | 54-69% |
| Series A | 20-30% | 38-55% |
| Series B | 15-25% | 28-47% |
| Series C+ | 10-20% | 23-42% |

### Interpretation

| Final Founder Ownership | Assessment |
|------------------------|-----------|
| 50%+ at Series A | Strong, maintained significant control |
| 30-50% at exit | Healthy, typical for successful outcomes |
| 15-30% at exit | Normal for companies that raised multiple rounds |
| < 15% at exit | Heavy dilution, but can still be life-changing at large exits |

**Key notes:**
- Option pool is almost always created from the pre-money valuation, which dilutes existing shareholders (primarily founders), not the new investor.
- A 10% option pool on a $10M pre-money / $12M post-money means the "true" pre-money for founders is $8.8M.
- Dilution compounds. Two rounds of 25% dilution = 43.75% total dilution, not 50%.
- Focus on the absolute dollar value of your stake, not the percentage. 10% of a $1B company > 50% of a $10M company.
- Anti-dilution provisions (full ratchet vs. weighted average) in term sheets can cause additional dilution in down rounds.

**Funding round valuation benchmarks (Carta Q3 2025):**

| Stage | Valuation Benchmark |
|-------|-------------------|
| Pre-Seed | SAFE valuation cap median $7.5-$15M |
| Seed | $16M pre-money median, $20M post-money |
| Series A | $49.3M pre-money median (AI startups: $84M) |
| Series B | $118.9M pre-money median |

> Valuations from Carta Q3 2025 data. AI startups command 40-70% premium.

---

## Cross-Calculator Relationships

How metrics from each calculator feed into others. Use this to build a complete financial picture.

### Dependency Map

```
Market Size (TAM/SAM/SOM)
    |
    v
Startup Costs --> Funding Calculator --> Equity Dilution
    |                   |
    v                   v
Monthly Burn -----> Runway Calculator
    |                   |
    v                   v
Break-Even <---- Revenue Growth Projections
    |
    v
Unit Economics:
    CAC ---------> LTV:CAC Ratio
    LTV ---------> LTV:CAC Ratio
    LTV:CAC -----> Valuation (multiple justification)
    |
    v
ROI Calculator (investor returns)
    |
    v
Valuation (exit modeling)
    |
    v
Equity Dilution (exit payout)
```

### Key Metric Chains

| Starting Metric | Feeds Into | Which Drives |
|----------------|-----------|-------------|
| TAM/SAM/SOM | Revenue projections | Valuation, Runway, Funding |
| Monthly Burn | Runway | Funding amount and timing |
| Funding Amount | Dilution | Founder exit payout |
| CAC | LTV:CAC Ratio | Unit economics health |
| LTV:CAC Ratio | Valuation multiple | Company value, investor returns |
| Revenue + Growth | Rule of 40 | Valuation multiple selection |
| Break-Even Point | Runway (default alive/dead) | Fundraising urgency |
| Valuation at Exit | x Founder Ownership | Founder exit payout |
| Exit Payout / Investment | ROI, Return Multiple | Investor decision-making |

### Common Analysis Workflows

**"Should I raise funding?"**
1. Runway Calculator - how long until cash runs out?
2. Break-Even Calculator - can I reach profitability first? (default alive/dead)
3. Funding Calculator - how much do I need?
4. Equity Dilution - what will it cost me in ownership?

**"Are my unit economics healthy?"**
1. CAC Calculator - what does it cost to get a customer?
2. LTV Calculator - what is each customer worth?
3. LTV:CAC Ratio - is the relationship sustainable (target 3:1)?
4. CAC Payback - how quickly do I recover acquisition cost?
5. Break-Even - at current unit economics, when do I break even?

**"What is my company worth?"**
1. Market Size - is the opportunity large enough?
2. Valuation Calculator - revenue/SDE multiple or comparable deals
3. Rule of 40 - is growth + profitability balanced?
4. LTV:CAC - do healthy unit economics justify a premium multiple?

**"What will my equity be worth at exit?"**
1. Equity Dilution - model ownership through all planned rounds
2. Valuation Calculator - estimate exit valuation
3. Exit Payout = Final Ownership % x Exit Valuation
4. ROI Calculator - compute return multiple and annualized ROI

---

## 11. SaaS Magic Number

Measures sales efficiency: how much revenue does each dollar of S&M spend generate?

### Formula

```
Magic Number = (Net New ARR This Quarter) / (S&M Spend Previous Quarter)

Alternatively:
Magic Number = [(Revenue This Quarter - Revenue Last Quarter) x 4] / S&M Spend Last Quarter
```

### Benchmarks

| Magic Number | Assessment | Action |
|-------------|-----------|--------|
| > 1.0 | Very efficient | Invest aggressively in S&M |
| 0.75 - 1.0 | Efficient | Scale spend confidently |
| 0.5 - 0.75 | Acceptable | Optimize before scaling |
| < 0.5 | Inefficient | GTM model may be broken; fix before spending more |

### Key Notes
- Use previous quarter's spend (not current) because there's a lag between spending and revenue.
- A Magic Number above 0.75 signals that each incremental S&M dollar generates attractive returns.
- Below 0.5 usually means the go-to-market model needs rethinking, not more budget.

---

## 12. Burn Multiple

Measures capital efficiency: how much are you burning to generate each dollar of new ARR?

### Formula

```
Burn Multiple = Net Burn / Net New ARR

Where:
  Net Burn = Total Expenses - Total Revenue (cash out minus cash in)
  Net New ARR = ARR end of period - ARR start of period
```

### Benchmarks

| Burn Multiple | Assessment |
|-------------|-----------|
| < 1x | Excellent - generating more ARR than burning |
| 1-1.5x | Great - very efficient growth |
| 1.5-2x | Good - acceptable for early stage |
| 2-3x | Concerning - need to improve efficiency |
| > 3x | Poor - unsustainable, fix immediately |

### Key Notes
- David Sacks (Craft Ventures) popularized this metric. VCs increasingly prioritize it over raw growth rate.
- Burn Multiple = the inverse of efficiency. Lower is better.
- A company burning $500K/mo to add $250K in new ARR has a 2x burn multiple.
- At Series A+, VCs expect Burn Multiple < 2x. At Series B+, < 1.5x.

---

## 13. SaaS Quick Ratio

Measures revenue growth health: how much new revenue vs lost revenue?

### Formula

```
SaaS Quick Ratio = (New MRR + Expansion MRR) / (Churned MRR + Contraction MRR)
```

### Benchmarks

| Quick Ratio | Assessment |
|-------------|-----------|
| > 4.0 | Excellent - strong growth, low churn |
| 3.0 - 4.0 | Good - healthy growth dynamics |
| 2.0 - 3.0 | Acceptable - but churn is a drag |
| 1.0 - 2.0 | Concerning - barely growing net revenue |
| < 1.0 | Shrinking - losing more than gaining |

### Key Notes
- Mamoon Hamid (Kleiner Perkins) recommends 4+ as the target for healthy SaaS.
- Quick Ratio captures the full revenue picture that MRR growth alone hides.
- A company adding $50K new MRR but losing $25K to churn has Quick Ratio of 2.0 - growing, but half the gains are eaten by churn.
- Improving Quick Ratio: reduce churn (denominator) or increase expansion revenue (numerator).

---

## 14. Rule of X Calculator

Bessemer's growth-weighted replacement for the Rule of 40. Accounts for the fact that investors value revenue growth 2-3x more than profitability.

### Formula

```
Rule of X = Revenue Growth Rate + (2.3 x FCF Margin)

Where:
  Revenue Growth Rate = year-over-year revenue growth as a percentage
  FCF Margin = Free Cash Flow / Revenue as a percentage
```

### Benchmarks

| Score | Assessment |
|-------|-----------|
| > 40 | Strong |
| 25-40 | Healthy |
| 10-25 | Needs improvement |
| < 10 | Concerning |

### Comparison: Rule of X vs Rule of 40

| Metric | Rule of 40 | Rule of X |
|--------|-----------|-----------|
| Formula | Growth + Profit Margin | Growth + (2.3 x FCF Margin) |
| R-squared (valuation correlation) | ~50% | ~62% |
| Growth weighting | Equal to profitability | 2-3x more than profitability |
| Use case | Quick health check | More accurate valuation predictor |

### Key Notes
- Rule of X has an R-squared of 62% vs 50% for Rule of 40, making it a better predictor of how public markets value SaaS companies.
- The 2.3x multiplier on FCF margin reflects empirical market data: investors consistently pay more for growth than for profitability.
- Companies above the Rule of X threshold trade at significantly higher revenue multiples.
- Use Rule of 40 for a quick gut check, Rule of X for more rigorous valuation and benchmarking.
- Both metrics work best for SaaS companies at scale ($10M+ ARR).

---

### Quick Reference: Warning Signs Across Calculators

| Signal | Metric | Threshold |
|--------|--------|-----------|
| Burning too fast | Runway | < 6 months |
| Acquisition too expensive | LTV:CAC | < 1:1 |
| Slow payback | CAC Payback | > 18 months |
| Overvalued raise | Dilution per round | > 30% |
| Weak margins | Contribution Margin | < 30% |
| Unbalanced growth | Rule of 40 | < 20 |
| Market too small | TAM | < $100M |
| Break-even too distant | Break-even timeline | > 36 months |
| Inefficient GTM | Magic Number | < 0.5 |
| Burning too much per $ ARR | Burn Multiple | > 3x |
| Churn eating growth | SaaS Quick Ratio | < 2.0 |
| Rule of X score low | Rule of X | < 10 |
