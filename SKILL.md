---
name: ceo-assistant
description: Use when working on any startup or business task - idea validation, financial modeling, pitch decks, market research, competitive analysis, fundraising, board updates, OKRs, hiring plans, go-to-market strategy, decision-making, or any CEO/founder operational need
---

# CEO Assistant - Office of the CEO

Your AI chief of staff for building and running a startup. Encodes validated frameworks, real industry benchmarks, and financial formulas from 200+ sources.

## Slash Commands (18 active)

| Command | What it does |
|---|---|
| `/ceo-validate` | Full validation with parallel research agents + 15-criteria scoring |
| `/ceo-score` | Quick viability scoring (15-criteria weighted rubric) |
| `/ceo-calc` | 10 financial calculators with formulas and benchmarks |
| `/ceo-spreadsheet` | Generate .xlsx financial models |
| `/ceo-pitch-deck` | Sequoia-format pitch deck with live competitor/market research |
| `/ceo-presentation` | Cinematic HTML presentations via presentation-chef |
| `/ceo-compete` | Competitive analysis with live web scraping |
| `/ceo-market-size` | TAM/SAM/SOM with top-down + bottom-up research |
| `/ceo-lean-canvas` | 1-page Lean Canvas (9 blocks) |
| `/ceo-gtm` | Go-to-market strategy with channel analysis |
| `/ceo-fundraise` | Round sizing, valuation modeling, investor targeting |
| `/ceo-board-update` | Monthly investor update email |
| `/ceo-okrs` | Quarterly OKRs with EOS Rocks integration |
| `/ceo-metrics` | Track metrics over time with persistence and alerts |
| `/ceo-persona` | Customer persona with live research |
| `/ceo-interview` | Mom Test customer discovery interview scripts |
| `/ceo-hiring` | Hiring plans, JDs, interview scorecards, comp benchmarks |
| `/ceo-legal` | Stage-appropriate legal checklists with cost estimates |
| `/ceo-decision` | Decision frameworks (Type 1/2, Pre-Mortem, Inversion, RAPID) |

## Capabilities

### 1. Idea Validation
Runs your idea through a 15-criteria weighted scoring rubric across Market, Competitive, Financial, Execution, and Risk dimensions. Produces a 0-100 viability score with industry-specific benchmarks. See docs/validation-scoring-rubric.md for the full rubric.

**Process:**
1. Describe your idea (one paragraph)
2. Identify target industry from 13 tracked verticals
3. Score against validation criteria
4. Generate GO/NO-GO recommendation with specific risks and opportunities
5. Suggest next validation steps (interviews, landing page, MVP)

**Viability Score Interpretation:**
| Score | Rating | Success Rate | Action |
|---|---|---|---|
| 85-100 | Exceptional | 89% | Proceed with confidence |
| 75-84 | Strong | 75% | Address minor concerns |
| 65-74 | Moderate | 52% | Address key challenges first |
| 50-64 | Weak | 28% | Significant pivots needed |
| 0-49 | Very Weak | 8% | Explore different ideas |

### 2. Financial Calculators
14 calculators with real formulas and industry benchmarks. See financial-calculators.md for complete reference.

Quick formulas:
- **ROI** = ((Returns - Investment) / Investment) x 100
- **CAC** = Total S&M Spend / New Customers
- **LTV** = ARPU x Gross Margin x (1 / Churn Rate)
- **Runway** = Cash / Net Monthly Burn
- **Break-Even Units** = Fixed Costs / (Price - Variable Cost)
- **TAM** = Total Customers x Annual Spend
- **Post-Money** = Pre-Money + Investment
- **Rule of 40** = Growth Rate% + Profit Margin% (target >= 40)
- **Magic Number** = Net New ARR This Q / S&M Spend Last Q (target > 0.75)
- **Burn Multiple** = Net Burn / Net New ARR (target < 2x)
- **SaaS Quick Ratio** = (New + Expansion MRR) / (Churned + Contraction MRR) (target > 4)
- **Rule of X** = Growth Rate% + (2.3 x FCF Margin%) (Bessemer's upgrade to Rule of 40)

### 3. Business Documents
Generates structured business documents from templates. See business-templates.md.

**Available templates:**
- Pitch Deck (Sequoia 10-12 slide format)
- Lean Canvas (1-page business plan)
- Business Model Canvas (9 blocks)
- Competitive Analysis (5-competitor matrix)
- Customer Persona
- Go-to-Market Strategy
- Board Deck / Investor Update
- SWOT Analysis
- Financial Projections (3-year P&L)
- Validation Interview Script (Mom Test)

### 4. Industry Intelligence
Benchmarks for 13 industries. See industry-benchmarks.md.

| Industry | Success Rate | CAC Range | LTV Range | Time to PMF |
|---|---|---|---|---|
| SaaS B2B | 62% | $200-500 | $1.5-5K | 10-14mo |
| E-commerce | 48% | $30-100 | $150-500 | 6-12mo |
| Mobile App | 35% | $2-10 | $10-50 | 8-16mo |
| FinTech | 58% | $50-200 | $500-2K | 12-18mo |
| HealthTech | 55% | $100-400 | $1-5K | 14-24mo |
| EdTech | 52% | $50-150 | $300-1.5K | 10-16mo |
| Marketplace | 42% | $20-80 | $200-800 | 12-24mo |
| FoodTech | 38% | $15-50 | $100-400 | 8-14mo |
| PropTech | ~40% | $200-10K | varies | 6-24mo |
| TravelTech | ~35% | $30-2K | varies | 6-18mo |
| GameTech | ~20% | $2-30 | $10-50 | 6-18mo |
| AI/ML | ~45% | $50-500 | $500-5K | 8-18mo |

### 5. Operations Frameworks

**OKRs (Quarterly):**
Format: "I will [objective] as measured by [key results]"
- 3-5 objectives per quarter
- 3-5 key results per objective (quantitative, measurable)
- Target 60-70% achievement (stretch goals)

**EOS Level 10 Meeting (Weekly, 90 min):**
1. Segue - good news (5 min)
2. Scorecard review (5 min)
3. Rock review (5 min)
4. Customer/Employee headlines (5 min)
5. To-do list (5 min)
6. IDS: Identify, Discuss, Solve (60 min)
7. Conclude (5 min)

**Rocks (90-day priorities):**
- 3-7 per person, SMART formatted
- 80%+ completion target
- Review weekly, reset quarterly

### 6. Decision Frameworks

**Funding Decision:**
- Bootstrap if: want control, B2B/SaaS, can reach $1M+ ARR organically
- Raise if: winner-take-all market, need speed, targeting $100M+ exit
- Angel ($25-500K) for pre-seed/seed, VC ($500K+) for seed/Series A+

**Build vs Buy:**
- No-code for 80% of MVPs (<$10K, <8 weeks)
- Custom after validation and funding (>10K users, unique requirements)

**Solo vs Co-founder:**
- Solo for lifestyle/bootstrapped businesses
- Co-founder for venture-backed (2x better odds, VCs prefer teams)

**PMF Signals (Sean Ellis Test):**
- Survey: "How would you feel if you could no longer use [product]?"
- 40%+ "very disappointed" = PMF achieved
- Additional: NRR >100%, organic > paid acquisition, retention curves flattening

### 7. Startup Failure Prevention

Top reasons startups fail (from 1000+ failures):
1. No market need - 42%
2. Ran out of cash - 29%
3. Wrong team - 23%
4. Got outcompeted - 19%
5. Pricing/cost issues - 18%

**Prevention checklist:**
- [ ] Validated demand with 30-50 customer interviews
- [ ] TAM >= $10M with >10% annual growth
- [ ] Landing page conversion >2-5%
- [ ] LTV:CAC >= 3:1
- [ ] 18-24 months runway post-raise
- [ ] Clear competitive differentiation

## Reference Files

| File | What it contains |
|---|---|
| docs/financial-calculators.md | 10 calculators with formulas, benchmarks, interpretation |
| docs/validation-frameworks.md | Complete validation methodology, interview scripts, comparison frameworks |
| docs/validation-scoring-rubric.md | 15-criteria weighted scoring rubric with explicit guidelines |
| docs/business-templates.md | 12 templates: pitch deck, lean canvas, personas, competitive analysis, etc. |
| docs/industry-benchmarks.md | 13 industries with CAC, LTV, PMF timelines, failure rates |
| docs/startup-glossary.md | 82 terms with definitions and benchmarks |
| research/skills-landscape.md | Survey of all existing business/startup skills |
| research/ceo-capability-map.md | Full capability map across 10 CEO domains |
| docs/decision-frameworks.md | 12 decision frameworks (Bezos Type 1/2, Pre-Mortem, RAPID, etc.) |
| docs/ceo-operating-system.md | CEO cadences, meeting templates, 1-on-1s, board prep |
| research/financial-models-deep-dive.md | SaaS metrics, 6 valuation methods, cap tables, revenue projections |

## Complementary Skills

For deeper methodology on specific topics, these external skills are recommended:
- **wondelai/skills** - 24 book-based frameworks (Lean Startup, Mom Test, Blue Ocean, EOS, etc.)
- **garrytan/gstack** - CEO review, office hours, security officer
- **slavingia/skills** - Minimalist Entrepreneur workflow
- **Agent GTM Skills** - 18 go-to-market playbooks
