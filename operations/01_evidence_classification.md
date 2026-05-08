# Evidence Classification System — Tier A / B / C

## Purpose
Prevent contamination across evidentiary tracks. Courts, regulators, media, and internal intelligence each have different admissibility standards. Mixing them creates legal vulnerability.

## Three Tiers

### Tier A — Court/Regulatory Admissible
| Requirement | Standard |
|-------------|----------|
| Chain of custody | Complete, signed, timestamped |
| Authentication | Cryptographic hash + RFC 3161 token |
| Preservation | WORM storage, immutable |
| Collection | Forensic tool with audit log |
| Witness | Available for testimony if needed |
| Original | Unmodified original retained |
| Metadata | Full provenance recorded |

**Use for**: SEC/FSMA/FMA complaints, civil litigation, regulatory referrals.

### Tier B — Investigative Intelligence
| Requirement | Standard |
|-------------|----------|
| Corroboration | 2+ independent sources preferred |
| Source tracking | Confidential if needed, but logged |
| Storage | Encrypted, access-controlled |
| Confidence scored | Yes (see scoring model) |
| Link analysis | Entity resolution applied |
| Caveat | Marked "NOT FORMALLY AUTHENTICATED" |

**Use for**: Internal analysis, pattern detection, lead generation, journalist briefings.

### Tier C — Media / Public Narrative
| Requirement | Standard |
|-------------|----------|
| Publicly sourced | Verifiable by recipient |
| Redacted | PII removed, GDPR-compliant |
| Contextualized | Full thread preserved, not cherry-picked |
| Attributable | On-the-record or clearly sourced |
| Proportional | No overclaiming or speculation |

**Use for**: Press briefings, white papers, case studies, public campaigns.

## Classification Flow
```
Raw Evidence Collected
    │
    ├─→ Is it from an official regulator publication? → Tier A
    ├─→ Is it a direct institution communication? → Tier A
    ├─→ Is it corroborated third-party intel? → Tier B
    ├─→ Is it a single-source lead? → Tier B (low confidence)
    └─→ Is it for public consumption only? → Tier C
```

## Evidence Tagging
Every evidence item MUST include:
- `EVID-{YYYYMMDD}-{SEQ}` — Unique ID
- `TIER-{A|B|C}` — Classification tier
- `CONF-{1-5}` — Confidence score
- `SOURCE-{type}` — Origin type
- `HASH-{SHA256}` — Content fingerprint
- `TS-{RFC3161_token}` — Timestamp proof

## Cross-Contamination Prevention
- Tier A evidence is NEVER shared with media before regulatory filing
- Tier B intelligence is NEVER cited as fact in public materials
- Tier C materials are NEVER submitted as evidence in formal proceedings
- Escalation packages separate tiers clearly with headers
