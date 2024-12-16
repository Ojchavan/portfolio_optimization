Portfolio Optimization Toolkit
Overview
This portfolio optimization toolkit provides a comprehensive set of functions for financial portfolio analysis and optimization. It includes methods for calculating rolling correlations, monthly returns, portfolio volatility, Sharpe ratio, and various portfolio optimization strategies.
Features

Rolling Correlation Calculation
Monthly Returns Conversion
Portfolio Volatility Estimation
Minimum Variance Portfolio Optimization
Constrained Portfolio Optimization
Sharpe Ratio Optimization
Rolling Sharpe Ratio Calculation

Requirements

Python 3.7+
NumPy
Pandas
SciPy

Installation
bashCopypip install numpy pandas scipy
Key Functions
1. Rolling Correlation
calculate_rolling_correlation(returns, stock1, stock2, window=252)

Calculates rolling correlation between two stocks
Default window is 252 trading days (1 year)

2. Monthly Returns
calculate_monthly_returns(returns)

Converts daily returns to monthly total returns

3. Portfolio Volatility
portfolio_volatility(weights, returns, periods_per_year)

Calculates portfolio volatility
Annualizes volatility based on trading periods

4. Minimum Variance Portfolio
optimize_minimum_variance_portfolio(returns, periods_per_year)

Finds portfolio weights that minimize overall portfolio volatility
Constrains weights between 0 and 1
Ensures total weight sums to 1

5. Constrained Portfolio
optimize_constrained_portfolio(returns, periods_per_year)

Optimizes portfolio with additional constraints
Allows weights between -1 and 2
Limits sum of long positions to 1.3

6. Sharpe Ratio Optimization
optimize_sharpe_ratio_portfolio(returns, periods_per_year, risk_free_rate=0)

Maximizes portfolio Sharpe Ratio
Constrains individual asset weights to 0-30%
Uses default zero risk-free rate

7. Rolling Sharpe Ratio
calculate_rolling_sharpe_ratio(returns, weights, window=252, min_periods=200)

Calculates rolling Sharpe Ratio for a portfolio
Provides dynamic performance assessment
