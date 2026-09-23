Telco Customer Churn Prediction and Analysis

This project analyzes the Telco Customer Churn dataset to identify factors associated with customer loss and builds a predictive model to identify accounts at risk of leaving.
The work was completed as part of the AICTE | IBM SkillsBuild Data Analytics with AI Internship Program 2026, sponsored by Bharat Cares.
Project Overview
The workflow covers raw data cleaning, exploratory data analysis, statistical testing, model training, and evaluation.
Steps Performed	
1.	Preprocess raw customer data.
2.	Analyze churn distribution across contract types.
3.	Apply a chi-square test to evaluate the relationship between contract type and churn.
4.	Run logistic regression using statsmodels to test additional variables.
5.	Train a Random Forest classifier to predict customer attrition.
6.	Evaluate model performance using accuracy, precision, recall, and F1 score.
7.	Extract feature importance values to rank the primary factors influencing predictions.
<img width="833" height="482" alt="Screenshot 2026-09-24 030255" src="https://github.com/user-attachments/assets/c4b7d0ef-024b-4108-9977-3815ff081d20" />
<img width="682" height="475" alt="Screenshot 2026-09-24 030301" src="https://github.com/user-attachments/assets/d27ffaeb-9fdf-46b2-948b-a7894b424bce" />
<img width="582" height="488" alt="Screenshot 2026-09-24 030313" src="https://github.com/user-attachments/assets/35fdabeb-c567-4cae-8e2c-1195e42bb689" />

Dataset Details
●	Dataset: Telco Customer Churn
●	Records: 7,043
●	Features: 21
●	Target Variable: Churn (Yes / No)
●	Source: Kaggle (https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
Summary of Results
Metric	Result
Total customers	7,043
Churned customers	1,869
Churn rate	26.54%
Chi-square statistic (Contract vs. Churn)	1,184.6
Chi-square p-value	< 0.001
Model	Random Forest Classifier
Accuracy	75.2%
Precision (Churn)	52.1%
Recall (Churn)	79.4%
F1 Score	62.9%
Feature importance rankings indicate that tenure, two-year contract status, TotalCharges, fiber optic internet service, MonthlyCharges, and electronic check payment methods contribute most to predicting customer attrition.
Tools Used
Category	Tool
Programming	Python 3.11+
Data processing	Pandas, NumPy
Data visualization	Matplotlib, Seaborn
Statistical analysis	SciPy, statsmodels
Machine learning	Scikit-learn
Environment	Jupyter Notebook
Project File Structure
telco_churn_project/
├── data/
│   └── Telco-Customer-Churn.csv          # Dataset
├── model/
│   ├── churn_model.pkl                  # Trained Random Forest model
│   └── feature_columns.pkl              # Feature order used during training
├── report_images/                       # EDA and evaluation plots
├── Suraj_Joshi_Telco-Customer-Churn.ipynb # Main analysis notebook
├── Suraj_Joshi_ProjectReport.docx        # Project report
├── requirements.txt                     # Python dependencies
└── README.md                            # Project documentation

Running the Project
1. Place the Dataset
Confirm that Telco-Customer-Churn.csv is stored in the data/ directory.
2. Create a Virtual Environment
Isolate dependencies by creating a virtual environment.
python -m venv venv

Activate on Windows:
venv\Scripts\activate

Activate on macOS/Linux:
source venv/bin/activate

3. Install Dependencies
Install the required Python packages:
pip install -r requirements.txt

4. Launch Jupyter Notebook
Run the notebook server:
jupyter notebook

Open Suraj_Joshi_Telco-Customer-Churn.ipynb.
5. Execute Analysis
Run the notebook cells sequentially to:
●	Clean and preprocess raw data.
●	Run exploratory analysis and statistical tests.
●	Fit logistic regression and train the Random Forest model.
●	Export the trained model to model/churn_model.pkl.
Notes on the Data
●	The raw TotalCharges field contains 11 missing entries, corresponding to new accounts with a tenure of 0. These missing values were set to 0 rather than dropped.
●	The target variable Churn is imbalanced (26.5% positive cases). Accuracy alone does not reflect performance, so evaluation emphasizes recall to prioritize detecting accounts likely to cancel service.
●	CustomerID is excluded from modeling because it serves as an identifier rather than a predictive characteristic.
Author : 
Suraj Joshi
AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026
