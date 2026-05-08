# SEC Smart Money Dataset — Institutional Intelligence with AI Scoring

## Dataset Profile
- **Files**: `MASTER_DATA_ENRICHED.csv`, `insider_transactions_data.csv`, `institutional_holdings_data.csv`, `PREMIUM_CROSS_MARKET_SIGNALS.csv`
- **Size**: 31 MB (671 enriched records)
- **Period**: Q1 2025
- **Source**: SEC EDGAR (13F-HR + Form 4)
- **License**: Attribution 4.0 International

## Schema (Enriched Dataset — 36 columns)
| Column | Description |
|--------|-------------|
| `cik` | SEC Central Index Key |
| `company_name` | Issuer name |
| `form_type` | 13F-HR or 4 |
| `filing_date` | Filing timestamp |
| `parse_status` | PENDING/COMPLETE/ERROR |
| `security_type_table` | 13F Holding, Non-Derivative, Derivative |
| `transaction_type` | Holding, Buy, Sell, Grant, Award |
| `insider_analytics` | AI-generated insider role/pattern classification |
| `filing_analysis` | AI analysis of filing content |
| `conviction_score` | 0–100 confidence in transaction signal |
| `confidence_score` | Parse confidence (26.51–100.0, mean 80.14) |

## Cross-Market Signals (PREMIUM_CROSS_MARKET_SIGNALS.csv)
- **355 signals** combining Form 4 buys + 13F institutional holdings
- Key fields: `form4_high_confidence_buys`, `form13f_holding_value`, `form13f_conviction_score`
- Example: Amazon had multiple high-confidence insider buys + $1.7B institutional holdings

## Key Findings
- Dataset applies **AI-powered analytics** to raw SEC filings
- **10 normalization phases** completed for schema consistency
- Cross-market signals integrate **insider trading + institutional holdings**
- Examples of high-conviction signals detected
- Enables **quantitative conviction scoring** of SEC filing intelligence

## Campaign Value
1. **AI-enhanced transparency analysis** — Use the same methodology for ETF custody filings
2. **Conviction scoring** — Apply to target institutions for opacity metrics
3. **Cross-market signal detection** — Identify coordinated institutional behavior
4. **Automated SEC filing analysis** — Template for building your own filing analyzer
5. **Institutional holding patterns** — Track major holders of financial intermediaries

## Analysis Potential
- Build automated ETF custody filing monitoring system
- Create opacity conviction scores for financial institutions
- Cross-reference insider activity with custody structure changes
- Develop predictive models for institutional behavior
