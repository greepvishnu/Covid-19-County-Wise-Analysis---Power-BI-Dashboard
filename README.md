# Covid-19-County-Wise-Analysis---Power-BI-Dashboard
This project involves creating an interactive Power BI dashboard to analyze county-wise Covid-19 data. The dashboard provides insights into Covid cases across various counties, allowing users to explore the data using visual filters and interactive charts.

## Dashboard Link: https://opendata.maryland.gov/api/views/tm86-dujs/rows.csv?accessType=DOWNLOAD

## Problem Statement:

The goal of this project is to create an interactive Power BI dashboard using a Covid dataset, focusing on county-wise data. The objective is to demonstrate proficiency in data cleaning, modeling, and visualization. The final deliverable is a Power BI report (.PBIX) containing at least five distinct visualizations that offer insights into Covid cases.

## Project Scope:

# Data Understanding and Preparation:

Data Review: Understand the dataset's structure and contents.
Data Cleaning: Handle missing values, correct data types, and ensure the dataset is suitable for analysis.

# Data Modeling:

Import the cleaned dataset into Power BI.
Establish relationships between tables (if applicable).
Create calculated columns and measures using DAX functions to support the analysis.

# Dashboard Creation:

Build a Power BI dashboard with at least five distinct visualizations:
Visualizations include bar charts, line charts, pie charts, tables
Ensure clarity, usability, and adherence to best practices in data visualization.

# Best Practices & Interactivity:

Titles and Labels: Use descriptive titles and labels for all visualizations.
Interactivity: Implement slicers and filters to enhance user interaction.
Best Practices:
Avoid clutter and unnecessary elements.
Select appropriate chart types based on the data.
Maintain visual consistency in terms of color and formatting.

## Steps Followed:

# Loading the Dataset & Data Cleaning:

Step 1: Loaded the dataset (CSV file) into Power BI Desktop.

Step 2: Cleaned and preprocessed the data using Power Query Editor.

Step 3: Removed the OBJECTID column and converted the Date column to the correct data type.

Step 4: Unpivoted the columns and created new fields for County and Number of Cases, ensuring correct data types.

Step 5: Created calculated columns for Year and Month using DAX functions, adjusting data types accordingly.

# Dashboard Creation and Visualizations:

Step 6: Added visual filters (slicers) for "County" and "Year".

Step 7: Added two card visuals:
           One for Total Counties.
           One for Total Cases.

Step 8: Added two bar charts:
         A vertical bar chart showing the relationship between Year and Number of Cases.
         A horizontal bar chart showing the relationship between County and Number of Cases.

Step 9: Added a pie chart to visualize the percentage distribution of cases on a quarterly basis.

Step 10: Created a line chart to compare Month-wise number of cases.

Step 11: Created a detailed table report showing Year, Month, and Number of Cases.

#DAX Function for Year-over-Year Analysis:

To analyze the year-over-year change in Covid cases, the following DAX function was used:
        year over year change = var previous = calculate(sum('MD_COVID-19_-_Cases_by_County'[No of Cases]), 
                                all('MD_COVID-19_-_Cases_by_County'), 
                                PREVIOUSYEAR('MD_COVID-19_-_Cases_by_County'[Date]))
                     var curr = calculate(sum('MD_COVID-19_-_Cases_by_County'[No of Cases]))
                   var result = (curr - previous) / previous * 100
                   return result

# Root Cause Analysis (RCA):

Step 12: Created a second page in the report using Page Navigator with the title "RCA of Cases".

Step 13: Utilized a Decomposition Tree to conduct a root cause analysis of the Covid cases.
