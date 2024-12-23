# Retail Superstore Sales Analysis  

This project analyzes sales trends, profit margins, and customer segmentation for a retail superstore using a dataset containing transactional and customer-related metrics. The goal is to uncover insights that can drive business decisions and develop predictive models for forecasting sales.  

---

## Dataset Overview  

The dataset includes the following columns:  

| Column Name            | Values                | Description                                                                 |
|------------------------|-----------------------|-----------------------------------------------------------------------------|
| `Category`             | Text                 | Product category (e.g., Office Supplies, Technology, Furniture).           |
| `City`                 | Text                 | Customer city.                                                             |
| `Country`              | Text                 | Customer country.                                                          |
| `Customer.ID`          | Text                 | Unique identifier for customers.                                           |
| `Discount`             | 0 to 1               | Discount percentage applied to the sale.                                   |
| `Market`               | Text                 | Geographical market of the sale.                                           |
| `Profit`               | Float                | Profit generated from the sale.                                            |
| `Quantity`             | Positive Integer     | Quantity of items purchased.                                               |
| `Region`               | Text                 | Geographical region of the sale.                                           |
| `Sales`                | Positive Float       | Total revenue from the sale.                                               |
| `Shipping.Cost`        | Float                | Cost incurred for shipping the product.                                    |
| `Segment`              | Text                 | Customer segment (e.g., Consumer, Corporate, Home Office).                 |

---

## Project Steps  

1. **Data Exploration and Cleaning**  
   - Checked dataset structure, missing values, and duplicate rows.  
   - Cleaned categorical values by removing leading spaces and special characters.  
   - Encoded categorical variables using label encoding and standardized numerical features.  

2. **Exploratory Data Analysis (EDA)**  
   - **Univariate Analysis**: Explored the distribution of `Sales`, `Profit`, and `Discount` using histograms and boxplots.  
   - **Bivariate Analysis**: Examined relationships between `Sales` and `Profit`, and the impact of `Discount` on `Profit`.  
   - **Correlation Heatmap**: Visualized relationships between numerical variables to identify key drivers of sales and profit.  

3. **Model Building**  
   - Developed a **Linear Regression** model to predict `Sales`.  
   - Engineered new features, such as sales-to-shipping-cost ratio, to enhance model accuracy.  
   - Split the data into training and testing sets (80-20 split).  

4. **Evaluation**  
   - Evaluated the Linear Regression model using:  
     - **Mean Squared Error (MSE)**: `0.3799`  
     - **R-squared (R²)**: `0.6735`  
   - Analyzed the model coefficients to interpret the impact of features on sales.  

---

## Tools and Technologies  

- **Programming Language**: Python  
- **Libraries**:  
  - Data Analysis: `pandas`, `NumPy`  
  - Visualization: `matplotlib`, `seaborn`  
  - Machine Learning: `scikit-learn`  

---

## Results and Insights  

- **Sales Analysis**:  
  - High discounts correlate with reduced profit margins, indicating a need for optimized pricing strategies.  
  - Certain customer segments (e.g., Corporate) and regions (e.g., Central) generate higher sales.  

- **Model Performance**:  
  - The Linear Regression model explained ~67.35% of the variance in sales.  
  - Key predictors of sales included `Quantity`, `Region`, and `Shipping Cost`.  

- **Visualization Highlights**:  
  - The heatmap revealed strong correlations between sales and profit but weak correlations with discount rates.  
  - Scatterplots highlighted non-linear relationships between key variables, such as `Profit` and `Quantity`.  

---

## Future Work  

- Experiment with advanced machine learning models (e.g., Random Forest or XGBoost) for better predictions.  
- Conduct segmentation analysis to identify high-value customers.  
- Explore time-series forecasting to predict future sales trends.  

---
