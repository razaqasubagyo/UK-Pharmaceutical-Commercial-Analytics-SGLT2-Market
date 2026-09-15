
# Data Sources

This project uses publicly available NHS datasets.

## Sources

- NHS Business Services Authority — English Prescribing Dataset
- NHS Patients Registered at a GP Practice

## Analysis Period

January 2025 – June 2026

For year-on-year comparisons:

Jan–Jun 2026 is compared with Jan–Jun 2025.

## Scope

The prescribing analysis focuses on four SGLT2 molecules:

- Dapagliflozin
- Empagliflozin
- Canagliflozin
- Ertugliflozin

## Data Preparation Notes

The raw prescribing data was filtered to the SGLT2 market before analysis.

Historical prescribing files and later SNOMED-enabled files contained slightly different schemas. These were harmonised in Power Query before being appended into a single prescribing fact table.

GP registered-population data was aggregated to practice level and matched using practice codes for population-normalised geographic analysis.

Special, unidentified, or unmatched prescribing codes were retained in overall market analysis but excluded from population-normalised geographic measures where no valid registered-population denominator was available.

## Raw Data Availability

Raw NHS prescribing files are not included in this repository due to file size.

The original datasets are publicly available from NHS data sources.
