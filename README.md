# Time Series Sales Forecast for Walmart

## Table of Contents
1. [Introduction](#introduction)
2. [Objective](#objective)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [Model Training and Evaluation](#model-training-and-evaluation)
7. [Results](#results)
8. [Insights](#insights)
9. [Usage](#usage)
10. [Contributing](#contributing)
11. [License](#license)

## Introduction
Accurate sales forecasting is crucial for Walmart to optimize inventory management, staffing, and marketing strategies. This project focuses on developing a time series forecasting model to predict future sales based on historical sales data.

## Objective
To build a time series forecasting model that predicts future sales for Walmart stores based on historical sales data, enabling better inventory and operational planning.

## Dataset
The dataset contains historical sales data for Walmart stores. Key features include:
- `Store`: Unique identifier for each store.
- `Dept`: Department within the store.
- `Date`: The date of the weekly sales record.
- `Weekly_Sales`: Sales amount for the week.
- `IsHoliday`: Whether the week includes a holiday.

## Methodology
1. **Data Cleaning**:
   - Remove or impute missing values in sales data.
   - Drop unnecessary columns that do not contribute to the forecasting model.
   - Convert date columns to datetime format.
   - Ensure the data is aggregated at the correct time intervals (e.g., weekly).

2. **Exploratory Data Analysis (EDA)**:
   - Analyze historical sales trends and seasonality.
   - Visualize sales patterns and identify potential anomalies.
   - Explore relationships between sales and holidays.

3. **Data Preprocessing**:
   - Aggregate sales data at the required time frequency (e.g., weekly).
   - Encode categorical variables (e.g., `Store`, `Dept`) if needed.
   - Normalize or scale features if required.

4. **Model Selection and Training**:
   - Evaluate various Machine Learning regression models (RandomForest, ExtraTrees, XGBoost, Catboost, HistGradientBoosting )
   - Use cross-validation techniques to select the best model based on performance metrics.

5. **Model Evaluation**:
   - Assess the model using metrics such as Weighted Mean Absolute Error (WMAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).
   - Validate the model on a holdout dataset to ensure its accuracy and robustness.

## Exploratory Data Analysis (EDA)
- Visualization of historical sales data to understand trends and seasonality.
- Analysis of sales patterns related to holidays and special events.
- Identification of anomalies or irregularities in sales data.
  
   

## Model Training and Evaluation
- Comparison of different forecasting models.
- Evaluation using performance metrics such as WMAE, MSE, and RMSE.
- Selection of the best model based on forecasting accuracy.

## Results
- Summary of the model's forecasting performance.
- Key metrics such as WMAE, MSE, and RMSE.
- Forecasted sales for future periods.

## Insights

The following visualizations illustrate key findings and trends from the analysis:

  ### Visualizations
  *Figure 1: Average sales for each department.*
   ![Average Sales for Each Department](TSSF%20Walmart/Untitled%20Folder/assets/avg_dept_sales.png)

  *Figure 2: Top 20 selling departments during holidays, with non-holiday comparison.*
  ![Top 20 Selling Departments During Holidays](TSSF%20Walmart/Untitled%20Folder/assets/top20_departments_holidays.png)
  
  
  *Figure 3: Correlation of features with each other and the target variable.*
   ![Correlation of Features](TSSF%20Walmart/Untitled%20Folder/assets/fts_corr.png)
   


  *Figure 4: Sales trend over time (2010-2012).*
   ![Sales Trend Over Time](TSSF%20Walmart/Untitled%20Folder/assets/sales_trend.png)


  *Figure 5: Sales trend for 2011.*
   ![Sales Trend for 2011](TSSF%20Walmart/Untitled%20Folder/assets/sales_trend_2011.png)
  


*Figure 6: Sales trend for each store type (A, B, C).*
   ![Sales Trend for Each Store Type](TSSF%20Walmart/Untitled%20Folder/assets/sales_trend_by_sType.png)
   


*Figure 7: Distribution of Weekly Sales for each store type (A, B, C).*
   ![Distribution of Weekly Sales for each Store Type](TSSF%20Walmart/Untitled%20Folder/assets/dist_of_weekly_sales_byType.png)


These insights help in understanding the sales patterns and trends, which are crucial for accurate sales forecasting and operational planning.

## Usage
1. Clone the repository:
    ```bash
    git clone https://github.com/Kimo2111/WalmartSalesForecast.git
    ```
2. Install the necessary dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the data cleaning and preprocessing script:
    ```bash
    python preprocess_data.py
    ```
4. Train the forecasting model:
    ```bash
    python train_model.py
    ```
5. Evaluate the model:
    ```bash
    python evaluate_model.py
    ```

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
