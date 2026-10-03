# Molecule Solubility Prediction

This project uses machine learning to predict the aqueous solubility of molecules from four simple molecular descriptors, comparing a linear model against two tree-based ensemble models.

## 🧪 Dataset Overview

The dataset contains **1,144 molecules**, each described by **4** chemical features. It is the Delaney (ESOL) solubility dataset with precomputed descriptors, loaded from the [dataprofessor/data](https://github.com/dataprofessor/data) repository.

## Target Variable
- `logS`: Logarithm of aqueous solubility (regression target)

## Feature Columns
- `MolLogP`: Octanol-water partition coefficient (logP)
- `MolWt`: Molecular weight of the molecule
- `NumRotatableBonds`: Number of rotatable bonds
- `AromaticProportion`: Proportion of atoms that are aromatic

## Methods
- Features and target are separated, then split 70/30 into training and test sets (`random_state=100`).
- Three regression models are trained:
  - **Linear Regression**
  - **Random Forest** (1,000 trees, max depth 10)
  - **Gradient Boosting**
- Models are compared using mean squared error (MSE) and R² on both the training and test sets.
- Predicted vs. experimental logS is plotted for each model, and a correlation heatmap shows how the features relate to each other and to solubility.

## Results

| Model             | Train R² | Test MSE | Test R² |
|-------------------|----------|----------|---------|
| Linear Regression | 0.759    | 0.913    | 0.794   |
| Random Forest     | 0.971    | 0.596    | 0.865   |
| Gradient Boosting | 0.926    | 0.601    | 0.864   |

Random Forest and Gradient Boosting performed almost identically on the test set and both clearly outperformed Linear Regression, suggesting the relationship between these descriptors and solubility is not purely linear. Random Forest's gap between training R² (0.97) and test R² (0.87) indicates some overfitting.

## Libraries Used
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

## How to Run

**Option 1: Google Colab (no setup needed)**

[Open the notebook in Colab](https://colab.research.google.com/github/emaadhasan/molecule-solubility/blob/main/Solubility.ipynb), then click **Runtime → Run all**.

**Option 2: Run locally**

```bash
git clone https://github.com/emaadhasan/molecule-solubility.git
cd molecule-solubility
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook Solubility.ipynb
```
