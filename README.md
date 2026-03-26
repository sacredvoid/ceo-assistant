# CEO Assistant v2.0

### Claude Code (recommended)
```
/plugin marketplace add sacredvoid/ceo-assistant
```

[![Built with Claude Code](https://img.shields.io/badge/Built%20with-Claude%20Code-7c3aed?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0id2hpdGUiPjxwYXRoIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyem0wIDE4Yy00LjQyIDAtOC0zLjU4LTgtOHMzLjU4LTggOC04IDggMy41OCA4IDgtMy41OCA0LTggOHoiLz48L3N2Zz4=)](https://claude.ai/code)
[![MIT License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-0ea5e9?style=for-the-badge&logo=github)](https://sacredvoid.github.io/ceo-assistant)

**Your AI chief of staff for building and running a startup.** CEO Assistant gives you 28 commands covering every stage from finding your community to fundraising, with real industry benchmarks, 14 financial calculators, and validated frameworks from YC, Sequoia, Bessemer, and a16z. Whether you're validating an idea against a 15-criteria scoring rubric, building your first MVP, or generating pitch decks with live market research, you get grounded outputs built on 200+ scraped sources and 13 industry verticals -- not generic advice.

**New in v2.0 - The Minimalist Entrepreneur Playbook:**

- **9 new commands** from Sahil Lavingia's The Minimalist Entrepreneur, covering the full journey from community to sustainable growth.
- **Find your community** (`/ceo-community`) - identify communities you already belong to and evaluate which ones to serve.
- **Processize before you productize** (`/ceo-processize`) - turn any idea into a manual process you can start delivering today, before writing a line of code.
- **Build your MVP** (`/ceo-mvp`) - the three-stage path: manual, processized, productized. Ship in a weekend.
- **First 100 customers** (`/ceo-first-customers`) - the concentric circles strategy: friends, community, strangers. Manual sales first.
- **Pricing strategy** (`/ceo-pricing`) - cost-based vs value-based, the zero price effect, the math of financial independence.
- **Marketing plan** (`/ceo-marketing`) - content-first marketing through three levels: educate, inspire, entertain.
- **Grow sustainably** (`/ceo-grow`) - profitability as a superpower. Spend less than you make. Infinite runway.
- **Company values** (`/ceo-values`) - define culture before hiring. Values as stories, not slogans.
- **Minimalist review** (`/ceo-review`) - gut-check any decision against 8 minimalist principles.

**v1.0 - The Analytical Toolkit (19 commands):** Full validation with live market research, 14 financial calculators, competitive analysis, pitch decks, board updates, OKRs, hiring plans, legal checklists, and 12 decision frameworks. Built by scraping 200+ pages from IdeaProof.io, Carta, Bessemer, a16z, First Page Sage, and YC.

**The combination:** v1 tells you whether your idea is viable with data. v2 tells you how to actually build it with discipline. Use `/ceo-validate` to score your idea, then `/ceo-processize` to start delivering value by hand, then `/ceo-first-customers` to sell your way to product-market fit.

## Installation

### Claude Code Plugin (recommended)
```
/plugin marketplace add sacredvoid/ceo-assistant
```

### Manual Install
```bash
git clone https://github.com/sacredvoid/ceo-assistant.git
cp ceo-assistant/commands/*.md ~/.claude/commands/
```

Then type `/ceo-validate` in Claude Code to validate your first idea.

## Usage

```
/ceo-validate [describe your idea]
/ceo-processize [describe your product]
/ceo-first-customers
```

### Use it for:
- **Idea validation** - "Score my SaaS idea for restaurant inventory management"
- **Manual-first process** - "How do I deliver this by hand before building software?"
- **First customers** - "Create my outreach plan for the first 100 customers"
- **Financial modeling** - "Calculate my runway, CAC, and break-even"
- **Pitch decks** - "Generate a Sequoia-format pitch deck with live research"
- **Competitive analysis** - "Who are my competitors and how do they compare?"
- **Decision making** - "Should I raise funding or bootstrap? Review this through the minimalist lens."

## What It Does

1. **Validates** - Scores ideas against a 15-criteria weighted rubric with live market research, tar pit detection, and industry benchmarks
2. **Plans** - Generates lean canvases, go-to-market strategies, financial projections, and pitch decks
3. **Executes** - Walks you through manual-first processes, first customer outreach, pricing, and marketing
4. **Operates** - Tracks metrics, generates board updates, runs OKRs, and supports CEO-level decision making

---

## Example: Validate a SaaS Idea

**Command:** `/ceo-validate AI-powered inventory management for independent restaurants`

**Output:**
> **Viability Score: 72/100 - Moderate**
>
> | Category | Weight | Score | Weighted |
> |----------|--------|-------|----------|
> | Market Timing | 12% | 8/10 | 9.6 |
> | Market Size | 10% | 7/10 | 7.0 |
> | Problem Severity | 10% | 8/10 | 8.0 |
> | Competition | 8% | 5/10 | 4.0 |
> | ... (15 criteria total) |
>
> **Tar Pit Check:** NOT a tar pit. Restaurant tech has historically been difficult (high churn, low willingness to pay), but AI-driven waste reduction is a genuine cost-saving proposition with measurable ROI, unlike "discovery" or "reservation" plays.
>
> **Competitors Found:** MarketMan ($200/mo, Series A), BlueCart (acquired by US Foods), Lightspeed inventory module (bundled). Gap: none are AI-native for demand forecasting.
>
> **GO/NO-GO: CONDITIONAL GO** - Strong problem severity and timing, but crowded market requires clear AI differentiation. Validate with 10 restaurant owner interviews first.

Three parallel agents ran live research on market size, competitors, and trends. The scoring rubric weighs 15 criteria across Market (42%), Competitive (16%), Financial (18%), Execution (12%), and Risk (12%) dimensions.

---

## Example: Processize Before Building

**Command:** `/ceo-processize meal prep delivery service for busy parents`

**Output:**
> **One-sentence description:** You plan a week of kid-friendly meals, shop the ingredients, prep everything on Sunday, and deliver portioned containers to families by Monday morning.
>
> **The Magic Piece of Paper:**
>
> 1. **Trigger:** Customer fills out a Google Form with family size, allergies, and preferences
> 2. **Plan meals** - Select 5 dinners from your tested recipe bank (30 min)
> 3. **Generate shopping list** - Map ingredients to quantities for all families (15 min)
> 4. **Shop** - Buy everything at one grocery run (90 min for 5 families)
> 5. **Prep** - Cook and portion into labeled containers (4 hours for 5 families)
> 6. **Deliver** - Drop off Monday morning with reheating instructions (60 min for 5 families)
>
> **Time per customer:** ~75 min at 5 families/batch
>
> **Initial price:** $149/week per family (5 dinners, 4 servings each)
>
> **First 3 people to deliver to this week:**
> 1. Your neighbor with three kids who always complains about dinner
> 2. The parent from school pickup who mentioned hating meal planning
> 3. Post in your local parents' Facebook group
>
> **First thing to automate (not now):** The shopping list generation - it's the most repetitive step

This shows the manual-first approach from The Minimalist Entrepreneur. No app, no code, no landing page. Just a Google Form, a grocery run, and a Sunday afternoon.

---

## Example: Financial Calculator

**Command:** `/ceo-calc runway for my startup - $500K raised, $45K monthly burn, $12K monthly revenue`

**Output:**
> **Runway Calculation**
>
> | Metric | Value | Health |
> |--------|-------|--------|
> | Cash on hand | $500,000 | |
> | Monthly burn (gross) | $45,000 | |
> | Monthly revenue | $12,000 | |
> | Net monthly burn | $33,000 | |
> | **Runway** | **15.2 months** | Healthy (>12mo) |
>
> **Benchmarks (Seed Stage):**
> - Median seed burn: $50-80K/mo (you're below - good)
> - Target runway post-raise: 18-24 months (you're at 15 - watch it)
> - Default alive test: Revenue growing >15% MoM needed to reach profitability before cash runs out
>
> **Recommendation:** At current trajectory, start fundraising conversations at month 9 (6 months before zero). If revenue grows 20% MoM, you hit profitability at month 11.

14 calculators available: ROI, TAM/SAM/SOM, Startup Costs, Funding, Break-Even, Runway, Valuation, CAC, LTV, Equity Dilution, Magic Number, Burn Multiple, SaaS Quick Ratio, Rule of X.

---

## Example: Minimalist Review

**Command:** `/ceo-review Should I raise a $2M seed round? We have 80 paying customers at $49/mo.`

**Output:**
> **Recommendation: Don't raise. Not yet.**
>
> **The minimalist version:** You have 80 customers at $49/mo = $3,920 MRR. You're close to ramen profitability. Raising $2M now means giving up 15-20% equity when you haven't proven you can get to 200 customers organically.
>
> | Principle | Assessment |
> |-----------|-----------|
> | Community first | You have a community (80 customers). Stay close to them. |
> | Build as little as possible | Are you building features they asked for, or features you think VCs want? |
> | Sell before you scale | 80 customers is good. 200 is better. Can you get there with manual sales? |
> | Profitability is the goal | At $49/mo and 200 customers = $9,800 MRR. Is that enough? |
> | Reversible? | Raising is irreversible. Dilution is permanent. |
>
> **Biggest risk:** Raising too early locks you into a growth trajectory that may not match your market's natural pace. Gumroad grew 15% in 2017, 25% in 2018, 40% in 2019 - patience paid off.
>
> **Try this week:** Email your 80 customers and ask why they signed up. The answers will tell you whether to raise or sell your way to 200.

This combines v1's analytical framework with v2's minimalist principles, giving you both the data-driven and philosophy-driven perspective.

---

## The 28 Commands

### The Minimalist Entrepreneur Playbook (v2.0)

| Command | What It Does |
|---------|-------------|
| `/ceo-community` | Find your community - the foundation of a minimalist business |
| `/ceo-values` | Define company values and culture before hiring |
| `/ceo-processize` | Turn an idea into a manual-first process you deliver today |
| `/ceo-mvp` | Build your MVP: manual, processized, then productized |
| `/ceo-first-customers` | Strategy for selling to your first 100 customers |
| `/ceo-pricing` | Pricing strategy: cost-based vs value-based, zero price effect |
| `/ceo-marketing` | Content marketing plan: educate, inspire, entertain |
| `/ceo-grow` | Sustainable growth - profitability as a superpower |
| `/ceo-review` | Gut-check any decision against 8 minimalist principles |

### The Analytical Toolkit (v1.0)

| Command | What It Does | Output |
|---------|-------------|--------|
| `/ceo-validate` | Full validation with parallel research agents + 15-criteria scoring | Validation report with viability score, competitors, market data |
| `/ceo-score` | Quick viability scoring (no live research) | Score card with per-criterion breakdown |
| `/ceo-calc` | 14 financial calculators with benchmarks | Calculations with health indicators |
| `/ceo-spreadsheet` | Generate .xlsx financial models | Actual Excel file |
| `/ceo-pitch-deck` | Sequoia-format pitch deck with live research | 12-slide deck content |
| `/ceo-presentation` | Cinematic HTML presentations | Self-contained .html file |
| `/ceo-compete` | Competitive analysis with live web scraping | Feature matrix, pricing comparison, positioning map |
| `/ceo-market-size` | TAM/SAM/SOM with top-down + bottom-up research | Market sizing with sources |
| `/ceo-lean-canvas` | 1-page Lean Canvas (9 blocks) | Formatted canvas |
| `/ceo-gtm` | Go-to-market strategy with channel analysis | GTM plan with 90-day timeline |
| `/ceo-fundraise` | Round sizing, valuation, investor targeting | Fundraising plan with dilution model |
| `/ceo-board-update` | Monthly investor update email | Copy-paste ready email |
| `/ceo-okrs` | Quarterly OKRs with EOS Rocks | Formatted OKRs with scoring guide |
| `/ceo-metrics` | Track metrics over time with persistence | Dashboard with trends and alerts |
| `/ceo-persona` | Customer persona with live research | Persona cards |
| `/ceo-interview` | Mom Test customer discovery scripts | Interview script + analysis framework |
| `/ceo-hiring` | Hiring plans, JDs, interview scorecards | Role-specific documents |
| `/ceo-legal` | Stage-appropriate legal checklists | Prioritized checklist with costs |
| `/ceo-decision` | Decision frameworks (Type 1/2, Pre-Mortem, RAPID) | Structured decision analysis |

---

## How It Works

### Two Knowledge Bases

**The Analytical Engine (v1)** encodes hard data: 15-criteria scoring rubrics, 14 financial calculators with real formulas, benchmarks for 13 industry verticals (CAC, LTV, churn, time-to-PMF), and 12 decision frameworks from Bezos, Munger, Grove, and Bain. When you run `/ceo-validate`, three parallel agents hit the web simultaneously for market size, competitors, and trends, then score everything against the rubric.

**The Minimalist Playbook (v2)** encodes Sahil Lavingia's philosophy from building Gumroad: start with community, processize before you productize, sell manually to your first 100 customers, charge from day one, grow at the speed of your customers, and treat profitability as a superpower. These commands walk you through each stage with specific outputs (outreach lists, pricing math, the "magic piece of paper" process doc).

### The Suggested Workflow

```
/ceo-community         Find your people
    |
/ceo-validate          Score the idea (live research + 15-criteria rubric)
    |
/ceo-processize        Design the manual version
    |
/ceo-first-customers   Sell to 100 people by hand
    |
/ceo-pricing           Set your price (cost-based or value-based)
    |
/ceo-mvp               Build only what you've proven manually
    |
/ceo-marketing         Scale with content, not ads
    |
/ceo-grow              Stay profitable, grow sustainably
    |
/ceo-fundraise         Raise only if you must (and from a position of strength)
```

### Data Sources

Built by scraping and synthesizing 200+ web pages:

- **IdeaProof.io** (63 pages) - Validation frameworks, industry benchmarks, calculators
- **Carta State of Startups 2025** - Funding round sizes, valuations, dilution data
- **Bessemer Cloud 100 2025** - Rule of X, growth benchmarks, efficiency scores
- **a16z Growth Metrics Guide** - Percentile benchmarks, network effects, AI retention
- **First Page Sage / Phoenix Strategy Group** - CAC by channel (2026 data)
- **YC Startup School** - Tar pit detection, 10-5-20 pricing, interview frameworks
- **Sequoia** - Arc PMF framework, pitch deck structure, crucible moments
- **The Minimalist Entrepreneur** (Sahil Lavingia) - Community-first building, processizing, sustainable growth
- **SaaStr, Lenny's Newsletter, Kyle Poyar / OpenView** - SaaS benchmarks, pricing evolution

---

## Industry Benchmarks

Real data for 13 verticals. Updated March 2026.

| Industry | Success Rate | CAC Range | LTV Range | Time to PMF |
|----------|-------------|-----------|-----------|-------------|
| SaaS B2B | 62% | $200-500 | $1.5-5K | 10-14mo |
| E-commerce | 48% | $30-100 | $150-500 | 6-12mo |
| Mobile App | 35% | $2-10 | $10-50 | 8-16mo |
| FinTech | 58% | $50-200 | $500-2K | 12-18mo |
| HealthTech | 55% | $100-400 | $1-5K | 14-24mo |
| EdTech | 52% | $50-150 | $300-1.5K | 10-16mo |
| Marketplace | 42% | $20-80 | $200-800 | 12-24mo |
| FoodTech | 38% | $15-50 | $100-400 | 8-14mo |
| AI/ML | ~45% | $50-500 | $500-5K | 8-18mo |
| PropTech | ~40% | $200-10K | varies | 6-24mo |
| TravelTech | ~35% | $30-2K | varies | 6-18mo |
| GameTech | ~20% | $2-30 | $10-50 | 6-18mo |

Plus detailed sub-benchmarks (churn rates, retention, funding stages, failure modes) for each.

---

## Financial Calculators

14 calculators with real formulas and industry benchmarks:

| Calculator | Key Formula |
|-----------|-------------|
| ROI | ((Returns - Investment) / Investment) x 100 |
| TAM/SAM/SOM | Customers x Annual Spend (bottom-up) |
| Startup Costs | Legal + Tech + Marketing + Salaries + Buffer |
| Funding | (Monthly Burn x Runway Target) x 1.25 |
| Break-Even | Fixed Costs / (Price - Variable Cost) |
| Runway | Cash / Net Monthly Burn |
| Valuation | Revenue x Multiple (by stage and type) |
| CAC | Total S&M Spend / New Customers |
| LTV | ARPU x Gross Margin x (1 / Churn Rate) |
| Equity Dilution | Investment / Post-Money Valuation |
| Magic Number | Net New ARR This Q / S&M Spend Last Q |
| Burn Multiple | Net Burn / Net New ARR |
| SaaS Quick Ratio | (New + Expansion MRR) / (Churned + Contraction) |
| Rule of X | Growth Rate + (2.3 x FCF Margin) |

---

## Decision Frameworks

12 frameworks for CEO-level decision making:

| Framework | When to Use |
|-----------|------------|
| Bezos Type 1/Type 2 | Every decision - classify before deliberating |
| Pre-Mortem (Gary Klein) | Before any major initiative |
| Inversion (Munger) | Strategy sessions, annual planning |
| RAPID (Bain) | When decisions stall at 10+ person teams |
| Disagree and Commit | When the team is split |
| Second-Order Thinking | Pricing, competitive strategy, policy changes |
| Working Backwards (Amazon) | Before building any new product/feature |
| Wartime/Peacetime CEO | Matching leadership to company state |
| Pivot vs Persevere | Quarterly decision point |
| ICE/RICE/Weighted Scoring | Product prioritization |
| Task-Relevant Maturity (Grove) | Calibrating delegation level |
| Regret Minimization (Bezos) | Career/company-defining forks |

---

## What's Inside

```
ceo-assistant/
├── SKILL.md                              Meta-skill with command router
├── commands/                             28 slash command workflows
│   ├── ceo-validate.md                   Full validation with live research
│   ├── ceo-community.md                  Find your community (new)
│   ├── ceo-processize.md                 Manual-first process design (new)
│   ├── ceo-mvp.md                        Build your MVP (new)
│   ├── ceo-first-customers.md            First 100 customers strategy (new)
│   ├── ceo-pricing.md                    Pricing strategy (new)
│   ├── ceo-marketing.md                  Content marketing plan (new)
│   ├── ceo-grow.md                       Sustainable growth (new)
│   ├── ceo-values.md                     Company values & culture (new)
│   ├── ceo-review.md                     Minimalist decision review (new)
│   ├── ceo-score.md                      Quick 15-criteria scoring
│   ├── ceo-calc.md                       14 financial calculators
│   ├── ceo-compete.md                    Competitive analysis
│   └── ... (15 more)
├── docs/
│   ├── financial-calculators.md          14 calculators with formulas + benchmarks
│   ├── validation-frameworks.md          Complete validation methodology
│   ├── validation-scoring-rubric.md      15-criteria weighted scoring rubric
│   ├── business-templates.md             15 templates (pitch deck, lean canvas, etc.)
│   ├── industry-benchmarks.md            13 industries with CAC, LTV, PMF data
│   ├── decision-frameworks.md            12 decision frameworks
│   ├── ceo-operating-system.md           CEO cadences, 1-on-1s, board prep
│   └── startup-glossary.md               82+ terms with benchmarks
├── research/
│   ├── v3-research-findings.md           Latest research compilation (10K+ words)
│   ├── skills-landscape.md               Ecosystem survey of existing skills
│   ├── ceo-capability-map.md             10 CEO domains mapped
│   └── financial-models-deep-dive.md     SaaS metrics, valuations, cap tables
├── examples/
│   ├── validation-report.md              Example /ceo-validate output
│   └── financial-calc.md                 Example /ceo-calc output
└── index.html                            GitHub Pages landing page
```

---

## Complementary Skills

| Skill | What It Adds |
|-------|-------------|
| [wondelai/skills](https://github.com/wondelai/skills) | 24 book-based frameworks (Lean Startup, Mom Test, Blue Ocean, EOS, $100M Offers, etc.) |
| [garrytan/gstack](https://github.com/garrytan/gstack) | YC CEO's toolkit - plan review, office hours, shipping, security |
| [slavingia/skills](https://github.com/slavingia/skills) | The original Minimalist Entrepreneur skills (v2 commands were adapted from this) |
| [Agent GTM Skills](https://agentgtmskills.com/) | 18 go-to-market playbooks with current benchmarks |

---

## Contributing

PRs welcome. Especially:
- Updated benchmark data (cite your sources)
- New command workflows
- Industry-specific validation criteria
- Corrections to formulas or benchmarks

---

## License

[MIT](LICENSE) - Use it however you want.

---

*28 commands. 60K+ words of frameworks. 14 calculators. 13 industries. From community to IPO.*

*Built by [sacredvoid](https://github.com/sacredvoid) | Powered by [Claude Code](https://claude.ai/code)*
