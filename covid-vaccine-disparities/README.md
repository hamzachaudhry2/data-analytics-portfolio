# COVID-19 Vaccine Uptake — Geographic Disparity Analysis

## Problem
What structural factors explain global vaccination inequality, 
and can clustering alone recover geographic patterns without 
any geographic input?

## Data
- Source: Our World in Data COVID-19 dataset
- 163 countries
- Key variables: GDP per capita, HDI, vaccination rates, 
  healthcare infrastructure indicators

## Approach
- Built 3 OLS regression models with HC3 robust standard errors
- Applied K-Means clustering (k=4) with no geographic input
- Validated clustering output against actual continental geography
- Used Claude (Anthropic) to accelerate literature review by ~30%

## Results
- R² of 0.497 across OLS models
- GDP per capita and HDI identified as dominant predictors
- Clustering recovered continental geography with ~75% accuracy

## Key Finding
Vaccination disparities are structural, not logistical — 
poorer countries with lower HDI were systematically 
under-vaccinated regardless of supply availability.

## Files
- `analysis.R` — main analysis script
- `report.pdf` — full thesis write-up
