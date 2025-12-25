# AlphaDecay_Analysis
Do well-known equity factors (momentum, low volatility, value) exhibit performance decay as they become crowded, and can crowding indicators predict future underperformance?
Factor Crowding & Alpha Decay Analysis
Overview

This repository contains a quantitative research project analyzing factor crowding and performance decay in equity markets. The objective is to study whether widely used equity factors—such as momentum and low volatility—exhibit deteriorating risk-adjusted returns during periods of increased crowding, and whether crowding indicators can help explain or predict such decay.

The project is designed to mirror a buy-side research workflow, starting from raw market data and ending with statistically validated insights and visual diagnostics.

Research Motivation

Equity factor strategies are well-documented in academic literature and widely implemented by asset managers. However, as these strategies become popular, they may suffer from:
Increased correlation among constituents
Elevated turnover and transaction costs
Valuation stretches
Reduced future returns
This project focuses not only on whether factors work, but when and why they stop working.

Research Questions

Do common equity factors exhibit performance decay over time?
Can crowding indicators explain periods of underperformance?
Is there a statistically significant relationship between crowding and future factor returns?
Can factor exposure be improved by conditioning on crowding regimes?

Data

Equity price and volume data (daily frequency)
Market capitalization data
Risk-free rate (for risk-adjusted metrics)
The analysis can be applied to:
US equities (e.g., S&P 500 universe), or
Indian equities (e.g., NIFTY 500 universe)
(Exact universe and sources are documented within the notebooks.)

Factor Construction

The following factors are constructed using standard cross-sectional methodologies:
Momentum: 12–1 month returns, monthly rebalancing
Low Volatility: Rolling historical volatility
(Optional extensions include value or quality factors)

Stocks are ranked cross-sectionally and grouped into long–short portfolios using decile-based selection.

Crowding Metrics

Crowding is proxied using a combination of quantitative indicators, including:
Factor portfolio turnover
Cross-sectional return correlations
Valuation dispersion and relative premiums
Volume-based activity measures (where applicable)
These indicators are analyzed individually and as a composite crowding signal.

Methodology

Rolling-window performance analysis (returns, Sharpe, drawdowns)
Regime-based comparison (high vs low crowding)
Regression of future factor returns on current crowding metrics
Statistical validation using robust estimators and resampling techniques
Transaction costs and realistic rebalancing assumptions are incorporated to avoid over-optimistic results.

Results & Insights

Key outputs include:
Evidence of factor performance deterioration during crowded regimes
Visual diagnostics linking crowding measures to future returns
Comparative analysis of static vs crowding-aware factor exposure
Detailed results and charts are available in the /results directory.

Repository Structure
├── data/          # Raw and processed datasets
├── notebooks/     # Exploratory analysis and research notebooks
├── src/           # Modular Python code (signals, metrics, backtests)
├── results/       # Charts, tables, and summary outputs
├── README.md

Tools & Libraries

Python
NumPy, Pandas
statsmodels
scikit-learn
matplotlib

Limitations

Results are sensitive to universe selection and data quality
Crowding is proxied indirectly and cannot be observed perfectly
This research is exploratory and not intended as a production trading system

Disclaimer

This repository is intended solely for educational and research demonstration purposes.
It does not constitute investment advice or a recommendation to trade any securities.
