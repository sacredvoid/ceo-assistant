# CEO Assistant Skill

## What This Is
A Claude Code skill suite for startup founders and CEOs. 18 slash commands backed by 44K+ words of reference docs covering validation, financial modeling, pitch decks, competitive analysis, hiring, legal, operations, and metrics tracking.

## Structure
- `SKILL.md` - Main skill definition with capability overview
- `docs/` - Reference documents (calculators, frameworks, templates, benchmarks, glossary, scoring rubric)
- `research/` - Research reports (skills landscape, capability map, financial models deep dive)
- Slash commands live in `~/.claude/commands/ceo-*.md`
- Metrics persistence at `~/.claude/ceo-metrics.json`

## Commands
All commands are prefixed `ceo-`: validate, score, calc, spreadsheet, pitch-deck, presentation, compete, market-size, lean-canvas, gtm, fundraise, board-update, okrs, metrics, persona, interview, hiring, legal.

## Data Sources
- IdeaProof.io (63 pages scraped): validation frameworks, industry benchmarks, calculators
- wondelai/skills: 24 book-based business frameworks cataloged
- 12+ skill marketplaces surveyed
- Deep web research: financial models, pitch deck frameworks, CEO operations

## Data Vintage
- Industry benchmarks: 2024-2025 (from IdeaProof, sourced Jan 2026)
- SaaS valuation multiples: 2025 data
- Failure analysis: CB Insights 2019 + IdeaProof 2024 dataset
- Success rate estimates: modeled from IdeaProof's 10K+ validation dataset, not independently verified

## Known Limitations
- Benchmarks are static (no live data refresh) - commands use WebSearch to supplement
- Success rate percentages are directional estimates, not empirical guarantees
- Financial calculators produce estimates, not accounting-grade figures
- Legal checklists are frameworks, not legal advice
