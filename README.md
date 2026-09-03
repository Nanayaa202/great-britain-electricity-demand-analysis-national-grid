# Great Britain Electricity Demand Analysis

## Project Overview

This project investigates how electricity demand in Great Britain changed between 2018 and 2024, with a focus on long-term trends, seasonality, within-day demand patterns, and embedded wind and solar generation.

The project originally includes electricity data covering 2018–2025. During data-quality analysis, 2025 was identified as a partial year and is therefore retained in the dataset but excluded from full-year comparisons.

## Main Research Question

**How has electricity demand in Great Britain changed since 2018, and how are these patterns associated with seasonality, weather and changes in embedded renewable generation?**

---

## Project Workflow

`Raw Data → Power Query → Excel EDA → SQL → Python → Power BI`

### Current Progress

- [x] Raw data review
- [x] Power Query cleaning
- [x] Data-quality validation
- [x] Analysis dataset preparation
- [x] Excel exploratory data analysis
- [ ] SQL analysis
- [ ] Python statistical analysis
- [ ] External weather analysis
- [ ] Power BI dashboard
- [ ] Final project write-up

---

## 1. Data Cleaning and Validation

Power Query was used to combine and prepare the annual electricity datasets.

The resulting master dataset contains:

- **124,368 observations**
- **23 variables**
- Complete annual data for **2018–2024**
- **1,632 observations for partial-year 2025**

Quality checks included:

- Duplicate checks using `SETTLEMENT_DATE + SETTLEMENT_PERIOD`
- Annual completeness checks
- Missing-value investigation
- Renewable generation vs capacity checks
- Settlement-period validation
- Source-year validation

No duplicate half-hourly observations were identified.

Structural nulls were retained where variables were introduced in later years rather than automatically treating them as data errors.

Thirteen unusual zero observations in `ENGLAND_WALES_DEMAND` were flagged for further investigation.

Settlement-period counts of 46, 48 and 50 were investigated and retained after being identified as valid UK daylight-saving behaviour.

---

## 2. Analysis Dataset Preparation

A separate `Electricity Demand Analysis` query was created as a **Power Query Reference** to the cleaned master dataset.

Additional analytical variables were created:

- Year
- Month Number
- Month Name
- Season
- Time of Day

This created an analysis-ready dataset while preserving the original cleaning workflow.

---

## 3. Excel Exploratory Data Analysis

Excel PivotTables and PivotCharts were used to explore annual, monthly, seasonal and half-hourly electricity-demand patterns.

### Findings So Far

#### Long-Term Demand

Average National Demand decreased from approximately:

**30,247 MW in 2018 → 26,287 MW in 2024**

This represents an overall decline of approximately **13.1%**.

The decline was not continuous. A pronounced fall occurred in 2020, followed by a partial recovery in 2021.

#### Seasonality

Winter consistently recorded the highest average National Demand, while summer recorded the lowest.

The winter-summer demand difference remained relatively stable despite the broader decline in electricity demand.

#### Within-Day Demand

Demand typically reached its lowest point around settlement periods **9–10**, approximately **04:00–05:00**.

Peak demand generally occurred around settlement periods **37–38**, approximately **18:00–19:00**.

Peak timing also varied by season.

#### Embedded Renewables

Between 2018 and 2024:

- Wind capacity increased by approximately **11.7%**
- Wind generation increased by approximately **15.7%**
- Solar capacity increased by approximately **36.6%**
- Solar generation increased by approximately **20.4%**

Installed capacity and actual generation did not move together consistently every year and are therefore treated as separate measures.

---

## Important Analytical Limitation

The analysis currently identifies **patterns and associations**, not causation.

For example, renewable capacity expanded during a period when National Demand declined. This does not demonstrate that renewable expansion caused the reduction in electricity demand.

External factors such as weather, economic activity, energy prices and behavioural changes require additional evidence before causal explanations can be made.

---

## 4. Current Stage: SQL

The next stage is to import the cleaned analysis dataset into SQL.

SQL will be used to:

- Query the complete dataset systematically
- Reproduce important Excel findings
- Filter and group specific periods
- Perform repeatable data-quality checks
- Investigate more focused analytical questions

### SQL Analysis Questions

1. How has National Electricity Demand changed between 2018 and 2024?
2. How does National Demand vary in relation to embedded wind and solar generation?
3. Which seasons record the highest and lowest embedded renewable generation relative to capacity?
4. Which settlement periods record the highest average National Demand, and has peak timing changed?
5. Is there a consistent monthly demand pattern between 2018 and 2024?
6. How does storage behaviour vary in relation to National Demand across settlement periods?

Statistical correlation analysis will be developed further during the Python stage.

---

## Next Steps

### SQL
Structured querying, aggregation and data validation.

### Python
Statistical and exploratory analysis, including relationships between National Demand and embedded renewable generation and capacity.

### External Data
Potential integration of weather data to investigate the relationship between temperature and electricity demand.

### Power BI
Development of an interactive dashboard to communicate the final findings.

---

## Tools

`Power Query` | `Excel` | `SQL` | `Python` | `Power BI`

---

## Project Status

**In Progress**
