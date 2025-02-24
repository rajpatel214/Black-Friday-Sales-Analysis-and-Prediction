**Project Title: Black Friday Sales Analysis and Prediction**

### **Objective:**
The primary goal of this project is to analyze customer purchasing behavior and predict the purchase amount based on various demographic and product-related features. The dataset consists of transaction records from a Black Friday sale, providing insights into factors influencing customer spending patterns.

### **Dataset Overview:**
The dataset includes attributes such as:
- **User demographics** (Gender, Age, Marital Status, City Category, Stay in Current City Years)
- **Product-related information** (Product Categories, Product ID, Occupation)
- **Target variable**: **Purchase Amount** (amount spent by the customer during the sale)

### **Predictive Modeling Approach:**
The analysis includes building multiple regression models to predict the purchase amount based on the given independent variables. The following models were implemented:

#### **1. Linear Regression:**
- This model attempts to establish a linear relationship between the independent variables and the purchase amount.
- **Performance:**
  - R2 Score (Test): **0.1298**
  - R2 Score (Train): **0.1316**
  - RMSE (Test): **4693.57**
  - RMSE (Train): **4678.90**
- The model exhibited poor performance due to the presence of non-linearity in the data and the limited ability of linear regression to capture complex relationships.

#### **2. Ridge Regression:**
- Ridge regression applies L2 regularization to control overfitting and improve generalization.
- **Performance:**
  - R2 Score (Test): **0.1298**
  - R2 Score (Train): **0.1316**
  - RMSE (Test): **4693.57**
  - RMSE (Train): **4678.90**
- Ridge regression did not significantly improve performance compared to standard linear regression.

#### **3. Lasso Regression:**
- Lasso regression applies L1 regularization, which helps in feature selection by reducing coefficients of less important features to zero.
- **Performance:**
  - R2 Score (Test): **0.1298**
  - R2 Score (Train): **0.1316**
  - RMSE (Test): **4693.57**
  - RMSE (Train): **4678.90**
- The results were almost identical to Ridge regression, showing limited impact.

#### **4. ElasticNet Regression:**
- A hybrid model combining L1 (Lasso) and L2 (Ridge) regularization techniques.
- **Performance:**
  - R2 Score: **0.1182**
  - RMSE: **4724.80**
- The performance was slightly lower than Lasso and Ridge, indicating that simple linear regression models may not be the best fit for this dataset.

#### **5. Gradient Boosting Regressor (GBR):**
- A tree-based ensemble learning method that optimizes the predictive accuracy by iteratively correcting errors.
- **Performance:**
  - R2 Score: **0.6607**
  - RMSE: **2930.72**
- Gradient Boosting significantly outperformed linear regression-based models, demonstrating its effectiveness in capturing complex relationships within the data.

### **Final Conclusion:**
- Simple linear regression models such as Linear, Ridge, Lasso, and ElasticNet performed poorly, with R2 scores below **0.14**, indicating that these models struggle to capture the patterns in customer purchase behavior.
- Gradient Boosting Regressor emerged as the best-performing model, achieving an **R2 score of 0.66**, demonstrating its ability to model non-linearity in the data.
- The dataset contains complex relationships that are better captured by tree-based ensemble methods rather than traditional linear models.
