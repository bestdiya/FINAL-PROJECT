# FINAL-PROJECT

---

## Tools & Libraries Used

- **Python** (Pandas, NumPy)  
- **Matplotlib / Seaborn**  
- **Scikit-learn**  
- **XGBoost**  
- **LightGBM**  
- **Jupyter Notebook**  
- **Excel** (for final LTV review)  

---

## Step-by-Step Chronology

### Step 1: Data Preprocessing
- Loaded the [Kaggle Retail Dataset](https://www.kaggle.com/datasets/sergeymedvedev/customer_segmentation)  
- Removed nulls and invalid Customer IDs  
- Converted `InvoiceDate` to datetime  
- Filtered only positive quantities and prices  

### Step 2: RFM Feature Engineering
- **Recency**: Days since last purchase  
- **Frequency**: Number of unique invoices  
- **AOV**: Average order value  
- **LTV**: Sum of total spent per customer (target variable)  

### Step 3: Advanced Feature Engineering
- Added:  
  - **Customer Tenure**  
  - **Days Active**  
  - **Top 10 Product Category Purchases** using one-hot encoding  

### Step 4: Model Training
- Split dataset into training and testing  
- Trained:  
  - **XGBoost Regressor**  
  - **Random Forest Regressor**  
  - **LightGBM Regressor**  

### Step 5: Model Evaluation
- Evaluated using **MAE** and **RMSE**  
- Best model (XGBoost) improved from:  
  - MAE: `1174.90` → `503.48`  
  - RMSE: `6178.59` → `846.49`  

### Step 6: Visualization
- Bar plot comparing models by MAE & RMSE  
- Scatter plot of actual vs predicted LTV  

### Step 7: Final Output
- Exported customer-wise predicted LTV  
- Segmented customers into 4 LTV tiers for business targeting  

---

## Sample Output

| CustomerID | Recency | Frequency | AOV   | Predicted_LTV |
|------------|---------|-----------|-------|---------------|
| 12345      | 12      | 8         | 142.6 | 2104.52       |
| 67890      | 3       | 2         | 94.12 | 527.89        |

---

## Final Report
> Find the 2-page PDF in `LTV_Report.pdf`

---
