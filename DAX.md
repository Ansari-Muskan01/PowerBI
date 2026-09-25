# DAX – Data Analysis Expressions


**DAX Aggregated functions :** Aggregation functions perform calculations on multiple rows and return one result.<BR>

SUM() : Adds all numeric values in a column.<BR>
AVERAGE() : Calculates the average of numeric values.<BR>
MIN() : Returns the largest value from a column.<BR>
MAX() : Counts numeric values in a column.<BR>
COUNT() : Counts numeric values in a column.<BR>
COUNTA() : Counts non-blank values in a column.<BR>
DISTINCTCOUNT() : Counts unique values in a column.<BR>

**Questions :**<BR>
1 - Calculate the total salary paid to all employees. (HINT: SUM())<BR>
2 - Calculate the average engagement score of all employees. (HINT: AVERAGE())<BR>
3 - Find the minimum salary among all employees. (HINT: MIN())<BR>
4 - Find the maximum salary among all employees. (HINT: MAX())<BR>
5 - Count the number of employees using Employee_ID. (HINT: COUNT())<BR>
6 - Count the number of employees who have a Gender value. (HINT: COUNTA())<BR>
7 - Calculate the number of unique departments using Department_ID. (HINT: DISTINCTCOUNT())<BR>


**DAX Iterative Functions :** Iterative functions are used when we need to perform a calculation for each row first, and then get one final result.<BR>

SUMX() : Calculates a value for each row and then adds all the calculated values.<BR>
AVERAGEX(): Calculates a value for each row and then finds the average of the calculated values.<BR>
MINX() : Calculates a value for each row and then finds the smallest calculated value.<BR>
MAXX() : Calculates a value for each row and then finds the largest calculated value.<BR>
COUNTX() : Checks a value for each row and counts how many results are available.<BR>

**Questions:** <BR>
1 - Calculate the total salary of employees who have completed more than 5 years of experience. (Hint: Use SUMX() with FILTER())<BR>
2 - Count the number of employees whose performance rating is 4 or higher. (Hint: Use COUNTX() with FILTER())<BR>
3 - Find the minimum salary among employees whose performance rating is 4.  (Hint: Use MINX() with FILTER().)<BR>
4 - Calculate the average salary of employees who have received a promotion in the last 3 years. (Hint: Use AVERAGEX() with FILTER().)<BR>
5 - Find the maximum salary among employees who have completed more than 5 years of experience. (Hint: Use MAXX() with FILTER().)<BR>

Normal functions → directly work on a column.
X functions → first calculate for each row, then give the final result.


DAX Operators

1 - Arithmetic Operators
+    Addition
-    Subtraction
*    Multiplication
/    Division

Comparison Operators
=     Equal to
<>    Not equal to
>     Greater than
<     Less than
>=    Greater than or equal to
<=    Less than or equal to

Logical Operators
&&    AND
||    OR

Calculate the salary after a 10% hike.
Calculate the remaining salary amount after deducting 10%.
