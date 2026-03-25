# Generate Business Presentation

Create a polished HTML presentation using the presentation-chef skill.

## Input
Ask: "What type of presentation?"
1. Investor pitch deck
2. Board meeting deck
3. Product demo / overview
4. Company all-hands
5. Custom topic

## Process

### For Pitch Deck
1. Run the /ceo-pitch-deck workflow to generate slide content
2. Ask for company branding (colors, logo URL if available)
3. Invoke the presentation-chef skill to create cinematic HTML presentation

### For Board Deck
1. Run the /ceo-board-update workflow for content
2. Include metrics visualizations, cash burn chart, growth trajectory
3. Generate via presentation-chef

### For Product Demo
1. Ask for key features, target audience, value proposition
2. Structure: Problem -> Solution -> Demo -> Impact -> Next Steps
3. Generate via presentation-chef

### For All-Hands
1. Ask for: company update, metrics, wins, challenges, roadmap, team updates
2. Structure: State of the Company -> Metrics -> Wins -> Challenges -> Roadmap -> Team -> Q&A
3. Generate via presentation-chef

## Design
- Dark theme with glassmorphism (presentation-chef default)
- One key message per slide
- Data visualizations for metrics
- Professional typography
- Slide transitions and animations
- 10-15 slides max

## Output
Self-contained .html file saved to current directory. Opens in any browser. Ready for presentation.
