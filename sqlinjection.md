# SQL Injection

- **SQL (Structured Query Language)** Injection, mostly referred to as SQLi, is an attack on a web application database server that causes malicious queries to be executed. When a web application communicates with a database using input from a user that hasn't been properly validated, there runs the potential of an attacker being able to steal, delete or alter private and customer data and also attack the web application authentication methods to private or customer areas. This is why SQLi is one of the oldest web application vulnerabilities, and it can also be the most damaging.

## What is a Database?
- A database is a way of electronically storing collections of data in an organised manner. A database is controlled by a DBMS, which is an acronym for  Database Management System. DBMSs fall into two camps: Relational and Non-Relational; the focus of this room will be on Relational databases; some common ones you'll come across are MySQL, Microsoft SQL Server, Access, PostgreSQL and SQLite. We'll explain the difference between Relational and Non-Relational databases at the end of this task, but first, it's important to learn a few terms.

-  is a feature-rich language used for querying databases. These SQL queries are better referred to as statements.

- The simplest of the commands which we'll cover in this task is used to retrieve (select), update, insert and delete data. Although somewhat similar, some database servers have their own syntax and slight changes to how things work. All of these examples are based on a MySQL database. After learning the lessons, you'll easily be able to search for alternative syntax online for the different servers. It's worth noting that SQL syntax is not case-sensitive.

## What is SQL Injection?

- The point wherein a web application using SQL can turn into SQL Injection is when user-provided data gets included in the SQL query.

Example: "https://website.thm/blog?id=1"

- From the URL above, you can see that the blog entry selected comes from the id parameter in the query string. The web application needs to retrieve the article from the database and may use an SQL statement that looks something like the following:

**SELECT * from blog where id=1 and private=0 LIMIT 1;**

- From what you've learned in the previous task, you should be able to work out that the SQL statement above is looking in the blog table for an article with the id number of 1 and the private column set to 0, which means it's able to be viewed by the public and limits the results to only one match.

- As was mentioned at the start of this task, SQL Injection is introduced when user input is introduced into the database query. In this instance, the id parameter from the query string is used directly in the SQL query.
----

Let's pretend article ID 2 is still locked as private, so it cannot be viewed on the website. We could now instead call the URL:

**https://website.thm/blog?id=2;--**

Which would then, in turn, produce the SQL statement:

**SELECT * from blog where id=2;-- and private=0 LIMIT 1;**

The semicolon in the URL signifies the end of the SQL statement, and the two dashes cause everything afterwards to be treated as a comment. By doing this, you're just, in fact, running the query:

**SELECT * from blog where id=2;--**

Which will return the article with an ID of 2 whether it is set to public or not.

This was just one example of an SQL Injection vulnerability of a type called In-Band SQL Injection; there are three types in total: In-Band, Blind and Out-of-Band, which we'll discuss over the following tasks.

[Next](InBandSQLi.md)