# SORTING

### SORT 

```sql
SELECT *
FROM products
ORDER BY products.price ASC, products.weight DESC;
```

- `ASC` is default, can be `DESC`
- doesn't only have to be integers, alpha also works

### OFFSET

Skip some number of rows.

### LIMIT

Only get a certain number of rows.

```sql
-- 10 most expensive products
SELECT *
FROM products
ORDER BY products.price DESC
LIMIT 10
```