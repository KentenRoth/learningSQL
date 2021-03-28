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

The OR operator is similar in use to AND, but does basically the opposite. When you use OR you will get all data that comes back true from any of the logical operators. Just like AND there is 2 ways of using OR. You can spell it out like 'OR' the other option is using doube pipes like '||'.

```
SELECT <column_name> FROM <table_name> WHERE
    <logical Operator> OR <Locigal Operator>;
```

```
SELECT <column_name> FROM <table_name> WHERE
    <Logical Operator> || <Logical Operator>;
```

Another logical operator is BETWEEN. Between will take 2 arguments and will return the data that falls inbetween the arguments provided. Something to note is that when using between it is inclusive for example if you have between 5 and 10 you will get 5 and 10.

```
SELECT <column_name> FROM <table_name> WHERE
    <colum_name> BETWEEN <argument 1> AND <argument 2>;
```

NOT BETWEEN does the exact opposite as between. It will return all data outside of the arguments that you provided.

```
SELECT <column_name> FROM <table_name> WHERE
    <column_name> NOT BETWEEN <argument 1> AND <argument 2>
```
