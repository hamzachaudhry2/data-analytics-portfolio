# Canadian Household Debt & Interest Rate Analysis
## Problem
How has Canadian household debt evolved since 1990, and has the composition 
of that debt shifted in ways the headline debt-to-income number doesn't 
capture on its own?

## Data
- Sources: Statistics Canada Table 38-10-0238-01 (National Balance Sheet 
  Accounts), Bank of Canada Valet API (policy interest rate, series V39079)
- 145 quarters (1990-2026) for debt data; 2009-2026 for policy rate data
- Key variables: consumer credit, mortgages, non-mortgage loans, 
  debt-to-income ratio, Bank of Canada target overnight rate

## Approach
- Built a star-schema data model in Power BI linking two independent public 
  datasets through a shared date dimension table
- Designed a 4-page report: Overview (KPIs + trend), Debt Composition 
  (100% stacked share-of-total view), Rate Impact (dual-axis overlay), and 
  a Methodology page documenting sources and scope limitations
- Used DAX measures to correctly convert raw units (millions to billions) 
  and isolate specific category values from a shared long-format value column

## Results
- Household debt-to-income ratio: 179.55% as of the latest quarter, up from 
  ~85% in 1990
- Mortgages' share of total household debt rose from 66.4% to 74.6% since 1990, 
  while consumer credit's share fell from 25.4% to 20.7%, even as its dollar 
  value kept growing
- Debt-to-income ratio kept climbing through the 2022-2023 rate-hike cycle 
  before easing only recently, despite the policy rate nearly quintupling

## Key Finding
Rising Canadian household debt isn't just a story of "more borrowing" — the 
composition has shifted meaningfully toward mortgage debt over three decades, 
and rate increases haven't produced the immediate debt slowdown a simple 
supply-and-demand view of borrowing costs would predict.

## Files
- `Canadian_Consumer_Credit_Dashboard.pbix` — full Power BI report (4 pages)
- Screenshots of each page for quick viewing without Power BI installed
