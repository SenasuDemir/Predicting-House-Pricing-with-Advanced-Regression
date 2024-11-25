# Predicting-House-Pricing-with-Advanced-Regression
This project aims to predict the sale prices of properties in Ames, Iowa, using various features such as lot size, house style, and neighborhood information. We developed and tested multiple regression models and evaluated their performance to identify the best-performing model.

---

## Data Description

The dataset includes the following fields:

### Target Variable:
- **`SalePrice`**: The property's sale price in dollars. This is the variable we aim to predict.

### Features:
- **`MSSubClass`**: The building class  
- **`MSZoning`**: The general zoning classification  
- **`LotFrontage`**: Linear feet of street connected to the property  
- **`LotArea`**: Lot size in square feet  
- **`Street`**: Type of road access  
- **`Alley`**: Type of alley access  
- **`LotShape`**: General shape of property  
- **`LandContour`**: Flatness of the property  
- **`Utilities`**: Type of utilities available  
- **`LotConfig`**: Lot configuration  
- **`LandSlope`**: Slope of property  
- **`Neighborhood`**: Physical locations within Ames city limits  
- **`Condition1`**: Proximity to main road or railroad  
- **`Condition2`**: Proximity to main road or railroad (if a second is present)  
- **`BldgType`**: Type of dwelling  
- **`HouseStyle`**: Style of dwelling  
- **`OverallQual`**: Overall material and finish quality  
- **`OverallCond`**: Overall condition rating  
- **`YearBuilt`**: Original construction date  
- **`YearRemodAdd`**: Remodel date  
- **`RoofStyle`**: Type of roof  
- **`RoofMatl`**: Roof material  
- **`Exterior1st`**: Exterior covering on house  
- **`Exterior2nd`**: Exterior covering on house (if more than one material)  
- **`MasVnrType`**: Masonry veneer type  
- **`MasVnrArea`**: Masonry veneer area in square feet  
- **`ExterQual`**: Exterior material quality  
- **`ExterCond`**: Present condition of the material on the exterior  
- **`Foundation`**: Type of foundation  
- **`BsmtQual`**: Height of the basement  
- **`BsmtCond`**: General condition of the basement  
- **`BsmtExposure`**: Walkout or garden level basement walls  
- **`BsmtFinType1`**: Quality of basement finished area  
- **`BsmtFinSF1`**: Type 1 finished square feet  
- **`BsmtFinType2`**: Quality of second finished area (if present)  
- **`BsmtFinSF2`**: Type 2 finished square feet  
- **`BsmtUnfSF`**: Unfinished square feet of basement area  
- **`TotalBsmtSF`**: Total square feet of basement area  
- **`Heating`**: Type of heating  
- **`HeatingQC`**: Heating quality and condition  
- **`CentralAir`**: Central air conditioning  
- **`Electrical`**: Electrical system  
- **`1stFlrSF`**: First-floor square feet  
- **`2ndFlrSF`**: Second-floor square feet  
- **`LowQualFinSF`**: Low-quality finished square feet (all floors)  
- **`GrLivArea`**: Above-grade (ground) living area square feet  
- **`BsmtFullBath`**: Basement full bathrooms  
- **`BsmtHalfBath`**: Basement half bathrooms  
- **`FullBath`**: Full bathrooms above grade  
- **`HalfBath`**: Half baths above grade  
- **`Bedroom`**: Number of bedrooms above basement level  
- **`Kitchen`**: Number of kitchens  
- **`KitchenQual`**: Kitchen quality  
- **`TotRmsAbvGrd`**: Total rooms above grade (does not include bathrooms)  
- **`Functional`**: Home functionality rating  
- **`Fireplaces`**: Number of fireplaces  
- **`FireplaceQu`**: Fireplace quality  
- **`GarageType`**: Garage location  
- **`GarageYrBlt`**: Year garage was built  
- **`GarageFinish`**: Interior finish of the garage  
- **`GarageCars`**: Size of garage in car capacity  
- **`GarageArea`**: Size of garage in square feet  
- **`GarageQual`**: Garage quality  
- **`GarageCond`**: Garage condition  
- **`PavedDrive`**: Paved driveway  
- **`WoodDeckSF`**: Wood deck area in square feet  
- **`OpenPorchSF`**: Open porch area in square feet  
- **`EnclosedPorch`**: Enclosed porch area in square feet  
- **`3SsnPorch`**: Three-season porch area in square feet  
- **`ScreenPorch`**: Screen porch area in square feet  
- **`PoolArea`**: Pool area in square feet  
- **`PoolQC`**: Pool quality  
- **`Fence`**: Fence quality  
- **`MiscFeature`**: Miscellaneous feature not covered in other categories  
- **`MiscVal`**: $Value of miscellaneous feature  
- **`MoSold`**: Month sold  
- **`YrSold`**: Year sold  
- **`SaleType`**: Type of sale  
- **`SaleCondition`**: Condition of sale  

---

## Goals

### Data Preparation:
1. Handle missing values.
2. Process categorical and numeric variables.
3. Rank and engineer features.
4. Analyze feature correlation.
5. Select the best variables.

### Modeling:
1. Combine training and test data.
2. Clean and impute missing values.
3. Split the training data for validation.
4. Train models and evaluate their performance.
5. Use advanced regressors like Gradient Boosting and Random Forest.
6. Measure performance using metrics such as:
   - **Mean Absolute Error (MAE)**
   - **Root Mean Squared Error (RMSE)**
   - **R-Squared (R²)**

---

## Model Performance

| **Model**               | **R²**    | **RMSE**      | **MAE**        |
|--------------------------|-----------|---------------|----------------|
| **XGBRegressor**         | 0.9042    | 27,105.41     | 17,504.63      |
| **Gradient Boosting**    | 0.8910    | 28,908.89     | 18,946.75      |
| **Random Forest**        | 0.8273    | 36,391.49     | 23,526.96      |
| **ElasticNet**           | 0.8154    | 37,624.40     | 22,753.24      |
| **Ridge**                | 0.8111    | 38,061.58     | 23,629.58      |
| **Lasso**                | 0.8104    | 38,138.66     | 23,673.37      |
| **Linear Regression**    | 0.8103    | 38,144.69     | 23,672.53      |
| **Decision Tree**        | 0.7773    | 41,325.74     | 26,228.77      |
| **Extra Tree**           | 0.7525    | 43,571.96     | 27,807.57      |
| **KNeighbors**           | 0.6919    | 48,616.54     | 28,548.24      |

### Best Performing Model: **XGBRegressor**
- **R²**: 0.9042  
- **RMSE**: $27,105.41  
- **MAE**: $17,504.63  

---

## Observations

- **High Accuracy**: The XGBRegressor model explains 90.42% of the variance in sale prices.  
- **Outliers**: A few data points deviate significantly from predictions, potentially due to unusual property characteristics or data noise.  
- **General Trend**: The model captures the overall trend in housing prices effectively.

---

## Conclusion

This project demonstrates the application of machine learning models to predict house prices accurately. The best-performing model, XGBRegressor, is a strong candidate for real-world use in predicting housing prices. Further feature engineering and exploration of outliers could further improve model performance.
