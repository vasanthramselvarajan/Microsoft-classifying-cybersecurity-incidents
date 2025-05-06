# Cybersecurity Incident Triage Classification

This repository provides a machine learning model designed to classify cybersecurity incidents into three triage grades: **True Positive (TP)**, **Benign Positive (BP)**, and **False Positive (FP)**. The model leverages the GUIDE dataset, which includes evidence, alerts, and incidents, to predict the triage grade based on historical data and customer responses.

## Objective

The goal is to enhance the efficiency of Security Operation Centers (SOCs) by automating the triage process. By accurately classifying cybersecurity incidents, SOC analysts can prioritize and respond to critical threats faster. The model's predictions help to guide response systems, improving the overall security posture of enterprise environments.

## Approach

### 1. Data Exploration and Understanding
- **Initial Inspection**: Load the `train.csv` dataset and inspect the data's structure (features, variable types, target distribution).
- **Exploratory Data Analysis (EDA)**: Use visualizations and statistical summaries to detect patterns, correlations, and potential anomalies. Pay special attention to class imbalances, which may require specific handling strategies.

### 2. Data Preprocessing
- **Handling Missing Data**: Identify and address missing values through strategies like imputation or removal.
- **Feature Engineering**: Create or modify features to improve model performance (e.g. deriving new features from timestamps, or normalizing numerical variables).
- **Encoding Categorical Variables**: Convert categorical features to numerical values using methods like one-hot encoding, label encoding, or target encoding.

### 3. Data Splitting
- **Train-Validation Split**: Split the `train.csv` data into training and validation sets (e.g., 70-30 or 80-20) to facilitate model tuning and evaluation.
- **Stratification**: Use stratified sampling to maintain similar class distributions in both the training and validation sets, especially for imbalanced classes.

### 4. Model Selection and Training
- **Baseline Model**: Start with a simple model (e.g., logistic regression or decision tree) to set a performance benchmark.
- **Advanced Models**: Experiment with more complex models like Random Forest, XGBoost, LightGBM.
- **Cross-Validation**: Implement k-fold cross-validation to ensure reliable model evaluation and reduce overfitting risks.

### 5. Model Evaluation and Tuning
- **Performance Metrics**: Evaluate model performance using macro-F1 score, precision, and recall, ensuring balanced performance across all classes.
- **Hyperparameter Tuning**: Optimize hyperparameters using grid search or random search to enhance model accuracy.
- **Handling Class Imbalance**: Apply techniques like SMOTE (Synthetic Minority Over-sampling Technique), adjusting class weights, or using ensemble methods to boost the model's ability to handle minority classes.

### 6. Model Interpretation
- **Feature Importance**: Analyze the most influential features for predictions using methods like randomforest feature importance score, or model-specific importance measures.
- **Error Analysis**: Identify common misclassifications to gain insights into possible model or feature refinements.

### 7. Final Evaluation on Test Set
- **Testing**: Once the model is optimized, evaluate its performance on the `test.csv` dataset. Report the final macro-F1 score, precision, and recall.
- **Comparison to Baseline**: Compare the test set results to the baseline model to ensure consistent improvement.

### 8. Documentation and Reporting
- **Model Documentation**: Thoroughly document the entire process, including data preprocessing, model selection, evaluation metrics, and challenges encountered.
  
## Results
- A machine learning model capable of accurately predicting the triage grade of cybersecurity incidents (TP, BP, FP) with high **macro-F1 score**, **precision**, and **recall**.
- Comprehensive analysis of model performance, including insights into which features are most influential in the prediction process.

## Project Evaluation Metrics
The success and effectiveness of the project will be evaluated based on the following metrics:
- **Macro-F1 Score**: A balanced metric that accounts for the performance across all classes (TP, BP, FP), ensuring that each class is treated equally.
- **Precision**: Measures the accuracy of positive predictions, crucial for minimizing false positives.
- **Recall**: Measures the model's ability to correctly identify all relevant instances (true positives), ensuring that real threats are not missed.

This solution aims to improve SOC efficiency by automating the triage process, providing accurate incident classifications, and ultimately strengthening enterprise cybersecurity.
