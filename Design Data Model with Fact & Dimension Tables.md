Identify fact and dimension tables

Fact and Dimension Tables

Before understanding Star Schema and Snowflake Schema, we first identify Fact Tables and Dimension Tables.

Customer_ID →Primary Key

Customer Name —>Qualitative data

Segment → Qualitative data

Customer Age group—> Qualitative data

Gender —> Qualitative data

Loyalty Status→ Qualitative data

Join Date → Qualitative data  


Table Date contains:

 

Date_ID →Primary Key

Year —>Qualitative data

Month → Qualitative data

Quarter—> Qualitative data

Day_name —> Qualitative data

Week_number→ Qualitative data

is_weekend → Qualitative data



Table Product contains:

 

Product_ID →Primary Key

Category —>Qualitative data

Sub-Category → Qualitative data

Brand—> Qualitative data

Day_name —> Qualitative data

Product_Name→ Qualitative data

Unit_Price → Qualitative data

Launch_year—>Qualitative data



Table Region contains:

 

Region_ID →Primary Key

Region —>Qualitative data

City → Qualitative data

State—> Qualitative data

Country —> Qualitative data

Zone→ Qualitative data

Pin_Code → Qualitative data



 

Order_ID →Primary Key

Customer_ID—->Foreign key

Product_ID—>Foreign key

Region_ID—> Foreign key

Date_ID —> Foreign key

Sales→Quantitative data

Quantity →Quantitative data

Profit—> Quantitative data

Discount—> Quantitative data

Cost_price—>Quantitative data

Selling_price—>Quantitative data

Shipping_cost–>Quantitative data

Order_priority —> Qualitative data

Delivery_Days—> Quantitative data

Financial_year—>Qualitative data


Understand Star schema and Snowflake schema
