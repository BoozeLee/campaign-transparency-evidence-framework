# SEC Insider Trading (Form 4) — Executive Stock Transaction Intelligence

## Dataset Profile
- **File**: `insider_transactions_data.csv` (from sec_insider)
- **Size**: 13 MB (49,709 records)
- **Period**: Q4 2025 (October 1 — December 5, 2025)
- **Source**: SEC EDGAR
- **License**: CC0-1.0

## Schema
| Column | Description |
|--------|-------------|
| `cik` | SEC Central Index Key |
| `company_name` | Company name |
| `form_type` | 4 or 4/A (amendment) |
| `filing_date` | Filing timestamp |
| `filing_url` | Direct link to filing |

## Key Findings
- **49,709 insider transactions** from **19,809 unique insiders**
- Covers CEOs, CFOs, Directors, and major shareholders
- **100% completeness** score with zero missing fields
- **4,176 duplicate filings** flagged — non-trivial overlap suggests amendment activity
- Data freshness: **3 days** from filing
- All Form 4 transactions (open market, grants, awards, conversions)

## Campaign Value
1. **Insider sentiment analysis** — Track executive confidence in financial institutions
2. **Suspicious timing detection** — Cross-reference trades with 8-K material events
3. **Custody/trustee insider activity** — Monitor insiders at target institutions
4. **Pattern recognition** — Identify systematic insider selling before negative disclosures
5. **Regulatory evidence** — Use insider trading patterns to support opacity claims

## Analysis Potential
- Build insider sentiment indices for financial sector
- Detect clusters of insider selling before material events
- Identify insiders with consistently suspicious timing
- Cross-reference with SEC enforcement actions
