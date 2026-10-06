# DAX – Data Analysis Expressions


**DAX Aggregated functions :** Aggregation functions perform calculations on multiple rows and return one result.<BR>

SUM() : Adds all numeric values in a column.<BR>
Syntax: SUM(Table[Column])<BR>

AVERAGE() : Calculates the average of numeric values.<BR>
Syntax: AVERAGE(Table[Column])<BR>

MIN() : Returns the smallest value from a column.<BR>
Syntax: MIN(Table[Column])<BR>

MAX() : Returns the largest value from a column.<BR>
Syntax: MAX(Table[Column])<BR>

COUNT() : Counts numeric values in a column.<BR>
Syntax: COUNT(Table[Column])<BR>

COUNTA() : Counts non-blank values in a column.<BR>
Syntax: COUNTA(Table[Column])<BR>

DISTINCTCOUNT() : Counts unique values in a column.<BR>
Syntax: DISTINCTCOUNT(Table[Column])<BR>

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
Syntax: SUMX(Table, Expression)<BR>

AVERAGEX(): Calculates a value for each row and then finds the average of the calculated values.<BR>
Syntax: AVERAGEX(Table, Expression)<BR>

MINX() : Calculates a value for each row and then finds the smallest calculated value.<BR>
Syntax: MINX(Table, Expression)<BR>

MAXX() : Calculates a value for each row and then finds the largest calculated value.<BR>
Syntax: MAXX(Table, Expression)<BR>

COUNTX() : Checks a value for each row and counts how many results are available.<BR>
Syntax: COUNTX(Table, Expression)

**Questions:** <BR>
1 - Calculate the total salary of employees who have completed more than 5 years of experience. (Hint: Use SUMX() with FILTER())<BR>
2 - Count the number of employees whose performance rating is greater than 4. (Hint: Use COUNTX() with FILTER())<BR>
3 - Find the minimum salary among employees whose performance rating is 4.  (Hint: Use MINX() with FILTER().)<BR>
4 - Calculate the average salary of employees whose Promotion_Last_3_Years value is "Yes". (HINT: Use AVERAGEX() with FILTER().)<BR>
5 - Find the maximum salary among employees who have completed more than 5 years of experience. (Hint: Use MAXX() with FILTER().)<BR>

Normal functions → Directly work with a column and return one result.<BR>
X functions → Evaluate an expression row by row and then return one final result.<BR>

**DAX Logical Functions**

IF() : Checks a condition and returns one value if the condition is TRUE and another value if the condition is FALSE.<BR>
Syntax: IF(Condition, Value_If_True, Value_If_False)<BR>

AND() : Checks whether all given conditions are TRUE.<BR>
Syntax: AND(Condition1, Condition2)<BR>

OR() : Checks whether at least one of the given conditions is TRUE.<BR>
Syntax: OR(Condition1, Condition2)<BR>

NOT() : Reverses the result of a condition. TRUE becomes FALSE and FALSE becomes TRUE.<BR>
Syntax: NOT(Condition)<BR>

SWITCH() : Checks multiple conditions or values and returns the matching result.<BR>
Syntax: SWITCH(Expression, Value1, Result1, Value2, Result2, ..., Else)<BR>

Questions :<BR>
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

# Date Function

YEAR() returns the year from a date.<BR>
Syntax: YEAR(Date)<BR>

MONTH() returns the month number from a date, from 1 to 12.<BR>
Syntax: MONTH(Date)<BR>

DAY() returns the day of the month from a date, from 1 to 31.<BR>
Syntax: DAY(Date)<BR>

QUARTER() returns the quarter number from a date, from 1 to 4.<BR>
Syntax: QUARTER(Date)<BR>

WEEKDAY() returns a number representing the day of the week.<BR>
Syntax: WEEKDAY(Date, Return_Type)<BR>

WEEKNUM() returns the week number of a date within the year.<BR>
Syntax: WEEKNUM(Date, Return_Type)<BR>

DATE() creates a date using a specified year, month, and day.<BR>
Syntax: DATE(Year, Month, Day)<BR>

EDATE() returns a date that is a specified number of months before or after a given date.<BR>
Syntax: EDATE(Start_Date, Months)<BR>

DATEDIFF() calculates the difference between two dates using a specified time unit.<BR>
Syntax: DATEDIFF(Start_Date, End_Date, Interval)<BR>

EOMONTH() returns the last date of a month. Using -1 and adding 1 gives the first date of the current month.<BR>
Syntax: EOMONTH(Start_Date, Months)<BR>

TODAY() returns the current date.<BR>
Syntax: TODAY()<BR>

NOW() returns the current date and time.<BR>
Syntax: NOW()<BR>

FORMAT() converts a value into a specified format. "MMMM" returns the full month name, and "dddd" returns the full weekday name.<BR>
Syntax: FORMAT(Value, Format_String)<BR>

Questions :<BR>
1 - Create a new column that extracts the year from the Date_of_Joining column. Hint: YEAR()<BR>
2 - Create a new column that extracts the month number from the Date_of_Joining column. Hint: MONTH()<BR>
3 - Create a new column that extracts the day from the Date_of_Joining column. Hint: DAY()<BR>
4 - Create a new column that returns the quarter number from the Date_of_Joining column. Hint: QUARTER()<BR>
5 - Create a new column that returns the day of the week number for each employee's Date_of_Joining. Hint: WEEKDAY()<BR>
6 - Create a new column that returns the week number of the year for each employee's Date_of_Joining. Hint: WEEKNUM()<BR>
7 - Create a new column that creates a date using the year, month, and day from Date_of_Joining. Hint: DATE()<BR>
8 - Create a new column that adds 1 year to each employee's Date_of_Joining. Hint: EDATE()<BR>
9 - Create a new column that returns the number of days between Date_of_Joining and Last_Review_Date. Hint: DATEDIFF()<BR>
10 - Create a new column that returns the first date of the month in which the employee joined. Hint: EOMONTH()<BR>
11 - Create a new column that returns the current date. Hint: TODAY()<BR>
12 - Create a new column that returns the current date and time. Hint: NOW()<BR>
13 - Create a new column that shows the joining month name from Date_of_Joining. Hint: FORMAT()<BR>
14 - Create a new column that shows the joining weekday name from Date_of_Joining. Hint: FORMAT()<BR>
15 - Create a new column that identifies whether the employee's Date_of_Joining falls on a weekday or weekend. Hint: WEEKDAY() + IF()<BR>

# Text Function

& : Joins two or more text values together.<BR>
Syntax: Text1 & Text2<BR>

LEFT() : Returns a specified number of characters from the beginning of a text value.<BR>
Syntax: LEFT(Text, Number_Of_Characters)<BR>

RIGHT() : Returns a specified number of characters from the end of a text value.<BR>
Syntax: RIGHT(Text, Number_Of_Characters)<BR>

MID() : Returns a specified number of characters from a text value, starting from a given position.<BR>
Syntax: MID(Text, Start_Position, Number_Of_Characters)<BR>

LEN() : Returns the number of characters in a text value.<BR>
Syntax: LEN(Text)<BR>

UPPER() : Converts text into uppercase letters.<BR>
Syntax: UPPER(Text)<BR>

LOWER() : Converts text into lowercase letters.<BR>
Syntax: LOWER(Text)<BR>

TRIM() : Removes extra spaces from text, leaving a single space between words.<BR>
Syntax: TRIM(Text)<BR>

SEARCH() : Finds the position of one text value inside another text value. It is not case-sensitive.<BR>
Syntax: SEARCH(Find_Text, Within_Text, Start_At, Not_Found_Value)<BR>

FIND() : Finds the position of one text value inside another text value. It is case-sensitive.<BR>
Syntax: FIND(Find_Text, Within_Text, Start_At, Not_Found_Value)<BR>

SUBSTITUTE() : Replaces existing text with new text in a text value.<BR>
Syntax: SUBSTITUTE(Text, Old_Text, New_Text, Instance_Num)<BR>

REPLACE() : Replaces a specified number of characters in a text value with new text.<BR>
Syntax: REPLACE(Text, Start_Position, Number_Of_Characters, New_Text)<BR>

1 - Create a new column by joining Employee_ID and Gender with " - " between them.              	  (Hint: &)            Expected Output: 10117 - Female<BR>
2 - Create a new column that returns the first 3 characters of Employee_ID.                     	  (Hint: LEFT())       Expected Output: 101<BR>
3 - Create a new column that returns the last 2 characters of Employee_ID.                      	  (Hint: RIGHT())      Expected Output: 17<BR>
4 - Create a new column that extracts 3 characters starting from the 2nd character of Employee_ID. 	(Hint: MID())        Expected Output: 011<BR>
5 - Create a new column that returns the number of characters in Department_Name. 			            (Hint: LEN()) 	     Expected Output: 15<BR>
6 - Create a new column that converts Department_Name into uppercase. 				                    	(Hint: UPPER())      Expected Output: HUMAN RESOURCES<BR>
7 - Create a new column that converts JobRole_Name into lowercase. 					                        (Hint: LOWER())      Expected Output: manager<BR>
8 - Create a new column that removes any extra spaces from Department_Name. 				                (Hint: TRIM()) 	     Expected Output: Human Resources<BR>
9 - Create a new column that searches for the letter a in Department_Name. 				                  (Hint: SEARCH())     Expected Output: 3<BR>
10 - Create a new column that finds the position of the letter e in Location_Name. 			            (Hint: FIND())<BR>
11 - Create a new column that replaces the word Manager with Mgr in JobRole_Name. 			            (Hint: SUBSTITUTE()) Expected Output: Mgr<BR>
12 - Create a new column that replaces the first 2 characters of Employee_ID with "EMP". 		        (Hint: REPLACE())    Expected Output: EMP117<BR>

# Table 

Create a new table that contains only the employees whose Gender is "Male".    Hint: FILTER() <BR>
Create a new table that contains only the employees whose Gender is "Female".  Hint: FILTER() <BR>

**Custom Column** : A Custom Column is created in Power Query using a formula based on existing columns.<BR>

Path: Home → Transform Data → Power Query → Add Column → Custom Column<BR>
Create a custom column to calculate the employee's salary after adding a 10% bonus to their current salary.<BR>

**Enter Data :** Enter Data is used when you want to manually create a small table in Power BI.<BR>

Path: Home → Enter Data<BR>
Create a new table named Department_Employee_Count using Enter Data. Add each department and its corresponding number of employees based on the HR_Fact table.<BR>

