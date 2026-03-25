# Startup Financial Models - Deep Reference

A supplementary reference that goes deeper than the calculators doc. Covers SaaS metrics, unit economics, valuation methods, revenue projections, cap table mechanics, financial statements, and the metrics VCs actually evaluate.

---

## 1. SaaS Financial Models

### Core Revenue Metrics

```
MRR  = Number of Subscribers x ARPA (Average Revenue Per Account)
ARR  = MRR x 12
```

### MRR Decomposition

```
Net New MRR = New MRR
            + Expansion MRR
            - Contraction MRR
            - Churned MRR
            + Reactivation MRR
```

Every month, break down MRR movement into these five components. This tells you *where* growth is coming from and which lever is broken.

### Churn Formulas

```
Gross Revenue Churn % = (Churned MRR + Contraction MRR) / Starting MRR x 100

Net Revenue Churn %   = (Churned MRR - Expansion MRR) / Starting MRR x 100
```

- **Gross Revenue Churn** measures total revenue loss before accounting for upsells.
- **Net Revenue Churn** can go negative (a good thing), meaning expansion revenue exceeds losses.

### Revenue Retention Rates

```
NRR (Net Revenue Retention)   = (Starting MRR + Expansion - Contraction - Churned) / Starting MRR x 100

GRR (Gross Revenue Retention) = (Starting MRR - Contraction - Churned) / Starting MRR x 100
```

- NRR > 100% means you grow even without new customers. This is the single most important SaaS metric for Series A+.
- GRR can never exceed 100%. It measures how well you retain existing revenue before upsells.

### Churn and Retention Benchmarks

| Metric | Poor | Acceptable | Good | Elite |
|--------|------|------------|------|-------|
| Monthly Logo Churn | >5% | 3-5% | 1-3% | <1% |
| Annual Gross Revenue Churn | >15% | 10-15% | 5-10% | <5% |
| Net Revenue Retention (NRR) | <90% | 90-100% | 100-110% | >120% |

**What these mean in practice:**
- Monthly logo churn of 5% means you lose ~46% of customers per year. That is a leaky bucket you cannot outrun.
- NRR of 120% means a cohort that started at $100K MRR is worth $120K a year later, with zero new sales.
- Elite NRR (>120%) is the hallmark of companies like Snowflake, Datadog, and Twilio at scale.

---

## 2. Unit Economics Deep Dive

### Fully-Loaded CAC

Do not use the naive version (just ad spend / new customers). Fully-loaded CAC includes:

```
Fully-Loaded CAC = (Sales Salaries + Marketing Salaries + Ad Spend + Tools + Overhead)
                   / New Customers Acquired
```

Include: base salaries, commissions, benefits, software tools (CRM, marketing automation), agency fees, event costs, and allocated overhead. Exclude one-time brand campaigns or PR unless directly tied to acquisition.

### SaaS Magic Number

```
Magic Number = [(Revenue This Quarter - Revenue Last Quarter) x 4] / S&M Spend Last Quarter
```

This measures sales efficiency: how much incremental ARR you generate per dollar of sales and marketing spend.

| Magic Number | Interpretation |
|-------------|----------------|
| <0.5 | Broken - spending inefficiently, fix GTM before scaling |
| 0.5 - 0.75 | Acceptable - room to optimize but not alarming |
| 0.75 - 1.0 | Good - efficient spend, can justify scaling up |
| >1.0 | Excellent - pour fuel on the fire |

### LTV:CAC Benchmarks by Stage

| Stage | LTV:CAC Target | Context |
|-------|----------------|---------|
| Pre-seed | 2-3:1 OK | Data is noisy, directional is fine |
| Seed | Approaching 3:1 | Should be stabilizing |
| Series A | 3:1 | The canonical benchmark |
| Series B+ | 3-4:1 | Efficiency expected at scale |

**Why 3:1?** A 3:1 ratio means you recover CAC in roughly one-third of the customer lifetime, leaving margin for operations, R&D, and profit. Below 1:1, you lose money on every customer. Above 5:1, you are likely under-investing in growth.

### CAC Payback Period

```
CAC Payback (months) = CAC / (ARPA x Gross Margin %)
```

Target: <12 months for SMB, <18 months for mid-market, <24 months for enterprise.

---

## 3. Valuation Methods

### Method 1: VC Method

```
Pre-Money Valuation = Terminal Value / Target Return Multiple

Terminal Value = Projected Revenue in Year N x Expected Exit Multiple
Target Return = 10-30x depending on stage
```

**Example:** If you project $50M revenue in Year 5 at a 6x exit multiple, terminal value = $300M. A seed VC targeting 20x returns values you at $300M / 20 = $15M pre-money today.

### Method 2: Discounted Cash Flow (DCF)

```
Enterprise Value = Sum of [FCF_t / (1 + WACC)^t] + Terminal Value / (1 + WACC)^n
```

Where:
- `FCF_t` = Free Cash Flow in year t
- `WACC` = Weighted Average Cost of Capital (typically 15-30% for startups, reflecting risk)
- `n` = number of projection years (usually 5-7)
- Terminal Value = FCF_n x (1 + g) / (WACC - g), where g = long-term growth rate

**Reality check:** DCF is rarely used for early-stage startups because cash flows are negative and projections are speculative. It becomes relevant at Series B+ when you have 2-3 years of financial data.

### Method 3: Comparable Company Analysis (Comps)

```
Your Valuation = Your Metric x Comparable Company Multiple
```

Comparable multiples come from recent funding rounds, public company data, or acquisition prices of similar companies at similar stages.

### Revenue Multiples by Stage

| Stage | Typical Pre-Money Valuation | Implied Multiple |
|-------|----------------------------|-----------------|
| Pre-seed | $5-15M | Often pre-revenue, based on team/TAM |
| Seed | $10-20M | 20-50x ARR (if any) |
| Series A | $30-50M | 15-30x ARR |
| Series B | $80-150M | 10-20x ARR |

### 2025 SaaS Valuation Multiples

| Category | ARR Multiple |
|----------|-------------|
| Private SaaS (median) | 4.1-5.3x ARR |
| Public SaaS (median) | 5.6x ARR |
| High-growth SaaS (>40% growth) | 8-15x ARR |
| AI/ML SaaS | 10-50x ARR |

AI multiples are inflated and will compress. Use 10-15x as a reasonable planning assumption for AI startups with real traction; 50x only applies to outliers with viral adoption.

### Method 4: Berkus Method (Pre-Revenue)

Assign $0-500K to each of five risk-reduction dimensions:

| Dimension | Max Value | What It Measures |
|-----------|-----------|-----------------|
| Sound Idea | $500K | Problem worth solving, market exists |
| Prototype | $500K | Working product reduces technology risk |
| Quality Team | $500K | Founders can execute |
| Strategic Relationships | $500K | Partnerships, advisors, early customers |
| Product Rollout / Sales | $500K | Evidence of traction or clear path to revenue |

**Maximum pre-money valuation: $2.5M**

Best for: angel rounds, pre-seed, idea-stage companies.

### Method 5: Scorecard Method

1. Find the average pre-money valuation for comparable startups in your region and sector.
2. Score the startup across weighted dimensions and adjust the average valuation accordingly.

| Factor | Weight | Assessment Range |
|--------|--------|-----------------|
| Strength of Team | 30% | 0.5x - 1.5x |
| Size of Opportunity | 25% | 0.5x - 1.5x |
| Product/Technology | 15% | 0.5x - 1.5x |
| Competitive Environment | 10% | 0.5x - 1.5x |
| Marketing/Sales Channels | 10% | 0.5x - 1.5x |
| Need for Additional Funding | 5% | 0.5x - 1.5x |
| Other | 5% | 0.5x - 1.5x |

**Example:** If the regional average is $5M and your weighted score totals 1.2x, your valuation = $6M.

### Method 6: Rule of 40

```
Rule of 40 Score = Revenue Growth % + Profit Margin %
```

- A score >= 40 indicates a healthy balance between growth and profitability.
- Companies scoring above 40 trade at roughly 2x the multiples of those below 40.
- At early stages, this is almost entirely growth. At later stages, margin matters more.

| Rule of 40 Score | Interpretation |
|-----------------|----------------|
| <20 | Struggling, needs course correction |
| 20-40 | Acceptable, typical for scaling companies |
| 40-60 | Strong, attractive to growth investors |
| >60 | Elite, commands premium valuations |

---

## 4. Revenue Projection Models

### T2D3 Framework

The gold-standard SaaS growth trajectory for venture-backed companies:

```
Year 1: Triple revenue
Year 2: Triple revenue
Year 3: Double revenue
Year 4: Double revenue
Year 5: Double revenue
```

**Example starting at $1M ARR:**

| Year | Growth | ARR |
|------|--------|-----|
| 0 | - | $1M |
| 1 | 3x | $3M |
| 2 | 3x | $9M |
| 3 | 2x | $18M |
| 4 | 2x | $36M |
| 5 | 2x | $72M |

This gets you from $1M to $72M ARR in 5 years. Very few companies achieve this. Use it as an aspirational ceiling, not a planning assumption.

### S-Curve Model

For modeling adoption of a product within a market:

```
y = L / (1 + e^(-k(x - x0)))
```

Where:
- `L` = maximum adoption (market ceiling)
- `k` = steepness of the curve (growth rate)
- `x0` = midpoint (inflection point where growth peaks)

Useful for: market sizing, product adoption forecasting, cohort growth modeling.

### Bass Diffusion Model

For modeling how new products spread through a population:

```
f(t) = [p + q * F(t)] * [1 - F(t)]
```

Where:
- `p` = coefficient of innovation (external influence, e.g., marketing)
- `q` = coefficient of imitation (internal influence, e.g., word of mouth)
- `F(t)` = fraction of the total market that has adopted by time t

- High `p`, low `q` = marketing-driven adoption (enterprise SaaS)
- Low `p`, high `q` = viral/word-of-mouth adoption (PLG, consumer)

### Bottom-Up Revenue Model

The most practical model for early-stage startups:

```
Revenue = Leads x Conversion Rate x ACV (Annual Contract Value)
```

Layer in realism:
- **Sales rep ramp:** New reps take 3-6 months to reach full quota
- **Seasonality:** Enterprise deals cluster in Q4; SMB is more evenly distributed
- **Pipeline stages:** Weight by close probability (Discovery 10%, Proposal 30%, Negotiation 60%, Verbal 90%)

**Example:**

| Month | Leads | Conv. Rate | ACV | New ARR |
|-------|-------|-----------|-----|---------|
| M1 | 200 | 2% | $12K | $48K |
| M6 | 500 | 3% | $15K | $225K |
| M12 | 1,000 | 4% | $18K | $720K |

### Growth Rate Benchmarks by Stage

| Stage | Expected YoY Growth |
|-------|-------------------|
| Seed | 2-3x (100-200%) |
| Series A | 2-3x (100-200%) |
| Series B | 1.5-2x (50-100%) |
| Series C+ | 50-100% |

Growth deceleration is natural. Investors adjust expectations by stage. A Series C company growing 80% YoY is outperforming; a seed company growing 80% YoY is underperforming.

---

## 5. Cap Table Management

### Equity Instrument Types

| Instrument | Description | Key Feature |
|-----------|-------------|-------------|
| Common Stock | Held by founders and employees | Last in liquidation preference |
| Preferred Stock (by series) | Held by investors (Series Seed, A, B, etc.) | Liquidation preference, anti-dilution, board seats |
| Options / Warrants | Right to purchase at a strike price | Typically common stock, subject to vesting |
| Convertible Notes | Debt that converts to equity | Interest rate, maturity date, conversion mechanics |
| SAFEs | Simple Agreement for Future Equity | No debt, no maturity, converts at next priced round |

### Standard Vesting Schedule

```
4-year vesting + 1-year cliff
After cliff: 1/48th vests monthly
```

- **Cliff:** No equity vests until the 1-year mark, then 25% vests at once.
- **Monthly after cliff:** Remaining 75% vests in equal monthly increments over 36 months.
- **Single-trigger acceleration:** All shares vest on acquisition (rare, usually reserved for C-suite).
- **Double-trigger acceleration:** Shares vest only if acquired AND terminated without cause.

### Option Pool

- Standard size: 10-20% of fully diluted shares
- VCs typically require 10-15% unallocated option pool pre-money (before their investment)
- This dilutes founders, not investors. Factor it into valuation negotiations.
- Negotiate pool size based on actual hiring plan for the next 18-24 months, not arbitrary percentages.

### Fully Diluted Shares Calculation

```
Fully Diluted Shares = Outstanding Common Stock
                     + Preferred Stock (as-converted to common)
                     + All Outstanding Options (vested + unvested)
                     + All Convertible Instruments (notes + SAFEs, as-converted)
                     + Unallocated Option Pool
```

This is the denominator used for ownership percentage calculations and per-share pricing.

### SAFE Conversion Mechanics

```
Conversion Price = Valuation Cap / Fully Diluted Shares (pre-money)

Shares Issued to SAFE Holder = Investment Amount / Conversion Price
```

The investor gets the **lower** of:
- **Cap price:** Valuation Cap / Fully Diluted Shares
- **Discount price:** Price Per Share in Priced Round x (1 - Discount %)

**Example:** $500K SAFE with $8M cap and 20% discount. Series A prices at $10M pre-money, $2/share.
- Cap price: $8M / 4M shares = $2.00/share, investor gets 250K shares
- Discount price: $2.00 x 0.80 = $1.60/share, investor gets 312.5K shares
- Investor takes the discount (lower price = more shares)

### 2025 Market Data

- SAFEs comprise approximately 90% of pre-seed rounds
- Post-money SAFEs (YC standard) are now the default; understand that post-money SAFEs include the option pool increase, which means more dilution than you might expect
- Convertible notes are still common in markets outside Silicon Valley and for bridge rounds

---

## 6. Financial Statements (Simplified for Startups)

### Profit & Loss (Income Statement)

```
Revenue
- Cost of Goods Sold (COGS)
= Gross Profit
  - Sales & Marketing
  - Research & Development
  - General & Administrative
= EBITDA (Earnings Before Interest, Taxes, Depreciation, Amortization)
  - Depreciation & Amortization
  - Interest
  - Taxes
= Net Income
```

**SaaS COGS typically includes:** hosting/infrastructure, customer support salaries, payment processing fees, third-party software embedded in the product.

**SaaS COGS typically excludes:** R&D salaries (those go under OpEx), sales commissions (S&M), office rent (G&A).

### Cash Flow Statement

```
Cash from Operations
  + Net Income
  + Non-cash adjustments (depreciation, stock-based comp)
  + Changes in working capital

+ Cash from Investing
  - Capital expenditures
  - Acquisitions

+ Cash from Financing
  + Equity raised
  + Debt raised
  - Debt repaid

= Net Change in Cash
```

For startups: cash from operations is almost always negative (you're burning cash). Cash from financing is where the money comes in (fundraising). This is fine as long as you have runway.

### Balance Sheet

```
Assets = Liabilities + Stockholders' Equity

Assets:
  Cash & Equivalents
  Accounts Receivable
  Prepaid Expenses
  Fixed Assets (net of depreciation)

Liabilities:
  Accounts Payable
  Accrued Expenses
  Deferred Revenue
  Debt (convertible notes, loans)

Equity:
  Common Stock
  Preferred Stock
  Additional Paid-In Capital
  Retained Earnings (usually negative for startups)
```

**Deferred Revenue** is critical for SaaS: if a customer pays annually upfront, you recognize 1/12th per month. The remaining is a liability (you owe them the service). This is why cash and revenue diverge.

### What Investors Expect by Stage

| Stage | Financial Reporting Required |
|-------|----------------------------|
| Pre-seed | P&L + 18-month cash forecast |
| Seed | P&L + cash forecast + basic unit economics |
| Series A | Full 3 statements + 3-year projections + cohort analysis |
| Series B+ | Full 3 statements + scenario modeling (base/bull/bear) + board-ready package |

---

## 7. The 6 Metrics VCs Actually Care About

Everything above feeds into these six numbers. If you only track six things, track these.

### 1. Revenue Growth Rate

```
MoM Growth = (This Month MRR - Last Month MRR) / Last Month MRR x 100
YoY Growth = (This Year ARR - Last Year ARR) / Last Year ARR x 100
```

| Stage | Expectation |
|-------|------------|
| Seed | 15-20% MoM |
| Series A | 10-15% MoM or 2-3x YoY |
| Series B+ | 80-100%+ YoY |

### 2. Net Revenue Retention (NRR)

```
NRR = (Starting MRR + Expansion - Contraction - Churned) / Starting MRR x 100
```

- Target: >100% (you grow without new customers)
- Elite: >120%
- If NRR < 100%, you have a leaky bucket that gets harder to fill at scale

### 3. Gross Margin

```
Gross Margin = (Revenue - COGS) / Revenue x 100
```

| Business Model | Expected Gross Margin |
|---------------|---------------------|
| SaaS | 70-80% |
| Marketplace | 60-70% |
| Hardware + Software | 40-60% |
| Services/Consulting | 30-50% |

Low gross margin limits how much you can spend on S&M and R&D. Below 60%, the business does not have SaaS economics regardless of delivery model.

### 4. CAC Payback Period

```
CAC Payback (months) = Fully-Loaded CAC / (Monthly ARPA x Gross Margin %)
```

| Payback Period | Interpretation |
|---------------|----------------|
| <6 months | Excellent, very efficient |
| 6-12 months | Good for SMB/mid-market |
| 12-18 months | Acceptable for enterprise |
| >18 months | Concerning, need to improve |

### 5. Burn Multiple

```
Burn Multiple = Net Burn / Net New ARR
```

| Burn Multiple | Interpretation |
|--------------|----------------|
| <1x | Excellent, hyper-efficient growth |
| 1-1.5x | Good, efficient |
| 1.5-2x | Acceptable, watch it |
| 2-3x | Concerning, optimize before scaling |
| >3x | Burning cash inefficiently |

This is the metric that gained prominence post-2022. It directly answers: "How much cash do you burn to generate each dollar of new ARR?" In the capital-efficient era, this matters more than growth rate alone.

### 6. Runway

```
Runway (months) = Current Cash Balance / Monthly Net Burn
```

| Runway | Action |
|--------|--------|
| >18 months | Comfortable, focus on growth |
| 12-18 months | Start preparing for next round |
| 6-12 months | Actively fundraising or cutting burn |
| <6 months | Emergency mode, bridge or cut immediately |

**Rule of thumb:** Start fundraising when you have 9-12 months of runway. Rounds take 3-6 months to close. Running out of cash is the #1 startup killer.

---

## Quick Reference: Formula Cheat Sheet

| Metric | Formula |
|--------|---------|
| MRR | Subscribers x ARPA |
| ARR | MRR x 12 |
| Net New MRR | New + Expansion - Contraction - Churned + Reactivation |
| NRR | (Starting + Expansion - Contraction - Churned) / Starting x 100 |
| GRR | (Starting - Contraction - Churned) / Starting x 100 |
| Fully-Loaded CAC | Total S&M Spend / New Customers |
| LTV | ARPA x Gross Margin % x (1 / Monthly Churn Rate) |
| LTV:CAC | LTV / CAC |
| CAC Payback | CAC / (Monthly ARPA x Gross Margin %) |
| Magic Number | [(Rev This Q - Rev Last Q) x 4] / S&M Last Q |
| Burn Multiple | Net Burn / Net New ARR |
| Runway | Cash / Monthly Net Burn |
| Rule of 40 | Growth % + Margin % |
| Gross Margin | (Revenue - COGS) / Revenue x 100 |
