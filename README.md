# Customer-Churn-Prediction-and-Retention-Strategy (Data Science Portfolio, 2025)
Welcome to my project repository for the Customer Churn Prediction and Retention Strategy project.
The goal was to predict customer churn using machine learning, identify key churn drivers, and provide actionable retention strategies. This project helps businesses reduce churn, improve loyalty, and make data-driven decisions through predictive analytics and interpretability using SHAP.

📋 PROJECT OVERVIEW

Role: Data Science Intern
Duration: March 2025 – May 2025
Mode: Remote | Self-Driven Research
Dataset: Customer Churn Dataset (Telecom-based)

🚀 TASK STRUCTURE
🧩 Level 1: Data Preprocessing & Exploration
| Task | Title                          | Description                                                                                                                                                                                                                                                                                                                                    |
| ---- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **Data Collection & Cleaning** | Imported and inspected raw customer data; dropped leaky columns (e.g., *CustomerID*, *Churn Value*, *Churn Score*, *Churn Reason*) to prevent data leakage. Handled missing values in *Total Charges* via global median imputation *(note: done before splitting to align with code, but flagged as potential leakage for future refinement).* |
| 2    | **Exploratory Data Analysis**  | Identified key patterns, correlations, and churn factors through descriptive statistics, churn distribution plots, and correlation heatmaps for numerical features.                                                                                                                                                                            |
| 3    | **Feature Engineering**        | Addressed class imbalance using SMOTE on training data and encoded categorical variables (e.g., *Contract*, *Payment Method*) with Label Encoding.                                                                                                                                                                                             |
| 4    | **Encoding & Scaling**         | Applied Label Encoding for categorical data; ensured proper train-test split *(80/20, stratified)* to maintain integrity.                                                                                                                                                                                                                      |


🤖 Level 2: Model Development & Evaluation
| Task | Title                     | Description                                                                                                                                                 |
| ---- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **Model Training**        | Trained Logistic Regression, Random Forest, and XGBoost models on SMOTE-resampled training data to predict churn probability.                               |
| 2    | **Evaluation**            | Assessed models using Accuracy, Recall, Precision, ROC-AUC, Confusion Matrices, and ROC Curves. Achieved balanced performance *(e.g., ROC-AUC ~0.85–0.90).* |
| 3    | **Model Selection**       | Selected **Random Forest** for its strong balance of predictive performance, interpretability, and robustness to overfitting.                               |
| 4    | **Hyperparameter Tuning** | Tuned Random Forest via GridSearchCV *(parameters: n_estimators, max_depth, min_samples_split, min_samples_leaf)* for optimal ROC-AUC.                      |


⚖️ Level 3: Model Interpretability & Insights
| Task | Title                                  | Description                                                                                                                                                                                                                                                      |
| ---- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **Feature Importance & SHAP Analysis** | Used Random Forest feature importances and SHAP to interpret predictions, visualizing each feature’s contribution to churn *(e.g., top drivers like contract type and tenure).*                                                                                  |
| 2    | **Customer Segmentation**              | Segmented customers based on predicted churn probabilities; identified top 20% high-risk customers *(e.g., via 80th percentile threshold)* for targeted interventions.                                                                                           |
| 3    | **Insight Generation**                 | Discovered data-driven relationships linking churn with contract type, tenure, monthly charges, payment methods, and other features.                                                                                                                             |
| 4    | **Retention Strategy**                 | Proposed actionable strategies for high-risk groups, including loyalty offers for low-tenure customers, flexible plans for high-charge users, and long-term contract incentives. Included an example high-risk customer profile with decoded categorical values. |


🌐 Level 4: Future Enhancements & Deployment
| Task | Title                         | Description                                                                                                                           |
| ---- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| 1    | **Advanced Modeling**         | *Planned:* Extend with neural networks or ensemble stacking to improve recall on minority churn cases *(not implemented).*            |
| 2    | **Model Saving & Deployment** | *Planned:* Serialize models *(e.g., via joblib)* and deploy as an interactive dashboard using Streamlit or Flask *(not implemented).* |
| 3    | **Automation & Monitoring**   | *Planned:* Implement automated churn alerts and real-time dashboards for ongoing retention campaigns *(not implemented).*             |


🧰 TOOLS USED
|  **Category**              |  **Tools / Libraries**                  |
| -------------------------- | --------------------------------------- |
|    Programming             | Python                                  |
|    Data Processing         | Pandas, NumPy                           |
|    Visualization           | Matplotlib, Seaborn                     |
|    Modeling                | Scikit-learn, Random Forest, imbalanced-learn |
|    Explainability          | SHAP                                    |
|    Development Environment | Jupyter Notebook, VS Code               |
|    Version Control         | Git, GitHub                             |

🎯 OUTCOME

This project successfully developed an end-to-end machine learning pipeline for predicting customer churn and explaining key drivers of attrition.
By leveraging Random Forest (tuned for ROC-AUC ~0.87) and SHAP interpretability, the model identified top churn factors such as contract type, tenure duration, monthly charges, and payment methods.

The insights derived enable telecom and subscription-based businesses to:
1. **Reduce Churn**: Proactively target high-risk customers, potentially saving ~20% of at-risk users through interventions.
2. **Improve Retention**: Enhance satisfaction with tailored strategies (e.g., discounts for short-tenure users), boosting loyalty.
3. **Drive Data-Driven Decisions**: Use predictive analytics for real-time monitoring, with a base churn rate of ~27% in test data.

Key Metrics:
ROC-AUC ≈ 0.87 (Tuned Random Forest)
Accuracy ≈ 0.80
Recall ≈ 0.75
Business Impact: Estimated to save ~50–100 customers in a 1,000-customer scenario via targeted retention.

