# IPL_Analysis
Tableau dashboard analyzing IPL matches (2008-2020)
# IPL Analysis Dashboard (2008-2020)

## Overview
This Tableau dashboard visualizes key metrics from IPL matches (2008-2020):
- IPL Winners by Year
- Orange Cap Winners
- Purple Cap Winners
- Number of 4's per season
- Number of 6's per season
- Matches won as per the toss
- % of winning by toss

## Files
- `IPL_Analysis_Dashboard.twbx`: Tableau dashboard file
- `data/`: Folder containing datasets
- `screenshot/`: Folder containing dashboard screenshot

## Dashboard Preview
![Dashboard Screenshot](screenshot/dashboard.png)

## Tableau Functions Used
- **Calculated Fields**:
  - **Total Fours per Season**: `SUM(IF [RunsScored] = 4 THEN 1 ELSE 0 END)`
  - **Total Sixes per Season**: `SUM(IF [RunsScored] = 6 THEN 1 ELSE 0 END)`
  - **Matches Won After Toss**: `IF [Toss Winner] = [Match Winner] THEN 1 ELSE 0 END`
  - **Winning % After Toss**: `SUM([Matches Won After Toss]) / COUNT([Match ID]) * 100`
- **Filters**:
  - Filtered by `Year`, `Team`, and `Venue`.
- **Visualization Types**:
  - Bar charts .
  - Donut chart for toss analysis.
