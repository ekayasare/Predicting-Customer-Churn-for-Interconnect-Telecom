# Final Sprint Project – Churn Prediction for Interconnect Telecom

This was my final and most comprehensive project in the TripleTen Data Science program. Everything I’d learned so far — from EDA and data cleaning to modeling and evaluation — came together here. The challenge? Build a machine learning model to predict **customer churn** for Interconnect Telecom and help the company boost its retention strategy.

### Predicting Customer Churn with Contract & Service Data

Churn is a massive issue in the telecom industry. Interconnect Telecom wanted to know which customers were at risk of leaving so they could step in with personalized retention offers. My job was to develop a reliable churn prediction model with a target **AUC-ROC score of 0.85+**.

#### The Data

The data came in four separate files, each covering a different aspect of the customer experience:

- **`personal.csv`**: Customer demographics (`gender`, `SeniorCitizen`, `Partner`, `Dependents`)
- **`contract.csv`**: Core account info including `BeginDate`, `EndDate`, contract `Type`, and `TotalCharges`
- **`phone.csv`**: Whether the customer had a phone plan or multiple lines
- **`internet.csv`**: Internet services like `StreamingTV`, `OnlineSecurity`, etc.

I merged all of this into one clean dataset, carefully handling missing values and aligning records across the files.

#### The Process

1. **Data Inspection & Preprocessing**  
   - Checked all data types, handled missing values (especially in the internet data), and converted date columns to datetime format.
   - Fixed the `TotalCharges` column which was incorrectly stored as text.

2. **Feature Engineering**  
   - Created a binary target variable from the `EndDate` column (`No` = active, else = churned).
   - Generated new features based on service usage and contract types.

3. **Model Training**  
   - Trained several models including Logistic Regression, Random Forest, and Gradient Boosting.
   - Evaluated performance using **F1 score**, **accuracy**, and especially **AUC-ROC**, which reflects how well the model distinguishes churners from loyal users.

4. **Final Model & Evaluation**  
   - Achieved an AUC-ROC score exceeding the 0.85 target 
   - Identified key churn indicators like contract type, tenure, and internet service combinations.

### Results & Takeaways

This project was the ultimate test of my end-to-end data science workflow. I got to practice everything — merging complex datasets, thoughtful preprocessing, feature engineering, and optimizing model performance with real business impact in mind.
