# Bankruptcy Risk Prediction

For this project, I used financial data from Polish companies to predict whether a company would go bankrupt. I compared Random Forest and Gradient Boosting models and focused on how class imbalance affected their performance.

This project is based on concepts I learned through the WorldQuant University Applied Data Science Lab.

## Dataset

I used the Polish Companies Bankruptcy dataset from the UCI Machine Learning Repository. For the 3-year cohort used in this project, there were 10,503 companies with 64 financial features. Only 495 companies, or about 4.7%, went bankrupt.

Because bankrupt companies made up such a small part of the dataset, I focused on precision, recall, F1 score, and average precision instead of relying only on accuracy.

## Models

I compared two classification models:

- Random Forest
- Gradient Boosting

I split the data into training and test sets using a stratified split and oversampled the minority class only in the training data. I also handled missing values as part of the model pipeline.

## Results

| Model | Accuracy | Precision | Recall | F1 | Average Precision |
| --- | --- | --- | --- | --- | --- |
| Random Forest | 0.96 | 0.62 | 0.21 | 0.32 | 0.43 |
| Gradient Boosting | 0.94 | 0.43 | 0.66 | 0.52 | 0.64 |

Random Forest had higher overall accuracy and precision, but it only identified about 21% of the companies that actually went bankrupt. Gradient Boosting identified about 66% of the bankrupt companies and had a higher F1 score and average precision.

This showed me why accuracy can be misleading with an imbalanced dataset. Even though Gradient Boosting had slightly lower accuracy, it was much better at identifying the minority class.

## Tools

Python, Pandas, NumPy, Scikit-learn, Imbalanced-learn, Matplotlib

## What I Learned

This project helped me better understand how class imbalance affects classification models and why the metrics used to evaluate a model depend on the problem. I also got more experience comparing models using precision, recall, confusion matrices, and precision-recall curves instead of relying on one metric.

## Source

Dataset: Polish Companies Bankruptcy, UCI Machine Learning Repository

Project inspiration: WorldQuant University Applied Data Science Lab, Project 5
