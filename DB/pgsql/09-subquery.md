# SUBQUERIES

Sometimes, gaining a value is too cumbersome for one query.

In those cases, we have subqueries:

```sql
SELECT name, price, department
FROM products
WHERE price > (SELECT MAX(price)
               FROM products
               WHERE department = 'Toys');
```

Subqueries can be used as sources:

```sql
SELECT p1.name,
       (SELECT COUNT(name) FROM products) -- source of a value
FROM (SELECT * FROM products) AS p1 -- source of rows
         JOIN (SELECT * FROM products) AS p2 ON p1.id = p2.id -- source of rows
WHERE p1.id IN (SELECT id FROM products); -- source of a column
```

Focus should be on the shapes:
- `SELECT * FROM orders` - many rows, many columns
- `SELECT id FROM orders` - many rows, single column
- `SELECT COUNT(*) FROM orders` - one row, one column (aka **scalar query**)