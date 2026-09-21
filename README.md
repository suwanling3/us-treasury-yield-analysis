# U.S. Treasury Yield Analysis
## Project Overview
This project analyzes daily U.S. Treasury yields across different maturities to examine changes in interest-rate levels, yield-curve shapes, yield spreads, daily volatility, and extreme market movements.

The project combines exploratory data analysis with financial-market interpretation. Rather than focusing on predictive modeling, the analysis aims to understand how Treasury yields behaved over time and how unusual movements can be investigated using financial and macroeconomic context.

**Project type:** Financial Data Analysis / Exploratory Data Analysis
**Period:** January 2015 – September 2026
**Tools:** Python, Pandas, Matplotlib, Seaborn

## Research Question

    3.1 How did Treasury yields evolve across different maturities overtime?
    3.2 How did the shape of the Treasury yield curve evolve during different interest-rate environments?
    3.3 What can the 10-year minus 2-year and 10-year minus 3-month spreads tell us about changes in the yield curve?
    3.4 Which maturities experienced relatively high daily yield volatility?
    3.5 What were the most extreme daily yield movements in the dataset, and what market events occurred around those dates?
    3.6 How can these findings be relevant to financial-market monitoring and operations?

## Dataset
The project uses daily U.S. Treasury par yield curve rates from the Federal Reserve Board’s H.15 Selected Interest Rates dataset.\
The dataset contains Treasury yields across multiple maturities, including:\
* 3-month
* 6-month
* 1-year
* 2-year
* 3-year
* 5-year
* 7-year
* 10-year
* 20-year
* 30-year\
The analysis focuses on observations from 2015-01-01 to 2026-09-15.\
The source data contain observations reported as ND for unavailable values.These observations are treated as missing values during data cleaning.

## Methodology
The project follows the workflow below:

### 1.Data Cleaning
* Converted dates into a datetime format
* Selected Treasury maturity columns
* Converted yield observations into numeric values
* Treated ND observations as missing values
* Removed incomplete observations where necessary
* Checked the resulting dataset for data-quality issues

### 2.Exploratory Data Analysis

The analysis examines:

* Overall Treasury yield trends
* Yield distributions
* Correlations between maturities
* Representative yield curves
* Yield-curve changes across different dates

### 3.Yield-Curve Analysis

The project compares yield curves across different market environments and examines:

* Normal yield curves
* Flattening
* Steepening
* Yield-curve inversion

Two commonly monitored spreads are also analyzed:

* 10-year minus 2-year Treasury yield
* 10-year minus 3-month Treasury yield

### 4.Volatility Analysis
Daily yield changes are calculated in basis points (bps) to examine the magnitude of day-to-day movements.\
Standard deviation is used as a descriptive measure of the dispersion of daily yield changes across maturities.

### 5.Extreme-Movement Analysis
The analysis identifies the largest positive and negative daily yield changes for each maturity.\
Selected extreme observations are then investigated in their surrounding trading-day context and compared with major market events.

## Key findings
    Treasury yields moved through several distinct rate regimes. Yields fell sharply in early 2020, remained historically low during the pandemic period, and rose substantially during the 2022 tightening cycle.
    The yield curve changed shape materially over time. The curve was relatively normal in 2019, sharply lower in 2020, inverted during the 2022–2024 period, and later returned to a positive slope in the longer maturities.
    Treasury maturities are strongly correlated. Most maturities tend to move together, but differences in their movements create changes in curve slope and shape.
    Intermediate maturities showed the highest daily volatility in this sample. The 7Y Treasury had the highest std of daily yield changes at approximately 5.55 bp.
    Extreme daily moves were related with different market environments. The largest positive and negative observations occurred around periods of major inflation/rate repricing, the COVID-19 market shock, and the 2023 banking-sector stress.

## Business Implications
    fixed-income trading / operations perspective
    Market monitoring: Tracking multiple maturities helps capture a broad market move from a maturity-specific movement.
    Exception monitoring: Large daily changes can be used as a simple trigger for reviewing unusual market movements, pricing inputs, or downstream records.
    Curve awareness: Monitoring spreads such as 10Y–2Y and 10Y–3M provides a compact way to identify changes in curve slope and inversion.
    Operational risk control: During high-volatility periods, larger market moves may increase the importance of timely data validation, trade confirmation, reconciliation, and exception handling.
    Further automation: Daily yield-change thresholds could be incorporated into a monitoring workflow to flag unusual movements for manual review.
   
The analysis is descriptive and should not be interpreted as a trading signal. In a production environment, additional market and transaction-level data would be needed before using these indicators for risk or investment decisions.

## Limitations & future work
    Limitations:
       * Treasury constant maturity yields are benchmark yields rather than individual bond transaction prices.
       * The analysis is descriptive rather than causal.
       * Macroeconomics variables such as inflation, Fed policy and economic growth are not explicitly modeled.
    Future work
        * Add inflation, Federal Funds Rate, and other macroeconomic indicators.
        * Compare Treasury yield movements with major economic announcements and FOMC decisions.
        * Extend the analysis from yields to bond-price sensitivity and duration.


## Technologies
Python | Pandas | Matplotlib | Seaborn | Jupyter Notebook

## Data Source
Federal Reserve Board, **H.15 Selected Interest Rates.**
The analysis uses publicly available Treasury yield data for educational and analytical purposes.

