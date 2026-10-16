# JOINS

- joins 
  - produces values by merging rows from different tables
  - used for getting data from multiple resources
- aggregation
  - calculates a value from different rows
  - used with *average*, *most*, *least* etc.

## Joins

```sql
SELECT comments.contents, users.username
FROM comments
         JOIN users ON comments.user_id = users.id;
```

