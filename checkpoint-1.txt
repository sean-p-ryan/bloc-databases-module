>What data types do each of these values represent?

1) "A Clockwork Orange" is a string
2) 42 is an integer
3) 09/02/1945 is a date (or "datetime")? data type
4) 98.7 is a float
5) $15.99 is a float

>Explain when a database would be used. Explain when a text file would be used.

A database is used when the data stored needs to persist, or exist after each run of the program that updates it. A text file would be used in situations where data does not need to persist, and the developer must be able to read the data without much effort. A JSON file in an application is an example of such a text file.

>Describe one difference between SQL and other programming languages.

SQL is a declarative rather than a procedural language, meaning that when searching for data values, a programmer must only specify the data that needs to be found rather than the steps required to find it.

>In your own words, explain how the pieces of a database system fit together at a high level.

In a database system, individual pieces of information are stored in a column and row structure that allows programmers to access individual pieces of information (or query the data) using declarative queries.

>Explain the meaning of table, row, column, and value.

A "table" is a complete collection of related data. The "columns" in the table label the type of data that is stored underneath them, and the rows contain the units of data that make up a complete set, or record.

>List three data types that can be used in a table.

Text (strings), dates, and numeric values (or integers) can be used in a table.

>What would be the result of each of these queries?
```
SELECT date, amount
FROM payments;
```

This would return all records under the "date" and "amount" column heads in the table "payments." It would look like this:
```
Date          Amount
5/1/2016     1500.00
5/10/2016      37.00
5/15/2016     124.93
5/23/2016      54.72
```
```
SELECT amount
FROM payments
WHERE amount > 500;
```

This would return only the payment dates and amounts for payments over 500 in the "payments" table. It would look like this:
```
Date        Amount
5/1/2016   1500.00
```
```
SELECT *
FROM payments
WHERE payee = 'Mega Foods';
```

This would return the complete records (all columns) for payments made to 'Mega Foods' stored in the "payments" table. It would look like this:
```
Date            Payee       Amount        Memo
5/15/2016     Mega Foods    124.93      Groceries
```

>Given this users table, write SQL queries using the following criteria and include the output:

The email and sign-up date for the user named DeAndre Data.
```
SELECT email, signup
FROM users
WHERE name = 'DeAndre Data';
```

OUTPUT:
```
email                 signup
datad@comcast.net   2008-01-20
```

>The user ID for the user with email 'aleesia.algorithm@uw.edu'.
```
SELECT userid
FROM users
WHERE email = 'aleesia.algorithm@uw.edu';
```

OUTPUT:
```
userid
  1
```

>All the columns for the user ID equal to 4.
```
SELECT *
FROM users
WHERE userid = 4;
```

```
userid          name               email          signup
   4       Brandy Boolean  bboolean@nasa.gov    1999-10-15
```
