# Top 100 ETF Holdings — ETF Custody & Asset Transparency

## Dataset Profile
- **File**: `top100_etf_holdings.csv`
- **Size**: 2.1 MB (132,182 records)
- **Date**: As of July 9, 2025
- **Source**: Web-scraped ETF provider data
- **License**: CC-BY-SA-4.0

## Schema
| Column | Description |
|--------|-------------|
| `etf_symbol` | ETF ticker (e.g., VOO, SPY, IVV) |
| `etf_title` | Full ETF name and exchange |
| `as_of` | Data timestamp |
| `holding_symbol` | Underlying asset ticker |
| `holding_name` | Underlying asset company name |
| `weight_pct` | Portfolio weight (decimal, e.g., 0.0683 = 6.83%) |
| `shares` | Number of shares held |
| `market_value_usd` | Market value in USD |

## Key Findings
- **132,182 individual holdings** across the **top 100 ETFs by AUM**
- Top holdings include MSFT (6.83% of VOO), NVDA (6.6%), AAPL (6.02%)
- Provides **full portfolio transparency** for largest ETFs
- Weight percentages allow concentration analysis
- Market values enable cross-verification with 13F filings

## Campaign Value
**This is one of the most critical datasets for the ETF custody transparency campaign:**

1. **Custody verification** — Compare ETF holdings with what custodians report
2. **Counterparty identification** — Identify which institutions hold ETF shares
3. **Concentration risk analysis** — Find ETFs with concentrated exposure to opaque assets
4. **Weight discrepancies** — Detect differences between reported and actual holdings
5. **Short selling / lending tracking** — Identify shares available for lending programs

## Analysis Potential
- Cross-reference holdings with SEC 13F filings for discrepancy detection
- Identify ETFs with unusually high weight in hard-to-value assets
- Track ETF rebalancing patterns over time
- Build network of ETF-to-issuer relationships
- Detect synthetic replication vs. physical replication discrepancies

## Research Questions for Campaign
1. Do custodians report holding the same shares that ETFs disclose?
2. Are there systematic discrepancies in weight reporting?
3. Which ETFs have the highest concentration in financial intermediary stocks?
4. Can we track the custody chain from ETF → custodian → sub-custodian?
