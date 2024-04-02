# **Credit Card Fraud Detection**

**Introduction:**
Credit card fraud is a significant concern for both financial institutions and consumers worldwide. Detecting fraudulent transactions promptly is crucial to prevent financial losses and maintain trust in the banking system. This project focuses on leveraging machine learning techniques to detect fraudulent credit card transactions accurately.

**Dataset Overview:**
The dataset used in this project contains transactions made by European cardholders during September 2013. It includes a total of 284,807 transactions, with 492 instances of fraud. Notably, the dataset is highly unbalanced, with frauds accounting for only 0.172% of all transactions. To preserve confidentiality, the dataset features have undergone a Principal Component Analysis (PCA) transformation, except for 'Time' and 'Amount'. The 'Time' feature represents the seconds elapsed between each transaction and the first transaction in the dataset, while the 'Amount' feature denotes the transaction amount.

**Approach:**
1. **Data Preprocessing:**
   - Standardization: To ensure uniformity in the data, the 'Time' and 'Amount' features are standardized using RobustScaler. This transformation makes the data less sensitive to outliers.
   - Handling Imbalance: Due to the significant class imbalance, where the majority of transactions are non-fraudulent, the dataset is rebalanced using the RandomOverSampler technique from the imbalanced-learn library. This technique generates synthetic samples of the minority class to achieve a balanced distribution.

2. **Modeling:**
   - Three machine learning algorithms are trained on the balanced dataset:
     - Random Forest
     - XGBoost
     - KNN Classifier

3. **Evaluation:**
   - Model performance is evaluated using the Area Under the Precision-Recall Curve (AUPRC) metric, which is suitable for imbalanced classification tasks.
   - The AUC scores obtained for each model are as follows:
     - Random Forest: AUC = 0.88
     - XGBoost: AUC = 0.90
     - KNN Classifier: AUC = 0.91

**Files Included:**
1. `creditcard.csv`: The dataset containing credit card transactions.
2. `Credit Card Fraud Detection.ipynb`: Jupyter Notebook containing the code for data preprocessing, modeling, and evaluation.
3. `README.md`: This file, providing an overview, approach, evaluation results, and instructions to run the code.

**Instructions to Run:**
1. Clone the repository: `git clone https://github.com/your_username/Credit-Card-Fraud-Detection.git`.
2. Install required dependencies: `pip install -r requirements.txt`.
3. Open and run `Credit Card Fraud Detection.ipynb` in Jupyter Notebook or any compatible environment.
4. Ensure the dataset `creditcard.csv` is placed in the same directory as the notebook.

**References:**
- Dataset Source: [Kaggle]([https://www.kaggle.com/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud))
- Python Libraries: pandas, numpy, seaborn, matplotlib, scikit-learn, imbalanced-learn.

**Author:**
- Shanmugagouthaman Karuppiah
- shanmugagouthaman46@gmail.com
- (https://www.linkedin.com/in/shanmugagouthaman-kr-068816169/)


**License:**
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

**Acknowledgements:**
- Credit to Kaggle and the dataset contributors.
- Thanks to scikit-learn and imbalanced-learn libraries for providing useful tools for data preprocessing and modeling.
