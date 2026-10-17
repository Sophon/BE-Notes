# AGGREGATION AND GROUPING

The goal is to reduce a set of data into something smaller.

## Grouping

- the goal is to reduce many values into fewer values
- `GROUP BY`
- can only select from what's in the `GROUP BY` clause


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
