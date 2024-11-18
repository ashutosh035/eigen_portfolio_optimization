# Eigen Portfolios: Optimizing Portfolios using Principal Component Analysis

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://shields.io)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

## Project Description

Eigen Portfolios leverages **Principal Component Analysis (PCA)** to create optimized investment portfolios. The project addresses the limitations of traditional portfolio optimization methods, such as sensitivity to estimation errors, by constructing eigenportfolios that enhance risk-adjusted returns. Key features include dimensionality reduction, enhanced diversification, and a novel custom metric for risk-tolerant investors.

## Installation

### Prerequisites
- Python (>=3.8)
- Libraries: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`
- Financial data (e.g., S&P 500 stock price dataset)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/ashutosh035/eigen-portfolios.git
   ```
2. Navigate to the project directory:
   ```bash
   cd eigen-portfolios
   ```
3. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. **Data Preparation**: Preprocess the historical stock price data and compute daily asset returns.
   ```python
   from data_preparation import preprocess_data
   preprocess_data("sp500_data.csv")
   ```
2. **PCA Implementation**: Apply PCA to the normalized covariance matrix of asset returns.
   ```python
   from pca_analysis import perform_pca
   eigenvalues, eigenvectors = perform_pca(normalized_data)
   ```
3. **Portfolio Construction**: Construct eigenportfolios based on principal components.
   ```python
   from portfolio import construct_eigenportfolio
   portfolio_weights = construct_eigenportfolio(eigenvectors, variance_threshold=0.99)
   ```
4. **Performance Evaluation**: Analyze portfolio performance using Sharpe Ratio and other metrics.
   ```python
   from evaluation import evaluate_portfolio
   sharpe_ratio = evaluate_portfolio(portfolio_weights, test_data)
   ```

## Features

- **Dimensionality Reduction**: PCA reduces dataset complexity while retaining 99% variance.
- **Enhanced Risk-Adjusted Returns**: Optimized portfolios achieve Sharpe Ratios as high as **1.74**.
- **Sophisticated Asset Allocation**: Supports both long and short positions for better diversification.
- **Custom Metric**: Combines return and Sharpe Ratio to favor high-performing risk-tolerant portfolios.

## Contributing

We welcome contributions from the community! To contribute:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with detailed changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Screenshots and GIFs

### Sharpe Ratio vs Return
![Sharpe Ratio vs Return](sharpe_vs_return.jpeg)

### Portfolio Weights Distribution
![Portfolio Weights Distribution](portfolio_weights.jpeg)

## Documentation

Detailed documentation is available [here](EIGEN_Portfolio_Optimization_Report.pdf).

## Changelog

### Version 1.0.0
- Initial release with PCA-based portfolio optimization.
- Sharpe Ratio and custom metric implementation.
- Visualization of portfolio performance.

---

Thank you for exploring Eigen Portfolios! For queries, please contact [ashutoshanand3007@gmail.com].