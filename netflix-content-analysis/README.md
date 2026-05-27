# Netflix Content Trend Analysis

## Problem
How has Netflix's content strategy evolved over time, and what 
patterns exist in genre, country of origin, and content type?

## Data
- Source: Kaggle Netflix Shows Dataset
- 8,807 titles (movies and TV shows)
- Key variables: content type, release year, country, genre, 
  duration, date added

## Approach
- Cleaned and preprocessed data in R (handled missing values 
  in country, date_added, and genre columns)
- Built univariate and multivariate visualizations using ggplot2
- Analyzed trends across content type, genre, country, 
  and movie duration

## Results
- Content additions peaked in 2019 after rapid growth from 2016
- Movies comprise 67% of the entire catalog
- US, India, and UK are the top 3 contributing countries
- Most movies fall in the 90–100 minute range
- Documentaries and international dramas dominate genre listings

## Key Finding
Netflix's growth strategy prioritized volume and international 
diversity — scaling content rapidly while maintaining familiar 
formats like feature-length films to retain global audiences.

## Files
- `netflixanalysis.Rmd` — full R Markdown analysis
- `netflixanalysis_report.pdf` — full project write-up with visualizations
