# Online Shoppers: Will a Session End in a Purchase?

This notebook predicts whether an online shopping session ends in a purchase. It uses the [UCI Online Shoppers Purchasing Intention dataset](https://archive.ics.uci.edu/dataset/468/online+shoppers+purchasing+intention+dataset), which has 12,330 sessions. About 15% of those sessions end in a purchase.

## What's in the notebook
- Data exploration, plus a look at class imbalance
- Preprocessing: a log transform, scaling and one-hot encoding, with a stratified 80/20 train/test split
- Four models, each tuned with a grid search (5-fold CV):
  - Logistic regression
  - Linear SVM
  - Polynomial SVM
  - RBF SVM
- A comparison of the models by F1, ROC AUC, precision, recall and runtime, each trained with and without `class_weight="balanced"`
- The best model's confusion matrix
- The logistic regression coefficients
- Each model's decision boundary on PageValues vs. ExitRates

## How to run it
1. Download `online_shoppers_intention.csv` from the UCI link above and put it in `data/`.
2. Install the packages:
   ```
   pip install numpy pandas scikit-learn matplotlib seaborn jupyter
   ```
3. Open `online_shoppers_analysis.ipynb` and run all cells.
