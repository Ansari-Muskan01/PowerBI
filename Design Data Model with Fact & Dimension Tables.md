# Sales Performance Analysis

A company wants to analyze its sales data and understand:<br>
1- How much sales are generated?<br>
2- Which products are performing well?<br>
3- Which customers are purchasing more?<br>
4- Which regions generate more sales?<br>
5- How sales change over time?<br>
6- How much profit is generated?<br>
7- What is the impact of discount?<br>
8- How many quantities are sold?<br>

# Data Modeling

Data Modeling is the process of organizing data into multiple related tables and defining relationships between them.

In Power BI, data modeling involves identifying Fact Tables and Dimension Tables and creating relationships between them using common columns such as Primary Keys and Foreign Keys.


# Star Schema

In Star Schema, one Fact Table is directly connected to multiple Dimension Tables.

Fact Table → Stores transactions and measurable values.<br>
Dimension Tables → Store information about customers, products, dates, regions, etc.<br>

# Snowflake Schema

In Snowflake Schema, Dimension Tables are further divided into smaller related tables.

Fact Table → Stores transactions and measurable values.<br>
Dimension Tables → Store descriptive information.<br>
Related Tables → Store more detailed information about the dimensions.<br>


# Types of Data
**1. Qualitative Data** : Qualitative Data is data that describes a category, characteristic, or type of something.

It usually tells us what type, which category, or what kind.<br>

Examples:<br>
Gender → Male, Female<br>
Segment → Premium, Regular<br>
Category → Electronics, Clothing<br>
Region → West, East<br>
Loyalty_Status → Loyal, New<br>

Easy way to remember: Qualitative Data = Description or Category<br>


**2. Quantitative Data** : Quantitative Data is data that represents a number or a measurable value.

It tells us how much, how many, or how long.<br>
Examples:<br>
Sales → ₹50,000<br>
Quantity → 10<br>
Profit → ₹5,000<br>
Unit_Price → ₹2,000<br>
Delivery_Days → 5<br>
Easy way to remember: Quantitative Data = Number or Measurement<br>

| Qualitative Data                       | Quantitative Data                  |
| -------------------------------------- | ---------------------------------- |
| Describes a category or characteristic | Represents a number or measurement |
| Gender                                 | Age                                |
| Category                               | Sales                              |
| Region                                 | Quantity                           |
| Loyalty Status                         | Profit                             |
| Segment                                | Price                              |



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


