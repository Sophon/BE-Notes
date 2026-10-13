# SIMPLE SQL STATEMENTS

### Create

```sql
    CREATE TABLE cities
    (
        name       VARCHAR(50),
        country    VARCHAR(50),
        population INTEGER,
        area       INTEGER
    )
```


```sql
INSERT INTO cities (name, country, population, area)
VALUES ('Tokyo', 'Japan', 38500000, 8223),
       ('Delhi', 'India', 28125000, 2240),
       ('Shanghai', 'China', 22125000, 4015),
       ('Sao Paolo', 'Brazil', 20935000, 3043);
```

### Read

```sql
SELECT *
FROM cities;
```

```sql
SELECT name, country
FROM cities;
```

```sql
SELECT name, population / area AS density
FROM cities;
```

- math operators:
    - `+`, `-`, `*`, `/`, `^`, `|/` (square root), `@` (abs), `%`