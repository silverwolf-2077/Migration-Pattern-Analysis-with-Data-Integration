# Migration Pattern Analysis and GenAI-Enhanced Dashboard

## Project Overview
This project analyzes U.S. county-to-county migration patterns and presents the results through an interactive dashboard. It combines migration flow data with socioeconomic and demographic indicators to better explain why migration patterns differ across counties. In addition to descriptive analysis, the project also incorporates natural language processing (NLP) on local news articles and a GenAI-powered dashboard feature that automatically generates concise narrative insights from user selections.

## Task Coverage
This project was developed to complete both **Task 2: Migration Pattern Analysis with Data Integration** and **Task 3: GenAI-Enhanced Interactive Dashboard**.

For Task 2, the project identifies the county pairs with the strongest migration interactions, determines the counties with the highest in-migration and out-migration, calculates net migration for the New York metropolitan area, enriches the migration dataset with contextual variables, and analyzes migration-related themes from local news coverage.

For Task 3, the project extends these results into a public interactive dashboard that allows users to explore migration patterns visually and interactively, while also including a GenAI-powered insight generation feature.

## Main Components

### 1. Migration Flow Analysis
The project examines county-level migration flows to identify the most connected county pairs by number of exemptions, as well as counties with the highest inbound and outbound migration volumes.

### 2. New York Metropolitan Area Net Migration
A focused regional analysis was conducted for the New York metropolitan area to calculate net migration and better understand whether the region experienced overall gains or losses in migration.

### 3. Data Enrichment
To provide explanatory context for migration patterns, the original dataset was augmented with additional public variables, including economic, housing, and demographic indicators such as median household income, unemployment rate, rent, population size, age structure, and rural-urban classification.

### 4. NLP Analysis of Local News
Relevant news articles from top migration counties were collected and analyzed using NLP methods to identify recurring themes related to migration. Common topics included housing affordability, employment opportunities, family considerations, and broader demographic change.

### 5. GenAI-Enhanced Dashboard
An interactive dashboard was built using R Shiny and Plotly to present the key findings. Users can explore county-level migration patterns, inspect major county interactions, compare contextual features across counties, and generate AI-written summaries based on the current dashboard view.

## GenAI Feature
The dashboard includes an automated insight generation component that converts structured dashboard outputs into short natural-language interpretations. Rather than producing new analysis independently, the model summarizes the currently displayed migration and county comparison results in a more accessible narrative form.

## Tools and Methods
- **R** for data cleaning, analysis, and modeling  
- **Shiny / flexdashboard / Plotly** for interactive dashboard development  
- **Public socioeconomic and demographic data sources** for enrichment  
- **NLP techniques** for text cleaning, tokenization, and theme extraction from news articles  
- **GenAI API integration** for automated insight generation  

## Project Outcome
This project demonstrates how migration data can be combined with contextual indicators, text analysis, and generative AI to produce a more interpretable and interactive analytical tool. It moves beyond static reporting by allowing users to explore migration patterns dynamically and receive concise AI-assisted summaries of the results.

## Live Dashboard
[Migration Dashboard](https://arwending.shinyapps.io/MigrationDashboard/)

## Data Sources

## Data Sources

- [U.S. Census Bureau: 2003 SAIPE State and County Estimates](https://www.census.gov/data/datasets/2003/demo/saipe/2003-state-and-county.html)
- [U.S. Bureau of Labor Statistics: Labor force data by county, 2003 annual averages](https://www.bls.gov/lau/tables.htm)
- [USDA Economic Research Service: 2003 Rural-Urban Continuum Codes](https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/documentation)
- [HUD USER: FY2003 50th Percentile Rents, Data by County](https://www.huduser.gov/portal/datasets/50per.html)
- [U.S. Census Bureau: Intercensal Estimates of the Resident Population by Five-Year Age Groups and Sex for Counties, 2000-2010](https://www.census.gov/data/datasets/time-series/demo/popest/intercensal-2000-2010-counties.html)
- Los Angeles Times. (2003, October 3). *[Escape From L.A.: It’s a Rainbow](https://www.latimes.com/archives/la-xpm-2003-oct-03-me-immigrate3-story.html)*.
- Los Angeles Business Journal. (2005, July 26). *[Population Growth in L.A. County Slows](https://labusinessjournal.com/news/population-growth-in-la-county-slows/)*.
- Brookings. (2003, November 1). *[Los Angeles in Focus: A Profile from Census 2000](https://www.brookings.edu/articles/los-angeles-in-focus-a-profile-from-census-2000/)*.
- Los Angeles Times. (2004, September 11). *[Clinging to Dream’s Frayed Edges](https://www.latimes.com/archives/la-xpm-2004-sep-11-me-exodus11-story.html)*.
- Los Angeles Times. (2004, May 24). *[In a Reverse Migration, Blacks Head to New South](https://www.latimes.com/archives/la-xpm-2004-may-24-me-migration24-story.html)*.
- Los Angeles Times. (2004, February 14). *[Southland’s Population Still on the Rise](https://www.latimes.com/archives/la-xpm-2004-feb-14-me-population14-story.html)*.
- Los Angeles Times. (2004, July 19). *[Will White Influx Put Down Roots in L.A. Core?](https://www.latimes.com/archives/la-xpm-2004-jul-19-oe-rodriguez19-story.html)*.
- Los Angeles Times. (2004, June 24). *[Inland Empire Makes It Big on U.S. Growth Chart](https://www.latimes.com/archives/la-xpm-2004-jun-24-me-cities24-story.html)*.
- Los Angeles Times. (2005, April 15). *[Inland Empire Is True to Its Name](https://www.latimes.com/archives/la-xpm-2005-apr-15-me-census15-story.html)*.
- Los Angeles Times. (2004, September 30). *[O.C. Whites a Majority No Longer](https://www.latimes.com/archives/la-xpm-2004-sep-30-me-census30-story.html)*.
