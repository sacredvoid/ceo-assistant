# CEO/Founder Skills Landscape - Research Report

**Date:** 2026-03-25
**Purpose:** Document all existing Claude Code skills relevant to a CEO/founder, identify gaps, and inform architecture decisions for the CEO Assistant skill.

---

## Executive Summary

There are hundreds of business and startup skills available across 12+ marketplaces and open-source repositories. The highest-signal sources are: Garry Tan's gstack (YC CEO), Sahil Lavingia's Minimalist Entrepreneur skills (Gumroad CEO), Anthropic's financial-services-plugins, wondelai/skills (24 book-based frameworks), Agent GTM Skills (18 go-to-market skills), and alirezarezvani/claude-skills (192+ including 28 C-level advisory).

This report catalogs what exists, evaluates quality and coverage, and identifies the gaps our CEO Assistant fills.

---

## Key Sources

### Tier 1: Official + Founder Collections

These are the most authoritative sources, either from Anthropic directly or from high-profile founders who built skills for their own workflows.

#### Anthropic Official Skills

| Skill | What It Does | Relevance to CEO |
|-------|-------------|-------------------|
| `/pptx` | Generate PowerPoint presentations | Board decks, investor pitches |
| `/xlsx` | Generate Excel spreadsheets | Financial models, KPI dashboards |
| `/docx` | Generate Word documents | Memos, proposals, contracts |
| `/brand-guidelines` | Create brand guideline documents | Brand consistency across team |
| `/skill-creator` | Build new Claude Code skills | Extending CEO tooling |

**Assessment:** Strong document generation primitives, but no business logic or frameworks baked in. These are output-format tools, not strategy tools.

#### Anthropic Financial Services Plugins

**Repo:** Research preview, not yet public
**Status:** Available as a plugin collection for financial analysis workflows

| Plugin | Capability |
|--------|------------|
| DCF Model | Discounted cash flow valuation with sensitivity tables |
| LBO Model | Leveraged buyout analysis |
| 3-Statement Model | Income, balance sheet, cash flow linked models |
| CIM Generator | Confidential Information Memorandum drafting |
| IC Memo Builder | Investment committee memo templates |
| Portfolio KPI Tracker | Fund-level performance metrics |

**Assessment:** Institutional-grade financial modeling, designed for PE/VC analysts. Useful for CEOs raising capital or running board-level financial reviews, but overkill for early-stage founders and missing startup-specific metrics (burn rate, runway, unit economics).

#### Garry Tan's gstack

**Repo:** [github.com/garrytan/gstack](https://github.com/garrytan/gstack)
**Author:** Garry Tan, CEO of Y Combinator

| Skill | What It Does | Notes |
|-------|-------------|-------|
| `/plan-ceo-review` | Brian Chesky-style CEO review process | Structured decision-making framework |
| `/office-hours` | Simulate YC office hours Q&A | Founder coaching format |
| `/ship` | Ship planning and release coordination | Engineering-product workflow |
| `/land-and-deploy` | Go-to-market deployment checklist | Launch coordination |
| `/qa` | Quality assurance workflows | Product quality |
| `/cso` | Chief of Staff operations | Operational coordination |
| `/pitch` | Pitch preparation and feedback | Investor readiness |
| `/fundraise` | Fundraising strategy and process | Capital raising |
| `/hiring` | Hiring frameworks | Team building |
| `/one-on-one` | 1:1 meeting structure | Management practice |
| `/weekly-update` | Weekly status update template | Communication cadence |
| `/okr` | OKR planning and tracking | Goal setting |
| `/retro` | Retrospective facilitation | Team learning |
| `/strategy` | Strategy development | Long-term planning |
| `/metrics` | Metrics review and analysis | Data-driven decisions |

**Assessment:** The highest-quality CEO-specific skill collection available. Built by someone who coaches hundreds of founders. Strong on operational cadence and decision-making, lighter on financial modeling and document generation.

#### Sahil Lavingia's Minimalist Entrepreneur Skills

**Repo:** [github.com/slavingia/skills](https://github.com/slavingia/skills)
**Author:** Sahil Lavingia, CEO of Gumroad

| Skill | What It Does | Book Chapter |
|-------|-------------|--------------|
| `/find-community` | Identify and analyze target communities | Ch. 1: Start with community |
| `/validate-idea` | Validate business ideas against community needs | Ch. 2: Build something people want |
| `/mvp` | Build minimum viable product spec | Ch. 3: Build as little as possible |
| `/first-customers` | Acquire first 10-100 customers | Ch. 4: Sell to your first customers |
| `/pricing` | Pricing strategy and value-based pricing | Ch. 5: Market by being you |
| `/marketing-plan` | Marketing plan using authentic voice | Ch. 5: Market by being you |
| `/company-values` | Define company values and culture | Ch. 6: Grow yourself |
| `/grow-sustainably` | Sustainable growth planning | Ch. 7: Build the house you want to live in |
| `/profitability` | Path to profitability analysis | Ch. 8: Where do we go from here? |

**Assessment:** Excellent for bootstrapped/lifestyle-business founders. Very opinionated (anti-VC, pro-profitability). Covers 0-to-1 journey well but stops at the growth-stage. Not useful for Series A+ companies or complex organizational challenges.

---

### Tier 2: Deep Framework Collections

These are substantial open-source collections with real depth, typically encoding specific methodologies from business books or GTM playbooks.

#### wondelai/skills

**Repo:** [github.com/wondelai/skills](https://github.com/wondelai/skills)
**Size:** 24 business skills, each based on a bestselling business book
**Quality:** High - each skill encodes the core framework from its source book, not just summaries

**Strategy Skills:**

| Skill | Source Book/Framework | Core Methodology |
|-------|-----------------------|-----------------|
| Blue Ocean Strategy | Kim & Mauborgne | Strategy canvas, four actions framework, eliminate-reduce-raise-create grid |
| Crossing the Chasm | Geoffrey Moore | Technology adoption lifecycle, bowling pin strategy, whole product model |
| Obviously Awesome | April Dunford | Positioning methodology - competitive alternatives, unique attributes, value mapping |
| Traction/EOS | Gino Wickman | Entrepreneurial Operating System - vision, traction, healthy components |

**Product Skills:**

| Skill | Source Book/Framework | Core Methodology |
|-------|-----------------------|-----------------|
| Lean Startup | Eric Ries | Build-measure-learn loop, validated learning, MVP, pivot/persevere |
| Design Sprint | Jake Knapp / GV | 5-day sprint: map, sketch, decide, prototype, test |
| Inspired | Marty Cagan | Product discovery, empowered teams, product vision, opportunity assessment |
| Continuous Discovery | Teresa Torres | Opportunity solution trees, weekly customer touchpoints, assumption testing |
| Jobs-to-be-Done | Clayton Christensen | Job map, progress-making forces, demand-side sales |

**Customer Development Skills:**

| Skill | Source Book/Framework | Core Methodology |
|-------|-----------------------|-----------------|
| The Mom Test | Rob Fitzpatrick | Customer conversation rules - no leading questions, ask about past behavior, seek commitment |

**Marketing Skills:**

| Skill | Source Book/Framework | Core Methodology |
|-------|-----------------------|-----------------|
| StoryBrand | Donald Miller | 7-part story framework, brand script, customer as hero |
| One-Page Marketing Plan | Allan Dib | Before/during/after marketing phases, 9-square plan |
| Scorecard Marketing | Daniel Priestley | Key person of influence pathway, content/community/commerce |
| Made to Stick | Chip & Dan Heath | SUCCESs framework: Simple, Unexpected, Concrete, Credible, Emotional, Stories |
| Contagious | Jonah Berger | STEPPS framework: Social Currency, Triggers, Emotion, Public, Practical Value, Stories |

**Sales Skills:**

| Skill | Source Book/Framework | Core Methodology |
|-------|-----------------------|-----------------|
| $100M Offers | Alex Hormozi | Value equation, offer stacking, dream outcome, perceived likelihood, time/effort |
| Predictable Revenue | Aaron Ross | Outbound prospecting machine, SDR/AE split, cold calling 2.0 |
| Influence Psychology | Robert Cialdini | 6 principles: reciprocity, commitment, social proof, authority, liking, scarcity |

**Leadership Skills:**

| Skill | Source Book/Framework | Core Methodology |
|-------|-----------------------|-----------------|
| Never Split the Difference | Chris Voss | Tactical empathy, calibrated questions, mirroring, labeling, accusation audit |
| Drive | Daniel Pink | Autonomy, mastery, purpose motivation framework |

**Retention & Growth Skills:**

| Skill | Source Book/Framework | Core Methodology |
|-------|-----------------------|-----------------|
| Hooked | Nir Eyal | Hook model: trigger, action, variable reward, investment |
| Tiny Habits | BJ Fogg | Behavior = Motivation + Ability + Prompt, habit stacking |
| CRO Methodology | Conversion optimization | Hypothesis testing, A/B framework, funnel analysis |
| Lean UX | Jeff Gothelf | Hypothesis-driven design, minimum viable experiments |

**Assessment:** The most intellectually rigorous skill collection available. Each skill is a genuine encoding of its source material, not a shallow summary. However, these are individual frameworks, not an integrated system. A CEO would need to know which framework to apply when, and there's no routing layer or meta-skill that connects them.

#### Agent GTM Skills

**Source:** [agentgtmskills.com](https://agentgtmskills.com)
**Size:** 18 GTM skills, 9,800+ lines of skill definitions
**Focus:** Go-to-market execution

| Category | Skills Included | Line Count (approx.) |
|----------|----------------|---------------------|
| Positioning | Competitive positioning, messaging hierarchy, value prop | ~1,200 |
| Pricing | Pricing models, packaging, competitive pricing analysis | ~800 |
| Outbound | Cold email, LinkedIn outreach, ABM, sequence design | ~1,500 |
| Inbound | Content strategy, SEO, landing pages, lead magnets | ~1,200 |
| Paid | Ad copy, campaign structure, budget allocation, ROAS | ~900 |
| Retention | Churn analysis, NPS, customer health scoring, expansion | ~1,100 |
| Ops | GTM metrics, attribution, pipeline management, forecasting | ~1,400 |
| Launch | Launch plans, beta programs, press kits, Product Hunt | ~700 |
| Partnerships | Partner programs, co-marketing, channel strategy | ~900 |

**Assessment:** Deep GTM coverage, clearly built by someone who has run multiple go-to-market motions. Strongest in outbound and ops. The 9,800+ line count suggests real depth, not just templates. Likely the best single source for post-PMF revenue execution.

#### Corey Haines' marketingskills

**Size:** 32 skills, 52 CLI tools
**Focus:** Growth marketing and conversion optimization

| Skill Area | Tools | Key Capabilities |
|------------|-------|-----------------|
| CRO | 8 tools | Audit checklists, A/B test design, funnel analysis, heatmap interpretation |
| Copywriting | 6 tools | Headlines, landing pages, email sequences, ad copy, PAS/AIDA frameworks |
| SEO | 5 tools | Keyword research, content briefs, technical audit, link building strategy |
| Onboarding | 4 tools | User onboarding flows, activation metrics, welcome sequences |
| Email | 5 tools | Drip campaigns, segmentation, deliverability, automation workflows |
| Analytics | 4 tools | Dashboard design, metric definitions, cohort analysis, attribution |
| Content | 6 tools | Content calendar, repurposing, distribution, thought leadership |
| Social | 4 tools | Platform strategy, posting cadence, engagement tactics, influencer outreach |
| Product Marketing | 4 tools | Launch plans, competitive intel, sales enablement, case studies |
| Lifecycle | 6 tools | Customer journey mapping, retention, expansion, win-back campaigns |

**Assessment:** Execution-focused marketing toolkit. More granular than Agent GTM (individual tools vs. strategic skills). Best for a CEO who is also acting as head of marketing in early stages.

#### alirezarezvani/claude-skills

**Repo:** [github.com/alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)
**Size:** 192+ skills across all business functions

| Category | Skill Count | Notable Skills |
|----------|-------------|----------------|
| Marketing | 43 | Brand audit, content strategy, GTM plan, social media calendar, SEO roadmap |
| Product | 12 | PRD writer, roadmap builder, feature prioritization, sprint planning |
| C-Suite Advisory | 28 | CEO coach, CFO advisory, CTO advisor, COO ops, CMO strategy, CHRO people |
| Sales | 15 | Pipeline builder, discovery call script, proposal generator, objection handler |
| Finance | 18 | Budget planner, fundraise model, cap table, revenue forecast, unit economics |
| Legal/Compliance | 12 | Terms of service, privacy policy, SOC 2 prep, GDPR audit, contract review |
| HR/People | 14 | Job descriptions, culture handbook, performance review, comp benchmarking |
| Engineering | 22 | Architecture review, code review, incident response, tech debt audit |
| Data/Analytics | 10 | Dashboard design, data model, KPI framework, experimentation platform |
| Design | 8 | Design system, UX audit, accessibility review, design sprint facilitation |
| Operations | 10 | Process documentation, vendor evaluation, tool stack audit, SOP builder |

**Assessment:** The broadest collection by far, but breadth over depth. Many skills are thin wrappers around prompts rather than deep framework implementations. The C-suite advisory block (28 skills) is unique, offering role-specific coaching that no other collection provides. Quality varies significantly, with some skills being genuinely useful and others being little more than structured prompts.

---

### Tier 3: Marketplaces & Directories

These are aggregation platforms where skills are published. Quality is highly variable, and many listings are duplicates or thin wrappers.

| Platform | Size | Business Category | Quality Signal | URL |
|----------|------|-------------------|----------------|-----|
| SkillsMP | 500K+ skills | Large business section | Low curation, high volume | skillsmp.com |
| SkillKit | 15K+ skills, 44 agent support | Mixed | Medium curation | skillkit.io |
| SkillHub | 7K+ skills | AI-evaluated quality scores | Automated quality scoring | skillhub.club |
| MCP Market | Hundreds | Business Model Canvas, Pitch Deck Builder, Financial Analysis | Curated, smaller | mcpmarket.com |
| BuildWithClaude | 53 plugins, 121 skills, 117 subagents | Various | Community-driven | buildwithclaude.com |
| ClaudeSkills.info | 658+ skills | Mixed | Directory format | claudeskills.info |
| AI Templates (aitmpl) | 1,000+ components | Templates and tools | Template-focused | aitmpl.com |

**Assessment:** High noise-to-signal ratio. Marketplaces are useful for discovery but most skills need evaluation before adoption. The best skills from these marketplaces are already captured in Tier 1 and Tier 2 above. The main value is as a discovery layer for niche use cases.

---

### Tier 4: MCP Server Integrations

These are not skills but Model Context Protocol servers that connect Claude Code to live business tools. Critical for a CEO who needs real-time data, not just frameworks.

| MCP Server | Category | What It Connects | CEO Use Case |
|------------|----------|-----------------|-------------|
| HubSpot MCP | CRM | Contacts, deals, pipeline, activities | Sales pipeline visibility, customer 360 |
| FreshBooks MCP | Invoicing | Invoices, expenses, time tracking, clients | Cash flow, AR/AP management |
| Xero MCP | Accounting | Chart of accounts, bank reconciliation, reports | Financial reporting, tax prep |
| ChartMogul MCP | Subscription Metrics | MRR, churn, LTV, cohorts, segments | SaaS metrics dashboard |
| Composio | Multi-SaaS | 850+ SaaS connectors via unified API | Swiss army knife for SaaS data |
| Jira/Atlassian MCP | Project Management | Issues, sprints, boards, roadmaps | Engineering velocity, sprint health |
| Slack MCP | Communication | Channels, messages, threads, search | Team communication, async updates |
| Linear MCP | Project Management | Issues, projects, cycles, views | Product development tracking |
| Notion MCP | Knowledge Base | Pages, databases, wikis | Company wiki, documentation |
| GitHub MCP | Code/DevOps | Repos, PRs, issues, actions | Engineering output, code quality |

**Assessment:** MCP servers transform Claude Code from an advisor into an operator. A CEO skill paired with live CRM, accounting, and project management data becomes dramatically more useful. The gap is that no existing skill connects framework-level thinking (wondelai) with live data (MCP servers).

---

## Coverage Matrix

How well each source covers the key CEO functions:

| CEO Function | gstack | slavingia | wondelai | Agent GTM | alirezarezvani | Anthropic Financial | Our CEO Assistant |
|-------------|--------|-----------|---------|-----------|----------------|--------------------|--------------------|
| Strategy & Vision | Strong | Medium | Strong | Weak | Medium | None | Strong |
| Fundraising & Finance | Medium | Weak | None | None | Medium | Strong | Strong |
| Product | Medium | Strong | Strong | Weak | Medium | None | Medium |
| Marketing & GTM | Weak | Medium | Strong | Strong | Strong | None | Medium |
| Sales | None | Medium | Medium | Strong | Medium | None | Weak |
| Operations & EOS | Strong | Weak | Medium | Medium | Medium | None | Strong |
| Team & Hiring | Medium | Weak | Medium | None | Medium | None | Weak |
| Board & Governance | Medium | None | None | None | Weak | Medium | Strong |
| Legal & Compliance | None | None | None | None | Medium | None | Weak |
| Financial Modeling | None | None | None | None | Weak | Strong | Strong |

**Legend:** Strong = deep, actionable coverage | Medium = covers the topic but not deeply | Weak = mentioned but thin | None = not addressed

---

## Gap Analysis

What our CEO Assistant adds that does not exist in any current skill or collection:

### Gap 1: Unified Meta-Skill Routing

**Problem:** No existing skill covers strategy + finance + product + marketing + ops under one interface. A CEO using today's tools would need to install and learn 5-10 separate skill collections, understand which framework to apply when, and manually context-switch between them.

**Our Solution:** A single "Office of the CEO" routing layer that triages requests to the right domain and methodology. The CEO says what they need; the skill figures out which framework to invoke.

### Gap 2: IdeaProof Validation Methodology

**Problem:** Existing validation skills (slavingia's `/validate-idea`, wondelai's Lean Startup and Mom Test) are framework-based but lack quantitative scoring. They guide you through a process but don't produce a comparable, benchmarked score.

**Our Solution:** IdeaProof's complete validation methodology with:
- Viability scoring (0-100) across multiple dimensions
- Industry benchmarks for 13 verticals (SaaS, marketplace, D2C, fintech, healthtech, edtech, devtools, hardware, media, agency, creator economy, climate, biotech)
- Weighted scoring that adjusts by business model
- Pass/fail thresholds with clear go/no-go recommendations

### Gap 3: Integrated Financial Calculators

**Problem:** Anthropic's financial-services-plugins are institutional-grade (DCF, LBO) but not startup-specific. alirezarezvani has basic finance skills but no linked calculator system. No existing skill provides the 10 interconnected calculators a startup CEO actually needs.

**Our Solution:** 10 financial calculators with formulas, cross-linked so outputs feed into each other:

| Calculator | Inputs | Outputs | Feeds Into |
|-----------|--------|---------|------------|
| Burn Rate | Monthly expenses, revenue | Monthly/annual burn | Runway |
| Runway | Cash, burn rate | Months remaining, fundraise deadline | Fundraising timeline |
| Unit Economics | CAC, LTV, payback | LTV:CAC ratio, payback period | Pricing, GTM |
| MRR/ARR | Customers, ARPU, churn | MRR, ARR, net revenue retention | Valuation |
| Valuation | ARR, growth rate, sector multiples | Revenue multiple, implied valuation | Fundraising |
| Dilution | Pre-money, raise amount, option pool | Post-money, founder %, dilution % | Cap table |
| TAM/SAM/SOM | Market data, assumptions | Market sizes, penetration rates | Strategy, pitch |
| Break-even | Fixed costs, variable costs, price | Break-even units, timeline | Financial plan |
| Revenue Forecast | Current metrics, growth assumptions | 12/24/36-month projections | Board deck |
| Hiring Plan | Roles, salaries, start dates | Monthly headcount cost, loaded cost | Burn rate |

### Gap 4: Full Business Document Generation

**Problem:** Anthropic's pptx/docx/xlsx handle file formats but have zero business logic. No existing skill generates complete, structured business documents with the right content, structure, and best practices baked in.

**Our Solution:** Complete document generation for:
- **Pitch Deck** (12-slide structure: problem, solution, market, product, traction, team, business model, competition, financials, ask, appendix)
- **Board Deck** (quarterly format: highlights, KPIs, financials, product update, team update, risks, asks)
- **Lean Canvas** (9-block canvas with guided fill)
- **Financial Projections** (3-year model with assumptions, scenarios)
- **Competitive Analysis** (feature matrix, positioning map, SWOT)
- **Investor Update** (monthly/quarterly template with KPIs, highlights, lowlights, asks)

### Gap 5: EOS + OKR Operational Frameworks

**Problem:** Garry Tan's gstack has `/okr` but it's lightweight. wondelai has Traction/EOS but it's a framework explainer, not an operational tool. No skill combines both EOS and OKR into a working system.

**Our Solution:** Integrated operational frameworks:
- EOS: Vision/Traction Organizer (V/TO), rocks, scorecard, issues list, L10 meeting structure
- OKR: Objective/key result drafting, scoring, cascade from company to team to individual
- Cadence: Weekly L10, monthly metrics review, quarterly rock planning, annual V/TO refresh
- Templates that connect EOS + OKR rather than treating them as separate systems

### Gap 6: Startup Glossary for Consistent Language

**Problem:** No existing skill includes a glossary. This matters because CEOs communicate across audiences (investors, engineers, marketers, board members) and terminology inconsistency creates confusion.

**Our Solution:** 82-term startup glossary covering:
- Financial terms (ARR, MRR, burn, runway, dilution, cap table, SAFE, convertible note)
- Product terms (PMF, MVP, sprint, backlog, north star metric)
- GTM terms (CAC, LTV, NRR, churn, expansion revenue, ICP)
- Fundraising terms (pre-money, post-money, term sheet, due diligence, bridge round)
- Operational terms (EOS, OKR, L10, rocks, scorecard)

---

## Architecture Decision

### What to Build vs. What to Reference

Rather than reimplementing wondelai's deep book frameworks or competing with Agent GTM's 9,800 lines of GTM skills, our CEO Assistant should follow a "build unique, reference deep, fill gaps" strategy:

| Approach | What | Examples |
|----------|------|---------|
| **Build** (encode directly) | IdeaProof's unique data, financial calculators, document templates, glossary | Viability scoring with 13-vertical benchmarks, 10 cross-linked calculators, pitch/board deck generators |
| **Reference** (point to, don't rebuild) | Deep book-based frameworks that already exist | wondelai/skills for Blue Ocean, Mom Test, $100M Offers, etc. |
| **Fill** (build where nothing exists) | Areas no skill covers | Board deck generation, investor update templates, integrated EOS+OKR |
| **Route** (meta-skill layer) | Unified interface across all domains | "Office of the CEO" that triages to the right tool/framework |

### Rationale

1. **Don't compete on depth with specialists.** wondelai's encoding of "Never Split the Difference" is excellent. Rebuilding it adds no value.
2. **Compete on integration.** No one has built the routing layer. That's the unique value.
3. **Own the data.** Viability benchmarks, financial formulas, and document structures are original IP that no other skill provides.
4. **Stay maintainable.** A 2,000-line skill that routes well beats a 20,000-line skill that tries to encode every framework internally.

### Recommended Skill Structure

```
CEO Assistant Skill
|
|-- /ideaproof        -> Unique: validation + scoring + benchmarks
|-- /finance          -> Unique: 10 calculators, cross-linked
|-- /pitch-deck       -> Unique: 12-slide generator with content guidance
|-- /board-deck       -> Unique: quarterly board deck generator
|-- /investor-update  -> Unique: monthly/quarterly investor update
|-- /lean-canvas      -> Unique: guided 9-block canvas
|-- /competitive      -> Unique: competitive analysis framework
|-- /eos              -> Unique: integrated EOS + OKR system
|-- /glossary         -> Unique: 82-term reference
|-- /strategy         -> Routes to: wondelai (Blue Ocean, Crossing the Chasm, Obviously Awesome)
|-- /product          -> Routes to: wondelai (Lean Startup, Inspired, JTBD, Design Sprint)
|-- /marketing        -> Routes to: wondelai (StoryBrand, Made to Stick) + Agent GTM
|-- /sales            -> Routes to: wondelai ($100M Offers, Predictable Revenue) + Agent GTM
|-- /negotiate        -> Routes to: wondelai (Never Split the Difference)
|-- /customer-dev     -> Routes to: wondelai (Mom Test) + slavingia (find-community)
```

---

## Appendix: Source Quality Ranking

| Rank | Source | Quality | Depth | Breadth | Maintenance | Best For |
|------|--------|---------|-------|---------|-------------|----------|
| 1 | wondelai/skills | 9/10 | 10/10 | 7/10 | Active | Deep framework application |
| 2 | Garry Tan's gstack | 9/10 | 8/10 | 6/10 | Active | CEO operational cadence |
| 3 | Agent GTM Skills | 8/10 | 9/10 | 5/10 | Active | GTM execution |
| 4 | Anthropic Financial | 8/10 | 9/10 | 4/10 | Preview | Institutional finance |
| 5 | Sahil Lavingia's skills | 8/10 | 7/10 | 4/10 | Active | Bootstrapped founders |
| 6 | Corey Haines' marketing | 7/10 | 7/10 | 6/10 | Active | Marketing execution |
| 7 | alirezarezvani/claude-skills | 5/10 | 4/10 | 10/10 | Active | Broad coverage, light depth |
| 8 | Marketplace listings | 3/10 | 2/10 | 10/10 | Varies | Discovery only |

---

## Appendix: Key Repo Links

| Source | URL |
|--------|-----|
| Garry Tan's gstack | https://github.com/garrytan/gstack |
| Sahil Lavingia's skills | https://github.com/slavingia/skills |
| wondelai/skills | https://github.com/wondelai/skills |
| alirezarezvani/claude-skills | https://github.com/alirezarezvani/claude-skills |
| Agent GTM Skills | https://agentgtmskills.com |
| Corey Haines' marketingskills | https://github.com/coreyhaines/marketingskills |
| SkillsMP | https://skillsmp.com |
| SkillKit | https://skillkit.io |
| SkillHub | https://skillhub.club |
| MCP Market | https://mcpmarket.com |
| BuildWithClaude | https://buildwithclaude.com |
| ClaudeSkills.info | https://claudeskills.info |
| AI Templates | https://aitmpl.com |
