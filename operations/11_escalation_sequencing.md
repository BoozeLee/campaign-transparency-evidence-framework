# Escalation Sequencing & Litigation Hold Triggers

## Purpose
Define clear, deterministic thresholds for escalating from monitoring to regulatory action. Prevents premature engagement and ensures readiness when escalation occurs.

## Escalation Levels

### Level 0 — Monitoring
| State | Normal intelligence gathering |
|-------|------------------------------|
| Activity | Data collection, pattern analysis, no external engagement |
| Evidence Handling | Standard encrypted storage |
| Legal Status | No legal hold — standard retention |
| Media | None |

### Level 1 — Inquiry
| State | Active investigation of specific concern |
|-------|------------------------------------------|
| Trigger | Concern classification reached (see signal/violation doc) |
| Activity | Informal information requests, focused data collection |
| Evidence Handling | Confidence scoring active, corroboration sought |
| Legal Status | No legal hold — monitor retention |
| Media | Prep internal briefing materials |

### Level 2 — Preparation
| State | Preparing regulatory referral |
|-------|------------------------------|
| Trigger | Breach Indicator classification on material issue |
| Activity | Build evidence package, consult legal advisor, identify regulator |
| Evidence Handling | WORM storage enabled, RFC 3161 timestamping active |
| Legal Status | Legal hold PREPARATION — ready to activate |
| Media | Draft journalist briefing, embargo template ready |

### Level 3 — Engagement
| State | Regulatory referral submitted or media engagement active |
|-------|----------------------------------------------------------|
| Trigger | Confirmed Violation OR Breach Indicator + 2+ independent corroborations |
| Activity | File regulatory complaint, brief selected journalists |
| Evidence Handling | Full WORM + timestamping + chain of custody |
| Legal Status | Legal hold ACTIVATED — no deletion, intensified logging |
| Media | Controlled journalist briefings, embargoed materials |

### Level 4 — Escalation
| State | Public campaign, multiple regulatory referrals, media coverage |
|-------|--------------------------------------------------------------|
| Trigger | Regulatory inaction or institution non-response |
| Activity | Multi-regulator simultaneous filing, media coordination, parliamentary engagement |
| Evidence Handling | Maximum security — mirrored storage, legal counsel review |
| Legal Status | Legal hold STAYS ACTIVE — no changes without counsel |
| Media | Coordinated multi-outlet briefings, white paper publication |

## Escalation Decision Matrix

| Condition | Signal | Concern | Breach Indicator | Confirmed Violation |
|-----------|--------|---------|-----------------|-------------------|
| Single instance | Level 0 | Level 1 | Level 2 | Level 3 |
| Multiple instances, same institution | Level 1 | Level 2 | Level 3 | Level 3 |
| Multiple instances, multiple institutions | Level 1 | Level 2 | Level 3 | Level 4 |
| Pattern persists >6 months | Level 1 | Level 2 | Level 3 | Level 4 |
| Institution non-responsive | Level 1 | Level 2 | Level 3 | Level 3 |
| Media interest emerges | Level 1 | Level 2 | Level 3 | Level 4 |

## Escalation Authorization
| Level | Authorized By | Notification |
|-------|---------------|--------------|
| 0 → 1 | Lead investigator | Team log |
| 1 → 2 | Campaign director | Full team notification |
| 2 → 3 | Campaign director + legal counsel | All stakeholders |
| 3 → 4 | Campaign director + legal counsel + board/advisors | Full activation |

## De-escalation
Escalation level may DECREASE only when:
- Issue resolved to campaign's satisfaction
- Institution demonstrates remediation
- Evidence does not support continued pursuit
- Legal counsel advises withdrawal

De-escalation must be documented with rationale.

## Escalation Status Template
```
ESCALATION STATUS REPORT
────────────────────────
Current Level:    {0-4}
Date Reached:     {YYYY-MM-DD}
Authorized By:    {name}

Trigger Event:
  {description}

Active Measures:
  - {measure 1}
  - {measure 2}

Next Threshold:
  {what would trigger next level}

De-escalation Conditions:
  {what would cause reduction}
```
