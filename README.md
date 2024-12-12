# Complete-a-SQL-join

In this scenario, you’ll investigate a recent security incident that compromised some machines.

You are responsible for getting the required information from the database for the investigation.

Here’s how you’ll do this task: First, you’ll use an inner join to identify which employees are using which machines. Second, you’ll use left and right joins to find machines that do not belong to any specific user and users who do not have any specific machine assigned to them. Finally, you’ll use an inner join to list all login attempts made by all employees.

## Task 1. Match employees to their machines
First, you must identify which employees are using which machines. The data is located in the machines and employees tables.

You must use a SQL inner join to return the records you need based on a connecting column. In the scenario, both tables include the device_id column, which you’ll use to perform the join.

1. Run the following query to retrieve all records from the machines table:

```
SELECT * 
FROM machines;
```


You’ll note that this query is not sufficient to perform the join and retrieve the information you need.

2. Complete the query to perform an inner join between the machines and employees tables on the device_id column. Replace X and Y with this column name:

```
SELECT * 
FROM machines 
INNER JOIN employees ON machines.X = employees.Y;
```

![image](https://github.com/user-attachments/assets/ef04c123-c79c-4353-97a8-059d40425217)


## Task 2. Return more data
You now must return the information on all machines and the employees who have machines. Next, you must do the reverse and retrieve the information of all employees and any machines that are assigned to them.

To achieve this, you’ll complete a left join and a right join on the employees and machines tables. The results will include all records from one or the other table. You must link these tables using the common device_id column.

1. Run the following SQL query to connect the machines and employees tables through a left join. You must replace the keyword X in the query:

```
SELECT * 
FROM machines 
X JOIN employees ON machines.device_id = employees.device_id;
```

![image](https://github.com/user-attachments/assets/3c2c9225-a6d5-4d08-8908-5cd6b023e58e)


2. Run the following SQL query to connect the machines and employees tables through a right join. You must replace the keyword X in the query to solve the problem:

```
SELECT * 
FROM machines
X JOIN employees ON machines.device_id = employees.device_id;
```

![image](https://github.com/user-attachments/assets/00e7525c-78ec-4fec-853a-c25bed6b59ae)



Task 3. Retrieve login attempt data
To continue investigating the security incident, you must retrieve the information on all employees who have made login attempts. To achieve this, you’ll perform an inner join on the employees and log_in_attempts tables, linking them on the common username column.

- Run the following SQL query to perform an inner join on the employees and log_in_attempts tables. Replace X with the name of the right table. Then replace Y and Z with the name of the column that connects the two tables:
```
SELECT * 
FROM employees 
INNER JOIN X ON Y = Z;
```

![image](https://github.com/user-attachments/assets/076d2170-43e1-4e6f-9e52-0be618daaab9)


## Conclusion

You have completed this activity and should be able to use joins to combine data from multiple tables in a database.

You now have practical experience in using

`INNER JOIN`,
`LEFT JOIN`, and
`RIGHT JOIN`.
