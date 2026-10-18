# AGGREGATION AND GROUPING

The goal is to reduce a set of data into something smaller.

## Grouping

- the goal is to reduce many values into fewer values
- `GROUP BY`
- can only select from what's in the `GROUP BY` clause

### Having
Similar to `WHERE` but instead of filtering rows, we filter groups.
Usually combined with an aggregate function.

```sql
--- more than 15 comments
SELECT photos.url, COUNT(*)
FROM photos
         JOIN comments ON comments.photo_id = photos.id
GROUP BY photos.url
HAVING COUNT(*) > 15;
```

## AGGREGATION

- the goal is to reduce many values into one
- common aggregate functions:
  - `COUNT()` - ignores `NULL` unless `COUNT(*)`
  - `SUM()`
  - `AVG()`
  - `MIN()`/`MAX()`

```sql
SELECT COUNT(*), users.username
FROM comments
         JOIN users ON users.id = comments.user_id
GROUP BY users.username
```


## Order

1. data source: `FROM`, then `JOIN`
2. filtering: `WHERE`
3. grouping: `GROUP`
4. filter groups: `HAVING`
5. compute output: `SELECT`
6. remove duplication: `DISTINCT`
7. sorting: `ORDER BY`
8. cut: `LIMIT`, `OFFSET`
