# UK-Pharmaceutical-Commercial-Analytics---SGLT2-Market
Power BI commercial analytics project analysing NHS SGLT2 prescribing trends, competitive market share, growth drivers and geographic opportunity across England.

## Project Overview

This project transforms publicly available NHS prescribing and GP population data into commercial intelligence for the SGLT2 inhibitor market in England.

The analysis evaluates:

- Market growth and prescribing trends
- Competitive market share by molecule
- Contribution to category growth
- Geographic utilisation across Integrated Care Boards (ICBs)
- Commercial opportunity segmentation
- Analytical limitations and decision-making implications

## Business Question

> Where are the strongest commercial opportunities within the SGLT2 inhibitor market in England, how is the competitive landscape changing, and which geographic areas show potential for further market development?

## Dashboard

### Executive Commercial Overview

![Executive Commercial Overview](images/executive_overview.png)

Key findings:
- SGLT2 prescribing increased by approximately 20% YoY in 2026 YTD.
- Dapagliflozin represented approximately 73% of prescription-item market share.
- Category growth was highly concentrated, with dapagliflozin contributing more than 100% of net market growth as several competing molecules declined.

### Geographic Opportunity Analysis

![Geographic Opportunity](images/geographic_opportunity.png)

Geographic utilisation was normalised using registered GP population.

A Market Development Index (MDI) was developed:

MDI = Local prescriptions per 1,000 / England prescriptions per 1,000 × 100

ICBs were segmented into:

- Priority Market
- Emerging Opportunity
- Mature Market
- White Space / Investigate

based on utilisation and YoY growth relative to national benchmarks.

### Commercial Insights & Recommendations

![Commercial Insights](images/commercial_insights.png)

The analysis converts prescribing patterns into decision-oriented recommendations while explicitly recognising that low utilisation does not automatically represent commercial opportunity.

## Data Sources

- NHS Business Services Authority — English Prescribing Dataset
- NHS Digital — Patients Registered at a GP Practice

Analysis period:
**January 2025 – June 2026**

2026 YTD comparisons represent:
**January–June 2026 vs January–June 2025**

## Data Preparation

Power Query was used to:

- Combine monthly prescribing extracts
- Harmonise schema differences between historical and SNOMED-enabled datasets
- Standardise molecule and product presentation fields
- Transform monthly period fields into date values
- Match GP practices with registered population data
- Exclude unmatched/special practice codes from population-normalised geographic calculations

## Data Model

![Data Model](images/data_model.png)

The model follows a star-schema structure centred around:

- Fact_Prescribing
- Dim_Date
- Dim_Product
- Dim_Presentation
- Dim_Practice
- Practice Population

## Key DAX Measures

Measures developed include:

- Total Prescription Items
- Year-on-Year Growth
- Market Share
- Market Share Change
- Growth Contribution
- Registered Population
- Prescriptions per 1,000
- Market Development Index
- ICB YoY Growth
- Geographic Opportunity Segmentation

## Commercial Interpretation

The analysis indicates that SGLT2 market growth is not evenly distributed across molecules or geographic areas.

Dapagliflozin dominates category volume and accounts for the majority of incremental prescribing growth.

At geographic level, utilisation varies materially between ICBs. However, low utilisation is treated as a screening signal rather than direct evidence of unmet commercial demand.

## Limitations

- Prescription items do not represent unique patients.
- NIC should not be interpreted as manufacturer revenue.
- Volume market share does not necessarily equal revenue market share.
- Registered population is a proxy rather than the clinically eligible population.
- Indication-level prescribing cannot be directly observed.
- Some special or historical prescribing codes could not be matched to registered population data.
- Observed relationships should not be interpreted as causal.

## Future Development

Potential extensions include:

- Diabetes prevalence
- CKD prevalence
- Heart failure prevalence
- Age structure
- Deprivation
- Local prescribing policy
- Formulary information
- Monthly population denominators
- Product-level value analysis

## Tools & Skills

**Power BI | DAX | Power Query | Data Modelling | Star Schema | Healthcare Analytics | Commercial Analytics | Market Share Analysis | Geographic Benchmarking | Data Visualisation**

## Author

**Razaqa Muhammad Hanif Subagyo**

MSc Management of Information Systems & Digital Innovation  
Warwick Business School
