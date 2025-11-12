# DA401-Final
Author: Sydney Lavin
Date: 11/25
# Project Overview
This research investigates the relationship between wellness labeling, like organic, and the prices and marketing of food products (fruits and vegetables). Using real datasets for fruits and vegetables across the Midwest and Northeast, the analysis explores whether organic labeling preidcts higher prices and price premiums, as well as how marketing activity differs between organic and conventional products.
# Goals
See whether organic products have higher prices than conventional products
Test if the organic price premium has changed over time
# Project Structure
The repository is organized to keep data, code, figures, and results clear and reproducible.
Folder descriptions:
   - data: Contains all raw and cleaned datasets for analysis. These files are not modified by scripts.
   - experiments: Used for testing models, early regression checks, and exploratory data analysis.
   - figures: Stores all figures generated from the analysis (price trends, residuals, and ad count boxplots).
   - one_time_scripts: Holds scripts used for initial setup, data downloads, or file merging.
   - results: Contains regression outputs, summary statistics, and model coefficients.
   - utilities: Includes helper scripts and reusable functions for data cleaning, modeling, and plotting.
   - main.ipynb: Central analysis file combining data import, cleaning, regression modeling, and visualization.
   - README.md: The main documentation file summarizing the project, results, and structure.
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
   Used multiple linear regression (current_ad_count ~ is_organic + C(product_class) + C(region)) to predict ad counts.
   Visualized ad differences by label and product type using boxplots
# Results
1. Organic products consistently cost more than non-organic ones.
2. The organic price premium started around 39% and has slowly increased over time (about 0.005% per day).
3. The relationship is statistically significant but weak (R-squared = 0.017), suggesting other factors (like economy or demand) also affect prices.
4. Non-organic products receive significantly more ads than organic ones.
5. On average, organic items have about 214 fewer ads than comparable non-organic items.
6. Fruits have more ads than vegetables, and the Northeast region advertises slightly more than the Midwest.
7. The model’s R-squared = 0.061, meaning label, region, and product type explain about 6% of ad variation.
# Meaning
Organic products remain more expensive and are becoming slightly more so over time.
They receive less advertising, suggesting that higher prices are likely due to production costs or consumer willingness to pay rather than increased marketing efforts.
Price and advertising differences are real and statistically significant, but weakly explained by the variables studied, indicating that other market factors play major roles.
# Visuals
Figure 3: Average product prices over time
Figure 4: Scatterplot of residuals
Figure 5: Boxplot of advertisments
# Tools/Libraries
1. Python
2. Pandas - data work
3. Matplotlib - data visualization
4. Seaborn - data visualization
5. Statsmodels - analysis
# Conclusion
The analysis does not support the initial hypothesis that the price gap between organic and non-organic products would shrink over time. Instead, the premium is slowly increasing. Furthermore, organic products are advertised significantly less than non-organic ones, showing that organic price differences are not marketing driven, but more likely related to production costs, supply factors, or consumer demand.
