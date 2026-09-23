# Olist E-Commerce: What Drives Customer Satisfaction?

A data cleaning and analysis project on the Olist Brazilian e-commerce dataset, exploring which factors most affect customer satisfaction (review scores) to help the company improve the customer experience.

**Tools:** Python (pandas) in Google Colab · Tableau
**Data:** ~100,000 orders (2016-2018) across 9 relational tables

---

## Business Task
Analyze the Olist Brazilian e-commerce dataset to identify which factors drive customer satisfaction (review scores), helping the company reduce negative reviews and improve the customer experience.

## The Data
- **Source:** [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle)
- **Scope:** ~100,000 orders, split across 9 related tables (orders, reviews, items, products, customers, and more)

## Data Cleaning (Python / pandas)
This project focused heavily on real-world data cleaning:
- Handled missing values differently based on context: filled empty review comments (145k+ nulls) instead of dropping rows, since the review score was intact.
- Filtered to delivered orders only, since undelivered orders have no delivery time to analyze.
- Removed a small number of orders marked "delivered" but missing a delivery date (data inconsistency).
- Converted date columns from text to datetime and engineered new features (delivery time in days, delivery vs. promised date).
- Merged multiple tables (orders, reviews, items, products, category translation) to build a single analysis table.
- Summarized multi-item orders to one row per order.

## Key Findings

**1. Delivery time is the strongest driver of satisfaction.**
Average delivery time drops steadily as review scores rise: 20.8 days (1 star) down to 10.2 days (5 stars). Review scores collapse once delivery passes ~15 days.

**2. Beating the delivery estimate matters, not just speed.**
5-star orders arrived ~13 days ahead of the promised date, versus ~4 days early for 1-star orders.

**3. Shipping cost affects satisfaction; product price does not.**
Higher freight costs are linked to worse reviews. Product price showed no consistent pattern.

**4. Product category matters.**
Simple, easy-to-ship items rate highest (books 4.54, food & drink 4.45). Large or complex items rate lowest (office furniture 3.65, audio 3.84).

## Recommendation
Olist should prioritize delivery speed above all, keeping deliveries under 15 days and continuing to beat delivery estimates. Quality and logistics improvements should focus on low-rated, high-volume categories like office furniture and bed_bath_table.

## Dashboard
🔗 **[View the interactive dashboard on Tableau Public](https://public.tableau.com/app/profile/samuel.alfaro/viz/OlistCustomerSatisfactionAnalysis_17901450913680/Dashboard1)**

## Files in this repo
- `Olist_Customer_Satisfaction.ipynb` — full Python notebook (data cleaning + analysis)

---
*Built by Samuel Alfaro Ramirez — aspiring Data Analyst focused on business and e-commerce analytics.*
