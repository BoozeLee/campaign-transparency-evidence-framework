# Cross-Border Financial Transparency Campaign — Data Analysis Library

## Overview
This directory contains **20 detailed analysis articles** covering datasets downloaded from Kaggle for the cross-border financial transparency campaign. Each article covers: schema, key findings, campaign value, and analysis potential.

## Operations Manual (12 Documents)
The `operations/` subdirectory contains the full litigation-grade operational framework. Start here:
> **[operations/00_operations_index.md](operations/00_operations_index.md)** — Full index of all 12 operations documents

### Quick Reference by Function
| Function | Primary Document |
|----------|-----------------|
| Evidence classification (Tier A/B/C) | [01_evidence_classification.md](operations/01_evidence_classification.md) |
| Evidence confidence scoring (1-5) | [02_confidence_scoring.md](operations/02_confidence_scoring.md) |
| WORM storage, RFC 3161, legal hold | [03_preservation_and_timestamping.md](operations/03_preservation_and_timestamping.md) |
| Narrative attack resistance | [04_narrative_attack_resistance.md](operations/04_narrative_attack_resistance.md) |
| OSINT verification integration | [05_osint_verification_layers.md](operations/05_osint_verification_layers.md) |
| Signal vs. violation classification | [06_signal_vs_violation.md](operations/06_signal_vs_violation.md) |
| Journalist evidence packaging | [07_journalist_evidence_packaging.md](operations/07_journalist_evidence_packaging.md) |
| Jurisdictional risk mapping | [08_jurisdictional_risk_mapping.md](operations/08_jurisdictional_risk_mapping.md) |
| OPSEC protocol | [09_opsec_protocol.md](operations/09_opsec_protocol.md) |
| Pattern intelligence framework | [10_pattern_intelligence_framework.md](operations/10_pattern_intelligence_framework.md) |
| Escalation sequencing & triggers | [11_escalation_sequencing.md](operations/11_escalation_sequencing.md) |

## Dataset Categories

### Tier 1 — Directly Relevant to ETF Custody Transparency
| # | Article | Dataset | Size | Source |
|---|---------|---------|------|--------|
| 1 | [ETF Holdings — Top 100](etf_holdings_top100.md) | Full holdings of 100 largest ETFs | 2.1 MB | Web |
| 2 | [Alpha Insights — US Funds](alpha_insights_us_funds.md) | 2,310 ETFs + 23,783 mutual funds | 2.0 GB | Financial data |
| 3 | [SEC Smart Money](sec_smart_money.md) | AI-enriched 13F + Form 4 analysis | 31 MB | SEC EDGAR |
| 4 | [UK PSC Beneficial Ownership](uk_psc_beneficial_ownership.md) | 4.9M UK company beneficial owners | 3.3 GB | Companies House |

### Tier 2 — Regulatory Enforcement & Fraud
| # | Article | Dataset | Size | Source |
|---|---------|---------|------|--------|
| 5 | [SEC 8-K Material Events](sec_8k_material_events.md) | 12,925 material event filings | 11 MB | SEC EDGAR |
| 6 | [SEC Insider Trading Q4 2025](sec_insider_trading.md) | 49,709 insider transactions | 13 MB | SEC EDGAR |
| 7 | [Insider Trading Form 4 (Historical)](insider_trading_form4.md) | 7,704 historical insider trades | 301 KB | SEC EDGAR |
| 8 | [Financial Fraud Companies](financial_fraud_companies.md) | 226 fraud companies with CIK | 4 KB | SEC |
| 9 | [Crypto Regulation Enforcement](crypto_regulation_enforcement.md) | 63 enforcement actions | 4 KB | Regulatory |

### Tier 3 — Compliance & Risk
| # | Article | Dataset | Size | Source |
|---|---------|---------|------|--------|
| 10 | [Public Company Compliance](public_company_compliance.md) | 42,302 OSHA/regulatory records | 1.1 MB | US Federal |
| 11 | [KYC/AML Risk Dataset](kyc_risk_dataset.md) | 2,000 clients + 50,000 transactions | 899 KB | Synthetic |
| 12 | [Global Black Money](global_black_money.md) | 10,000 suspicious transactions | 1.4 MB | Synthetic |

### Tier 4 — Transparency & Governance Indicators
| # | Article | Dataset | Size | Source |
|---|---------|---------|------|--------|
| 13 | [Corruption Perception Index](corruption_perception_index.md) | Multi-country CPI scores | 723 KB | Transparency Int'l |
| 14 | [Economic Freedom Index](freedom_economic_index.md) | 184 countries scored | 12 KB | Heritage Foundation |
| 15 | [S&P 500 Integrity Scores](sp500_integrity_scores.md) | 503 companies, 11 dimensions | 14 KB | Corporate ethics |
| 16 | [ESG Ratings](esg_ratings.md) | 722 companies ESG graded | 42 KB | Finnhub |

### Tier 5 — Supporting & Contextual
| # | Article | Dataset | Size | Source |
|---|---------|---------|------|--------|
| 17 | [Corruption & Bribery Incidents](corruption_bribery.md) | 3,476 citizen reports | 103 KB | Crowdsourced |
| 18 | [Corporate Greenwashing](corporate_greenwashing.md) | ESG deception indicators | 21 KB | Academic |
| 19 | [Corporate Misconduct (China)](corporate_misconduct.md) | 41,514 firm-year observations | 4.3 MB | Chinese A-shares |
| 20 | [Modern Slavery Index](modern_slavery.md) | 179 countries | 6 KB | Walk Free |

## Campaign Integration Map

```
ETF CUSTODY TRANSPARENCY CAMPAIGN
├── Primary Data Sources
│   ├── ETF Holdings ──────────────────→ top100_etf_holdings.csv
│   ├── US Fund Universe ──────────────→ ETFs.csv, MutualFunds.csv
│   ├── Beneficial Ownership ──────────→ UK PSC (3.3 GB)
│   └── SEC Smart Money ──────────────→ AI-enriched 13F/Form 4
│
├── Regulatory Evidence
│   ├── SEC 8-K Filings ──────────────→ material events tracking
│   ├── Insider Trading ──────────────→ Form 4 transactions
│   ├── Financial Fraud ──────────────→ fraud companies with CIK
│   └── Crypto Enforcement ───────────→ regulatory action patterns
│
├── Compliance & Risk Assessment
│   ├── KYC/AML Risk ────────────────→ sanctions screening template
│   ├── Public Compliance ────────────→ regulatory violation history
│   └── Black Money Patterns ─────────→ suspicious transaction typologies
│
└── Country & Governance Benchmarking
    ├── Corruption Perception ────────→ jurisdiction risk scoring
    ├── Economic Freedom ──────────────→ institutional quality metrics
    ├── Integrity Scores ──────────────→ corporate ethics benchmark
    ├── ESG Ratings ──────────────────→ governance quality proxy
    └── Modern Slavery ────────────────→ human rights context
```

## Total Data Volume
- **21 datasets** across 5 tiers
- **~5.7 GB** total extracted data
- Covers **SEC, UK Companies House, global indices, and regulatory data**

## Key Cross-Dataset JOIN Keys
- `CIK` (SEC Central Index Key) — Links SEC 8-K, Insider Trading, Smart Money, Compliance, and Fraud datasets
- `ticker` — Links Integrity Scores, ESG Ratings, Insider Trading, and ETF Holdings
- `company_number` (UK) — Core key for UK PSC registry
- `Country` / `Region` — Links CPI, Freedom Index, Modern Slavery, and Black Money datasets

## Next Steps
1. Build cross-reference pipeline using CIK as primary key
2. Load ETF holdings → identify custodians → cross-check with 13F filings
3. Apply KYC risk scoring framework to real ETF custody chain data
4. Cross-reference UK PSC with OFAC/FATF sanctions lists
5. Build composite opacity scores for target financial institutions
