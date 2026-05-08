# Culture and Corporate Misconduct — Chinese A-Share Corporate Governance

## Dataset Profile
- **File**: `Culture and Corporate Misconduct new.csv`
- **Size**: 4.3 MB (41,514 records)
- **Source**: Chinese A-share listed companies
- **License**: CC0-1.0

## Schema (21 columns)
| Column | Description |
|--------|-------------|
| `code` | Company stock code |
| `year` | Observation year |
| `Size` | Company size (log) |
| `Lev` | Leverage ratio |
| `ROA` | Return on Assets |
| `Growth` | Revenue growth |
| `Dual` | CEO/Chairman duality indicator |
| `TOP1` | Largest shareholder percentage |
| `FirmAge` | Company age (log) |
| `misconduct` | Type of misconduct |
| `misconduct_binary` | Misconduct flag (0/1) |
| `wh_100km/200km/300km` | Distance to water sources (for environmental violations) |

## Key Findings
- 41,514 firm-year observations of Chinese listed companies
- Links corporate governance variables (ownership concentration, leverage, duality) to misconduct
- Includes geographic variables for environmental violation analysis
- Provides a framework for modeling misconduct risk

## Campaign Value
1. **Governance → misconduct model** — Framework for predicting institutional misconduct
2. **Ownership concentration** — TOP1 variable shows how ownership structure affects behavior
3. **Cross-cultural comparison** — Compare governance patterns across regulatory regimes
4. **Misclassification framework** — Methodology for categorizing types of misconduct

## Analysis Potential
- Apply governance→misconduct model to Western financial institutions
- Correlate ownership concentration with opacity in ETF custody
- Use geographic distance variables for environmental enforcement analysis
- Build cross-cultural governance comparison framework
