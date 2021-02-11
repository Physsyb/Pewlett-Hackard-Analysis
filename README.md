# Pewlett-Hackard-Analysis
# Overview of the Project
> Explain the purpose of this analysis.

Now that Bobby has proven his SQL chops, his manager has given both of you two more assignments: determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. Then, you’ll write a report that summarizes your analysis and helps prepare Bobby’s manager for the “silver tsunami” as many current employees reach retirement age. Here are the deliverables for this project;
* Deliverable 1: The Number of Retiring Employees by Title
* Deliverable 2: The Employees Eligible for the Mentorship Program
* Deliverable 3: A written report on the employee database analysis (README.md) to help the manager prepare for the upcoming "silver tsunami."

## Resources
* Data Tools: PostgreSQL, pgAdmin
* Software: pgAdmin 4.29, Python 3.8.3, Flask Version 1.0.2

# Deliverable 1
> Using the ERD you created in this module as a reference and your knowledge of SQL queries, create a Retirement Titles table that holds all the titles of current employees who were born between January 1, 1952 and December 31, 1955. Because some employees may have multiple titles in the database—for example, due to promotions—you’ll need to use the `DISTINCT ON` statement to create a table that contains the most recent title of each employee. Then, use the `COUNT()` function to create a final table that has the number of retirement-age employees by most recent job title.
1. Retrieve the emp_no, first_name, and last_name columns from the Employees table.
2. Retrieve the title, from_date, and to_date columns from the Titles table.
3. Create a new table using the INTO clause.
4. Join both tables on the primary key.
5. Filter the data on the birth_date column to retrieve the employees who were born between 1952 and 1955. Then, order by the employee number.
![1](https://user-images.githubusercontent.com/76136277/107707952-af798800-6c90-11eb-9700-d92a1ab72d92.PNG)

6. Copy the query from the `Employee_Challenge_starter_code.sql `and add it to your `Employee_Database_challenge.sql` file.
7. Retrieve the employee number, first and last name, and title columns from the Retirement Titles table.
    * These columns will be in the new table that will hold the most recent title of each employee.
8. Use the `DISTINCT ON` statement to retrieve the first occurrence of the employee number for each set of rows defined by the `ON ()` clause.
9. Create a Unique Titles table using the INTO clause.
10. Sort the Unique Titles table in ascending order by the employee number and descending order by the last date (i.e. to_date) of the most recent title.
![2](https://user-images.githubusercontent.com/76136277/107707810-79d49f00-6c90-11eb-930f-d19052becf1f.PNG)

11. Write another query in the `Employee_Database_challenge.sql` file to retrieve the number of employees by their most recent job title who are about to retire.
12. First, retrieve the number of titles from the Unique Titles table.
13. Then, create a Retiring Titles table to hold the required information.
14. Group the table by title, then sort the count column in descending order.
![3](https://user-images.githubusercontent.com/76136277/107707578-12b6ea80-6c90-11eb-95c1-4154741f2b42.PNG)

# Deliverable 2
> Using the ERD you created in this module as a reference and your knowledge of SQL queries, create a mentorship-eligibility table that holds the current employees who were born between January 1, 1965 and December 31, 1965.

In the `Employee_Database_challenge.sql` file, write a query to create a Mentorship Eligibility table that holds the employees who are eligible to participate in a mentorship program.
1. Retrieve the `emp_no`, first_name, last_name, and birth_date columns from the Employees table.
2. Retrieve the from_date and to_date columns from the Department Employee table.
3. Retrieve the title column from the Titles table.
4. Use a `DISTINCT ON` statement to retrieve the first occurrence of the employee number for each set of rows defined by the `ON ()` clause.
5. Create a new table using the `INTO` clause.
6. Join the Employees and the Department Employee tables on the primary key.
7. Join the Employees and the Titles tables on the primary key.
8. Filter the data on the `to_date` column to get current employees whose birth dates are between January 1, 1965 and December 31, 1965.
9. Order the table by the employee number.
![4](https://user-images.githubusercontent.com/76136277/107707435-d97e7a80-6c8f-11eb-9284-447666889414.PNG)

# Deliverable 3
> A written report on the employee database analysis. 

#### The analysis should contain the following:
* Overview of the analysis
* Results
* Summary
## Overview of the analysis
> A written report to help the manager prepare for the upcoming "silver tsunami."

## Results
> Provide a bulleted list with four major points from the two analysis deliverables. Use images as support where needed.

* #### From the unique_title table, there are 90,398 of staff born between January 1, 1952 and December 31st, 1955. This means the percentage of retirement is very high.
![7](https://user-images.githubusercontent.com/76136277/107712347-43e6e900-6c97-11eb-8cbb-db53ee74c6fd.PNG)
* #### Looking at the job titles, the company would need to hire lots of people to fill the positions of those retiring. The number of people retiring by tittle is attached in the screenshot below;
![5](https://user-images.githubusercontent.com/76136277/107709964-0cc30880-6c94-11eb-8681-f08d298e7446.PNG)
* #### There are about 1940 staff  born between January 1, 1965 and December 31, 1965 eligible for the mentorship program. This means that there would be few employees to mentor the next generation of employees.
![6](https://user-images.githubusercontent.com/76136277/107712356-477a7000-6c97-11eb-81a6-fd9b2900c1e9.PNG)
* #### Overall, lots of resources will be spent by the employer because of the number of positions that needs to the filled. Also, the employer might need to channel more resources into the mentorship program.

 
## Summary
> Provide high-level responses to the following questions, then provide two additional queries or tables that may provide more insight into the upcoming "silver tsunami."

1. #### How many roles will need to be filled as the "silver tsunami" begins to make an impact?
     * 90,398 roles will need to be filled.    
![7](https://user-images.githubusercontent.com/76136277/107712347-43e6e900-6c97-11eb-8cbb-db53ee74c6fd.PNG)

2. #### Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
     * No, there are just 1940 employees eligible to participate in the mentorship program.
![6](https://user-images.githubusercontent.com/76136277/107712356-477a7000-6c97-11eb-81a6-fd9b2900c1e9.PNG)
