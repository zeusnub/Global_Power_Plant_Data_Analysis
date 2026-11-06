# Global Power Plant Database — Data Cleaning & Analysis

An end-to-end analysis of the **Global Power Plant Database** published by the World Resources Institute (WRI): data quality, installed electricity-generation capacity, country-wise distribution, fuel mix, and historical electricity generation. The project includes a structured spreadsheet workflow, data-quality checks, analytical summaries, and a KPI-driven dashboard.

> **Tools:** ONLYOFFICE Desktop Editors · Excel-compatible Spreadsheet Formulas · Spreadsheet Charts  
> **Dataset:** [Global Power Plant Database (WRI)](https://github.com/wri/global-power-plant-database)  
> **Source CSV:** [Global Power Plant Database CSV](https://raw.githubusercontent.com/wri/global-power-plant-database/master/output_database/global_power_plant_database.csv)  
> **Dashboard:** Available in the Excel workbook under the `Dashboard` sheet.

---

## Business Questions

This project explores questions relevant to the global energy sector:

1. Which countries have the highest installed electricity-generation capacity?
2. What is the total installed capacity represented in the dataset?
3. Which primary fuel types are most commonly used across power plants?
4. How does installed capacity vary across different fuel categories?
5. What do historical electricity-generation trends look like?
6. Which columns contain the highest proportion of missing values?
7. Are plant identifiers unique, and which plant names appear more than once?
8. What data-quality issues should be considered before interpreting the results?

---

## Dashboard and Analysis

The dashboard brings together the major findings from the data-cleaning and analysis process.

| **Component** | **What it shows** | **Based on** |
|---|---|---|
| **KPI Overview** | Total plants, installed capacity, countries represented, fuel categories and repeated-name records | `quality_summary` |
| **Country Analysis** | Leading countries by installed electricity-generation capacity | `analysis_tables` |
| **Fuel Distribution** | Plant distribution across primary fuel categories | `analysis_tables` |
| **Generation Trends** | Historical reported electricity generation from 2013–2019 | `analysis_tables` |
| **Data Quality Snapshot** | Key missing-value and duplicate-name metrics | `quality_summary`, `missing_values` |

The dashboard is included in the workbook and is supported by separate analysis and data-quality sheets.

---

## Key Findings

- **Dataset coverage:** 34,936 power plant records across 167 countries, containing 36 original data fields.
- **Installed capacity:** Approximately **5,706,975.4 MW** across the records in the dataset.
- **Plant identifiers:** No duplicate plant IDs were detected.
- **Repeated plant names:** 770 records belong to repeated-name groups, covering 362 distinct plant names.
- **Fuel categories:** The dataset represents 15 primary fuel categories.

An important observation from the data-quality assessment was that repeated plant names do not necessarily indicate duplicate facilities. Different power plants can share the same name, so these records were flagged for review rather than automatically removed.

---

## Data Cleaning and Quality Assessment

The project includes a structured data-quality workflow covering:

- Missing-value analysis across all 36 original fields.
- Missing plant names and plant identifiers.
- Numeric capacity validation.
- Duplicate plant ID checks.
- Repeated plant-name identification.
- Installed capacity summary statistics.
- Country and primary-fuel category coverage.

**Data handling decisions:**

- The original `raw_data` sheet is preserved without modifying the source records.
- The `working_data` sheet contains additional data-quality flags while retaining the original fields.
- Repeated plant names are treated as review candidates, not confirmed duplicates.
- Missing generation values are not interpreted as zero.
- Missing secondary-fuel fields are not automatically imputed.
- The dataset represents a historical snapshot and should not be treated as a live inventory of currently operating power plants.

---

## Dataset

The project uses the **Global Power Plant Database**, published by the World Resources Institute (WRI).

The dataset contains plant-level information including country, plant name, unique identifier, installed capacity, geographic coordinates, primary and secondary fuel types, commissioning year, ownership, and historical reported or estimated electricity generation.

| **Dataset Detail** | **Value** |
|---|---:|
| Total plant records | 34,936 |
| Countries represented | 167 |
| Original data fields | 36 |
| Total installed capacity | 5,706,975.4 MW |
| Duplicate plant IDs detected | 0 |
| Records with repeated plant names | 770 |
| Distinct repeated plant names | 362 |
| Primary fuel categories | 15 |

**Data Source:** [World Resources Institute — Global Power Plant Database](https://github.com/wri/global-power-plant-database)

---

## Repository Structure

```text
Global-Power-Plant-Analysis/
│
├── README.md
├── .gitignore
├── LICENSE
│
├── docs/
│   └── DATA_SOURCE.md
│
└── workbook/
    └── Global_Power_Plant_Data_Cleaning_Analysis_Dashboard_Fixed.xlsx
```

### Workbook Structure

| **Sheet** | **Purpose** |
|---|---|
| `Read_Me` | Project overview, scope, and workflow |
| `raw_data` | Original source dataset |
| `working_data` | Analysis dataset with additional quality flags |
| `quality_summary` | Dataset-level quality metrics and capacity statistics |
| `missing_values` | Missing-value counts and percentages for each original field |
| `duplicate_check` | Records belonging to repeated plant-name groups |
| `analysis_tables` | Country, fuel, and historical generation summaries |
| `Dashboard` | KPI cards and analytical charts |
| `Formula_Guide` | Spreadsheet formulas with explanations and examples |

---

## How to Reproduce

1. Download the dataset from the [WRI Global Power Plant Database repository](https://github.com/wri/global-power-plant-database).
2. Open the workbook using ONLYOFFICE Desktop Editors or Microsoft Excel.
3. Start with the `Read_Me` sheet to understand the project scope.
4. Review `quality_summary` and `missing_values` to understand the data-quality checks.
5. Inspect `duplicate_check` to review records with repeated plant names.
6. Explore `analysis_tables` for country-level capacity, fuel distribution, and generation summaries.
7. Open the `Dashboard` sheet to explore the visual analysis.
8. Refer to `Formula_Guide` to understand the spreadsheet functions used throughout the project.

The workbook includes precomputed row-level quality flags and summary results to avoid slow, repeated full-column calculations in spreadsheet software.

---

## Skills Demonstrated

- Data cleaning and data-quality assessment.
- Missing-value analysis and data validation.
- Duplicate identifier and repeated-name checks.
- Spreadsheet functions such as `COUNTA`, `COUNTBLANK`, `COUNT`, `SUM`, `AVERAGE`, `MAX`, `MIN`, `COUNTIF`, `SUMIF`, and `IF`.
- Data aggregation and summary-table construction.
- Country-wise installed capacity analysis.
- Fuel distribution and capacity analysis.
- Historical electricity-generation trend analysis.
- KPI development and dashboard design.
- Data interpretation and communicating analytical limitations.

---

## Limitations

- The analysis is based on a historical dataset snapshot and does not represent a live power plant inventory.
- Repeated plant names do not automatically indicate duplicate physical facilities.
- Missing values have different meanings depending on the field and should not be indiscriminately imputed.
- Reported and estimated generation values are separate measures and should be interpreted independently.
- Country-level capacity totals depend on the coverage and records available in the source dataset.

---

## About

**Ajith B**  
Computer Science (Data Science) Graduate

[LinkedIn](https://www.linkedin.com/in/ajith-b-7549b2376) · [GitHub](https://github.com/zeusnub)

*Dataset credit: World Resources Institute (WRI). Please refer to the original repository for dataset documentation, methodology, and licensing information before reuse.*
