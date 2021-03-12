#CRUD Operations in MySQL

CRUD stands for 'Create', 'Read', 'Update', and 'Delete'.

When doing crud operations make sure you are in the correct database.

First thing we need to do is create some data that will go into the columns. When adding data, if it is a string you need to have " " around it. The order you list the columns is the order you also need to have the values you want to insert.

```
    INSERT INTO <table_name>(<column_name>, <column_name>)
    VALUES(<data for column 1>, <data for column 2>);
```

If you want to add more than 1 value you can by adding a comma after the ():

```
    INSERT INTO <table_name>(<column_name>, <column_name>)
    VALUES(<data for column 1>, <data for column 2>),
        (<data for column 1>, <data for column 2>),
        (<data for column 1>, <data for column 2>);
```

After you have inserted Data you will want to see what data you have. To get ALL of the data:

`SELECT * from <table_name>`

If you only want to return things from a specific column of the table, You can also put more than 1 column if you seperate them with a comma.

`SELECT <column_name> FROM <table_name>`

`SELECT <column_name>, <column_name> FROM <table_name>`
