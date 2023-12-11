# kaggle-predict-sales
- Ranked first 7% in Kaggle Competition
## Sales Prediction using XGBoost Algorithm

### Team Members
- **彭晴 (Peng Qing)**
  - School of Statistics, Southwest University of Finance and Economics
  - Class of 2018, Major: Economic Statistics
  - Student ID: 41809024

- **申鸿雨 (Shen Hongyu)**
  - School of Statistics, Southwest University of Finance and Economics
  - Class of 2018, Major: Economic Statistics
  - Student ID: 41809021

### Abstract
Mining rich semantic information hidden in heterogeneous information networks is a crucial task in data mining. This project focuses on predicting monthly sales for each product in every store of a Russian e-commerce company, 1C, using XGBoost algorithm. The provided dataset spans from January 2013 to October 2015, encompassing daily sales data, item information, shop details, and more.

### Key Words
- Sales Prediction
- Clustering
- XGBoost

### 1. Overview
#### 1.1 Problem Statement
The competition involves predicting the monthly sales of each product in every store for the next month based on daily sales data provided by 1C, a Russian e-commerce company.

#### 1.2 Significance
Accurate predictions can assist e-commerce platforms in preparing inventory, implementing targeted marketing strategies, and maximizing profit margins. Our model, achieved through data preprocessing and XGBoost model construction, secured a top 7% position among 10,000+ teams.

#### 1.3 Approach
- Data preprocessing involved handling outliers, merging duplicate categories, and extracting features from shop names.
- Features were fused, and the daily sales data were transformed into monthly data.
- Extensive feature engineering included lagging monthly sales, revenue changes, and average item sales.
- XGBoost, chosen for its efficiency and robustness, served as the predictive model.

### 2. Data Overview
#### 2.1 Data Description
1. **item_categories.csv**
   - Item_category_name
   - Item_category_id

2. **item.csv**
   - Item_name
   - Item_id
   - Item_category_id

3. **salestrain.csv**
   - Date
   - Date_block_num
   - Shop_id
   - Item_id
   - Item_price
   - Item_cnt_day

4. **shopname.csv**
   - Shop_name
   - Shop_id

#### 2.2 Data Preprocessing
1. **Outlier Removal:** Eliminated outliers with item_cnt_day > 800 and item_price > 3000.
2. **Duplicate Category Merging:** Merged duplicate shop names with minor differences.
3. **Feature Extraction:** Extracted "City" and "Category" features from shop names.

### 3. Feature Fusion
Transformed daily sales data into monthly data and introduced lagged features to capture historical trends. Feature importance analysis revealed the significance of historical price changes.

### 4. Model Tuning
#### 4.1 Model Introduction
XGBoost, an ensemble algorithm, was chosen for its robustness and efficiency.

#### 4.2 Core Concept
XGBoost builds multiple decision trees to form a powerful predictive model. Parameters such as `n_estimators`, `early_stopping_rounds`, `max_depth`, `min_child_weight`, and `learning_rate` were adjusted to enhance accuracy and prevent overfitting.

#### 4.3 Model Construction
The objective function of XGBoost, considering regularization terms, was optimized to minimize the difference between predicted and actual values.

### 5. Parameter Adjustment
Manual tuning involved adjusting parameters based on a series of experiments with validation sets. Key parameters adjusted include `n_estimators`, `early_stopping_rounds`, `learning_rate`, `max_depth`, and `min_child_weight`.

### 6. Reflection
#### 6.1 Shortcomings
- Limited experiment trials due to manual tuning and platform constraints.
- Lack of efficiency in parameter adjustment strategy.

#### 6.2 Improvements
- Consider grid search for more systematic parameter tuning.
- Increase the number of experiment trials for better accuracy.

---

Feel free to check out our complete project and analysis in the provided Jupyter notebook and explore our journey in fine-tuning the XGBoost model for sales prediction!
