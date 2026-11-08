# SET OPERATIONS

A **set** is the outcome of one of the individual queries.
Then we have set operators.

### UNION

Joins two sets of rows.

- skips duplicates by default; `UNION ALL` keeps duplicates
- must have the same columns and types of data
- parentheses are unnecessary but very useful for formatting and explicitly scopes `ORDER` or `LIMIT`

```sql
(SELECT name, department, price, weight, price / weight AS ratio
 FROM products
 ORDER BY price DESC
 LIMIT 4)
UNION
(SELECT name, department, price, weight, price / weight AS ratio
 FROM products
 ORDER BY ratio DESC
 LIMIT 4);
```

### INTERSECT

Gives rows that are common.

```sql
(SELECT name, department, price, weight, price / weight AS ratio
 FROM products
 ORDER BY price DESC
 LIMIT 4)
INTERSECT
(SELECT name, department, price, weight, price / weight AS ratio
 FROM products
 ORDER BY ratio DESC
 LIMIT 4);
```

As a result, the row that was dropped by `UNION` is the result of the `INTERSECT`.

- `INTERSECT ALL` - keeps duplicates

```sql
SELECT unnest([5, 5, 6, 6, 6, 6, 7, 8]) AS x
INTERSECT ALL
SELECT unnest([5, 6, 6, 7, 7, 9]);
--- returns 5 6 6 7
```


### EXCEPT

Rows of A except rows of B.

In other words, `setOf(A).filterNot { it in B }`.

```sql
(SELECT *
 FROM products
 ORDER BY price DESC
 LIMIT 4)
EXCEPT
(SELECT *
 FROM products
 ORDER BY price / weight DESC
 LIMIT 4);
```