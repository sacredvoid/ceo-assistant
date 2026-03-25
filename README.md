<div align="center">

<img src="https://images.unsplash.com/photo-1553877522-43269d4ea984?w=1200&h=400&fit=crop" alt="CEO Assistant" width="100%"/>

# CEO Assistant - Office of the CEO

**Your AI chief of staff for building and running a startup.**<br>
**19 commands. 60K+ words of frameworks. 14 calculators. 13 industries. Zero bullshit.**

[![Built with Claude Code](https://img.shields.io/badge/Built%20with-Claude%20Code-7c3aed?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0id2hpdGUiPjxwYXRoIGQ9Ik0xMiAyQzYuNDggMiAyIDYuNDggMiAxMnM0LjQ4IDEwIDEwIDEwIDEwLTQuNDggMTAtMTBTMTcuNTIgMiAxMiAyem0wIDE4Yy00LjQyIDAtOC0zLjU4LTgtOHMzLjU4LTggOC04IDggMy41OCA4IDgtMy41OCA4LTggOHoiLz48L3N2Zz4=)](https://claude.ai/code)
[![MIT License](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-0ea5e9?style=for-the-badge&logo=github)](https://sacredvoid.github.io/ceo-assistant)

</div>

---

## What It Does

Turn Claude Code into a startup CEO's AI chief of staff. Validate ideas with live market research and a 15-criteria scoring rubric. Generate pitch decks, financial models, competitive analysis, and board updates. Track metrics over time with persistent storage. Make better decisions with frameworks from YC, Sequoia, Bessemer, and a16z.

Not generic advice. Real formulas, real benchmarks (updated March 2026 from Carta, Bessemer, a16z, First Page Sage), real workflows that use WebSearch and parallel agents to pull live data.

---

## Quick Start

```bash
# Clone the repo
git clone https://github.com/sacredvoid/ceo-assistant.git

# Copy commands to your Claude Code commands directory
cp ceo-assistant/commands/*.md ~/.claude/commands/

# Copy reference docs (commands reference these via @ceo-assistant/)
mkdir -p ~/ceo-assistant
cp -r ceo-assistant/docs ~/ceo-assistant/
cp ceo-assistant/SKILL.md ~/ceo-assistant/

# Initialize metrics tracking
echo '{"company":null,"industry":null,"snapshots":[]}' > ~/.claude/ceo-metrics.json
```

Then type `/ceo-validate` in Claude Code to validate your first idea.

---

## The 19 Commands

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

## What's Inside

```
ceo-assistant/
├── SKILL.md                              Meta-skill with command router
├── commands/                             19 slash command workflows
│   ├── ceo-validate.md                   Full validation with live research
│   ├── ceo-score.md                      Quick 15-criteria scoring
│   ├── ceo-calc.md                       14 financial calculators
│   ├── ceo-compete.md                    Competitive analysis
│   ├── ceo-decision.md                   Decision frameworks
│   └── ... (14 more)
├── docs/
│   ├── financial-calculators.md          14 calculators with formulas + benchmarks
│   ├── validation-frameworks.md          Complete validation methodology
│   ├── validation-scoring-rubric.md      15-criteria weighted scoring rubric
│   ├── business-templates.md             15 templates (pitch deck, lean canvas, etc.)
│   ├── industry-benchmarks.md            13 industries with CAC, LTV, PMF data
│   ├── decision-frameworks.md            12 decision frameworks
│   ├── ceo-operating-system.md           CEO cadences, 1-on-1s, board prep
│   └── startup-glossary.md              82+ terms with benchmarks
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

## Data Sources

This skill was built by scraping and synthesizing 200+ web pages:

- **IdeaProof.io** (63 pages) - Validation frameworks, industry benchmarks, calculators
- **Carta State of Startups 2025** - Funding round sizes, valuations, dilution data
- **Bessemer Cloud 100 2025** - Rule of X, growth benchmarks, efficiency scores
- **a16z Growth Metrics Guide** - Percentile benchmarks, network effects, AI retention
- **First Page Sage / Phoenix Strategy Group** - CAC by channel (2026 data)
- **YC Startup School** - Tar pit detection, 10-5-20 pricing, interview frameworks
- **Sequoia** - Arc PMF framework, pitch deck structure, crucible moments
- **SaaStr** - Fundability benchmarks, 3 metrics that matter
- **Lenny's Newsletter** - AI Growth Playbook, DRICE prioritization
- **Kyle Poyar / OpenView** - SaaS benchmarks, pricing evolution
- **First Round Review** - Operational frameworks, tactical GTM
- **wondelai/skills** - 24 book-based business frameworks (cataloged)
- **12+ skill marketplaces** surveyed for landscape analysis

---

## How It Was Built

Built in a single Claude Code session using ~50 parallel agents:

1. **Scraped** IdeaProof.io (63 pages across guides, calculators, frameworks, validators)
2. **Researched** 12 domains simultaneously (YC, a16z, Bessemer, pricing, fundraising, growth, AI startups, legal, team building, mental models, benchmarks, skill marketplaces)
3. **Audited** against competing skills (garrytan/gstack, slavingia/skills, wondelai/skills, alirezarezvani/claude-skills)
4. **Fixed** 38 gaps found via deep audit
5. **Updated** all benchmarks with 2025-2026 data from 140+ web searches

Total: ~50 agents, 200+ pages scraped, 60K+ words of output.

---

## Complementary Skills

For deeper methodology on specific topics:

| Skill | What It Adds |
|-------|-------------|
| [wondelai/skills](https://github.com/wondelai/skills) | 24 book-based frameworks (Lean Startup, Mom Test, Blue Ocean, EOS, $100M Offers, etc.) |
| [garrytan/gstack](https://github.com/garrytan/gstack) | YC CEO's toolkit - plan review, office hours, shipping, security |
| [slavingia/skills](https://github.com/slavingia/skills) | Minimalist Entrepreneur workflow - community, validation, first customers |
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

<div align="center">

**Built by [sacredvoid](https://github.com/sacredvoid) | Powered by [Claude Code](https://claude.ai/code)**

</div>
