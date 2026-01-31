# Innomatics-internship-hackathon-2026
# Food Delivery Data Integration & Analytics Hackathon

## Project Overview
This project involves building an **ETL (Extract, Transform, Load) Pipeline** to integrate fragmented data from three different sources: Transactional CSV data, User Master JSON data, and Restaurant Master SQL data. 

The goal was to create a "Single Source of Truth" dataset to analyze order trends, user behavior, and business performance for a food delivery platform.

## Tech Stack
- **Language:** Python 3.12
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, SQLite3
- **Environment:** Jupyter Notebook

## Data Sources
1. **orders.csv**: Contains transactional details including `order_id`, `user_id`, `restaurant_id`, and `order_amount`.
2. **users.json**: Contains user demographics and `membership_type` (Gold vs. Regular).
3. **restaurants.sql**: A SQL script containing restaurant master data including `cuisine` and `city` information.

## Workflow & Implementation
- **Data Extraction**: Handled multi-format ingestion, including executing SQL scripts in an in-memory SQLite database to extract relational tables.
- **Data Cleaning**: Standardized ID keys, handled missing values (NaN), and corrected date-time formatting for accurate seasonality analysis.
- **Data Merging**: Performed a **Left Join** strategy to ensure 100% retention of transactional records while enriching them with user and restaurant metadata.
- **Visualization**: Generated 4 key analytical plots:
    - **Revenue by City**: Identifying high-value geographic markets.
    - **Membership Impact**: Analyzing the spending delta between Gold and Regular members.
    - **Seasonality Trends**: Identifying peak order months.
    - **Cuisine Distribution**: Mapping market share by food category.

## Key Insights
- Successfully generated the `final_food_delivery_dataset.csv`.
- Identified the top-performing city and cuisine type through automated data grouping.
- Quantified the impact of membership tiers on total revenue.

## How to Run
1. Clone the repository.
2. Ensure `orders.csv`, `users.json`, and `restaurants.sql` are in the root directory.
3. Run the Jupyter Notebook `Soham_Internship_Analysis.ipynb`.
