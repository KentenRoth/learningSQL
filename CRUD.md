# CRUD Operations in MySQL

There will be more examples of this at the very bottom.

CRUD stands for 'Create', 'Read', 'Update', and 'Delete'.

When doing crud operations make sure you are in the correct database.

First thing we need to do is create some data that will go into the columns. When adding data, if it is a string you need to have " " around it. The order you list the columns is the order you also need to have the values you want to insert.

```
    INSERT INTO <table_name>(<column_name>, <column_name>) VALUES
        (<data for column 1>, <data for column 2>);
```

If you want to add more than 1 value you can by adding a comma after the ():

```
    INSERT INTO <table_name>(<column_name>, <column_name>) VALUES
        (<data for column 1>, <data for column 2>),
        (<data for column 1>, <data for column 2>),
        (<data for column 1>, <data for column 2>);
```

After you have inserted Data you will want to see what data you have. To get ALL of the data:

`SELECT * from <table_name>`

If you only want to return things from a specific column of the table, You can also put more than 1 column if you seperate them with a comma.

`SELECT <column_name> FROM <table_name>`

`SELECT <column_name>, <column_name> FROM <table_name>`

When you need to update something you need to specify the table, column name, what your changing it to and what column name is being changed. When updating, the WHERE <column_name> does not have to be the same as the SET <column_name>. An example would be

```
    UPDATE <table_name> SET <column_name>='<what its changing to>'
        WHERE <column_name>='<item you want to change>';
```

When deleting from the database you need to make sure what you are targeting is the correct thing. Once you delete it there is no edit undo.

`DELETE FROM <table_name> WHERE <column_name>='<what you want to delete>';`

For the example I created a table that has 4 columns, pet_id, type, name, and age,

```
CREATE TABLE indoor_pets
  (pet_id INT NOT NULL AUTO_INCREMENT,
   type VARCHAR(50) NOT NULL,
   name VARCHAR(50) DEFAULT 'No Name Yet',
   age INT NOT NULL DEFAULT 1,
   PRIMARY KEY (pet_id)
   );
```

Inserting data into the table. Each item that is inserted has to have the same number of values as columns you list. If you want to use the default value for one of the places you need to put DEFAULT in that spot.

```
INSERT INTO indoor_pets(type, name, age) VALUES
    ('cat', 'Princess', 10),
    ('cat', 'Mouse', 4),
    ('Chinchilla', 'Buddy', DEFAULT),
    ('Dog', DEFAULT ,12),
    ('Ferret', 'Tommy', 3);
```

Reading data from the table:

`SELECT * FROM indoor_pets;`

Now lets find a specific pet and return the entire row for that pet.

`SELECT * FROM indoor_pets WHERE name='Princess';`

Lets update the name of the Dog from 'No Name Yet' to 'Whiskey', and lets change the name of our Chinchilla to Bud. In the expamples we are going to change the name by getting the row having the same SET and WHERE column and from have a different SET and WHERE column.

```
UPDATE indoor_pets SET name='Whiskey'
    WHERE pet_id=4;
```

```
UPDATE indoor_pets SET name='Bud'
    WHERE name='Buddy';
```

Now for the last step of CRUD we will be deleting from the table. Once this has been run that item has been removed from the table, and there is no going back.

`DELETE FROM indoor_pets WHERE pet_id=5;`

This is the basics of the CRUD operations. There is also a Joins operation that is important and I will have a section just on that in the future when I have a better grasp on it.
