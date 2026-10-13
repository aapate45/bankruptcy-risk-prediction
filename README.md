# Bankruptcy Risk Prediction

**Independent reconstruction** inspired by WorldQuant University Applied Data Science Lab Project 5. This repository is not an original recovered course submission.

## Goal
Compare Random Forest and Gradient Boosting classifiers on rare-event bankruptcy prediction, emphasizing the trade-off between **recall** (finding bankrupt firms) and **precision** (avoiding false alarms).

## Dataset
[UCI Polish Companies Bankruptcy](https://archive.ics.uci.edu/dataset/365/polish+companies+bankruptcy+data), using the 3-year cohort (10,503 financial statements, 64 financial-ratio features, 495 bankruptcies). The dataset is fetched when you run the notebook; it is not redistributed here. License: CC BY 4.0.

## Method
1. Inspect class imbalance and missing values.
2. Create stratified train/test split.
3. Impute missing values and randomly oversample **training data only** inside an `imblearn` pipeline.
4. Fit Random Forest and Histogram-based Gradient Boosting classifiers.
5. Compare precision, recall, F1, average precision, confusion matrices, and precision–recall curves.
6. Inspect Random Forest feature importance and discuss limitations.

## Run
```bash
python -m pip install -r requirements.txt
jupyter notebook bankruptcy_risk_prediction.ipynb
```
Run all notebook cells to generate results. Results are intentionally not fabricated in this README.

## Attribution
- Dataset: Tomczak, S. (2016), *Polish Companies Bankruptcy*, UCI Machine Learning Repository, [DOI 10.24432/C5F600](https://doi.org/10.24432/C5F600), CC BY 4.0.
- Educational inspiration: [WorldQuant University Data Science Lab](https://www.wqu.edu/data-science-lab), Project 5.
- Implementation: independent reconstruction; not copied from another learner’s coursework.
