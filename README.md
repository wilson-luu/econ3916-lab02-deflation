# Deflating Economic Data — Nominal vs. Real
## Objective
To rigorously isolate actual changes in purchasing power from background inflation by building programmatic deflation models using Federal Reserve Economic Data (FRED).
## Methodology
- Data Ingestion: Systematically retrieved the Consumer Price Index (CPIAUCSL) and Total Private Average Hourly Earnings (AHETPI) via FRED's public CSV endpoint without requiring an API key.
- Algorithmic Deflation: Developed a reusable Python function, deflate_series(), to programmatically convert any nominal time series into constant base-year (2020) dollars.
- Index Transformation: Cleaned and aligned the semi-annual Economist Big Mac Index against monthly FRED CPI readings using the .asof() method to ensure strict chronological matching.
- Interactive Visualization: Deployed an interactive exploration dashboard using ipywidgets to dynamically render the impact of shifting base years on nominal/real divergence.
## Key Findings
- The Illusion of Nominal Growth: While nominal hourly earnings appear to have surged consistently over the past fifty years (from $2.50 to $32.53), deflating to constant 2020 dollars reveals a completely different structural reality: real earnings moved only from $20.92 to $25.20, demonstrating prolonged periods of flat or declining purchasing power.
- Isolating Real Price Increases: Between 2000 and the present, the US Big Mac nominal price increased by 178%. However, after adjusting for a 95% increase in the CPI over the same period, the real price increase of the burger was only 43%, highlighting how inflation visually overstates actual localized price hikes.
