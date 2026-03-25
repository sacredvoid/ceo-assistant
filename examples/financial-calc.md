# Example: /ceo-calc Output

> Input: "My SaaS has $15K MRR, 150 customers, 4% monthly churn, spending $8K/mo on marketing, acquiring 20 new customers/month. We have $400K in the bank and burn $45K/mo total."

---

## Financial Dashboard

### Unit Economics

| Metric | Value | Benchmark | Health |
|--------|-------|-----------|--------|
| ARPU | $100/mo | - | - |
| CAC | $400 | $200-500 (SaaS SMB) | Good |
| LTV | $2,000 | $1,500-5,000 | Good |
| LTV:CAC | 5.0:1 | >3:1 target | Excellent |
| CAC Payback | 5.0 months | <12mo target | Excellent |
| Gross Margin | ~80% (assumed SaaS) | >70% | Good |

**Calculations shown:**
```
CAC = $8,000 marketing / 20 new customers = $400
Customer Lifespan = 1 / 0.04 churn = 25 months
LTV = $100 ARPU x 80% margin x 25 months = $2,000
LTV:CAC = $2,000 / $400 = 5.0:1
CAC Payback = $400 / ($100 x 0.80) = 5.0 months
```

### Runway

| Metric | Value | Health |
|--------|-------|--------|
| Monthly Revenue | $15,000 | - |
| Monthly Expenses | $45,000 | - |
| Net Burn | $30,000/mo | - |
| Cash Position | $400,000 | - |
| **Runway** | **13.3 months** | Concerning |
| Start Fundraising At | Now (< 15 months) | - |
| Zero Cash Date | ~May 2027 | - |

### Growth Health

| Metric | Value | Benchmark | Health |
|--------|-------|-----------|--------|
| MRR Growth | ~9% MoM* | 10-15% good | Acceptable |
| Magic Number | N/A (need quarterly data) | >0.75 | - |
| SaaS Quick Ratio | N/A (need expansion/contraction split) | >4.0 | - |
| Burn Multiple | ~24x** | <2x target | Critical |
| Rule of 40 | N/A (need annual growth + margin) | >40 | - |

*Estimated: 20 new customers x $100 = $2K new MRR / ($15K + churn loss)
**Burn Multiple = $30K net burn / ~$1.25K net new MRR = 24x (very high)

### Warnings

| Signal | Status |
|--------|--------|
| Runway < 6 months | No (13.3 months) but approaching danger |
| Churn > 5% | No (4%) but above best-in-class (1-3%) |
| LTV:CAC < 3:1 | No (5:1) - healthy |
| Burn Multiple > 3x | **YES (24x) - unsustainable spending efficiency** |

### Key Insight
Your unit economics are strong (5:1 LTV:CAC, 5-month payback) but your burn multiple is terrible (24x). You're spending $30K/mo in net burn to add ~$1.25K in net new MRR. The gap is your non-marketing expenses ($37K/mo) which dwarf revenue. Either cut burn dramatically or accelerate revenue growth. At current trajectory, you'll run out of cash before reaching profitability.

### Recommendation
1. Cut net burn to $20K/mo (extends runway to 20 months)
2. Focus on reducing churn from 4% to 2% (doubles LTV from $2K to $4K)
3. Start fundraising now - you need 6 months runway buffer for a raise
4. Target raise: ($20K burn x 18 months) x 1.25 = $450K minimum
