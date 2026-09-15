# Data Description
This dataset contains population-related information for different countries, regions, states, and cities across different years. It can be used to analyze population size, population distribution, growth, literacy, density, birth rate, and death rate.


| Column               | Description                                    |
| -------------------- | ---------------------------------------------- |
| **Country**          | Name of the country                            |
| **Population**       | Total population                               |
| **Region**           | The region where the country is located.       |
| **Year**             | Year for which the population data is recorded |
| **State**            | State/administrative region                    |
| **City**             | City name                                      |
| **Urban_Population** | Population living in urban areas               |
| **Rural_Population** | Population living in rural areas               |
| **Growth_Rate**      | Population growth rate                         |
| **Literacy_Rate**    | Percentage of literate population              |
| **Density_per_km2**  | Number of people living per square kilometre   |
| **Birth_Rate**       | Number of births in the population             |
| **Death_Rate**       | Number of deaths in the population             |



| Statistic         |       Value |
| ----------------- | ----------: |
| **Total Records** |      13,211 |
| **Total Columns** |          13 |
| **Country**       |           1 |
| **Regions**       |           6 |
| **States**        |           7 |
| **Cities**        |           7 |
| **Year Range**    | 2000 – 2024 |

Categorical Data



| Column           | Missing Values |
| ---------------- | -------------: |
| Region           |              6 |
| Year             |             14 |
| State            |              2 |
| City             |              3 |
| Urban_Population |              3 |
| Rural_Population |              3 |
| Growth_Rate      |             14 |
| Literacy_Rate    |              3 |
| Density_per_km2  |              3 |
| Birth_Rate       |              3 |
| Death_Rate       |             10 |


| Country | Records |
| ------- | ------: |
| India   |  13,211 |


| Region    | Records |
| --------- | ------: |
| Central   |   2,341 |
| East      |   2,201 |
| West      |   2,191 |
| Northeast |   2,170 |
| South     |   2,161 |
| North     |   2,141 |
| Blank     |       6 |


| State       | Records |
| ----------- | ------: |
| Tamil Nadu  |   1,943 |
| UP          |   1,927 |
| Rajasthan   |   1,922 |
| Gujarat     |   1,918 |
| Maharashtra |   1,860 |
| Bihar       |   1,840 |
| Karnataka   |   1,799 |
| Blank       |       2 |


| City      | Records |
| --------- | ------: |
| Hyderabad |   1,930 |
| Kolkata   |   1,915 |
| Pune      |   1,907 |
| Delhi     |   1,873 |
| Mumbai    |   1,869 |
| Bangalore |   1,864 |
| Chennai   |   1,850 |
| Blank     |       3 |




Questions:

1 - What is the total population in each city. (Hint : Stacked Column Chart)<br>
Fields: X-axis → city  , Y-axis → Population

2 -  What is the total population in each state. (Hint : Stacked Bar Chart)<br>
Fields: Y-axis → State ,  X-axis → Population , 

3 - Compare Urban and Rural Population for each city. (Hint : Clustered Column Chart)<br>
Fields:  X-axis → city , Y-axis → Urban_Population , Y-axis → Rural_Population

4 - Compare Urban and Rural Population for each state. (Hint : Clustered Bar Chart)<br>
Fields:  X-axis → state , Y-axis → Urban_Population , Y-axis → Rural_Population

5 - How does population change over the years? (Hint : Line Chart) <br>
Fields: X-axis → Year , Y-axis → Population

6 - How does Urban and Rural Population change over the years?  (Hint : Area Chart) <br>
Fields: X-axis → Year , Y-axis → Urban_Population, Rural_Population

7 - What is the death rate  across regions? (Hint : Pie Chart) <br>
Fields:  Legend → Region Values →  death_rate 

8 - What is the birth rate  across regions? (Hint : Donut Chart) <br>
Fields:  Legend → Region Values → birth_rate 

9 - Compare the percentage of Birth Rate and Death Rate across states. (100% Stacked Column Chart)
Fields: X-axis → State , Y-axis → Birth_Rate, Death_Rate


10 - What is the relationship between population and population density  (Hint : Scatter Chart)<BR>
Fields:  X-axis → Density_per_km2 , Y-axis → Population , Legend → Country   <BR>












