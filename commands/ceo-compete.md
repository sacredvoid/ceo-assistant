# Competitive Analysis

Research and analyze competitors using live web data.

## Input
Ask: "What's your product/service, and do you already know your competitors? If not, I'll find them."

## Step 1: Find Competitors
Use WebSearch to discover competitors:
- "[product category] competitors 2026"
- "[product category] alternatives"
- "best [product category] tools"
- Check G2, Capterra, Product Hunt, AlternativeTo results

## Step 2: Research Each Competitor (Parallel Agents)
For each competitor (up to 5), launch an agent to:
- WebFetch their homepage - extract value proposition, target market, key features
- WebSearch "[competitor] funding crunchbase" - find funding raised, valuation, investors
- WebSearch "[competitor] pricing" - find pricing model and tiers
- WebSearch "[competitor] reviews" - find user sentiment, common complaints

## Step 3: Build Analysis
Generate these deliverables:

### Feature Comparison Matrix
| Feature | Your Product | Competitor 1 | Competitor 2 | ... |
|---------|-------------|-------------|-------------|-----|

### Pricing Comparison
| Competitor | Free Tier | Entry Price | Mid Price | Enterprise |
|-----------|-----------|-------------|-----------|-----------|

### Positioning Map
2x2 matrix with recommended axes based on market dynamics (e.g., Price vs Feature Depth, or SMB vs Enterprise vs Self-Serve vs Sales-Led)

### Threat Assessment
| Competitor | Funding | Market Share | Growth | Threat Level |
|-----------|---------|-------------|--------|-------------|

### Gap Analysis
Where competitors are weak. Opportunities for differentiation.

## Step 4: Strategic Recommendations
- Positioning strategy (head-to-head, niche, or new category)
- Feature priorities based on gaps found
- Pricing strategy relative to competition

## Follow-up
Offer: "Want me to (a) create competitive battlecards for your sales team, (b) build a pitch deck positioning slide, or (c) monitor these competitors weekly?"
