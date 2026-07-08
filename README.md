# Operational Risk in Airlines

An analysis of historical weather-related flight delay data used to predict and mitigate future operational disruptions at major US airports (Chicago O'Hare, Los Angeles, and Orlando).

This was a **group project** completed as part of the MSc in Risk Analytics at Queen Mary University of London (Programme-Level Assessment, 2025). It was produced by five students working together. The repository is shared here as part of my portfolio, with my individual contribution set out below.

## Overview

The study estimates the expected number of weather-related flight delays per season and evaluates the operational risk this creates for airlines. The approach:

- Uses historical USDOT delay data for ORD, LAX, and MCO across four years (2014 to 2018).
- Applies the expectation formula to forecast expected delays from the previous year's delay proportion.
- Models delay counts with the binomial probability mass function (PMF) and builds 95% confidence intervals using the normal approximation.
- Classifies each season as low, medium, or high operational risk depending on where actual delays fall relative to the confidence interval.
- Adds a financial scenario analysis estimating the cost impact of delays on a case-study airline.

The work is structured around the ISO 31000 risk process: risk identification, analysis, evaluation, and monitoring.

## My contribution (Théo Poupel)

My work on the project fell into three areas:

- **Calculations.** With a teammate, I produced the weather-delay probability and binomial distribution calculations in Excel across the airports analysed: the weather-delay probabilities, the expected delays (mean = n x p), the standard deviation, the 95% confidence intervals, and the binomial probability mass function across percentiles. I also took part in selecting the statistical methods used.
- **Interpretation of the graphs.** I analysed and interpreted the binomial PMF graphs, reading the position, spread, and skew of each curve to explain the year-on-year variability and predictability of weather-related delays.
- **External research and risk evaluation.** I researched external weather records and news sources to identify the specific events, and their precise dates, behind each shift in the curves. I used this evidence to explain the results and to classify each season as low, medium, or high operational risk.

## Repository contents

- `Operational_Risk_in_Airlines_Report.pdf` - the full group report, including methodology, case studies, risk evaluation, limitations, and appendices.
- `PLA_workings.xlsx` - the Excel workbook containing the expectation and binomial PMF calculations.
- `APPENDIX_3_Python_Codes.ipynb` - Python code used to generate the graphs. This code was written by another member of the group.

## Known limitations

The analysis uses only the most recent year's delay proportion and a fixed confidence interval, which produces intervals that are narrower than the underlying variability warrants. A Bayesian hierarchical approach (modelling the delay probability as a Beta-distributed random variable and propagating the uncertainty) is proposed in the report as a more robust extension.

## Note

This is academic group work. Student ID numbers have been removed. Contributor names are included with the consent of the group.
