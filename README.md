# INFO 2950 Project: U.S. Airfare Trends (1993-2024)

This project analyzes how domestic U.S. airline fares changed from 1993 to 2024, with a focus on:
- how passenger volume relates to price,
- how route distance affects fare,
- how fare trends change after adjusting for inflation.

The analysis is implemented in Jupyter notebooks and uses a cleaned dataset produced from raw flight-route and CPI sources.

## Repository Contents

- `project.ipynb`: Main analysis notebook (EDA, modeling, conclusions).
- `dataCleaning.ipynb`: Data cleaning and CPI inflation-adjustment workflow.
- `flights.csv`: Final cleaned dataset used in `project.ipynb`.
- `US Airline Flight Routes and Fares 1993-2024.csv`: Raw flight data source.
- `CPI_data - Sheet1 .csv`: Raw CPI/inflation source.
- `Phase 1.pdf`: Project proposal / phase deliverable.

## Data Schema (`flights.csv`)

- `Year`: Calendar year of observation.
- `quarter`: Quarter of observation (1-4).
- `nsmiles`: Route distance in miles.
- `passengers`: Passenger count for the route-quarter.
- `fare`: Nominal average fare (USD).
- `fare_with_inflation`: Fare converted to 2024 dollars using CPI.

## Main Questions

1. How have U.S. domestic airline fares evolved over time (1993-2024)?
2. Does higher passenger volume correspond to lower airfare?
3. How does fare change with route distance?

## Key Findings (from `project.ipynb`)

- Higher passenger volume is associated with lower average fares.
- Longer route distance is associated with higher fares.
- Inflation-adjusted airfare shows a decreasing long-run trend over the study window.

## Reproducibility

### 1. Environment

Use Python 3.10+ and install:
- `pandas`
- `numpy`
- `scikit-learn`
- `statsmodels`
- `seaborn`
- `matplotlib`
- `scipy`

Example:

```bash
pip install pandas numpy scikit-learn statsmodels seaborn matplotlib scipy notebook
```

### 2. Run the notebooks

```bash
jupyter notebook
```

Recommended order:
1. Run `dataCleaning.ipynb` to regenerate `flights.csv` from raw files.
2. Run `project.ipynb` to reproduce plots, regressions, and conclusions.

## Notes and Limitations

- The analysis is limited to domestic U.S. flights.
- Coverage is 1993-2024 and may miss earlier market structure shifts.
- Smaller regional airports are underrepresented in the source data.

## Authors

- Anderson Ramirez (`ar2527@cornell.edu`)
- Cian Llerena (`cl2632@cornell.edu`)
- Sophia Escalante (`sae85@cornell.edu`)
- William Biloski (`wb292@cornell.edu`)
