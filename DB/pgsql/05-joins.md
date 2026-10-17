# JOINS

Produces values by merging rows from different tables.

Used for getting data from multiple resources.

```sql
SELECT comments.contents, users.username
FROM comments
         JOIN users ON comments.user_id = users.id;
```

### Types of `join`s:

1. Left outer join: `LEFT JOIN`
   - displays all records from the **left** table; `NULL` on the right record with no match
2. `RIGHT JOIN`
   - displays all records from the **right** table; `NULL` on the left record with no match
3. Inner join: `JOIN`
   - default
   - intersection - records that have a match between the two tables
4. Full outer join: `FULL JOIN`
   - everything from both

```sql
-- occurrences where the users commented on their own photo
-- with a three-way JOIN
SELECT photos.url, comments.contents, users.username
FROM photos
       JOIN comments ON photos.id = comments.photo_id
       JOIN users ON users.id = comments.user_id
WHERE photos.user_id = comments.user_id;
```

