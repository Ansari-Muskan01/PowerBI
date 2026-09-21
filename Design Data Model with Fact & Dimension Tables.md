# Sales Performance Analysis

A company wants to analyze its sales data and understand:

How much sales are generated?
Which products are performing well?
Which customers are purchasing more?
Which regions generate more sales?
How sales change over time?
How much profit is generated?
What is the impact of discount?
How many quantities are sold?


# Business Questions
| Area     | Question                                           |
| -------- | -------------------------------------------------- |
| Sales    | What is the total sales?                           |
| Profit   | What is the total profit?                          |
| Product  | Which products generate more sales?                |
| Customer | Which customer segments generate more sales?       |
| Region   | Which regions perform better?                      |
| Time     | How does sales change month by month/year by year? |
| Quantity | Which products have higher quantity sold?          |
| Discount | How does discount affect sales and profit?         |


Section 1 — Overall Performance

Total Sales
Total Profit
Total Quantity
Total Orders
Average Discount

Section 2 — Sales Analysis

Sales by Year
Sales by Category


Section 3 — Product & Customer Analysis
Top Products by Sales

Section 4 — Regional Analysis

Sales by Region


# Data Modeling

Data Modeling is the process of creating relationships between different tables so that we can analyze the data correctly.


## 1. Customer Table — Dimension Table

| Column | Type |
|---|---|
| Customer_ID | Primary Key |
| Customer_Name | Qualitative Data |
| Segment | Qualitative Data |
| Customer_Age_Group | Qualitative Data |
| Gender | Qualitative Data |
| Loyalty_Status | Qualitative Data |
| Join_Date | Qualitative Data |

Customer :  It contains information about customers.

---

## 2. Date Table — Dimension Table

| Column | Type |
|---|---|
| Date_ID | Primary Key |
| Year | Qualitative Data |
| Month | Qualitative Data |
| Quarter | Qualitative Data |
| Day_Name | Qualitative Data |
| Week_Number | Qualitative Data |
| Is_Weekend | Qualitative Data |

Date : It contains information about dates.

---

## 3. Product Table — Dimension Table

| Column | Type |
|---|---|
| Product_ID | Primary Key |
| Category | Qualitative Data |
| Sub_Category | Qualitative Data |
| Brand | Qualitative Data |
| Product_Name | Qualitative Data |
| Unit_Price | Quantitative Data |
| Launch_Year | Qualitative Data |

Product : It contains information about products.

---

## 4. Region Table — Dimension Table

| Column | Type |
|---|---|
| Region_ID | Primary Key |
| Region | Qualitative Data |
| City | Qualitative Data |
| State | Qualitative Data |
| Country | Qualitative Data |
| Zone | Qualitative Data |
| Pin_Code | Qualitative Data |

Region : It contains information about locations.

---

## 5. Sales Table — Fact Table

| Column | Type |
|---|---|
| Order_ID | Primary Key |
| Customer_ID | Foreign Key |
| Product_ID | Foreign Key |
| Region_ID | Foreign Key |
| Date_ID | Foreign Key |
| Sales | Quantitative Data |
| Quantity | Quantitative Data |
| Profit | Quantitative Data |
| Discount | Quantitative Data |
| Cost_Price | Quantitative Data |
| Selling_Price | Quantitative Data |
| Shipping_Cost | Quantitative Data |
| Order_Priority | Qualitative Data |
| Delivery_Days | Quantitative Data |
| Financial_Year | Qualitative Data |

Orders : It contains transaction information and measurable business values such as Sales, Quantity and Profit.

---

# Summary

| Table | Type | Contains Information About |
|---|---|---|
| Customer | Dimension | Customers |
| Date | Dimension | Dates |
| Product | Dimension | Products |
| Region | Dimension | Locations |
| Orders | Fact | Transactions and Measures |

### Easy Way to Remember

- **Customer → Who?**
- **Product → What?**
- **Date → When?**
- **Region → Where?**
- **Orders → What happened?**

---
Instead of keeping all information in one large table, we keep related information in separate tables and connect them using relationships.

Here:

Sales = Fact Table
Customer = Dimension Table
Product = Dimension Table
Date = Dimension Table
Region = Dimension Table

# Star Schema

A **Star Schema** has one central Fact Table and multiple Dimension Tables directly connected to it.



                 Customer
                    |
                    |
Product -------- Sales -------- Date
                    |
                    |
                  Region




This is called a Star Schema because the structure looks like a star.



