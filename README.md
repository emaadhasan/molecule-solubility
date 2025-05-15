# Molecule Solubility Prediction

This project applies machine learning to predict the solubility of molecules using a dataset of molecular descriptors. 

## 🧪 Dataset Overview

The dataset contains **800 molecules**, each described by **4** chemical features used to predict solubility.

## Target Variable
- `logS`: Logarithm of aqueous solubility (regression target)

## Feature Columns
- `MolLogP`: Octanol-water partition coefficient (logP)
- `MolWt`: Molecular weight of the molecule
- `NumRotatableBonds`: Number of rotatable bonds
- `AromaticProportion`: Proportion of atoms that are aromatic

## Data Processing
- Features and target variable are separated.
- Dataset is split into training and testing subsets.

## Model Building
- **Linear Regression**
- **Random Forest**
- **Gradient Boosting**

## Evaluation
- Models are compared using MAE, RMSE, and R² scores.
- Visualization techniques are used to understand correlation 

## Features
- Data preprocessing and visualization
- Correlation analysis
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

1. Visit [Google Colab](https://colab.research.google.com)
2. Click **File → Open Notebook**
3. Go to the **GitHub** tab
4. Paste this URL: https://github.com/emaadhasan/molecule-solubility
5. Select `Solubility.ipynb` and click **Open**

OR

Clone the repository:
  ```bash
  git clone https://github.com/emaadhasan/molecule-solubility.git
  cd molecule-solubility ```
