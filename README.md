# Retail-Price-Optimization

## Problem Statement

In competitive retail markets, pricing decisions have a direct impact on sales volume, profitability, and market share. Setting prices too high risks losing customers to competitors, while pricing too low can erode profit margins. Businesses often lack a data-driven method to balance these trade-offs and identify the optimal price point for maximizing profit.
This project addresses that challenge by building a machine learning–driven price optimization framework that analyzes historical sales, competitor pricing, and seasonal demand patterns to recommend optimal pricing strategies.

## Project Overview

This project focuses on **predicting product sales quantities and identifying profit-maximizing prices** using historical retail transaction data enriched with competitor price and logistics cost information.
The workflow includes data exploration & cleaning, feature engineering – creating metrics like *profit, profit margin, and price gaps vs. competitors*; extracting seasonal patterns (month, quarter, year).

The model training is done using **XGBoost regression** with **GridSearchCV** for hyperparameter tuning to accurately forecast sales quantity. Scenario Simulation is implemented using “what-if” pricing simulations to evaluate the impact of different price points on both quantity sold and profit.

*Price Sensitivity Analysis* can be done for ant specific values by generating price–profit curves to visually identify optimal price ranges.

The Power BI dashboard is also visualized used for showing key KPIs, category-wise performance, price–profit relationships, and seasonal sales trends for decision-making.

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost – Regression modeling for demand prediction
- GridSearchCV – Hyperparameter tuning to optimize model performance
- Power BI, Matplotlib/Seaborn
  
## Dataset Description

The dataset used in this project contains historical *transactional sales* data enriched with competitor pricing and logistical cost information.
Each row represents a single transaction for a specific product, along with details about pricing, category, and timing.

Key Columns
- product_category_name — Name of the product category (e.g., "computers_accessories", "furniture_decor").
- unit_price — Our selling price per unit for the product.
- comp_1, comp_2, comp_3 — Prices offered by three different competitors for the same or similar products.
- freight_price — Cost of shipping the product to the customer.
- qty — Quantity of items sold in the transaction.
- date — Transaction date, later used to extract month, year, and quarter for seasonal analysis.

Additional columns such as revenue, profit, margin and price gaps were engineered to improve model inputs and interpretability.

## Conclusion and Insights

This project successfully demonstrated how data-driven pricing strategies can significantly improve profitability while maintaining competitive market positioning. By analysing historical sales, competitor pricing, freight costs, and seasonal trends, the model was able to:

- Accurately forecast product demand under different pricing scenarios using XGBoost regression.
- Identify optimal price ranges for maximizing profit without sacrificing sales volume.
- Quantify the impact of competitor pricing, confirming that competitive dynamics are a major driver of customer purchasing behavior.
- Highlight the importance of seasonality, with certain categories showing predictable peaks and troughs in demand.

# Key Business Insights:

- Optimal Pricing Window – For many categories, profit peaked at higher-than-current price levels, indicating potential to increase margins without major volume loss.
- Competitor Sensitivity – Products with closer substitutes were more sensitive to competitor price changes, requiring more agile pricing strategies.
- Seasonal Opportunities – Certain categories could benefit from targeted promotions during low-demand months to smooth revenue fluctuations.
