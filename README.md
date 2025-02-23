# Supply-Chain-Analytics-using-MySql

**Aim**

1. Calculate the aggregate forecast accuracy report for all the customers for a given fiscal year
2. 


**Description**

**Atliq** is a hardware company which manufactures electronic hardware items like PC, Laptop, Hard Drive, mouse, Keyboards, pendrives etc It has operations all over the globe.

It sells to consumers through the following distribution channels:

              1. Direct Channel (Atliq E-stroe, Atliq Exclusive)
              2. Retailer (Croma, amazon)
              3. Distributer (Eg- Neptune in China)
              
It has two platforms:

              1. Brick and Mortar (like Croma, BestBuy)
              2. E-commerce (like Amazon, Flipkart)
              
**Supply Chain Management**

After manufacturing hardware in the production units, it is stored in a warehouse. From there, the inventory is distributed to various customers. The company must consider inventory demand forecasts to ensure a continuous and reliable supply.

Two potential scenarios can arise:

1. Out of Stock: This situation can lead to customer loss and negatively impact business.
2. Excess Inventory: This results in additional costs for storage and maintenance

**Net Error:**
   
Net Error is the difference between the actual value and the forecasted value. It can be either positive or negative, depending on whether the forecast overestimated or underestimated the actual value.

                  Net Error = Actual Value - Forecasted Value
             
A positive net error means the forecast underestimated the actual value, while a negative net error indicates the forecast overestimated the actual value.

**Absolute Error**

Absolute Error measures the magnitude of the error between the actual value and the forecasted value, ignoring whether the forecast was an overestimate or underestimate. It gives the absolute difference between the two values.

                 Absolute Error = |Actual Value − Forecasted Value|
                
The absolute error tells you the total error size, without considering whether the forecast was higher or lower than the actual result. It is always a non-negative number.

**Forecast Accuracy %:**

Forecast Accuracy % shows how close the forecasted values are to the actual values, expressed as a percentage. It is a way to measure the quality of your forecasts.

                Forecast Accuracy % = (1 − Absolute Error/Actual Value) × 100

A higher forecast accuracy percentage means that the forecasted values are close to the actual values, indicating better forecasting performance.

**ETL (Extract Transform Load) Process**

Data is imported from Atliq Database

**Dimension tables:**

dim_customer (customer_code, customer, platform, market, sub_zone, region)

dim_product (product_code, division, segment, category, product, variant)

**Fact tables/Transaction tables:**

fact_sales_monthly (monthly aggregated data in start of the month date, product_code, customer_code, sold_quantity )

fact_freight_Cost (market, fiscal_year, freight_pct, other_cost_pct)

fact_gross_price (product_code, fiscal_year, gross_price)

fact_manufacturing_cost (product_code, cost_year/fiscal_year, manufacturing_cost)

fact_post_invoice_deductions (customer_code, product_code, date, discounts_pct, other_deductions_pct)

fact_pre_invoice_deductions (customer_code, fiscal_year, pre_invoice_discount_pct)

fact_forecast_monthly (forecast_qty)

=======================================================================

**Conclusion**

Net Error shows the direction and magnitude of the error.

Absolute Error measures the magnitude of error without considering direction.

Forecast Accuracy % tells you how well your forecasts matched the actual values, expressed as a percentage.



