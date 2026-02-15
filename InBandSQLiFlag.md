# Blind SQLi

- Unlike In-Band SQL injection, where we can see the results of our attack directly on the screen, blind SQLi is when we get little to no feedback to confirm whether our injected queries were, in fact, successful or not, this is because the error messages have been disabled, but the injection still works regardless. It might surprise you that all we need is that little bit of feedback to successfully enumerate a whole database.


# Authentication Bypass

- One of the most straightforward Blind SQL Injection techniques is when bypassing authentication methods such as login forms. In this instance, we aren't that interested in retrieving data from the database; We just want to get past the login. 

- Login forms that are connected to a database of users are often developed in such a way that the web application isn't interested in the content of the username and password but more in whether the two make a matching pair in the users table. In basic terms, the web application is asking the database, "Do you have a user with the username bob and the password bob123?" the database replies with either yes or no (true/false) and, depending on that answer, dictates whether the web application lets you proceed or not. 

# CHEAT CODE SUMMARY

## BLIND SQL INJECTION (Authentication Bypass)

What it is:
- No visible errors or data output
- Only TRUE / FALSE responses
- Goal: force query to return TRUE


Typical vulnerable login query
- SELECT * FROM users
WHERE username='%username%' AND password='%password%'
LIMIT 1;

## Blind SQLi Authentication Bypass payload
- ' OR 1=1;--

1. Resulting query after injection
- SELECT * FROM users
WHERE username='' AND password='' OR 1=1;

- Why it works:
- 1=1 is always TRUE
- OR condition forces TRUE result
- Application believes login is valid

[**Next**](BlindSQLBoolean.md)
