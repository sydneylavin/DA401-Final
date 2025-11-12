# DA401-Final
Author: Sydney Lavin
Date: 11/25
# Project Overview
This research investigates the relationship between wellness labeling, like organic, and the prices and marketing of food products (fruits and vegetables). Using real datasets for fruits and vegetables across the Midwest and Northeast, the analysis explores whether organic labeling preidcts higher prices and price premiums, as well as how marketing activity differs between organic and conventional products.
# Goals
See whether organic products have higher prices than conventional products
Test if the organic price premium has changed over time
# Sources
USDA Agricultural Marketing Service
# Data
Date range: 01-01-2020 to 01-01-2025
# Methods
1. Cleaning:
   Removed empty/irrelevant coulmns
   Converted date columns to datetime format
   Standardized numeric columns for price and ad count
   Created binary variables for is_organic (1 = organic, 0 = non-organic)
   Filtered for consistent units (“per lb”)
2. Analysis
   Grouped prices by date and label to calculate average prices over time.
   Calculated organic price premiums (%) using an average
   Conducted OLS regression of price premium on time (organic_premium_pct ~ time_index)
