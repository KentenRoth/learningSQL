# Basic Queries

So we know how to get all the data back, but now its starting to get parts of data back. There is a good chance that we don't need everything everytime we make a call.

With Distinct it will return everything on the list without duplicates. So if you have the same number repeated in your DB if you use Distinct instead of returning every instince of something it will only return it once.

`SELECT DISTINCT <column_name> FROM <table_name>;`

Order by can be a very useful way of getting infromation back. This will order things in alphabetical order or numerical order. More than one column can be used to order the data. It will order by the first column_name passed then it will move to the 2nd column name passed to make fine adjustments. For expample if you have a list of books and authors. You sort by author last name then sort by author first name. This will have all of the authors in order by last name THEN it will adjust the first names. So your final results will be ordered by last name, then any author with matching last names will then be alphabtized by first name.

```
SELECT <column_name> FROM <table_name>
    ORDER BY <column_name>;
```

```
SELECT <column_name> FROM <table_name>
    ORDER BY <column_name>, <column_name>;
```

The next thing we can do is limit our results. This is something that could come in handy with pagination, or just limiting your results so you can have a faster response time. If you only provide 1 number it will return that many. If you provide 2 numbers, the first number is saying at what index you want to start at, and the 2nd number is saying how many you want to return. This is something that is used frequently with Order by.

`SELECT <column_name> FROM <table_name> LIMIT <num>;`

`SELECT <column_name> FROM <table_name> LIMIT <num>, <num>;`

When getting data you might need to do a search, that is where LIKE comes into play. Like has a couple 'wildcards' that will help search. The first 'wildcard' is % and what this means is anything. So if you are searching for something and you know it starts with 'co' you could use the %. It would look something like this:

`SELECT <column_name> FROM <table_name> LIKE 'co%';`

If you are looking for something and you know there is a 'co' some place in it, it would look something like this:

`SELECT <column_name> FROM <table_name> LIKE '%co%';`

The % wildcard says there can be any number or charactors in either direction of what you typed.

The other wildcard is _ and is used for things that are very specific. The _ is 1 charactor slot. It can be any charactor or number, but is only one spot. If you was looking for something like maybe account numbers, and you know they are always 8 digits you could do something like:

`SELECT <column_name> FROM <table_name> LIKE '________';`
