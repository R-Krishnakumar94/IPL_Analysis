# IPL_Analysis
Tableau dashboard analyzing IPL matches (2008-2020)
# IPL Analysis Dashboard (2008-2020)

## Overview
This project demonstrates a comprehensive data analysis and visualization of the Indian Premier League (IPL) matches from 2008 to 2020, using Tableau. It highlights key aspects of the tournament, such as winning teams, standout player performances, and season trends. The primary goal of this project is to explore and communicate complex data effectively through interactive visualizations.
# Key Features of the Dashboard
 - IPL Winners by Year:
    - Visualized as a table or bar chart showing the teams that won each season
    - Provides an understanding of dominant teams over the year
-  Orange Cap Winners: Displays the leading run-scorers of each season.
-  Purple Cap Winners: Highlights the leading wicket-takers each season.

Visualized as a table or bar chart showing the teams that won each season.
Provides an understanding of dominant teams over the years.

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
