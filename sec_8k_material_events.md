# SEC 8-K Material Events — Corporate Disclosure Intelligence

## Dataset Profile
- **File**: `material_events_data.csv`, `MASTER_DATA_RAW.csv`
- **Size**: 11 MB (12,925 records)
- **Period**: Q4 2025 (October 1 — December 5, 2025)
- **Source**: SEC EDGAR
- **License**: CC0-1.0

## Schema
| Column | Description |
|--------|-------------|
| `cik` | SEC Central Index Key (10-digit) |
| `company_name` | Registered corporate name |
| `form_type` | 8-K or 8-K/A (amendment) |
| `filing_date` | Date filed with SEC |
| `filename` | EDGAR internal filename |
| `filing_url` | Direct link to filing on SEC.gov |

## Key Findings
- **12,925 filings** from **5,167 unique companies**
- **100% completeness** — zero missing CIKs, dates, or company names
- **426 duplicate filings** identified and flagged
- Data freshness: **3 days** from filing to dataset publication
- Covers all 8-K material events: M&A, executive changes, bankruptcies, asset dispositions

## Campaign Value
1. **Real-time corporate surveillance** — Track material events at target institutions
2. **Bankruptcy/insolvency tracking** — Early warning of custody/trustee failures
3. **Executive turnover patterns** — Identify institutions with governance instability
4. **M&A activity monitoring** — Track consolidation in financial services sector
5. **Event-driven investigation triggers** — Use 8-K events to time information requests

## Analysis Potential
- Correlate material events with insider trading patterns
- Build event timelines for specific financial institutions
- Identify patterns of frequent 8-K filers (potential red flags)
- Cross-reference with ETF holdings to assess portfolio impact
