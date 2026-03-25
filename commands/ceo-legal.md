# Legal & Compliance Checklist

Generate stage-appropriate legal checklists with estimated costs and timelines.

## Input
Ask: "What stage? (a) Pre-incorporation, (b) Just incorporated, (c) Pre-fundraise, (d) Post-fundraise, (e) Scaling"

## Checklists by Stage

### Pre-Incorporation
- [ ] Choose entity type - Delaware C-Corp for VC track ($500-2K via Stripe Atlas/Clerky), LLC for bootstrapped
- [ ] Founders agreement - equity splits, vesting, roles, IP assignment ($2-5K with attorney)
- [ ] File 83(b) election within 30 DAYS of equity grant (free, but missing deadline is costly)
- [ ] IP assignment agreements for all founders (template, ~$500)

### Post-Incorporation
- [ ] EIN from IRS (free, same day)
- [ ] State registrations where you operate ($100-500/state)
- [ ] Standard NDA template ($500 or use free templates)
- [ ] Contractor agreements for any non-employee work ($500-1K)
- [ ] Privacy policy + Terms of Service ($1-3K or use generators)
- [ ] Business bank account

### Pre-Fundraise
- [ ] Clean cap table (use Carta, Pulley, or spreadsheet)
- [ ] Board consent for fundraising
- [ ] SAFE or convertible note templates (use YC SAFE - free)
- [ ] 409A valuation if issuing options ($5-15K)
- [ ] Option pool sized at 10-15% of fully diluted shares

### Post-Fundraise
- [ ] Investor rights agreement
- [ ] Board composition and governance
- [ ] D&O insurance ($2-5K/year)
- [ ] Regular board meetings (quarterly minimum)
- [ ] Monthly investor updates

## Industry-Specific Compliance
Load from @ceo-assistant/docs/industry-benchmarks.md:
- **FinTech**: FinCEN registration, state money transmitter licenses ($50-200K), PCI DSS
- **HealthTech**: HIPAA compliance ($50-150K initial), BAAs with all vendors, security assessments
- **EdTech**: FERPA, COPPA (if users under 13), SOC 2
- **SaaS/B2B**: SOC 2 Type II ($20-50K) often required for enterprise sales
- **Any with EU users**: GDPR compliance ($10-50K)

## Output
Prioritized checklist with cost estimates and deadlines.

**Disclaimer:** This is a planning framework, not legal advice. Work with a startup attorney for your specific situation. Recommendations: Clerky (incorporation), Stripe Atlas (quick setup), Cooley GO (free legal docs), YC SAFE (fundraising).
