# learningSQL

Currently I am learning MySQL and I am going to use this README for notes and keep track of the things I have been learning.

I have spent around 15 hours learning already. I will be transfering my hand written notes here over the next couple days, also while learning some markdown in the process!

When using SQL anything that will be for the database should be in all caps, anything that is created like columns, tables, values, etc will be lower case.

In the code below it will show <database_name> when coding you will not use the < > you will just enter your database_name or whatever is specified inside the < >. If I use ( ) that is part of the code and will be needed.

The ; is extremely important in SQL.

### The Beginning

First things that need to happen is Creating, Dropping, and Using a DB,

Creating a Database:
`CREATE DATABASE <database_name>;`

Deleting or Dropping a database:
`DROP DATABASE <database_name>;`

When wanting to use a specific database:
`USE <database_name>;`

Before you can add a table to your database you need to be "in" your database by using the USE <database_name> command.
Once we have a database we need to get tables for said database. The table name is usually plural. When using the create table you can add things after data type like `NOT NULL` which will not allow that field to be null when submitted. Also if you want to set a default value you can use `DEFAULT 'value'`

```
CREATE TABLE <table_name>
  (column_name data_type ,
  column_name data_type );
```

When creating a table you add in the columns you will need, but if you miss one you can always go back an add one.

```
ALTER TABLE <table_name>
ADD COLUMN <column_name> <data_type>;
```

When you want to ad an ID to the table that will auto increment:

```
CREATE TABLE <table_name>
  ( <column_name> INT NOT NULL,
    PRIMARY KEY (<column_name>)
  );
```

When you need to see all tables are in your currently selected database:

`SHOW TABLES;`

If you have a table that you cannot remember what the columns are you can check that with:

`DESC <table_name>;`

When you are wanting to drop a table:

`DROP TABLES <table_name>;`

Here is an example of creating and adding things to a database.

`CREATE DATABASE pets;`

`USE pets;`

```
CREATE TABLE indoor_pets
  (pet_id INT NOT NULL,
   type VARCHAR(50) NOT NULL,
   name VARCHAR(50) DEFAULT 'No Name Yet',
   age INT NOT NULL DEFAULT 1,
   PRIMARY KEY (pet_id)
   );
```

`SHOW TABLES;`

`DESC indoor_pets;`

Code above will create a database, you move into that database, you create a table that will have 4 columns, show the table 'indoor_pets' and then show the breakdown of the 4 columns inside the table.
