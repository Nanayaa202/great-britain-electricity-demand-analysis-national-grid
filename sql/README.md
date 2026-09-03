# SQL Analysis

## Status

**In Progress**

The SQL stage builds on the exploratory analysis completed in Excel.

Excel was used to identify broad patterns and generate analytical questions. SQL will now be used to investigate those questions systematically across the full cleaned dataset.

## Purpose

SQL will be used to:

- Reproduce important Excel findings.
- Query the full dataset using structured filters and aggregations.
- Compare demand across years, months, seasons and settlement periods.
- Investigate renewable generation and capacity.
- Investigate storage behaviour.
- Repeat selected data-quality checks using SQL.
- Create reusable queries that can be reviewed and rerun.

## Planned Analysis Questions

### 1. National Demand Trend

How has National Electricity Demand changed between 2018 and 2024?

### 2. Demand and Embedded Renewables

How does National Demand vary in relation to embedded wind and solar generation between 2018 and 2024?

Statistical correlation will be investigated later in Python.

### 3. Renewable Generation vs Capacity

Which seasons recorded the highest and lowest embedded wind and solar generation relative to capacity between 2018 and 2024, and how did these patterns change over time?

### 4. Peak Demand

Which settlement periods recorded the highest average National Electricity Demand, and how did the timing and magnitude of peak demand change between 2018 and 2024?

### 5. Monthly Demand Patterns

Is there a consistent monthly pattern in National Electricity Demand between 2018 and 2024, and how has this pattern changed over time?

### 6. Storage Behaviour

How does storage behaviour vary in relation to National Electricity Demand across different settlement periods between 2018 and 2024?

## Planned SQL Data Quality Checks

SQL will also be used to check:

- Row counts by year.
- Missing values in key variables.
- Duplicate `SETTLEMENT_DATE + SETTLEMENT_PERIOD` observations.
- Suspicious zero demand values.
- Settlement-period coverage.
- Data coverage for variables introduced in later years.

## Dataset Scope

The SQL database will contain the cleaned analysis dataset covering 2018–2025.

For full-year comparisons, analysis will primarily use:

**2018–2024**

The 2025 observations will remain available but will be treated as partial-year data.

## Files

As the SQL stage progresses, this folder will contain:

- `01_data_quality_checks.sql`
- `02_demand_trends.sql`
- `03_seasonal_analysis.sql`
- `04_peak_demand.sql`
- `05_renewable_analysis.sql`
- `06_storage_analysis.sql`

These files will be added progressively as the analysis is completed.
