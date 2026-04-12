# Between and Within: Income, Labour Markets, and Inter-State Migration in India

## Overview
This notebook replicates the empirical analysis from my Master's internal assessment paper submitted to the Department of Economics, University of Calcutta (2022). The analysis was implemented in Python in April 2026 as part of building a reproducible research portfolio.

## Research Question
Do the determinants of inter-state migration in India differ between states and within states over time?

## Data Sources
1. Migration: D-03: Migrants within the State/UT by place of last residence, duration of residence and reason of migration - 1991,2001,2011(https://censusindia.gov.in/census.website/data/census-tables-Migration)
2. Handbook of Statistics on Indian States-2021/2016(https://www.rbi.org.in/scripts/AnnualPublications.aspx?head=Handbook+of+Statistics+on+Indian+States)
* Table 1: State-wise Total Population
* Table 3: State-wise Population in Urban Area
* Table 8: State-wise Density of Population
* Table 21: Net State Domestic Product (Constant Prices)
* Table 156: State-wise Social Sector Expenditure
3. Labour Force Participation:B-01: Main workers, marginal workers, non-workers and those marginal workers, non-workers seeking/available for work classified by age and sex (all)- 1991,2001,2011(https://censusindia.gov.in/census.website/data/census-tables-Workers)

### Notes:
* Monetary variables are converted to consistent units.
* Population is converted to absolute numbers.
* Ratios are constructed to ensure comparability across states.

Note: Raw data files are not included in this repository due to size. 
All data sources are publicly available at the links above.

## Methodology
Two complementary panel estimators:
**Between-state estimator (BetweenOLS):** Identifies associations from persistent cross-state differences using state time-means
**Two-way Fixed Effects (PanelOLS):** Identifies associations from within-state changes over time, controlling for state and year fixed effects

## Key Findings
* Per capita income is the dominant cross-state predictor of migration (R² = 0.53), robust across six sequential specifications
* Within states over time, labour force participation and urbanisation are the significant correlates of migration
* The near-zero within-group R² indicates persistent cross-state differences dominate overall variation

## Requirements
pip install pandas numpy statsmodels linearmodels

## How to run
* You can utilise the 'Migration_Data' file provided in the data section or download the raw values from the sources listed above
* Run cells sequentially from top to bottom
