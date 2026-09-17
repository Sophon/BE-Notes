# CRUD operations

### SELECT

```SQL
SELECT * FROM myTable;
```

```SQL
SELECT column AS alias, secondColumn FROM myTable;
```

```SQL
SELECT firstField, secondField FROM myTable;
```

### WHERE
 
- filtering

```SQL
-- case INSENSITIVE by default
SELECT * FROM table WHERE name='john';
```

### UPDATE

- it's good practice to `SELECT` before `UPDATE`

```SQL
UPDATE table SET status='laid off'
WHERE age > 70
```

### DELETE

- it's good practice to `SELECT` before `DELETE`

```SQL
DELETE FROM table
WHERE age > 70
```