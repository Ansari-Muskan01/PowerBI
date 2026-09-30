# DAX – Data Analysis Expressions


**DAX Aggregated functions :** Aggregation functions perform calculations on multiple rows and return one result.<BR>

SUM() : Adds all numeric values in a column.<BR>
AVERAGE() : Calculates the average of numeric values.<BR>
MIN() : Returns the smallest value from a column.<BR>
MAX() : Returns the largest value from a column.<BR>
COUNT() : Counts numeric values in a column.<BR>
COUNTA() : Counts non-blank values in a column.<BR>
DISTINCTCOUNT() : Counts unique values in a column.<BR>

**Questions :**<BR>
1 - Calculate the total salary paid to all employees. (HINT: SUM())<BR>
2 - Calculate the average engagement score of all employees. (HINT: AVERAGE())<BR>
3 - Find the minimum salary among all employees. (HINT: MIN())<BR>
4 - Find the maximum salary among all employees. (HINT: MAX())<BR>
5 - Count the number of employees using Employee_ID. (HINT: COUNT())<BR>
6 - Count the number of employees whose Gender value is not blank.(HINT: COUNTA())<BR>
7 - Calculate the number of unique departments using Department_ID. (HINT: DISTINCTCOUNT())<BR>


**DAX Iterative Functions :** Iterative functions are used when we need to perform a calculation for each row first, and then get one final result.<BR>

SUMX() : Calculates a value for each row and then adds all the calculated values.<BR>
AVERAGEX(): Calculates a value for each row and then finds the average of the calculated values.<BR>
MINX() : Calculates a value for each row and then finds the smallest calculated value.<BR>
MAXX() : Calculates a value for each row and then finds the largest calculated value.<BR>
COUNTX() : Checks a value for each row and counts how many results are available.<BR>

**Questions:** <BR>
1 - Calculate the total salary of employees who have completed more than 5 years of experience. (Hint: Use SUMX() with FILTER())<BR>
2 - Count the number of employees whose performance rating is greater than 4. (Hint: Use COUNTX() with FILTER())<BR>
3 - Find the minimum salary among employees whose performance rating is 4.  (Hint: Use MINX() with FILTER().)<BR>
4 - Calculate the average salary of employees who have received a promotion in the last 3 years. (Hint: Use AVERAGEX() with FILTER().)<BR>
5 - Find the maximum salary among employees who have completed more than 5 years of experience. (Hint: Use MAXX() with FILTER().)<BR>

Normal functions → Directly work with a column and return one result.<BR>
X functions → Evaluate an expression row by row and then return one final result.<BR>

**DAX Logical Functions**

IF() : Checks a condition and returns one value if the condition is TRUE and another value if the condition is FALSE.<BR>
AND() : Checks whether all given conditions are TRUE.<BR>
OR() : Checks whether at least one of the given conditions is TRUE.<BR>
NOT() : Reverses the result of a condition. TRUE becomes FALSE and FALSE becomes TRUE.<BR>
SWITCH() : Checks multiple conditions or values and returns the matching result.<BR>

1 - Create a column to identify employees as "High Salary" if their salary is greater than 50000, otherwise "Low Salary". (Hint: IF())<BR>
2 - Create a column to identify employees as "Eligible" if their experience is greater than 5 years AND their performance rating is greater than 4. Otherwise, return "Not Eligible".(Hint: IF() with AND())<BR>
3 - Create a column to identify employees as "Eligible for Bonus" if their years of experience is greater than 5 OR their salary is greater than 70000. Otherwise, return "Not Eligible for Bonus". (Hint: IF() with OR())<BR>
4 - Create a column to identify employees as "Not High Performer" if their performance rating is not equal to 5. Otherwise, return "High Performer". (Hint: IF() with NOT())<BR>
5 - Create a column to categorize employees based on their performance rating:<BR>

5 → "Excellent"<BR>
4 → "Good"<BR>
3 → "Average"<BR>
2 → "Needs Improvement"<BR>
1 → "Poor"<BR>
(Hint: SWITCH())<BR>

**Custom Column** : A Custom Column is created in Power Query using a formula based on existing columns.<BR>

Path: Home → Transform Data → Power Query → Add Column → Custom Column<BR>
Create a custom column to calculate the employee's salary after adding a 10% bonus to their current salary.<BR>

**Enter Data :** Enter Data is used when you want to manually create a small table in Power BI.<BR>

Path: Home → Enter Data<BR>
Create a new table named Department_Employee_Count using Enter Data. Add each department and its corresponding number of employees based on the HR_Fact table.<BR>

