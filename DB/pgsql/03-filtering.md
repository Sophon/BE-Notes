# FILTERING RECORDS

## WHERE

```sql
SELECT name, area
FROM cities
WHERE area > 4000;
```

```sql
SELECT name, area
FROM cities
WHERE area BETWEEN 2_000 AND 4_000;
```

```sql
SELECT name, area
FROM cities
WHERE name IN('Delhi', 'Shanghai');
```

```sql
SELECT cities.name,
       population,
       cities.area
FROM cities
WHERE population BETWEEN 20_000_000 AND 40_000_000
  AND population / area > 5_000;
```

Order:

1. data source
2. filtering
3. select

`FROM cities` > `WHERE area > 4000` > `SELECT name, area`

Comparison operators:
- `=`, `!=`, `>`, `>=`
- `IN`, `NOT IN` - present in the list
- `BETWEEN`

## UPDATE

```sql
UPDATE cities
SET name = 'Tokio'
WHERE name = 'Tokyo';
```

## DELETE
```sql
DELETE FROM cities
WHERE name = 'Tokyo'
```

It's recommended to first use `WHERE` with `SELECT` before destructive commands. 