
# Project 2: Ames Housing Data and Kaggle Challenge

## Problem Statement

Estimate the value of a property is always a challenge as the buyer would like to buy a lower possible price while seller would like to sell at the highest possible price. As such, the company would require to establish a reliable property price estimate to help their agents

## Executive Summary

### Contents:
- Exploratory Data Analysis
   - Missing Data
- Data Cleaning
   - Filling the missing value
   - Creating Feature
- Exploratory Visualization
   - Multi-collinearity
   - Correlation between numeric data and saleprice
   - Correlation between categorical data and saleprice
- Pre - Processing
   - One-Hot Encode
   - Train/Test Split
   - Scale
- Modeling
   - Linear Regression
   - Lasso
   - Ridge
   - Model Fitting and Evaluation
   - Kaggle Scoring
- Conclusions and Recommendations

## Data Dictionary

|Feature|Description|
|---|---|
|SalePrice|the property’s sale price in dollars. This is the target variable that you’re trying to predict.
|MSSubClass|The building class
|MSZoning|The general zoning classification
|LotFrontage|Linear feet of street connected to property
|LotArea|Lot size in square feet
|Street|Type of road access
|Alley|Type of alley access
|LotShape|General shape of property
|LandContour|Flatness of the property
|Utilities|Type of utilities available
|LotConfig|Lot configuration
|LandSlope|Slope of property
|Neighborhood|Physical locations within Ames city limits
|Condition1|Proximity to main road or railroad
|Condition2|Proximity to main road or railroad (if a second is present)
|BldgType|Type of dwelling
|HouseStyle|Style of dwelling
|OverallQual|Overall material and finish quality
|OverallCond|Overall condition rating
|YearBuilt|Original construction date
|YearRemodAdd|Remodel date
|RoofStyle|Type of roof
|RoofMatl|Roof material
|Exterior1st|Exterior covering on house
|Exterior2nd|Exterior covering on house (if more than one material)
|MasVnrType|Masonry veneer type
|MasVnrArea|Masonry veneer area in square feet
|ExterQual|Exterior material quality
|ExterCond|Present condition of the material on the exterior
|Foundation|Type of foundation
|BsmtQual|Height of the basement
|BsmtCond|General condition of the basement
|BsmtExposure|Walkout or garden level basement walls
|BsmtFinType1|Quality of basement finished area
|BsmtFinSF1|Type 1 finished square feet
|BsmtFinType2|Quality of second finished area (if present)
|BsmtFinSF2|Type 2 finished square feet
|BsmtUnfSF|Unfinished square feet of basement area
|TotalBsmtSF|Total square feet of basement area
|Heating|Type of heating
|HeatingQC|Heating quality and condition
|CentralAir|Central air conditioning
|Electrical|Electrical system
|1stFlrSF|First Floor square feet
|2ndFlrSF|Second floor square feet
|LowQualFinSF|Low quality finished square feet (all floors)
|GrLivArea|Above grade (ground) living area square feet
|BsmtFullBath|Basement full bathrooms
|BsmtHalfBath|Basement half bathrooms
|FullBath|Full bathrooms above grade
|HalfBath|Half baths above grade
|Bedroom|Number of bedrooms above basement level
|Kitchen|Number of kitchens
|KitchenQual|Kitchen quality
|TotRmsAbvGrd|Total rooms above grade (does not include bathrooms)
|Functional|Home functionality rating
|Fireplaces|Number of fireplaces
|FireplaceQu|Fireplace quality
|GarageType|Garage location
|GarageYrBlt|Year garage was built
|GarageFinish|Interior finish of the garage
|GarageCars|Size of garage in car capacity
|GarageArea|Size of garage in square feet
|GarageQual|Garage quality
|GarageCond|Garage condition
|PavedDrive|Paved driveway
|WoodDeckSF|Wood deck area in square feet
|OpenPorchSF|Open porch area in square feet
|EnclosedPorch|Enclosed porch area in square feet
|3SsnPorch|Three season porch area in square feet
|ScreenPorch|Screen porch area in square feet
|PoolArea|Pool area in square feet
|PoolQC|Pool quality
|Fence|Fence quality
|MiscFeature|Miscellaneous feature not covered in other categories
|MiscVal|$Value of miscellaneous feature
|MoSold|Month Sold
|YrSold|Year Sold
|SaleType|Type of sale
|SaleCondition|Condition of sale
|Total_SF|Total Sqft of the house
|Age|Age of the house when sold
|Mod_Age|Age of the modification / addional work when sold

## Conclusions and Recommendations

### Conclusion:
The total Sqft create the the most impact on the selling prices of the houses, followed by the overall quality. It also appears that the neighborhood the house is in may give it a premium in terms of sales price. We can also see that Age of the house, quality of the houses' external material, the quality of the kitchen, garage area are less significant but still important

Overall, the factors that the models says have an impact on its sales price are within expectations of observable reality. The model though, does give us a better sense of how important each factor is with respect to another. Lasso seem to work better then ridge for this feature selection.

The model is is now quite useful in giving the agents a rough estimate which they can give to their clients with the basis on the total floor area, overall conditions and neighborhood, garage area as a guideline. The agent can also let the clients knows that what are the other feature they can work on to use inorder to fetch a better price for their property.


### Recommendation
1. Grouping of the neighborhood into regions groups, similiar to out singapore context, the different district.
2. Further looking into the dataset and reduce more redundant features such as the ultilities, foundation, screen pouch, electricity.
3. Looking deeper identify and remove the outliers. 





