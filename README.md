# Crypto Analysis

## Overview
This project provides a comprehensive analysis of the cryptocurrency market, focusing on key metrics such as price changes, market capitalization, and momentum scoring to evaluate growth trends in the crypto space.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction
The Crypto Analysis project is designed to make cryptocurrency data more accessible and understandable. It leverages live market data to generate insights into market movements, growth patterns, and comparative performance of various cryptocurrencies. The project supports informed decision-making through visual dashboards and analytical tools.

## Dataset
- **Source**: Live data fetched from the CoinGecko API
- **Key Metrics**: Current prices, market capitalization, 24-hour and 7-day price changes, volume, and more
- **Scope**: Top 100 cryptocurrencies by market capitalization (USD)

## Tech Stack
- **Data Visualization**: Power BI Desktop
- **API**: CoinGecko API (no authentication required)
- **Data Processing**: Manual cleaning and DAX formulas in Power BI

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/crypto-analysis.git
   ```
2. Ensure Power BI Desktop is installed on your system.
3. No additional dependencies are required beyond Power BI.

## Usage
1. Open the Power BI report files located in the `Reports/` directory.
2. Refresh data connections to fetch the latest cryptocurrency data from the API.
3. Interact with the dashboards to explore metrics, forecasts, and insights.
4. Use the built-in calculator for portfolio value estimation.

## Features
- **Momentum Analysis**: Calculates growth momentum with scoring and rating systems
- **Price Forecasting**: Provides 7-day price forecasts based on current trends
- **Risk Assessment**: Analyzes maximum, minimum, and average values for risk evaluation
- **Portfolio Calculator**: Estimates total investment value based on selected assets
- **Comparative Insights**: Compares performance across cryptocurrencies
- **Trend Identification**: Visualizes price fluctuations and market trends over time

## Results
The project delivers actionable insights through Power BI dashboards, including:
- Market movement visualizations
- Growth pattern identification
- High-performing cryptocurrency rankings
- Overall crypto market trend analysis
- Risk analysis with range calculations
- Forecasted returns and actual performance comparisons

## Project Structure
```
crypto-analysis/
├── raw_data/          # Raw API endpoints and data sources
├── clean_data/        # Processed datasets and DAX formula documentation
├── Reports/           # Power BI report files and dashboards
├── Result/            # Final analysis outputs and screenshots
├── .github/           # GitHub-specific files (e.g., instructions)
├── LICENSE            # Project license
└── README.md          # This file
```

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is licensed under the terms specified in the [LICENSE](LICENSE) file.

## Contact
For questions or suggestions, please open an issue on GitHub or contact [nikitagautam647@gmail.com].