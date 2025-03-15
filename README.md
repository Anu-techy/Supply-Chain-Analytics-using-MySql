# Supply-Chain-Analytics-using-MySql

**Aim**

1. Calculate the aggregate forecast accuracy report for all the customers for a given fiscal year using CTE

2. Create a stored procedure to Calculate the aggregate forecast accuracy report for all the customers for a given fiscal year 

3. Calculate the aggregate forecast accuracy report for all the customers for a given fiscal year by creating a temporary table

**ETL (Extract Transform Load) Process**

Data is imported from Database

**Dimension tables:**

dim_customer (customer_code, customer, platform, market, sub_zone, region)

dim_product (product_code, division, segment, category, product, variant)

**Fact tables/Transaction tables:**

fact_sales_monthly (monthly aggregated data in start of the month date, product_code, customer_code, sold_quantity )

fact_forecast_monthly (monthly aggregated data in start of the month date, fiscal_year, product_code, forecast_quantity)

fact_freight_Cost (market, fiscal_year, freight_pct, other_cost_pct)

fact_gross_price (product_code, fiscal_year, gross_price)

fact_manufacturing_cost (product_code, cost_year/fiscal_year, manufacturing_cost)

fact_post_invoice_deductions (customer_code, product_code, date, discounts_pct, other_deductions_pct)

fact_pre_invoice_deductions (customer_code, fiscal_year, pre_invoice_discount_pct)

fact_act_est (date, fiscal_year, product_code, customer_code, sold_quantity, forecast_quantity)

fact_act_est is a derived table by joining fact_sales_monthly and fact_forecast_monthly

=======================================================================

**Conclusion**

Net Error shows the direction and magnitude of the error.

Absolute Error measures the magnitude of error without considering direction.

Forecast Accuracy % tells you how well your forecasts matched the actual values, expressed as a percentage.

In supply chain management, forecast accuracy %, net error, and absolute error are essential for optimizing inventory levels, 
reducing costs, and improving demand planning to ensure smoother operations.
