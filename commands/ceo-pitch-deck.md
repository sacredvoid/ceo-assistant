# Generate Pitch Deck

Create an investor pitch deck following Sequoia's 10-12 slide format with live market research.

## Input
Ask: "Tell me about your startup - what it does, who it's for, what traction you have, and what you're raising."

## Process

### Step 1: Research (Parallel Agents)
Launch 2 agents:
- **Market Size Agent**: WebSearch for TAM/SAM data for this specific market
- **Competitor Agent**: WebSearch for direct competitors, their funding, positioning

### Step 2: Generate Slides
Load template from @ceo-assistant/docs/business-templates.md (Section 6: Pitch Deck).

For each of 12 slides, generate content:
1. **Title** - Company name, tagline, contact
2. **Problem** - Customer pain, current alternatives, why they're inadequate
3. **Solution** - Value proposition, how it works, key differentiator
4. **Why Now** - Market timing, trends, what changed recently
5. **Market Size** - TAM/SAM/SOM with real numbers from research
6. **Product** - Screenshots/description, key features
7. **Business Model** - Revenue model, pricing, unit economics
8. **Traction** - Metrics, growth rate, milestones achieved
9. **Competition** - 2x2 positioning matrix with real competitors found
10. **Team** - Key members, relevant experience, why this team wins
11. **Financials** - 3-year projections, burn rate, runway
12. **The Ask** - Amount, use of funds, milestones the money unlocks

### Step 3: Quality Check
Verify against the 20 Common Pitch Mistakes from @ceo-assistant/docs/business-templates.md (Section 11).
- Total word count under 600 across all slides
- One key message per slide
- No "we have no competitors" claims
- Specific metrics, not vague claims

## Output Options
Ask: "How would you like the output?"
- (a) Markdown document (default)
- (b) HTML presentation (uses presentation-chef skill for cinematic slides)
- (c) Slide-by-slide text for pasting into Google Slides/Keynote/PowerPoint
