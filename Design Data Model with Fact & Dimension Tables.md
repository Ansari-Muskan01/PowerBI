# Identify fact and dimension tables

Fact and Dimension Tables

Before understanding Star Schema and Snowflake Schema, we first identify Fact Tables and Dimension Tables.

# Identify Fact and Dimension Tables

Before understanding Star Schema and Snowflake Schema, we first identify the Fact Table and Dimension Tables.

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

**Customer = Dimension Table** because it contains information about customers.

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

**Date = Dimension Table** because it contains information about dates.

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

**Product = Dimension Table** because it contains information about products.

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

**Region = Dimension Table** because it contains information about locations.

---

## 5. Orders Table — Fact Table

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

**Orders = Fact Table** because it contains transaction information and measurable business values such as Sales, Quantity and Profit.

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

# Star Schema

A **Star Schema** has one central Fact Table and multiple Dimension Tables directly connected to it.

```text
                 Customer
                    |
                    |
Product -------- Orders -------- Date
                    |
                    |
                  Region
