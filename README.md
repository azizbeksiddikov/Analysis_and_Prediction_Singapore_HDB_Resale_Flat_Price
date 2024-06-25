# Analysis and Prediction of Singapore HDB Resale Flat Prices (2017-2024)

## Links:
Dataset:
Dataset: https://www.kaggle.com/datasets/darrylljk/singapore-hdb-resale-flat-prices-2017-2024
Report: https://docs.google.com/document/d/1GRqU_-iOh1_YoJD_mTOsACidcd0zvV1mMWc6pY8Xfk8/edit?usp=sharing
Tableau: https://public.tableau.com/views/SingaporeHDBResaleFlatPrices/Dashboard1?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link

## Objective
The main goal of this project is to analyze the resale prices of HDB flats in Singapore from January 2017 to June 2024 and build predictive models to estimate future resale prices based on various features.

## Data Description
The dataset contains detailed information on HDB flat resale transactions, including:
- **Month**: Month of sale
- **Town**: Designated residential area
- **Flat type**: Classification by room size
- **Block**: Block number of the flat
- **Street name**: Street name of the flat
- **Storey range**: Estimated range of floors
- **Floor area (sqm)**: Total interior space in square meters
- **Flat model**: Classification by generation
- **Lease commence date**: Start date of the lease
- **Remaining lease**: Remaining time on the lease
- **Resale price**: Cost of the flat sold

## Data Preprocessing
1. **Handling Missing Values**:
   - There were no missing values in the dataset.
2. **Deleting Duplicate Values**:
   - Removed duplicate entries to ensure data integrity and accuracy.
3. **Encoding Categorical Variables**:
   - `flat_type` and `storey_range` were ordinal encoded based on their natural order.
   - `flat_model` was one-hot encoded to handle categorical data without imposing any ordinal relationship.
4. **Feature Engineering**:
   - Extracted `flat_age` from the `lease_commence_date` and current year.
   - Converted `remaining_lease` to numeric format for better model compatibility.

## Exploratory Data Analysis (EDA)
1. **Trends Over Time**:
   - Analyzed resale price trends over the months and years.
   - Observed seasonal trends and price fluctuations.
2. **Distribution Analysis**:
   - Analyzed the distribution of flat prices based on different flat types, towns, and storey ranges.
   - Visualized the relationship between floor area and resale price.
3. **Price by Town**:
   - Displayed a bar chart of average resale prices by town.
4. **Price by Flat Type**:
   - Displayed a bar chart of average resale prices by flat type.

## Model Building and Evaluation
Several regression models were used to predict the resale price:
- Polynomial Regression
- Neural Network
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor

### Evaluation Metrics:
- **MAE (Mean Absolute Error)**: Average of absolute differences between predicted and actual values.
- **RMSE (Root Mean Squared Error)**: Square root of the average of squared differences between predicted and actual values.
- **R² (Coefficient of Determination)**: Proportion of variance in the dependent variable that is predictable from the independent variables.

### Model Performance:

| Model                  | MAE      | RMSE     | R²   |
|------------------------|----------|----------|------|
| Polynomial Regression  | 69549.3  | 91689.5  | 0.72 |
| Neural Network         | 83575.0  | 106484.6 | 0.63 |
| Decision Tree          | 38713.0  | 55757.8  | 0.90 |
| Random Forest          | 35900.5  | 51043.3  | 0.91 |
| Gradient Boosting      | 48223.0  | 63155.3  | 0.87 |
| XGBoost                | 48072.7  | 62809.6  | 0.87 |

## Feature Importance
The following chart shows the top 5 most important features affecting HDB resale prices based on the Random Forest model.

## Key Insights
1. **Trends**:
   - Observed an overall increase in resale prices over the analyzed period.
   - Significant price fluctuations during certain months due to market conditions.
2. **Model Performance**:
   - Random Forest and Decision Tree models performed the best with high R² values, indicating strong predictive power.
   - Polynomial Regression and Neural Network models were less accurate.
3. **Feature Importance**:
   - Floor area, flat type, and remaining lease were the most influential features affecting resale prices.

## Conclusion
1. **Summary**:
   - The analysis provided insights into trends and factors affecting HDB resale prices.
   - Various predictive models were built and evaluated for their accuracy.
2. **Future Work**:
   - Incorporate additional data such as economic indicators or proximity to amenities to improve predictions.
   - Explore more advanced machine learning models for better accuracy.
3. **Applications**:
   - The insights and predictions can assist policymakers, real estate agents, and buyers in making informed decisions.

