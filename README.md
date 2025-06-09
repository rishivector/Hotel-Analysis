# Hotel Revenue Analysis Dashboard

## Project Overview

This project presents a comprehensive analysis of hotel booking data from January 2018 to September 2020. The primary objective is to uncover revenue trends, compare the performance of different hotel types (City vs. Resort), and identify key business drivers.

The final output is an interactive dashboard created in Power BI, which provides a high-level overview of key metrics and allows for a deeper dive into yearly and seasonal performance.

## Tools Used

*   **SQL:** For data cleaning, transformation, and aggregation.
*   **Microsoft Power BI:** For data modeling, analysis, and interactive visualization.

## Methodology

### 1. Data Preparation (SQL)

The raw data was distributed across multiple tables, one for each year (2018, 2019, 2020). The following steps were performed in SQL to create a unified, analysis-ready dataset:

*   **Data Consolidation:** Used `UNION ALL` to combine the three yearly tables into a single master table.
*   **Data Enrichment:** Employed `LEFT JOIN` to integrate supplementary data from `market_segment` and `meal_cost` tables. This added valuable context to the main booking data.
*   **Revenue Calculation:** The core `revenue` metric was calculated using the formula: `(stays_in_weekend_nights + stays_in_week_nights) * adr`.

### 2. Dashboard Development (Power BI)

The consolidated dataset from SQL was imported into Power BI. The dashboard was designed to answer key business questions at a glance:

*   **KPI Cards:** Displaying top-level metrics such as Total Revenue, Average Daily Rate (ADR), Total Nights Booked, and Average Discount.
*   **Time-Series Analysis:** A line chart visualizes daily revenue trends, segmented by hotel type, to highlight seasonality and performance over time.
*   **Revenue Breakdown:** A donut chart and a detailed matrix table break down the total revenue by hotel type and year, providing a clear comparison of performance.

## Key Insights & Findings

The dashboard reveals several important insights into the hotel's performance:

*   **Overall Revenue:** The hotels generated a total revenue of **₹12.32 Million** between Jan 2018 and Sep 2020.
*   **Top Performing Hotel Type:** **City Hotels** are the main source of revenue, contributing **₹7.16M (58.1%)** compared to Resort Hotels' ₹5.16M (41.9%).
*   **Year-over-Year Performance:**
    *   **2019** was the most profitable year, with revenues reaching **₹6.69 Million**.
    *   A significant downturn is visible in **2020**, with revenue at ₹3.96M up to September, likely impacted by external factors and the partial data for the year.
*   **Seasonal Trends:** The revenue line chart clearly indicates seasonal peaks, with revenue consistently rising during the summer months each year.
*   **Customer Metrics:** The average daily rate (ADR) across all bookings was **₹99.71**.

## How to Use

To reproduce this analysis, you would need:
1.  The raw dataset files (for 2018, 2019, 2020, market segment, and meal cost).
2.  A SQL environment to run the data preparation script.
3.  Power BI Desktop to build and interact with the dashboard.
