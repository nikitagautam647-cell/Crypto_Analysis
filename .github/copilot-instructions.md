# Crypto Analysis Project - AI Agent Instructions

## Project Overview
This is a cryptocurrency market analysis project that fetches live data from CoinGecko API, processes it for Power BI visualization, and generates dashboards for market insights including momentum scoring, price forecasts, and comparative performance analysis.

## Architecture & Data Flow
- **raw_data/**: Contains API endpoints and raw data sources (e.g., `api.txt` with CoinGecko markets endpoint)
- **clean_data/**: Processed datasets and DAX formula documentation (`desc.md`)
- **Reports/**: Power BI report files (.pbix), DAX measures, and dashboard definitions
- **Result/**: Final dashboard screenshots and analysis outputs

Data flows from CoinGecko API → raw_data → clean_data processing → Power BI Reports → Result dashboards.

## Key DAX Patterns & Conventions
Use SWITCH statements for categorical scoring and ratings. Examples from `clean_data/desc.md`:

```dax
Momentum Score =
VAR M = [Growth Momentum]
RETURN
SWITCH(
    TRUE(),
    ISBLANK(M), BLANK(),
    M >= 0.50, 100,
    M >= 0.20, 80,
    M >= 0.00, 60,
    M >= -0.20, 40,
    M >= -0.50, 20,
    10
)
```

```dax
Momentum Rating =
VAR M = [Growth Momentum]
RETURN
SWITCH(
    TRUE(),
    ISBLANK(M), "No Data",
    M >= 0.50, "Strong Uptrend",
    M >= 0.20, "Moderate Uptrend",
    M >= 0.00, "Sideways/Stable",
    M >= -0.20, "Weak Downtrend",
    "Strong Downtrend / Reversal Risk"
)
```

Follow this pattern for new scoring measures: define thresholds, use SWITCH(TRUE(), ...) for cascading conditions.

## API Integration
Primary data source: CoinGecko `/api/v3/coins/markets` endpoint with parameters:
- vs_currency=usd
- order=market_cap_desc
- per_page=100
- price_change_percentage=24h,7d

Document new API endpoints in `raw_data/api.txt` with full URLs.

## Development Workflow
1. Fetch/update raw data from APIs
2. Process/clean data in clean_data/
3. Load into Power BI and create measures using established DAX patterns
4. Build dashboards in Reports/
5. Export results to Result/

## Dependencies
- Power BI Desktop (required for report development)
- CoinGecko API (no authentication required for basic endpoints)

## File Organization
- Place DAX formulas and measure documentation in `clean_data/desc.md`
- Store Power BI files in `Reports/`
- Keep dashboard images in `Result/`
- Raw data sources in `raw_data/`

## Extension Guidelines
When adding new analysis features:
- Follow existing DAX SWITCH patterns for scoring/rating measures
- Update `clean_data/desc.md` with new formulas
- Maintain data flow from raw → clean → reports → results
- Use descriptive measure names (e.g., "Growth Momentum", "Forecast Price")</content>
<parameter name="filePath">d:\nikita git\Crypto_Analysis\.github\copilot-instructions.md