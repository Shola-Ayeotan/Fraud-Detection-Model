# Fraudulent Transaction Detection
This project focused on detecting fraudulent credit card transactions using unsupervised machine learning algorithms. Fraudulent activity in banking often involves unauthorised transactions using stolen credit card details. The aim was to build a model that could accurately identify fraudulent transactions in real-time, enabling financial institutions to take immediate action.

## Approach

Unsupervised learning techniques were chosen for anomaly detection due to the absence of labelled fraud data. The following methods were implemented:
- Isolation Forest: This algorithm identified anomalies based on the ease with which data points could be isolated. Since fraudulent transactions are rare and different from normal transactions, they were expected to be isolated with fewer splits.

- Local Outlier Factor (LOF): This method detected anomalies by comparing the local density of data points, identifying transactions that significantly deviated from their nearest neighbours.

## Tech Stack
Programming Language: Python
Libraries Used: Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib

## Project Workflow
1. Data Loading & Configuration
- A config.ini file was used to store parameters that could be adjusted for different datasets.
- The dataset was loaded from credit_card_transactional_data.csv.

2. Exploratory Data Analysis (EDA)
- Statistical summaries and data distributions were examined.
- Missing values were identified and handled appropriately.
- Correlations between features were analysed.

3. Determining Contamination Factor
- The contamination parameter, representing the estimated proportion of anomalies, was determined using data insights.

4. Model Training & Evaluation
- The Isolation Forest and LOF models were trained on the dataset.
- Predictions were generated, classifying transactions as normal or fraudulent.
- Anomaly scores were analysed to understand model performance.

5. Visualisations
- Countplots and boxplots were used to compare fraudulent and legitimate transactions.
- Heatmaps were generated to highlight correlations between features.

6. Saving the Models
- Trained models were stored as .pkl files (IF_model.pkl and LOF_model.pkl) for future use, avoiding the need for retraining.
