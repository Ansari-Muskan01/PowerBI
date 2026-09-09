## Explore Population Dataset & Identify Key Insights

- **Learning Objectives**  : <br>
Understand the concept of Business Intelligence<br>
Understand Self-Service Business Intelligence<br>
Differentiate between ETL and ELT<br>
Identify popular SSBI tools<br>
Understand what Power BI is<br>
Install Power BI Desktop<br>
Understand the benefits of Power BI<br>
Understand Power BI architecture<br>
Understand the building blocks of Power BI<br>
Connect Power BI with a dataset<br>
Explore and analyze population data<br>
Identify meaningful insights from data<br>
Create interactive Power BI reports<br>


# What is Business Intelligence?
Business Intelligence (BI) is the process of collecting, analyzing, and presenting data to generate meaningful information and insights that help in better decision-making.

In simple words: BI converts raw data into meaningful insights that help us to make better decisions.

Example : Suppose we have population data

| Country  | Year   | Population     | 
| -------- | ------ | ---------------- 
| India    | 2020   |  1,380 Million | 
| China    | 2020   |  1,424 Million |   
| USA      | 2020   |  331 Million   | 

This is raw data.

Using BI, we can analyze this data and find useful information.

For example:<br>
China has the highest population among these countries.<br>
India has a higher population than the USA.<br>
We can compare population between different countries.<br>
We can analyze how population changes over time.<br>


BI Process : 
Raw Data → Analysis → Insight → Decision

Example of the BI Process

Raw Data: India = 1,380 Million, China = 1,424 Million, USA = 331 Million<br>
↓<br>

Analysis: Compare the population of the three countries.<br>
↓<br>

Insight: China has the highest population among the three countries, while the USA has the lowest..<br>
↓<br>

Decision: The organization can consider China and India for further business analysis because they have larger populations.<br>


## Why is BI important?
What is happening?<br>
Which country has the highest population?<br>
How is population changing over time?<br>
What are the important trends?<br>

# 2. Self-Service Business Intelligence

Self-Service Business Intelligence (SSBI) allows business users to analyze data and create reports or dashboards with minimal help from technical teams. <br> 

In simple words: Users can work with data themselves instead of depending completely on IT teams.<br>

Example :
Suppose a Sales Manager wants to know:<br>
Which city has the highest sales?<br>
Which product is performing best?<br>
How are sales changing month by month?<br>

In traditional BI, the manager may need to ask the IT or data team to prepare the report.<br>

With Self-Service BI, the manager can use a tool such as Power BI to connect to the data, create visualizations, apply filters, and analyze the results independently.<br>

Traditional BI vs Self-Service BI
| Traditional BI                                | Self-Service BI                            |
|---                                            |---                                         |
| Mostly depends on IT/data teams               | Business users can analyze data themselves |
| Report creation may require technical support | Users can create their own reports         |
| Changes may take more time                    | Reports can be created or modified quickly |
| Usually requires technical knowledge          | Designed to be more user-friendly          |

# 3) ETL vs ELT

**organization can collect data from different sources, such as:<br>**
Excel files<br>
CSV files<br>
Databases<br>
Websites<br>
Applications<br>

**Data may also contain:<br>**
Missing values<br>
Duplicate records<br>
Incorrect data formats<br>
Unnecessary columns<br>
Inconsistent data<br>

Before using this data for analysis, it may need to be cleaned and transformed.<b>

**What is ETL?**

ETL stands for Extract → Transform → Load.<br>

ETL is a data integration process in which data is extracted from different sources, transformed or cleaned, and then loaded into the target system.<br>

ETL Process

1. Extract : Data is collected from different sources.<br>

2. Transform : Data is cleaned and converted into the required format.<br>
For example:<br>
Remove duplicate records<br>
Handle missing values<br>
Change data types<br>
Remove unnecessary columns<br>

3. Load : The transformed data is loaded into the target system, such as a database or data warehouse.<br>

ETL Flow : Data Sources → Extract → Transform → Load → Target System <br>

Example : <br>
Suppose a company receives customer data from Excel and a database.<br>

During the transformation process:<br>
Removes duplicate customers<br>
Fixes incorrect formats<br>
Handles missing values<br>
Keeps only required columns<br>
The cleaned and transformed data is ready for analysis and reporting.


**What is ELT?**

ELT stands for Extract → Load → Transform.

In ELT, data is extracted from different sources and loaded into the target system first. The transformation is performed later inside the target system.

ELT Process

1. Extract : Data is collected from different sources.

2. Load : The data is loaded into the target system, often in its raw form.

3. Transform : The data is cleaned and transformed inside the target system when required.

ELT Flow : Data Sources → Extract → Load → Transform

Example : 
Suppose a company collects a large amount of customer data from multiple sources.
Instead of cleaning all the data before storing it, the company first loads the raw data into a cloud data warehouse.
Later, the data is cleaned and transformed inside the warehouse for analysis.



| ETL                                                   | ELT                                                        |
| ----------------------------------------------------- | ---------------------------------------------------------- |
| Extract → Transform → Load                            | Extract → Load → Transform                                 |
| Data is transformed before loading                    | Data is transformed after loading                          |
| Common in traditional systems                         | Common in modern cloud data platforms                      |
| Target receives processed data                        | Target can receive raw data first                          |
| Useful when transformation is required before storage | Useful when target system has strong processing capability |

Easy way to remember
ETL: Clean first, then store.
ELT: Store first, then clean.


# 4) SSBI Tools

1. Power BI : Microsoft's BI and data visualization platform.

2. Tableau : Popular tool for data visualization and interactive dashboards.

4. Looker : Google Cloud's platform for data analytics and BI.

5. Excel : Excel also provides several self-service BI capabilities such as:
PivotTables
PivotCharts
Power Query
Power Pivot


| Tool       | Company      | Main Use           |
| ---------- | ------------ | ------------------ |
| Power BI   | Microsoft    | BI & dashboards    |
| Tableau    | Salesforce   | Data visualization |
| Qlik Sense | Qlik         | Data analytics     |
| Looker     | Google Cloud | BI & analytics     |
| Excel      | Microsoft    | Data analysis      |


# 5) What is Power BI?
Simple Definition

Power BI is a Business Intelligence and data visualization platform developed by Microsoft.

It allows us to:

Connect to data
Clean and transform data
Analyze data
Create visualizations
Build interactive reports
Create dashboards
Share insights
