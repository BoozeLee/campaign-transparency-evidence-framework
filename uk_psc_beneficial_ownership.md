# UK People with Significant Control (PSC) — Beneficial Ownership Registry

## Dataset Profile
- **File**: `persons-with-significant-control-snapshot-2017-08-23.txt`
- **Size**: 3.3 GB (4,925,567 records)
- **Source**: UK Companies House
- **License**: CC0-1.0
- **Format**: JSON-lines (one JSON object per line)

## Schema
The dataset contains 20+ fields per person, stored as nested JSON:
- `company_number` — UK company registration number
- `name` — Full name of the PSC
- `name_elements` — Structured name (forename, surname, title)
- `date_of_birth` — Month and year of birth
- `nationality` — Nationality of the PSC
- `country_of_residence` — Country where the PSC resides
- `address` — Full address (line 1, line 2, premises, locality, region, postal code, country)
- `natures_of_control` — Array of control types (e.g., ownership-of-shares-50-to-75-percent)
- `notified_on` — Date the PSC was registered
- `ceased_on` — Date the PSC ceased (if applicable)
- `kind` — Type of PSC (individual, corporate, legal person, etc.)
- `etag` — ETag for API caching
- `links.self` — API link to the PSC record

## Key Findings
- Contains **~5 million PSC records** linked to UK-registered companies
- PSCs include individuals, corporate entities, and other legal persons
- Control types range from 25%+ share ownership to voting rights control
- Address data provides geographic distribution of beneficial owners
- Many PSCs have foreign nationalities, revealing cross-border ownership structures

## Campaign Value
This is a **foundational dataset** for the cross-border financial transparency campaign:
1. **Cross-border ownership tracking** — Foreign nationals listed as PSCs reveal international ownership networks
2. **Shell company identification** — Corporate PSCs can indicate layered ownership structures
3. **Sanctions evasion detection** — Cross-reference with sanctions lists to identify hidden control
4. **Real estate transparency** — UK property is often held through companies; PSC data reveals true owners
5. **ETF custody connections** — Identify beneficial owners of financial intermediaries

## Analysis Potential
- Map foreign ownership of UK companies by nationality
- Identify PSCs with addresses in tax havens
- Cross-reference with OFAC/FATF sanctions lists
- Network analysis of corporate PSC chains
- Temporal analysis of PSC registrations and cessations
