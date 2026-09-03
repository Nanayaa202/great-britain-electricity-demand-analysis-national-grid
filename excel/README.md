# Excel Exploratory Data Analysis

## Purpose

After cleaning and validating the dataset in Power Query, Excel was used for exploratory data analysis (EDA).

The purpose of this stage was to understand the main patterns in Great Britain's electricity demand before moving into more focused SQL and Python analysis.

## Analysis Completed

### 1. Annual National Demand

Average National Demand was compared between 2018 and 2024.

Average demand decreased from approximately:

**30,247 MW in 2018 → 26,287 MW in 2024**

This represents an overall decline of approximately **13.1%**.

The decline was not continuous. A pronounced fall occurred in 2020, followed by a partial recovery in 2021.

---

### 2. Monthly Demand Patterns

Monthly averages were compared across years to investigate whether the annual decline was concentrated in particular periods.

The 2020 decline was particularly pronounced during April and May.

Further comparison showed that by 2024, all 12 months recorded lower average National Demand than their corresponding months in 2019.

Average annual demand in 2024 was approximately **10.5% below 2019**.

---

### 3. Seasonal Demand

Average National Demand was compared across:

- Winter
- Spring
- Summer
- Autumn

Winter consistently recorded the highest average demand, while summer recorded the lowest.

Despite the broader decline in electricity demand, the winter-summer demand gap decreased by only approximately **3.3% between 2018 and 2024**.

---

### 4. Settlement Period Analysis

Half-hourly settlement periods were analysed to identify typical daily peaks and troughs.

Typical demand trough:

**Settlement periods 9–10 ≈ 04:00–05:00**

Typical demand peak:

**Settlement periods 37–38 ≈ 18:00–19:00**

The timing of the daily cycle remained relatively stable across 2018–2024.

Seasonal analysis also showed that peak timing shifted from approximately:

**Period 36 in Winter → Period 39 in Summer**

---

### 5. Embedded Renewable Trends

Embedded wind and solar capacity and generation were compared between 2018 and 2024.

| Measure | Change 2018–2024 |
|---|---:|
| Wind Capacity | +11.7% |
| Wind Generation | +15.7% |
| Solar Capacity | +36.6% |
| Solar Generation | +20.4% |
| Average National Demand | -13.1% |

Capacity and actual generation did not move together consistently every year.

This means installed renewable capacity and actual renewable generation are treated as separate measures in the analysis.

---

## Key Analytical Lesson

The Excel analysis identifies patterns but does not establish their causes.

For example, renewable capacity increased while National Demand declined over the same period. This does not demonstrate that renewable growth caused the decline in electricity demand.

The findings from Excel are being used to develop more focused questions for the SQL and Python stages.
