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
