# Simple Credit Card Fraud Detection

A streamlined project to detect fraudulent credit card transactions using machine learning.

## Overview

This project uses the Credit Card Fraud Detection dataset to build a Random Forest classifier that can identify fraudulent transactions. The dataset contains anonymized credit card transactions where only 0.17% are fraudulent, creating a classic imbalanced classification problem.

## Dataset

The Credit Card Fraud Detection dataset contains:
- `Time`: Seconds elapsed between first transaction and current
- `Amount`: Transaction amount
- `V1-V28`: Anonymized features (PCA transformed)
- `Class`: 1 for fraudulent transactions, 0 for legitimate

## Project Structure

```
simple-fraud-detection/
├── data/
│   └── creditcard.csv              # Credit Card Fraud dataset
├── outputs/                        # Generated files
│   ├── summary_stats.csv           # Basic statistics 
│   ├── amount_distribution.png     # Transaction amount visualization
│   ├── correlation_matrix.png      # Feature correlation heatmap
│   ├── confusion_matrix.png        # Model evaluation matrix
│   ├── roc_curve.png               # ROC curve for the model
│   └── feature_importance.png      # Top predictive features
├── fraud_detection.py              # Main Python script
└── requirements.txt                # Project dependencies
```

## Setup and Usage

1. Clone this repository and navigate to the project folder:
```
git clone https://github.com/yourusername/simple-fraud-detection.git
cd simple-fraud-detection
```

2. Create a virtual environment and install dependencies:
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Download the dataset from Kaggle (https://www.kaggle.com/mlg-ulb/creditcardfraud) and place it in the `data/` folder.

4. Run the analysis:
```
python fraud_detection.py
```

## Key Features

- **Data Exploration**: Basic statistics and visualizations
- **Handling Imbalance**: Uses SMOTE to address class imbalance
- **Machine Learning**: Random Forest classifier for fraud detection
- **Model Evaluation**: Confusion matrix, ROC curve, classification metrics
- **Feature Analysis**: Identifies most important variables for fraud detection

## Results

The model typically achieves:
- Precision: ~85-95% (percentage of predicted frauds that are actual frauds)
- Recall: ~85-95% (percentage of actual frauds that are detected)
- ROC-AUC: ~0.95-0.98

Key predictive features are typically V17, V14, V12, and V10, though this may vary slightly between runs.

## Next Steps

Potential improvements:
- Try different classification algorithms
- Implement threshold optimization
- Add cost-benefit analysis
- Create a real-time prediction pipeline
