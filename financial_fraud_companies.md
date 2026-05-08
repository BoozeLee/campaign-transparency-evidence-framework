# Companies Involved in Financial Fraud — Enforcement Target Registry

## Dataset Profile
- **File**: `fraud_companies_with_cik.csv`
- **Size**: 4 KB (226 records)
- **Source**: Compiled from SEC enforcement actions
- **License**: Apache 2.0

## Schema
| Column | Description |
|--------|-------------|
| `Company Name` | Legal name of company |
| `CIK Number` | SEC Central Index Key (10-digit) |

## Key Findings
- **226 companies** with verified financial fraud involvement
- Includes well-known names: Gartner, Philips, etc.
- Each entry has a **CIK number** enabling JOIN with full SEC EDGAR data
- Fraud types include accounting fraud, disclosure violations, and more

## Campaign Value
1. **CIK-based cross-referencing** — Link fraud companies to their SEC filings, insider trades, and 8-K events
2. **Recidivism tracking** — Monitor fraud companies for ongoing violations
3. **Pattern analysis** — Identify common characteristics of fraud companies
4. **Enhanced due diligence** — Use as a baseline for vetting financial intermediaries

## Analysis Potential
- Analyze insider trading patterns before/after fraud disclosures
- Track 8-K filings from fraud companies for related-party transactions
- Cross-reference with beneficial ownership data
- Build fraud prediction model using SEC filing patterns
