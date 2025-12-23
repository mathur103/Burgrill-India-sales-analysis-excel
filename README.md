-- Source: Raw transaction logs (invoice-level data)
-- Outlet: Rajouri, Delhi
-- Time Period: November 2025
-- Format: Excel export
-- Dataset: 
 - dashboard >a hreif-"https://github.com/mathur103/Burgrill-India-sales-analysis-excel/blob/main/Burgrill_India.xlsx"> datasetview</a>

# Key Fields Included

- Invoice Date & Time
- Gross Amount, Net Amount, Taxes, Discounts
- Order Source (Swiggy, Zomato, POS, etc.)
- Payment Mode
- Business Brand (Burgrill / The Sausage Fest)
- Customer Phone / Customer ID
  Note: The dataset required cleaning due to non-standard headers and data type inconsistencies.

# Business Objectives

- Identify which sales channels are contributing most to revenue and order volume.
- Analyze aggregator vs direct channel performance.
- Understand the impact of discounts across order sources.
- Identify peak operational hours to support staffing optimization.
- Segment customers to identify top contributors and repeat behavior.
- Compare performance of the primary brand vs secondary brand.

# Part 1: Data Wrangling & Preparation

* Data Cleaning
  - Removed non-standard header rows and structured the dataset into a usable tabular format.
  - Converted Invoice Date into a proper datetime format to enable time-based analysis.
  - Created helper columns such as:
    . Hour of the Day
    . Channel Type (Aggregator vs Direct)
    . Discount Percentage
    . Valid Transaction Flag
    . Data Quality Checks

* Data Quality Checks
  - Checked for missing values in critical fields such as:
    . Gross Amount
    . Net Amount
    . Order Source

* Brand Segregation

 - Segregated transactions for:
   . Primary Brand: Burgrill
   . Secondary Brand: The Sausage Fest
 - Calculated revenue and order contribution for each brand to understand their relative impact on total sales.


# Part 2: Exploratory Data Analysis (EDA)

* Sales Summary (November 2025)
 - Total Revenue
 - Total Orders
 - Average Order Value (AOV)
 - These metrics provide a high-level view of outlet performance for the month.

 * Channel Mix Analysis
  - Aggregators: Swiggy, Zomato , Magicpin
  - Direct Channels: POS / Dine-in / Takeaway
  - Key questions addressed:
    . Which channel has the highest AOV?
    . Which channel contributes the maximum number of orders?
    . How does revenue distribution vary across channels?

* Peak Hour Analysis

 - Analyzed transaction volume by hour of the day.
 - Created a visual representation (bar chart) to identify traffic patterns.
 - Insight:
    . Rush hours were identified as the time slots with the highest order volumes, indicating periods where kitchen staffing and operational capacity should be increased to reduce delays and improve service quality.

    
# Part 3: Advanced Metrics & Business Logic

 * Discount Impact Analysis

  - Calculated Discount % for each transaction using:
  - Discounts ÷ Gross Amount
  - Compared average discount levels across different order sources.
  - Objective:
    . To understand whether higher discounting is concentrated on specific aggregators and how it may be impacting profitability.

* Customer Segmentation

  - Using Customer Phone / Customer ID:
  - Identified the Top 5 customers by total revenue contribution.
  - Calculated the percentage of Repeat Customers (customers placing more than one order during the month).
  - This analysis helps understand customer loyalty and revenue concentration.

  Key Insights & Observations

# Aggregator channels contribute a significant portion of order volume but show variation in AOV and discount intensity.

  - Direct channels demonstrate relatively stronger profitability due to lower commission impact but with low volume.
  - Specific peak hours consistently drive maximum order volume, highlighting clear staffing optimization opportunities.
  - A small segment of repeat customers contributes disproportionately to total revenue.
  - The secondary brand contributes a very smaller share compared to the primary brand.

# Tools & Techniques Used

  - Microsoft Excel
  - Advanced formulas (SUMIFS, COUNTIFS, AVERAGEIFS, CONCAT, TEXT , DELIMITER  )
  - Pivot Tables
  - Charts & visualizations
  - Helper columns for business logic
  - Emphasis on formula-driven analysis with transparent calculations.


--Conclusion--
  This analysis provides Burgrill India’s management with clear visibility into channel-level performance, discount behavior, customer contribution, and operational peak periods.
  The insights can support informed decisions around commission negotiations, staffing optimization, and performance monitoring.















  
