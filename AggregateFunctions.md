# Aggregate Functions

One of the more common things that will be used is GROUP BY. What this does is group things to make data a little easier to work with. One thing about group by is it will stack rows, but only show you what is first in the row. For example, if each row is a piece of paper in a notebook. There are more pages there, but you can only see the top one, and you're not allowed to flip the pages. There will be more GROUP BY examples at the end that will show how it can be used with other functions.

`SELECT <column_name> FROM <table_name> GROUP BY <column_name>;`

Count is something that might not be extemely usefull outside of using it with Group by. What it does is simply count the number of things that are returned.

`SELECT COUNT(<column_name>) FROM <table_name>;`

Min and Max will return the highest and lowest values in a column. This does not have to be with just numbers, it can be with alphabetic columns also. One thing that is problem with these functions is, it does not return the entire row, it only returns the column you want. If you are trying to get the min or max, but also want the entire row of data, it's best to use ORDER BY.

`SELECT MIN(<column_name>) FROM <table_name>;`

`SELECT MAX(<column_name>) FROM <table_name>;`

Sum is another function that can be used, and is used mostly with group by. Sum will give you the sum of everything in the column.

`SELECT SUM(<column_name>) FROM <table_name>;`

Avg is to get the average of everything that you selected. This does not round to the nearest whole number, it will return a number with 4 decimal points. Even if the average is a whole number it will return something like 32.0000. Once again this is something that works best with GROUP BY.

`SELECT AVG(<column_name>) FROM <table_name>;`

So lets look at some of these functions used along with GROUP BY.
Using count will tell you how many are actually in the row.

```
SELECT COUNT(<column_name>) FROM <table_name>
        GROUP BY <column_name>;
```

Using average will return the average number of all the things in each group.

```
SELECT AVG(<column_name>) FROM <table_name>
        GROUP BY <column_name>;
```

Using Sum will add everything together that is in each group.

```
SELECT SUM(<column_name>) FROM <table_name>
        GROUP BY <column_name>;
```
