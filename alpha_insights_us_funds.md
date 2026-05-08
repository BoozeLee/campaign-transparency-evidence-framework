# Alpha Insights: US Funds — Complete US Fund Universe

## Dataset Profile
- **Files**: `ETFs.csv` (2,310 ETFs, 142 columns), `MutualFunds.csv` (23,783 funds, 298 columns), ETF/MF price history (2.0 GB total)
- **Size**: 2.0 GB (largest dataset)
- **Period**: Historical through February 2024
- **Source**: Financial data aggregator
- **License**: CC0-1.0

## Schema Highlights (ETFs — 142 columns)
| Column | Description |
|--------|-------------|
| `fund_symbol` | Ticker symbol |
| `fund_short_name` / `fund_long_name` | Fund names |
| `fund_category` | Investment category (e.g., Large Blend, Foreign Large Growth) |
| `fund_family` | Issuer family (Vanguard, BlackRock, State Street, etc.) |
| `exchange_code` / `exchange_name` | Listing exchange |
| `total_net_assets` | AUM |
| `avg_vol_3month` / `avg_vol_10day` | Trading volume |
| `day50_moving_average` | Price trend |
| `currency` | Denomination |

## Schema Highlights (Mutual Funds — 298 columns)
Includes all ETF columns plus:
- `initial_investment` / `subsequent_investment` — Minimum investment requirements
- `management_name` / `management_bio` — Fund manager details
- Expense ratios, turnover, load structures
- Performance data across multiple timeframes

## Price History Files
- `ETF prices.csv` (193 MB) — Historical ETF price data
- `MutualFund prices - [A-E/F-K/L-P/Q-Z].csv` (1.7 GB total) — Mutual fund NAV history

## Key Findings
- **2,310 ETFs** and **23,783 mutual funds** in the US market
- 142 data points per ETF, 298 per mutual fund
- Complete fund family mappings (Vanguard, BlackRock, State Street, Fidelity, etc.)
- Full price history for backtesting and analysis
- Category classifications enable peer group analysis

## Campaign Value
1. **Fund family relationships** — Map all funds to their parent companies (crucial for custody analysis)
2. **Custodian identification** — Fund family often reveals the custodian bank
3. **AUM concentration** — Identify largest fund families and their custody needs
4. **Category analysis** — Focus on funds in categories most relevant to transparency issues
5. **Management details** — Track individuals responsible for fund oversight

## Analysis Potential
- Build fund family → custodian relationship map
- Identify funds with unusual category classifications (potential red flag)
- Cross-reference ETF category with actual holdings for style drift
- Analyze AUM concentration in fund families using specific custodians
- Track management changes at funds holding opaque assets
