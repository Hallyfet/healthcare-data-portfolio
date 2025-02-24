# Statistical Analysis Projects
# This folder contains my statistical analysis work.
# House Price Statistical Analysis Project

This project conducts statistical analysis of King County house sale data to identify price patterns and key factors influencing home values.

## Dataset

The analysis uses the King County House Sales dataset, which contains information about houses sold in King County, Washington between May 2014 and May 2015. This is real-world data with the following features:

- `id`: Unique identifier for each house
- `date`: The date the house was sold
- `price`: Sale price (target variable)
- `bedrooms`: Number of bedrooms
- `bathrooms`: Number of bathrooms
- `sqft_living`: Square footage of living space
- `sqft_lot`: Square footage of the lot
- `floors`: Number of floors
- `waterfront`: Whether the house has a waterfront view
- `view`: View rating (0-4)
- `condition`: Condition rating (1-5)
- `grade`: Grade rating (1-13)
- `sqft_above`: Square footage above ground
- `sqft_basement`: Square footage of the basement
- `yr_built`: Year built
- `yr_renovated`: Year renovated (0 if never renovated)
- `zipcode`: ZIP Code
- `lat`: Latitude
- `long`: Longitude
- `sqft_living15`: Average square footage of nearby houses
- `sqft_lot15`: Average square footage of nearby lots

## Project Structure

```
house-price-analysis/
├── data/
│   └── kc_house_data.csv
├── outputs/
│   ├── summary_statistics.csv
│   ├── price_distribution.png
│   ├── price_by_condition.png
│   ├── correlation_matrix.png
│   ├── feature_coefficients.csv
│   ├── actual_vs_predicted.png
│   ├── geographical_prices.png
│   └── zipcode_price_analysis.csv
├── analysis.py
├── requirements.txt
└── README.md
```

## Setup and Installation

1. Clone this repository:
```
git clone https://github.com/yourusername/house-price-analysis.git
cd house-price-analysis
```

2. Install required dependencies:
```
pip install -r requirements.txt
```

3. Download the dataset:
   - The King County House Sales dataset can be downloaded from Kaggle: https://www.kaggle.com/harlfoxem/housesalesprediction
   - Place the CSV file in the `data/` directory

## Running the Analysis

To run the full analysis pipeline:

```
python analysis.py
```

This will:
1. Load and perform exploratory data analysis on the house price dataset
2. Generate visualizations of price distributions and relationships
3. Build a regression model to identify key price factors
4. Conduct geographical analysis of price patterns
5. Save all results to the `outputs/` directory

## Sample Outputs

The analysis produces the following outputs:

### Statistical Summaries
- `summary_statistics.csv`: Basic statistics for all numerical features
- `feature_coefficients.csv`: Importance of each feature in predicting price
- `zipcode_price_analysis.csv`: Price statistics by ZIP code

### Visualizations
- `price_distribution.png`: Distribution of house prices
- `price_by_condition.png`: Box plots of prices by house condition
- `correlation_matrix.png`: Heatmap showing correlations between features
- `actual_vs_predicted.png`: Scatter plot comparing predicted vs actual prices
- `geographical_prices.png`: Map showing house prices by location

## Key Findings

The analysis reveals several important insights about the King County housing market:

1. Square footage of living space is the strongest predictor of house price
2. House grade (quality) has a significant positive impact on price
3. Waterfront properties command a substantial premium
4. There are clear geographical patterns in housing prices, with certain ZIP codes having significantly higher median prices
5. The model can predict house prices with an R² score of approximately 0.65-0.70

## Extending the Analysis

Possible extensions to this project include:
- Time series analysis of price trends
- More advanced modeling techniques (random forests, gradient boosting)
- Feature engineering to improve prediction accuracy
- Interactive visualizations with Plotly or Bokeh
