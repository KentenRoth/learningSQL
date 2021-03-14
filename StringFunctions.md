# MySQL String Functions

This is a list of some String functions.

One thing that is import when using string functions is that the order which they are called is imporant. You might not get back what you are expecting if you have them in the wrong order.

Starting with Concat. When you there will not be a space between whatever it is your passing as column_name, so if you want to add space between you have to add ' ' between the column_name

`SELECT CONCAT (<column_name>, <column_name>) FROM <table_name>;`

`SELECT CONCAT (<column_name>, ' ', <column_name>) FROM <table_name>;`

Something you can do to bypass having to use ' ' after each column name if you have several you want to concat. This will place what ever you pass a sthe first argument between each column name.

`SELECT CONCAT_WS (' ', <column_name>, <column_name>, <column_name>) FROM <table_name>;`

Substring is something that will limit the amount of characters that is returned. This will take 2 or 3 arguments. If you only put 1 number it will start at the character index and return the rest of the string. If you have 2 numbers it will start at the first and go to the 2nd character at that index. if you use a negative number it will begin at the end and go towards the front that many characters.

`SELECT SUBSTRING (<column_name>, num, num) FROM <table_name>;`

`SELECT SUBSTRING (<column_name>, num) FROM <table_name>;`

`SELECT SUBSTRING (<column_name>, -num) FROM <table_name>;`
