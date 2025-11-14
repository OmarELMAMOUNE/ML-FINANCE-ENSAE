# Fed Rate Prediction Model 

## Project Overview

This project develops a predictive model for Federal Reserve interest rate movements (up or down) by analyzing the relationship between economic indicators, Federal Funds Futures (FFF) implicit rates, and historical Fed decisions.

## Background on Federal Funds Rate

### How the Fed Sets Rates

The Federal Open Market Committee (FOMC) sets the target federal funds rate based on:

- Economic growth indicators
- Inflation metrics
- Employment data
- Financial market conditions
- Global economic factors

The FOMC meets approximately eight times per year to review economic conditions and adjust monetary policy accordingly. The federal funds rate is the interest rate at which depository institutions lend reserve balances to other depository institutions overnight.

### EFFR (Effective Federal Funds Rate)

The **Effective Federal Funds Rate (EFFR)** is the volume-weighted median of overnight federal funds transactions reported by brokers and dealers. Key points:

- Published daily by the Federal Reserve Bank of New York
- Represents the actual rate at which banks are lending to each other
- Typically trades within the target range set by the FOMC
- Serves as a benchmark for many short-term interest rates

### Federal Funds Futures (FFF)

**Federal Funds Futures (FFF)** are financial contracts traded on the Chicago Mercantile Exchange (CME) that:

- Allow market participants to hedge or speculate on future FOMC rate decisions
- Are cash-settled to the average daily EFFR for the delivery month
- Have prices that reflect market expectations of future Fed policy
- Trade with monthly expirations extending


Data taken manually and merged from :

https://fred.stlouisfed.org/series/FEDFUNDS
https://www.cmegroup.com/markets/interest-rates/stirs/30-day-federal-fund.settlements.html
https://fred.stlouisfed.org/series/PCEPI
https://fred.stlouisfed.org/series/PAYEMS
https://fred.stlouisfed.org/series/GDP
https://fred.stlouisfed.org/series/INDPRO
https://fred.stlouisfed.org/series/CPIAUCSL
