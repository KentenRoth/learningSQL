# Logical Operators

When you need to return things, but exclude something specific. Using not equal (!=) is one way of doing it.

`SELECT <column_name> FROM <table_name> WHERE <column_name> != '<What you want to exclude>';`

Another way of excluding things being returned is using NOT LIKE. This is the exact same thing is LIKE only in reverse. This also uses the same wildcards and is setup the same way.

`SELECT <column_name> FROM <table_name> WHERE <column_name> NOT LIKE '<what you want to exclude>';`

Greater than and greater than or equal to. This will return things that are larger or larger than or equal to the number provided.

`SELECT <column_name> FROM <table_name> WHERE <column_name> > <num>;`

`SELECT <column_name> FROM <table_name> WHERE <colum_name> >= <num>;`

Less than and less than or equal to. This is the same as greater than except in reverse.

`SELECT <column_nmae> FROM <table_name> WHERE <column_name> < <num>;`

`SELECT <column_name> FROM <table_name> WHERE <column_name> <= <num>;`

Now we need to be able to chain things together, and to do that we can do it a couple different ways. We can use AND or &&. When using AND (&&) both sides have to be true for something to return. You can chain more than 2 things together, and it does not always have to be logical operators.

```
SELECT <column_name> FROM <table_name> WHERE
    <Logical Operator> AND <Logical Operator>;
```

```
SELECT <column_name> FROM <table_name> WHERE
    <Logical Operator> && <Logical Operator>;
```
