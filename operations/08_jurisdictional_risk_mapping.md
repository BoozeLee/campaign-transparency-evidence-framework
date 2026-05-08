# Jurisdictional Risk Mapping — Regulatory Intelligence

## Purpose
Different regulators have different mandates, powers, and responsiveness. Escalation strategy must adapt to the target regulator's institutional behavior, not a one-size-fits-all approach.

## Primary Target Regulators

### SEC (United States)
| Attribute | Profile |
|-----------|---------|
| **Mandate** | Investor protection, market integrity |
| **Style** | Litigation-oriented, enforcement-heavy |
| **Best Trigger** | Demonstrable disclosure violation, investor harm |
| **Response Time** | Months to years for investigation |
| **Key Leverage** | Public enforcement actions, media attention |
| **Known Weakness** | Overloaded, slow on novel issues |
| **Data Sources** | EDGAR, enforcement actions, investor alerts |

### ESMA (EU-wide)
| Attribute | Profile |
|-----------|---------|
| **Mandate** | Supervisory convergence, investor protection |
| **Style** | Coordinating, standard-setting |
| **Best Trigger** | Cross-border inconsistency, MiFID/MIFIR violation |
| **Response Time** | Medium — works through national regulators |
| **Key Leverage** | Public register warnings, supervisory briefings |
| **Known Weakness** | Limited direct enforcement power |
| **Data Sources** | FIRDS, public registers, ESMA warnings |

### FSMA (Belgium)
| Attribute | Profile |
|-----------|---------|
| **Mandate** | Investor protection, market supervision |
| **Style** | Investor-protection emphasis |
| **Best Trigger** | Retail investor harm, transparency failure |
| **Response Time** | Moderate |
| **Key Leverage** | Public warnings, sanction publications |
| **Known Weakness** | Smaller jurisdiction, resource constraints |
| **Data Sources** | FSMA warnings, sanctions page |

### FMA (Austria)
| Attribute | Profile |
|-----------|---------|
| **Mandate** | Prudential + AML + market conduct |
| **Style** | Prudential and AML emphasis |
| **Best Trigger** | AML failure, prudential concern |
| **Response Time** | Moderate |
| **Key Leverage** | Sanction publications, investor warnings |
| **Known Weakness** | Less transparent supervisory process |
| **Data Sources** | FMA sanctions archive, document database |

### FINMA (Switzerland)
| Attribute | Profile |
|-----------|---------|
| **Mandate** | Prudential, conduct, resolution |
| **Style** | Confidential supervisory — limited public disclosure |
| **Best Trigger** | Systemic risk, prudential failure |
| **Response Time** | Slow — investigates thoroughly before acting |
| **Key Leverage** | Enforcement proceedings (limited publication) |
| **Known Weakness** | Very opaque — hard to track action |
| **Data Sources** | FINMA enforcement list, media monitoring |

### FCA (United Kingdom)
| Attribute | Profile |
|-----------|---------|
| **Mandate** | Market integrity, consumer protection, competition |
| **Style** | Proactive, enforcement-capable |
| **Best Trigger** | Consumer harm, market manipulation |
| **Response Time** | Moderate to fast |
| **Key Leverage** | Decision notices, fine publications |
| **Known Weakness** | Post-Brexit regulatory divergence |
| **Data Sources** | FCA notices, warning list |

## Escalation Strategy by Regulator

```
FOR SEC TARGETS:
  Prepare litigation-grade package from Day 1
  Focus on demonstrable rule violation, not policy preference
  Reference specific SEC rules (Custody Rule, Reg SHO, etc.)
  Time filing for maximum impact (quarter-end, market stress)

FOR ESMA TARGETS:
  Emphasize cross-border coordination failure
  Reference MiFID II / MiFIR transparency requirements
  Coordinate with multiple national regulators simultaneously
  Use ESMA's Q&A process for interpretive questions

FOR FSMA/FMA TARGETS:
  Lead with investor impact
  Reference national transposition of EU directives
  Include local-language documentation
  Leverage investor warning systems
```

## Country Risk Indicators (from datasets)
```
Country Risk Profile
├── CPI Score (corruption) ───────────→ Lower = higher risk
├── Economic Freedom Index ───────────→ Lower = more opaque
├── Modern Slavery Prevalence ────────→ Higher = governance concerns
├── FATF/OFAC Status ────────────────→ Blacklist = extreme risk
└── PSC Transparency ────────────────→ Public registry = more traceable
```
