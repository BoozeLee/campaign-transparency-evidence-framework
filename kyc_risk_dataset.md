# Synthetic KYC & Transaction Risk Dataset — AML Compliance Intelligence

## Dataset Profile
- **Files**: `clients_with_fatf_ofac.csv` (2,000 clients), `transactions_with_fatf_ofac.csv` (50,000 transactions)
- **Size**: 899 KB
- **Source**: Synthetic AML/KYC data generator
- **License**: Apache 2.0

## Schema — Clients (12 columns)
| Column | Description |
|--------|-------------|
| `client_id` | Unique client identifier |
| `client_name` | Entity name |
| `client_type` | Financial Institution, NGO, Corporation, Individual |
| `sector` | Industry sector |
| `sector_risk` | Low, Medium, High |
| `country` | ISO country code |
| `pep_flag` | Politically Exposed Person indicator |
| `sanctions_flag` | Sanctions list match |
| `fatf_country_flag` | FATF high-risk jurisdiction |
| `ofac_country_flag` | OFAC sanctioned jurisdiction |
| `sectoral_sanctions_flag` | Industry-specific sanctions |
| `ownership_opacity_score` | Beneficial ownership transparency score |

## Schema — Transactions (12 columns)
| Column | Description |
|--------|-------------|
| `transaction_id` | Unique transaction ID |
| `client_id` | Party to the transaction |
| `amount` | Transaction value |
| `transaction_type` | SWIFT, Check, Wire, Crypto |
| `timestamp` | Date and time |
| `client_country` | Origin jurisdiction |
| `counterparty_country` | Destination jurisdiction |
| `ofac_match_flag` | OFAC sanctions match |
| `fatf_country_flag` | FATF jurisdiction flag |
| `structuring_pattern_flag` | Structuring/smurfing detection |
| `rapid_movement_flag` | Rapid fund movement detection |
| `trade_mispricing_flag` | Trade-based money laundering |

## Key Findings
- **2,000 clients** with comprehensive KYC risk profiles
- **50,000 transactions** with AML/OFAC risk flags
- Covers PEP, sanctions, FATF, OFAC, and sectoral risk indicators
- `ownership_opacity_score` directly relevant to beneficial ownership transparency
- Several transaction types: SWIFT, Check, Wire, Crypto
- Structuring and rapid movement flags for sophisticated ML detection

## Campaign Value
1. **Ownership opacity scoring** — Apply methodology to real ETF custody structures
2. **FATF/OFAC cross-referencing** — Template for sanctions screening of custody chains
3. **Transaction pattern detection** — Use structuring/rapid movement flags for suspicious ETF flows
4. **PEP screening** — Identify politically exposed persons in custody chains
5. **Risk scoring model** — Build composite risk scores for financial intermediaries

## Analysis Potential
- Apply KYC risk scoring framework to real ETF custody data
- Cross-reference UK PSC beneficial owners with OFAC/FATF lists
- Build sanctions screening pipeline for custody chain analysis
- Develop ownership opacity scores for financial institutions
