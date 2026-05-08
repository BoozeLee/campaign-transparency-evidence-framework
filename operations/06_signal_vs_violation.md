# Regulatory Signal vs. Violation Classification

## Purpose
Avoid conflating "unusual" with "illegal." Regulators respond to demonstrable inconsistencies and procedural failures, not to opacity itself. This classification system ensures proportional, credible escalation.

## Classification Framework

| Classification | Definition | Regulatory Response | Confidence Required |
|--------------|------------|-------------------|-------------------|
| **Signal** | Anomaly meriting further inquiry | Internal note, monitor | 1 (Lead) |
| **Concern** | Material inconsistency in disclosure | Informal query, request clarification | 2 (Indicative) |
| **Breach Indicator** | Evidence suggesting rule violation | Formal inquiry, request documents | 3 (Corroborated) |
| **Confirmed Violation** | Officially established violation | Enforcement action, penalty, referral | 5 (Confirmed per regulator) OR 4 (per independent verification of clear rule) |

## Examples by Classification

### Signal
- ETF holding weight doesn't match disclosed methodology
- Custodian changed without public disclosure
- Unusual concentration in hard-to-value assets
- Timing pattern around reporting dates

### Concern
- Two consecutive quarters of unexplained custodian changes
- Disclosed custody structure differs from 13F filings
- Insider selling precedes custodian change announcement
- Repeated failure to respond to investor inquiries within stated timelines

### Breach Indicator
- Custodian confirms different holdings than ETF discloses
- SEC filing omits required custody disclosure
- Multiple investors report same opacity pattern independently
- Internal document contradicts public disclosure

### Confirmed Violation
- SEC/FSMA/FMA enforcement action published
- Court ruling establishes violation
- Regulatory settlement admits facts
- Institution's own audit confirms breach

## Escalation Path
```
Signal ──→ Monitor quarterly
  │
  ├── persists ──→ Concern ──→ Informal inquiry
  │                            │
  │                            ├── resolved → Close
  │                            └── persists → Breach Indicator
  │                                           │
  │                                           ├── multiple → Regulatory Referral
  │                                           └── confirmed → Confirmed Violation
  │
  └── resolved → Close
```

## Classification Template
```
CLASSIFICATION RECORD
─────────────────────
Evidence ID:     EVID-{DATE}-{SEQ}
Title:           {brief description}

Current Classification: {Signal | Concern | Breach Indicator | Confirmed Violation}
Previous Classification: {if upgraded/downgraded}

Rationale:
  {specific regulatory rule or principle engaged}
  {specific fact pattern}
  {why this meets the classification threshold}

Regulatory Rules Engaged:
  - {rule reference 1}
  - {rule reference 2}

Supporting Evidence:
  - {evidence ID} — {confidence score}
  - {evidence ID} — {confidence score}

Next Action:
  {monitor / escalate to informal query / file regulatory referral / prepare complaint}
```
