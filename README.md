# Mean Variance Portfolio Optimisation

## Overview

This project demonstrates a practical implementation of Mean Variance Optimisation (MVO) used in investment portfolio construction, and its variants which address the pitfalls of MVO, including:

1. Resampled MVO
2. Reverse Optimisation
3. The Black-Litterman Model 

Each of these algorithms is covered in the CFA Level III curriculum.

For each approach, theory is reviewed before the models are hard coded.

Packages including `scipy.optimize`, `PyPortfolioOpt` and `CVXPY` are available to execute these algorithms directly, but this project demonstrates the “nuts and bolts” of how the algorithms operate by hard coding them.

In particular, a niche approach is used for classic MVO using n-dimensional spherical polars.

## CSV Files Included

The project imports `stock_prices.csv` for use in all algorithms and `ACWI_prices.csv` for reverse optimisation and the BL model only.

`stock_prices.csv` consists of weekly market-on-close price data over a 10 year period for the tickers GOOGL, TGT, NKE, V and GM.

`ACWI_prices.csv` consists of weekly market-on-close price data over the same period for the iShares MSCI ACWI ETF.

## Choosing Your Own Stocks

Should you wish to explore the code using your own choice of stocks: 

1. Download `MVO.env.example`
2. Rename the file to `MVO.env`
3. Insert your API keys for Alpha Vantage or FMP into the file
4. Use the `AV_data()` or `FMP_data()` functions provided in the first couple code blocks to retrieve the relevant price series

If you choose to do this, you may also need to change the (-) sign to a (+) in front of the lambda functions within the MVO functions to get the algorithms to descent to the correct stationary points.

## Thanks For Reading

I hope you find the project useful and informative.

