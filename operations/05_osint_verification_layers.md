# OSINT Verification Integration Plan

## Purpose
Integrate publicly available registries and databases to cross-verify evidence, identify beneficial ownership, and map institutional relationships.

## Primary OSINT Sources

### Sanctions & Watchlists
| Source | Coverage | API | Use Case |
|--------|----------|-----|----------|
| OpenSanctions | Global sanctions, PEPs, criminals | Free API | Cross-reference PSC names against sanctions lists |
| OFAC SDN List | US sanctions targets | Downloadable | Check counterparties in custody chains |
| EU Consolidated Sanctions | EU sanctions | XML feed | EU jurisdiction compliance checks |
| UN Sanctions List | UN Security Council | PDF/XML | International sanctions screening |

### Corporate Registries
| Source | Coverage | API | Use Case |
|--------|----------|-----|----------|
| OpenCorporates | 200M+ companies worldwide | API (paid tier) | Entity resolution, parent-subsidiary mapping |
| UK Companies House | UK companies | Free API | PSC lookups, company filings |
| SEC EDGAR | US public companies | Free bulk data | Cross-reference CIK → company → filings |
| GLEIF | Legal Entity Identifiers | Free API | LEI lookup for financial institutions |

### Offshore & Leaks Databases
| Source | Coverage | Access |
|--------|----------|--------|
| OCCRP Aleph | Panama Papers, Pandora Papers, Paradise Papers | Free (registration) |
| ICIJ Offshore Leaks Database | Offshore entity network | Free search |
| FinCEN Files | Suspicious activity reports | Journalist access |

### Court & Procurement
| Source | Coverage | Use Case |
|--------|----------|----------|
| PACER | US federal courts | Litigation history of target institutions |
| EU e-Justice | EU business registers | Cross-border entity verification |
| World Bank IDA/IBRD | Procurement contracts | Identify institutional counterparties |

## Integration Architecture

```
Evidence Item
    │
    ├─→ Hash → Check OpenSanctions → Score update
    ├─→ Company name → Check OpenCorporates → Entity resolution
    ├─→ Person name → Check OFAC/Sanctions → Risk flag
    ├─→ CIK/LEI → Check EDGAR/GLEIF → Cross-reference filings
    ├─→ Jurisdiction → Check CPI/Freedom Index → Context score
    └─→ Transaction pattern → Check Aleph → Link to known schemes
```

## Automated Verification Pipeline (Planned)
```
1. Extract entities from evidence (names, companies, jurisdictions)
2. Parallel lookup across OSINT sources
3. Merge results into entity profile
4. Flag matches/surprises for investigator review
5. Update confidence scores based on corroboration
6. Log all queries for audit trail
```

## OSINT Query Logging
Every query MUST be logged:
```
OSINT QUERY LOG
───────────────
Query ID:       OSINT-{YYYYMMDD}-{SEQ}
Target:         {entity searched}
Source:         {database used}
Timestamp:      {UTC}
Result:         {match / no match / partial match}
Evidence ID:    {linked evidence}
Investigator:   {name}
```
