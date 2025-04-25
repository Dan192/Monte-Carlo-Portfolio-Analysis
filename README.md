# Monte Carlo Portfolio Analysis

This project uses a Monte Carlo simulation to model possible short-term (5-day) portfolio outcomes based on 15 years of historical data for SPY, BND, GLD, QQQ, and VTI (sample portfolio used).

The simulation runs 10,000 trials to estimate potential gains and losses, helping visualize the risk and return distribution over a short time horizon.

## Key Features

- Historical data retrieval using `yfinance`
- 10,000 Monte Carlo simulation trials
- 5-day hypothetical "what-if" scenario analysis
- Value at Risk (VaR) calculation and visualization
- (Key Assumptions made) $1,000,000 portfolio, consisting of equally weighted securities

## Significance

This analysis highlights short-term volatility risks for diversified portfolios and can be built out to handle larger portfolios.  
Helps investors visualize possible "worst-case" scenarios in order to hedge risk.

## How to Run

1. Clone the repository.
2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt

## Important Notes

The yfinance library has been updated and thus may not be able to download large volumes of ticker information,
in my current code: 'auto_adjust = False' is an essential parameter inside Cell 7. Should someone fork this project in the future,
please be aware that yfinance may be unable to download thousands of tickers at once, you may need to adjust the code to split
your ticker request into multiple ticker requests consisting of ~500 tickers per.

