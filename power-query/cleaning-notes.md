# Power Query Cleaning and Validation

This folder documents the Power Query stage of the Great Britain Electricity Demand Analysis project.

## Purpose

Power Query was used to:

- Import and combine annual electricity datasets from 2018–2025.
- Standardise the yearly files into one master dataset.
- Check data types and structure.
- Investigate missing and unusual values.
- Validate yearly completeness.
- Check for duplicate half-hourly observations.
- Validate settlement-period behaviour.
- Prepare a clean dataset for exploratory analysis.

## Final Master Dataset

- Observations: 124,368
- Variables: 23
- Complete years: 2018–2024
- 2025: Partial year with 1,632 observations

## Key Quality Checks

### Duplicate Check
`SETTLEMENT_DATE + SETTLEMENT_PERIOD` was used as a composite key.

No duplicate half-hourly observations were identified.

### 2025 Completeness
2025 contained 1,632 observations representing 34 complete days from January to early February.

The data was retained but excluded from full-year comparisons.

### Structural Nulls
Missing values in variables introduced in later years were retained rather than automatically removed or replaced.

### Demand Quality
13 zero observations in `ENGLAND_WALES_DEMAND` were flagged because National Demand and Transmission System Demand remained positive during those observations.

### Settlement Periods
Days containing 46, 48 and 50 settlement periods were investigated.

The 46 and 50-period observations corresponded with UK daylight-saving transitions and were therefore retained as valid observations.

## Output

The cleaned master dataset was used to create a separate Power Query Reference called:

`Electricity Demand Analysis`

This became the analysis-ready dataset used for Excel exploratory analysis.
