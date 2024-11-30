# KQL Demo Notes

---

## Basic Query Structure
- **Data Source**: `TableName`
  - `| take 100` – Returns the first 100 rows.
  - `| sort by Timestamp desc` – Sorts by `Timestamp` in descending order.
  - `| top 100` – Retrieves the top 100 rows (usually based on a specific column).
  - `| distinct field1, field2` – Returns unique combinations of `field1` and `field2`.
  - `| project field1, field2` – Selects specific columns (`field1` and `field2`).

---

## Variable Assignment
- `Let a = b;` – Assigns `b` to variable `a`. **Note**: Always end with a semicolon (`;`).
- `Print b` – Outputs the value of `b`.

---

## Filtering and Conditions

### Time Filtering:
- `| where Timestamp > ago(3h)` – Filters for records within the last 3 hours.
- `| where Timestamp > ago(3d)` – Filters for records within the last 3 days.

### Column Filtering:
- `| where column1 == value1` – Filters records where `column1` equals `value1`.
- `| where column1 =~ value1` – Case-insensitive match.
- `| where column1 != value1` – Filters out records where `column1` does not equal `value1`.
- `| where column1 has "value"` – Filters for records where `column1` contains the string "value".
- `| where column1 startswith "prefix"` – Filters for records where `column1` starts with "prefix".
- `| where column1 in ("value1", "value2")` – Filters for records where `column1` is either "value1" or "value2".

### Escaping Special Characters:
- `\\` – Escape character for special characters in strings (e.g., `\\` for backslash).
- `@` – Denotes a literal, e.g., `@"text"` for exact matches.

### Null/Empty Checks:
- `| where isnotnull(column)` – Filters out records where `column` is null.
- `| where isempty(column)` – Filters for records where `column` is empty.

### Search Queries:
- `| search "test.com"` – Searches for records containing the string "test.com".
- `| search "admin" and "cmd"` – Searches for records containing both "admin" and "cmd".

---

## Joins in KQL

### Basic Join:
- `Table1 | join Table2 on field1` – Joins `Table1` with `Table2` using `field1`.

### Join Types:
- **Default Join**: The default join in KQL is an inner join. It returns rows that have matching values in both tables and removes duplicates based on the key in the left table.

  ```kql
  Table1 | join Table2 on field1
  ```

- **Inner Join**: Returns only matching rows from both tables.

  ```kql
  Table1 | join kind=inner Table2 on key
  ```

- **Left Outer Join**: Returns all rows from the left table and matching rows from the right table. If no match exists, `null` values will appear in the right table's columns.

  ```kql
  Table1 | join kind=leftouter Table2 on key
  ```

- **Right Outer Join**: Returns all rows from the right table and matching rows from the left table.

  ```kql
  Table1 | join kind=rightouter Table2 on key
  ```

- **Full Outer Join**: Returns all rows from both tables, with `null` values where no match exists.

  ```kql
  Table1 | join kind=fullouter Table2 on key
  ```

### Anti Joins:
- **Left Anti Join**: Removes matching rows, leaving only the rows from the left table that have no match in the right table.

  ```kql
  Table1 | join kind=leftanti Table2 on key
  ```

---

## Union
- **Union**: Similar to a join, but instead of combining rows based on a condition, it appends rows from multiple tables into a single result set.

  ```kql
  Table1 | union Table2
  ```

---

## Functions in KQL
- **Invoke Functions**: You can call a custom function within your query using the `invoke` keyword. Functions can be used for enrichment or complex transformations.

  ```kql
  Table1 | invoke FunctionName()
  ```

- **Using `$left` and `$right` for Join Comparisons**: When performing a join, you can refer to columns from the left and right tables using `$left` and `$right`.

  ```kql
  $left.column1 == $right.column2
  ```

---

## Summary of Common Operators:
- `=` – Equality operator.
- `!=` – Not equal operator.
- `=~` – Case-insensitive match.
- `has` – Checks if a column contains a value.
- `startswith` – Checks if a column starts with a specific string.
- `in` – Filters for specific values in a list.
- `isnotnull` – Checks if a column is not null.
- `isempty` – Checks if a column is empty.
```

This version removes the escape character (`\`) before the pipe (`|`) symbol for standard Markdown formatting. You can now directly copy this into any Markdown file.
