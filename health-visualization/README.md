# Health Visualization Projects
This folder contains my healthcare data visualization work.
# Health Visualization Project

This project analyzes global health indicators to identify patterns, correlations, and insights across different countries. The visualization tools help compare healthcare systems, identify areas for improvement, and understand the relationship between various health metrics.

## Features

- **Data Loading**: Loads health data from multiple countries with realistic metrics
- **Preprocessing**: Normalizes health indicators and calculates a composite health index
- **Visualizations**:
  - Life Expectancy vs Healthcare Expenditure scatter plot
  - Health Indicators Correlation heatmap
  - Top Countries by Health Index bar chart
  - Health Metrics Radar chart for comparing countries
  - PCA and Clustering Analysis to group countries by health profiles

## Data Sources

The data used in this project is based on realistic health metrics similar to those from:
- World Health Organization (WHO) Global Health Observatory
- World Bank Health Indicators
- OECD Health Statistics

## Project Structure

```
health-visualization-project/
│
├── health_data_analysis.py       # Main script for data processing and visualization
├── requirements.txt              # Project dependencies
├── README.md                     # Project documentation
│
└── outputs/                      # Output directory for visualizations and data
    ├── life_expectancy_vs_expenditure.png
    ├── health_indicators_correlation.png
    ├── top_countries_health_index.png
    ├── health_metrics_radar.png
    ├── health_indicators_pca_clustering.png
    └── processed_health_data.csv
```

## Installation and Setup

1. Clone this repository
2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the main script to generate all visualizations:

```bash
python health_data_analysis.py
```

All visualizations will be saved to the `outputs` directory.

## Example Outputs

### Life Expectancy vs Healthcare Expenditure
Shows the relationship between healthcare spending and population health outcomes, with point size representing physician density and color showing vaccination coverage.

### Health Indicators Correlation
A heatmap displaying how different health metrics correlate with each other, helping identify which factors most strongly influence overall health outcomes.

### Top Countries by Health Index
Bar chart of the best-performing countries according to the composite health index.

### Health Metrics Radar Chart
Multi-dimensional comparison of selected countries across normalized health metrics.

### PCA and Clustering Analysis
Dimensionality reduction and clustering to group countries with similar health profiles, revealing patterns not apparent in raw data.

## Extending the Project

You can extend this project by:
- Adding time-series analysis of health trends
- Incorporating additional data sources
- Creating an interactive dashboard with Plotly or Dash
- Implementing more sophisticated machine learning models

## License

This project is licensed under the MIT License - see the LICENSE file for details.
