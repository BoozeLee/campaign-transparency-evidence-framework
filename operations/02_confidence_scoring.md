# Evidence Confidence Scoring Model

## Purpose
Prevent weak evidence from contaminating filings, media briefings, or escalation packages. Every piece of evidence gets a confidence score recorded at ingestion.

## Score Definitions

| Score | Label | Definition | Examples |
|-------|-------|------------|----------|
| 5 | **Confirmed** | Official regulatory or judicial determination | SEC enforcement order, FMA sanction notice, court ruling, regulator-published investor warning |
| 4 | **Authenticated** | Institution-verified communication | Signed letter from compliance officer, board resolution, official filing (8-K, 13F), verified email from corporate domain |
| 3 | **Corroborated** | Multiple independent sources agree | Two+ whistleblowers giving same account, documents from different sources with matching data, journalist-confirmed with 2 sources |
| 2 | **Indicative** | Single credible source | One whistleblower, one leaked document, single-source news report with named source |
| 1 | **Lead** | Unverified, needs investigation | Anonymous tip, forum post, social media claim, pattern anomaly without explanation |

## Scoring Rules

1. **Score decays over time** — evidence older than 2 years drops 1 confidence level unless refreshed
2. **Score requires documentation** — every score MUST have a rationale recorded
3. **Score is reassessable** — new corroboration can upgrade; contradictory evidence must downgrade
4. **Tier boundaries** — Tier A requires score ≥ 4; Tier B requires score ≥ 2; Tier C has no minimum

## Scoring Template
```
EVIDENCE CONFIDENCE ASSESSMENT
─────────────────────────────
Evidence ID:     EVID-{DATE}-{SEQ}
Description:     {brief description}
Assessor:        {name/role}
Date Assessed:   {YYYY-MM-DD}

Score Assigned:  {1-5}
Rationale:       {why this score}

Supporting Items:
  - {item 1}
  - {item 2}

Corroboration Status:
  - Sources agreeing: {N}
  - Sources contradicting: {N}
  - Independent verification: {yes/no}

Score History:
  {date}: Initial score {N} — {rationale}
  {date}: Updated to {N} — {reason for change}
```

## Degradation Rules
- Score 5 → 4 after 3 years without reconfirmation
- Score 4 → 3 after 2 years without reconfirmation
- Score 3 → 2 if sole source becomes unavailable
- Score 2 → 1 if single source credibility is challenged
- Score 1 expires after 6 months without progression
