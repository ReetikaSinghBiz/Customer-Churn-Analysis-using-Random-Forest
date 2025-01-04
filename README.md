# Customer Churn Analysis using Random Forest

## Overview
This project focuses on analyzing customer churn in a telecom dataset using Random Forest. The model predicts customer churn and identifies key factors contributing to it, providing insights for customer retention strategies.



## Workflow

### 1. Data Exploration and Preprocessing
- **Dataset Features**:
  - Target variable: `Churn` (0 = Retained, 1 = Churned).
  - Predictors include customer account details, service usage, and billing information.
- **Data Cleaning**:
  - Converted binary columns (`Churn`, `ContractRenewal`, `DataPlan`) to categorical.
  - Handled missing values, duplicate rows, and outliers using Winsorization.

### 2. Data Visualization
- **Churn Rate**:
  - Visualized churn rate distribution using a pie chart.
- **Outliers**:
  - Examined data distributions with boxplots before and after Winsorization.

### 3. Data Partitioning
- Split the data into training (70%) and testing (30%) sets with stratified sampling to preserve class proportions.

### 4. Random Forest Model
- **Model Configuration**:
  - Random Forest Classifier with:
    - `n_estimators=25`
    - `max_depth=4`
    - `min_samples_split=100`
    - `min_samples_leaf=50`
- **Training**:
  - Trained the model on the training set and evaluated feature importance.

### 5. Feature Importance
- Identified top predictors of churn:
  1. `CustServCalls`
  2. `DayMins`
  3. `MonthlyCharge`
  4. `DataUsage`
  5. `ContractRenewal`

### 6. Model Evaluation
- **Metrics**:
  - Confusion Matrix
  - Accuracy
  - Classification Report (Precision, Recall, F1-score)
- Achieved high accuracy on both training and testing datasets.

### 7. Hyperparameter Tuning
- Conducted Grid Search to optimize model parameters.

### 8. Predictions
- Applied the model to live data for real-time churn predictions.



## Libraries Used
- **pandas**, **numpy**: For data manipulation and analysis.
- **seaborn**, **matplotlib**, **plotly**: For visualizations.
- **scikit-learn**: For Random Forest, metrics, and hyperparameter tuning.
- **pydot**: For Random Forest visualization.
- **pickle**: For model export.



## Key Outputs
1. **Churn Rate**: Pie chart illustrating the percentage of churned vs. retained customers.
2. **Feature Importance**: Bar chart of the top predictors.
3. **Model Performance**:
   - High accuracy and balanced classification metrics on both train and test datasets.
4. **Random Forest Tree Visualization**: Graphical representation of a tree in the Random Forest.



## How to Run
1. Ensure the dataset `telecom_churn.csv` is in your working directory.
2. Install required libraries:
   ```bash
   pip install pandas numpy seaborn matplotlib plotly scikit-learn pydot
3. Run the script in a Python environment (e.g., Jupyter Notebook).
4. Explore the final predictions and performance metrics.



## Results
The Random Forest model accurately predicts customer churn.
Key factors influencing churn were identified, offering actionable insights:
High customer service calls and excessive usage fees are strong churn indicators.
Recommendations for customer retention:
Improve service quality and billing transparency.



## Model Export
The trained model has been exported as a .pkl file for deployment:



## Author
Reetika Singh
