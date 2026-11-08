Booze ‘R’ Us: Iowa Liquor Demand Model

IOWA Alcohol Prediction Project · Author: Alexander Jung

Overview

This project models liquor purchases per capita to help the client decide how to stock existing stores, which products to promote, and where to expand. It is a guide to demand by location, not a sales forecast.

Data Sources
Iowa state alcohol sales data (2012 to present): every store purchase, including city, county, transaction date, alcohol category, sale dollars, liters sold, and price per liter.
U.S. Census Bureau data: population (aged 16+) and American Community Survey DP03 economic characteristics.
Privacy exclusions: health insurance, poverty-level income, and children-by-age family demographics were removed for privacy and integrity reasons.

Methodology
Target: liters sold per capita (total liters ÷ population aged 16+).
Model: ridge regression, which shrinks the least important coefficients toward zero. It started with 74 predictors, and highly correlated ones were then dropped.
Two models:
Grouped by city, year, and category
Grouped by county, year, and category
Evaluation: cross-validation, with a residual plot to check fit.

Limitations
The model estimates liters per capita. It does not predict sales or store profit.
Higher predicted liters per capita supports expansion and lower values argue against it, but neither guarantees profitability.
