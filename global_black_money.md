# Global Black Money Transactions — Suspicious Financial Flow Intelligence

## Dataset Profile
- **File**: `Big_Black_Money_Dataset.csv`
- **Size**: 1.4 MB (10,000 records)
- **Period**: 2013–2024 (synthetic/generated)
- **License**: Apache 2.0

## Schema (14 columns)
| Column | Description |
|--------|-------------|
| `Transaction ID` | Unique identifier |
| `Country` | Source country |
| `Amount (USD)` | Transaction value |
| `Transaction Type` | Offshore Transfer, Stocks Transfer, Real Estate, etc. |
| `Date of Transaction` | Timestamp |
| `Person Involved` | Anonymized person ID |
| `Industry` | Construction, Luxury Goods, Energy, etc. |
| `Destination Country` | Receiving jurisdiction |
| `Reported by Authority` | Boolean — flagged or not |
| `Source of Money` | Illegal, Tax Evasion, Corruption, Drug Trafficking, etc. |
| `Money Laundering Risk Score` | Risk rating (0–100) |
| `Shell Companies Involved` | Count of shell entities |
| `Financial Institution` | Bank or intermediary name |
| `Tax Haven Country` | Tax haven jurisdiction used |

## Key Findings (Synthetic Data)
- 10,000 labeled suspicious transactions across multiple countries
- Covers multiple money sources: illegal, tax evasion, corruption, drug trafficking
- Includes shell company involvement counts
- Tracks which transactions were reported to authorities vs. unreported
- Risk scores provide prioritization framework

## Campaign Value
1. **Methodology reference** — Understand the data schema for real suspicious transaction monitoring
2. **Shell company patterns** — Identify transaction attributes associated with shell use
3. **Reporting gap analysis** — Study the gap between detected and reported transactions
4. **Risk scoring framework** — Apply similar methodology to ETF custody transactions
5. **Industry concentration** — Note which industries are most associated with suspicious flows

## Analysis Potential
- Build risk scoring model applicable to real transaction data
- Identify transaction patterns most likely to evade reporting
- Correlate shell company usage with transaction size and jurisdiction
- Develop typologies for suspicious ETF custody transactions
