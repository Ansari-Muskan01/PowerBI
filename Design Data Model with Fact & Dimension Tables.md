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
**1. Qualitative Data** : Qualitative Data is data that describes a category or characteristic.<br>

**Examples:**<br>
Gender → Male, Female<br>
Segment → Premium, Regular<br>
Category → Electronics, Clothing<br>
Region → West, East<br>
Loyalty_Status → Loyal, New<br>

Easy way to remember: Qualitative Data = Description or Category<br>


**2. Quantitative Data** : Quantitative Data is data that represents a number or a measurable value.<br>

**Examples:**<br>
Sales → ₹50,000<br>
Quantity → 10<br>
Profit → ₹5,000<br>
Unit_Price → ₹2,000<br>
Delivery_Days → 5<br>

Easy way to remember: Quantitative Data = Number or Measurement<br>
<br>

| Qualitative Data                       | Quantitative Data                  |
| -------------------------------------- | ---------------------------------- |
| Describes a category or characteristic | Represents a number or measurement |
| Gender                                 | Age                                |
| Category                               | Sales                              |
| Region                                 | Quantity                           |
| Loyalty Status                         | Profit                             |
| Segment                                | Price                              |

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

# Data Description 

This dataset contains information about customers, products, dates, regions, and sales transactions.<br>

The data is divided into Dimension Tables and a Fact Table to make the data easier to organize and analyze.<br>

**Dimension Tables**<br>
**Customer Table** → Contains customer information such as Customer Name, Segment, Gender, and Loyalty Status.<br>
**Date Table** → Contains date-related information such as Year, Month, Quarter, and Week Number.<br>
**Product Table** → Contains product information such as Category, Sub-Category, Brand, Product Name, and Unit Price.<br>
**Region Table** → Contains location information such as Region, City, State, Country, and Zone.<br>

**Fact Table**<br>
Sales Table → Contains sales transaction information such as Sales, Quantity, Profit, Discount, Cost Price, Selling Price, and Shipping Cost.<br>


The tables are connected using Primary Keys and Foreign Keys.<br>

For example:
Customer_ID → connects Customer and Sales<br>
Product_ID  → connects Product and Sales<br>
Date_ID     → connects Date and Sales<br>
Region_ID   → connects Region and Sales<br>

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

Customer_ID : 	Unique ID of the customer<br>
Customer_Name	: Name of the customer<br>
Segment : 	Customer group<br>
Customer_Age_Group : 	Age group of the customer<br>
Gender : 	Gender of the customer<br>
Loyalty_Status	: Loyalty status of the customer<br>
Join_Date : 	Date when the customer joined<br>


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

Date_ID	: Unique ID for each date<br>
Year	: Year of the date<br>
Month: 	Month of the date<br>
Quarter	: Quarter of the year<br>
Day_Name	: Name of the day<br>
Week_Number: 	Week number of the year<br>
Is_Weekend: 	Shows whether the date is a weekend<br>

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


Product_ID :	Unique ID of the product
Category	: Main category of the product
Sub_Category	: Sub-category of the product
Brand	: Brand name of the product
Product_Name: 	Name of the product
Unit_Price: 	Price of one unit of the product
Launch_Year : 	Year when the product was launched

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

Region_ID : 	Unique ID of the region
Region : 	Name of the region
City : 	Name of the city
State : 	Name of the state
Country : 	Name of the country
Zone : Zone in which the location belongs
Pin_Code : Postal code of the location



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


