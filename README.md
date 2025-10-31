# Impact of EuroLeague Team Statistics on Season Standings  

## Overview  

This project aims to analyze how team-level statistics influence the final standings in the EuroLeague.  
Rather than focusing on single match outcomes, the study explores which aspects of a team’s overall performance — such as shooting accuracy, assists, rebounds, or turnovers — are most correlated with success throughout the season.  
By using EuroLeague team statistics from multiple seasons (2020 to 2025), the project identifies the most impactful factors that determine the difference between well-performing and lower-performing teams.  

## Motivation  

As a basketball fan, I wanted to explore the question: “What makes a team successful?”  
The EuroLeague provides plenty of structured data to investigate this question.  
My goal is to determine the most relevant statistical aspects that influence a team’s overall position in the standings.  

## Data  

The dataset is provided from the official EuroLeague website, specifically the “Teams Statistics” and “Final Standings” sections of the seasons from 2020–2021 to 2024–2025, including around 18 teams per season.  
The main statistics include field goal, three-point, and free-throw percentages; rebounds, assists, steals, blocks, turnovers, performance index rating, basic season information such as games played, wins and losses, final standing positions, and some combined metrics derived from these values.  

## Methodology  

1. **Data Collection:**  
   Team statistics were collected for several consecutive EuroLeague seasons using `pandas.read_html()` from the official EuroLeague website.  
   Each season’s data table was merged into a single dataset with a new column, `Season`, for temporal reference.  

2. **Data Cleaning and Feature Engineering:**  
   - Standardized column names: FG% (Field Goal Percentage), 3P% (Three-Point Percentage), FT% (Free Throw Percentage), REB (Rebounds), AST (Assists), STL (Steals), BLK (Blocks), TOV (Turnovers), PIR (Performance Index Rating).  
   - Calculated derived metrics such as AST/TOV ratio and Team Efficiency Index (PIR per game).  
   - Added Win% = W / (W + L) as the target variable.  

3. **Exploratory Data Analysis (EDA):**  
   - Computed **Spearman correlation** between each metric and final standings.  
   - Visualized patterns using heatmaps and scatter plots.  

4. **Modeling:**  
   - Applied Multiple Linear Regression and Random Forest Regressor models to evaluate feature impact.  
  
5. **Evaluation and Comparison:**  
   - Compared models to ensure consistent patterns across seasons.  
   - Highlighted features with strong positive or negative correlations with ranking success.
  




