# Public Company Federal Compliance Record — OSHA & Regulatory Violations

## Dataset Profile
- **File**: `public_companies_federal_compliance.csv`
- **Size**: 1.1 MB (42,302 records)
- **Source**: US Federal agencies (OSHA, EPA, DOL, etc.)
- **License**: CC BY 4.0

## Schema (38 columns)
| Column | Description |
|--------|-------------|
| `employer_name` | Company establishment name |
| `city`, `state`, `zip` | Physical location |
| `naics_code` / `naics_description` | Industry classification |
| `parent_name` | Corporate parent |
| `parent_cik` | SEC CIK of parent |
| `parent_ticker` | Stock ticker |
| `osha_inspections` | Number of OSHA inspections |
| `osha_violations` | Number of OSHA violations |
| `osha_total_penalties` | Total penalty amount |
| `osha_fatalities` | Workplace fatalities |
| `osha_hospitalizations` | Hospitalizations from incidents |

## Key Findings
- **42,302 records** covering US corporate compliance history
- Links subsidiary-level compliance to **parent CIK/ticker** for cross-referencing
- Includes OSHA, environmental, and other federal regulatory data
- Penalties, violations, and inspections quantified

## Campaign Value
1. **Regulatory compliance track record** — Use as proxy for institutional governance quality
2. **Subsidiary mapping** — Link corporate parents to their operating entities
3. **Cross-reference with SEC data** — CIK enables JOIN with EDGAR datasets
4. **Governance scoring** — Incorporate compliance history into institutional opacity scoring
5. **Pattern detection** — Identify institutions with systematic compliance failures

## Analysis Potential
- Build compliance score by CIK for all public companies
- Correlate compliance failures with insider trading patterns
- Identify financial sector firms with OSHA/environmental violations
- Map subsidiary networks of major financial institutions
