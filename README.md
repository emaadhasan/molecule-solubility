# Molecule Solubility Prediction

This project uses machine learning to predict the solubility of molecules based on molecular descriptors.

## Project Overview

### **Solubility of Molecules**

This notebook explores various regression models to estimate molecular solubility using selected features from a chemical dataset.

#### Data Processing
- Features and target variable are separated.
- Dataset is split into training and testing subsets.

#### Model Building
- **Linear Regression**
- **Random Forest**
- **Gradient Boosting**

#### Evaluation
- Models are compared using MAE, RMSE, and R² scores.
- Visualization techniques are used to understand feature importance and correlation.

## Features
- Data preprocessing and visualization
- Feature selection and correlation analysis
- Model training with:
  - Random Forest
  - Gradient Boosting
  - Linear Regression
- Performance comparison using standard regression metrics

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/emaadhasan/molecule-solubility.git
   cd molecule-solubility
