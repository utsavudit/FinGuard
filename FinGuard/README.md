# 🛡️ FinGuard: Fintech Fraud Detection System

## Project Overview  
FinGuard is a comprehensive machine learning-based fraud detection system designed to identify fraudulent financial transactions in real-time. The system analyzes transaction patterns, user behavior, and various financial indicators to classify transactions as legitimate or fraudulent, addressing the critical need for financial security in today's digital economy.

---

## Features  
- **Advanced Machine Learning Models**: Implementation of Random Forest, LightGBM, XGBoost, Logistic Regression, and SVM classifiers  
- **Comprehensive Data Processing**: Strategic missing value imputation, feature engineering, and data normalization  
- **Interactive Visualizations**: Matplotlib, Seaborn, and Plotly-based analytics and model comparison charts  
- **Real-time Fraud Detection**: Optimized for high-performance transaction processing with parallel computing support  
- **Imbalanced Data Handling**: Specialized techniques for dealing with fraud detection's inherent class imbalance  
- **Comprehensive Model Evaluation**: ROC-AUC analysis, confusion matrices, and detailed classification reports  

---

## Dataset  
The project uses the JPMorgan fraud payment dataset containing ~1.5 million financial transaction records with the following features:

| **Feature**               | **Description**                                                            |
|---------------------------|----------------------------------------------------------------------------|
| Transaction Details       | Transaction ID, timestamp, amount (USD), transaction type                 |
| Sender Information        | Sender ID, account, country, sector, line of business                     |
| Beneficiary Information   | Beneficiary ID, account, country                                          |
| Target Variable           | Label (0 = Legitimate, 1 = Fraudulent)                                    |

---

## Key Insights  

### Data Analysis Findings  
- **Class Imbalance**: Only 2.06% of transactions are fraudulent, requiring specialized handling techniques  
- **Geographic Patterns**: USA dominates both sender and beneficiary countries in transactions  
- **Entity Involvement**: JPMC-CLIENT entities are most commonly involved in fraudulent transactions  
- **Transaction Types**: Multiple types including QUICK-PAYMENT, DEPOSIT-CASH, PAY-CHECK, WITHDRAWAL  
- **Amount Distribution**: Both USD amount and sender sector follow non-normal distributions  

### Model Performance  
The system implements and compares multiple machine learning algorithms:
- **Random Forest**: Best overall performance with ensemble learning  
- **LightGBM**: Efficient gradient boosting with high accuracy  
- **XGBoost**: Robust performance with advanced regularization  
- **Logistic Regression**: Fast linear baseline model  
- **SVM**: Alternative classification approach  

All models are evaluated using accuracy, precision, recall, F1-score, and ROC-AUC metrics.

---

## Technical Implementation  

### Data Processing Pipeline  
- **Missing Value Handling**: Strategic imputation based on fraud/non-fraud patterns  
- **Feature Engineering**: Creation of send_rec and surge features for enhanced detection  
- **Data Encoding**: Label encoding for categorical variables  
- **Feature Scaling**: StandardScaler for normalization  
- **Stratified Sampling**: 70-30 train-test split maintaining class proportions  

### Visualization Components  
- **Exploratory Data Analysis**: Transaction type distributions, geographic patterns  
- **Model Comparison**: ROC curves, accuracy comparisons  
- **Feature Analysis**: Correlation heatmaps, feature importance plots  
- **Performance Metrics**: Confusion matrices, classification reports  
