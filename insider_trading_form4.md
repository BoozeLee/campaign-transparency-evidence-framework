# Insider Trading SEC Form 4 — Historical Insider Transaction Database

## Dataset Profile
- **File**: `Insider Trading (SEC Form 4) I.csv`
- **Size**: 301 KB (7,704 records)
- **Period**: Through December 2021
- **Source**: SEC EDGAR
- **License**: U.S. Government Works

## Schema (18 columns)
| Column | Description |
|--------|-------------|
| `Filing Date` | When the filing was submitted |
| `Trade Date` | When the trade occurred |
| `Ticker` | Stock symbol |
| `Company Name` | Issuer name |
| `Insider Name` | Individual's name |
| `Title` | Role (CEO, CFO, Dir, etc.) |
| `Trade Type` | A-Grant, S-Sale, P-Purchase, etc. |
| `Price` | Transaction price |
| `Qty` | Number of shares |
| `Owned` | Shares owned after transaction |
| `ΔOwn` | Change in ownership percentage |
| `Value` | Dollar value of transaction |

## Key Findings
- **7,704 insider trades** with full metadata
- Covers grants (A), sales (S), purchases (P), and other transaction types
- Includes price, quantity, and post-trade ownership
- ΔOwn field enables ownership percentage change analysis
- Historical data complementing the 2025 Q4 dataset

## Campaign Value
1. **Historical baseline** — Compare current insider activity to historical patterns
2. **Enforcement cross-reference** — Check if fraud companies had suspicious insider trades
3. **Ownership trajectory** — Track insider ownership changes over time
4. **Price analysis** — Correlate trade prices with subsequent events

## Analysis Potential
- Merge with 2025 Q4 insider data for continuous timeline
- Cross-reference with fraud companies dataset
- Analyze insider trading patterns around 8-K material events
- Build insider sentiment indicator for financial sector
