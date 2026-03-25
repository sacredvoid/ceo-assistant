# Changelog

## v3.0 - 2026-03-25

### Added
- Decision frameworks reference doc (12 frameworks: Bezos Type 1/2, Pre-Mortem, Inversion, RAPID, Disagree & Commit, Second-Order Thinking, Working Backwards, Wartime/Peacetime CEO, Pivot vs Persevere, ICE/RICE/Weighted Scoring, Task-Relevant Maturity, Regret Minimization)
- CEO Operating System doc (weekly/monthly/quarterly/annual cadences, 1-on-1 templates, board prep, decision logs, Sacks' Cadence, Founder Mode)
- Rule of X calculator (Bessemer's upgrade to Rule of 40, 62% R-squared)
- /ceo-decision command for structured decision-making
- Tar Pit Ideas detection in /ceo-validate workflow (YC/Dalton Caldwell)
- Sequoia Arc PMF framework (3 archetypes: Hair on Fire, Hard Fact, Future Vision)
- YC 10-5-20 pricing check and weekly growth benchmarks in /ceo-score
- v3 research compilation report (10K+ words from 12 research agents, 140+ searches)

### Updated
- CAC channel benchmarks updated 40-60% upward (Google Ads B2B: $267 -> $802, LinkedIn: $375 -> $982)
- Funding round valuations updated to Carta Q3 2025 data (pre-seed caps $7.5-15M, seed $16M pre-money)
- SaaS valuation multiples updated (public median 4-6x, AI 25-30x)
- AI/ML industry section expanded with gross margins, failure modes, defensibility framework

### Data Sources Added
- Carta State of Startups 2025, Bessemer Cloud 100 2025, a16z Growth Metrics Guide
- First Page Sage CAC 2026, Phoenix Strategy Group benchmarks
- YC Startup School curriculum, SaaStr metrics, First Round Review
- Lenny's Newsletter AI Growth Playbook, Kyle Poyar/OpenView SaaS benchmarks

## v2.0 - 2026-03-25

### Added
- 18 slash commands (ceo-validate, ceo-score, ceo-calc, ceo-spreadsheet, ceo-pitch-deck, ceo-presentation, ceo-compete, ceo-market-size, ceo-lean-canvas, ceo-gtm, ceo-fundraise, ceo-board-update, ceo-okrs, ceo-metrics, ceo-persona, ceo-interview, ceo-hiring, ceo-legal)
- 15-criteria weighted validation scoring rubric (docs/validation-scoring-rubric.md)
- 3 new SaaS calculators: Magic Number, Burn Multiple, SaaS Quick Ratio (13 total)
- Metrics persistence system (~/.claude/ceo-metrics.json)
- xlsx spreadsheet generation via Anthropic xlsx skill
- HTML presentation generation via presentation-chef skill
- Live web research built into validation and competitive analysis workflows
- Parallel agent dispatch for complex tasks (validation, competitive analysis)
- CLAUDE.md project documentation
- CHANGELOG.md version tracking

### Fixed
- Deprecated 7-factor scoring system in favor of 15-criteria rubric
- Sourced success rate claims as IdeaProof modeled estimates (not independent data)
- Filled in missing industry data for PropTech, TravelTech, GameTech, AI/ML
- Updated SKILL.md router table to reflect actual slash commands
- Added financial-models-deep-dive.md to reference files table

## v1.0 - 2026-03-25

### Initial Release
- SKILL.md meta-skill with capability overview
- 5 reference docs (financial-calculators, validation-frameworks, business-templates, industry-benchmarks, startup-glossary)
- 3 research reports (skills-landscape, ceo-capability-map, financial-models-deep-dive)
- 12 business document templates
- 10 financial calculators with formulas and benchmarks
- 13 industry verticals with benchmark data
- 82 glossary terms
