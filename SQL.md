SQL is a programming language for **Creating**, **Reading**, **Updating**, and **Deleting** Data. It is used to manage [[Relational Database]]s.

SQL uses slightly different syntax for these operations:
- Create
	- `CREATE`, `INSERT`
- Read
	- `SELECT`
- Update
	- `UPDATE`
- Delete
	- `DELETE`, `DROP`
# Basic Usage
When using SQL commands, capitalize the SQL commands so as to distinguish them from names of files or headers. All SQL commands also end in a semicolon `;`.
## Creating a Table
`CREATE TABLE table (column type, ...);`
## Creating a New Database File
`$ sqlite3 favorites.db`
You will see a new prompt: `sqlite> `
To put sqlite into CSV mode and import data (commands that start with "`.`"" are sqlite specific commands):
`.mode csv`
`.import file table`
`.schema` displays SQL commands used to create schema, i.e. the SQL commands behind the scenes that are run when you use, for example, `.import`.
This will display:
`CREATE TABLE IF NOT EXISTS "table"("column" TEXT, ...);`
## Creating Data
To create data in a table:
```sql
INSERT INTO table (column, ...) VALUES(value, ...);
```
## Reading Data
To select, or read data from a database, use `{sql }SELECT columns FROM table`
You can use the wildcard character `*` to select all columns.
This will:
1. Open the database
2. Iterate over every row
3. Print out every row
This is drastically simplified from python code, which would be around 9 lines of code to do the same thing.

Any file created in sqlite is persistent, it's stored in the drive, not in memory. So, you can see it using `ls` from the command line.

Re-opening the file in sqlite without csv mode will output the data in a much more organized table format rather than the data being separated into columns.

To get the number of rows in a file:
`SELECT COUNT(*) FROM table;`
An example output of this would be:
```
+----------+
| COUNT(*) |
+----------+
| 430      |
+----------+ 
```

To get a specific column from a file you can use this:
`SELECT column FROM table;`
Or, to get distinct items in a column, use:
`SELECT DISTINCT(column) FROM table;`
You can combine statements to get different values, such as:
`SELECT COUNT(DISTINCT(column)) FROM table`

Use the `AS` keyword to create an alias for (rename) a column for better readability:
`SELECT COUNT(DISTINCT(column)) AS n FROM TABLE`

Use the `WHERE` keyword to only return a value if it fits a given criteria:
`SELECT COUNT(*) FROM table WHERE column = value`
Note that:
- This will return the number of items in `table` that fit the criteria of `column = value`, where value can be an [[Integer|int]], [[String|string]], [[Boolean|bool]], etc.
- SQL uses a single `=` for equality rather than most languages which use a double `==`.
- You can use regular [[Boolean|boolean]] operators such as `AND`, `OR`, and `NOT`.

Use the `ORDER BY` keywords to list items from a query in order:
`SELECT column, COUNT(*) FROM table GROUP BY column ORDER BY COUNT(*) DESC`
Note that:
- The `GROUP BY`  keyword is used to group all items that have the same of a given value `column`.
- The `DESC` keyword is used to order the columns and their frequencies in descending order, where larger values are placed at the top. The default is `ASC`, or ascending order.
## Updating Data
To update existing data:
`UPDATE table SET column = value WHERE condition`
Note that:
- The `WHERE` keyword is used to check for a condition, e.g. `column = value`
	- If the `WHERE` keyword is omitted, all values in the database will be updated blindly, which can be **very dangerous**.
## Deleting Data
To delete data:
`DELETE FROM table WHERE column = value;`
Note that:
- `WHERE` is used to check for a condition. If it is omitted, **all data in the database will be deleted. This can be very dangerous**.
# Types
- Blob ([[Binary]] Large Object)
	- `0`s and `1`s, binary data
- [[Integer]]
- Numeric
	- Numbers that have a special format, e.g. dates and timestamps
- Real
	- Floating point value
- Text
	- [[String]]s

