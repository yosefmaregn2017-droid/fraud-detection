# Fraud Detection – E-commerce & Bank Transactions

This project aims to detect fraudulent transactions for e-commerce and banking using machine learning. It covers data cleaning, exploratory data analysis (EDA), feature engineering, and model building for highly imbalanced datasets. The goal is to build accurate and explainable fraud detection models.

---

## Project Structure

fraud-detection/
├── .vscode/                  # VS Code settings
├── .github/                  # GitHub workflows
├── data/                     # Data folder (add to .gitignore)
│   ├── raw/                  # Original datasets
│   └── processed/            # Cleaned & feature-engineered data
├── notebooks/                # Jupyter notebooks for EDA and modeling
├── src/                      # Python modules (if any)
├── tests/                    # Test scripts
├── models/                   # Saved model artifacts
├── scripts/                  # Additional scripts
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation
└── .gitignore

---

## Installation & Setup

1. Clone the repository:

```bash
git clone https://github.com/yosefmaregn2017-droid/fraud-detection.git
```

2. Navigate to the project directory:

```bash
cd fraud-detection
```

3. Create and activate a virtual environment:

```bash
python -m venv .venv
.venv\Scripts\activate  # Windows
source .venv/bin/activate # Mac/Linux
```

4. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Data

* **Fraud_Data.csv**: E-commerce transactions
* **IpAddress_to_Country.csv**: IP to country mapping
* **creditcard.csv**: Bank transaction dataset

**Note:** Only raw data should be stored in `data/raw`. Processed datasets are saved in `data/processed`.

---

## Notebooks

* `eda-fraud-data.ipynb`: EDA and feature engineering for e-commerce transactions
* `eda-creditcard.ipynb`: EDA for bank transactions
* `feature-engineering.ipynb`: Feature creation and transformation
* `modeling.ipynb`: Model training and evaluation
* `shap-explainability.ipynb`: SHAP analysis and interpretation

---

## Usage

1. Run `eda-fraud-data.ipynb` to explore and preprocess the dataset.
2. Save the processed dataset to `data/processed/`.
3. Use `modeling.ipynb` to train baseline and ensemble models.
4. Apply SHAP analysis using `shap-explainability.ipynb`.

---

## Class Imbalance Handling

* Target variable `class` is highly imbalanced (~2% fraud, ~98% non-fraud).
* Techniques:

  * Metrics: F1-score, Precision-Recall AUC instead of accuracy.
  * Resampling: SMOTE or undersampling during training.
  * Stratified split to maintain class ratios in train/test sets.

---

## License

This project is for educational purposes under 10 Academy AI Mastery course.
