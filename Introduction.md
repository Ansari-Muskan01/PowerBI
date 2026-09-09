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

For example:
China has the highest population among these countries.
India has a higher population than the USA.
We can compare population between different countries.
We can analyze how population changes over time.
Data → Analysis → Insight → Decision

BI Process : 
Raw Data → Analysis → Insight → Decision

Example of the BI Process

Raw Data: India = 1,380 Million, China = 1,424 Million, USA = 331 Million
↓

Analysis: Compare the population of the three countries.
↓

Insight: China has the highest population, followed by India, while the USA has a much lower population.
↓

Decision: An organization planning a new service can prioritize China and India because they have larger populations and potentially larger markets.

Why is BI important?

BI helps us answer questions like:
What is happening?
Which country has the highest population?
How is population changing over time?
What are the important trends?

# 2. Self-Service Business Intelligence

What is Self-Service BI?<br>
Self-Service Business Intelligence (SSBI) allows business users to analyze data and create reports or dashboards with minimal help from technical teams.

In simple words:
Users can work with data themselves instead of depending completely on IT teams.


# 3) ETL vs ELT

Data may come from different sources and may contain:
Missing values
Duplicate records
Incorrect formats
Unnecessary columns
Different data sources


What is ETL?
ETL = Extract → Transform → Load

ETL is a traditional process where data is:
Extracted from different sources
Transformed or cleaned
Loaded into the target system

What is ELT?<br>
ELT = Extract → Load → Transform<br>
The main difference is the order of Transform and Load.<br>

In ELT:
Data is extracted
Data is loaded into the target system
Transformation happens inside the target system

Flow :  Data Sources -> Extract -> Load ->Transform

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
