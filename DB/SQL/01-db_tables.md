# CREATING DATABASES AND TABLES

### Databases

```SQL
SHOW DATABASES;
```

```SQL
CREATE DATABASE my_db;
```

```SQL
DROP DATABASE my_db;
```

```SQL
USE my_db;
```

### Data types

| Category  | Data Type       | Description                                              | Example                    |
| --------- | --------------- | -------------------------------------------------------- | -------------------------- |
| Numeric   | `INT`           | Whole number (4 bytes)                                   | `42`                       |
| Numeric   | `BIGINT`        | Large whole number (8 bytes)                             | `9223372036854775807`      |
| Numeric   | `SMALLINT`      | Small whole number (2 bytes)                             | `32767`                    |
| Numeric   | `DECIMAL(p, s)` | Exact numeric with precision `p` and scale `s`           | `DECIMAL(10, 2)` → `99.99` |
| Numeric   | `FLOAT`         | Approximate floating-point number                        | `3.14`                     |
| Numeric   | `DOUBLE`        | Double-precision floating-point number                   | `3.141592653589793`        |
| String    | `CHAR(n)`       | Fixed-length string of length `n`                        | `CHAR(5)` → `'hello'`      |
| String    | `VARCHAR(n)`    | Variable-length string up to `n` characters              | `VARCHAR(255)` → `'name'`  |
| String    | `TEXT`          | Long variable-length string                              | `'A long paragraph...'`    |
| Date/Time | `DATE`          | Calendar date (YYYY-MM-DD)                               | `'2026-09-14'`             |
| Date/Time | `TIME`          | Time of day (HH:MM:SS)                                   | `'14:30:00'`               |
| Date/Time | `DATETIME`      | Date and time combined                                   | `'2026-09-14 14:30:00'`    |
| Date/Time | `TIMESTAMP`     | Date and time, often auto-updated                        | `'2026-09-14 14:30:00'`    |
| Boolean   | `BOOLEAN`       | True or false value                                      | `TRUE` / `FALSE`           |
| Binary    | `BLOB`          | Binary large object (images, files)                      | Binary data                |


### Tables

```SQL
SHOW TABLES;
```

```SQL
CREATE TABLE myTable (
    name VARCHAR(50),
    age INT
);
```

```SQL
DESC myTable;

-- identical to above but supports filtering
SHOW COLUMNS FROM myTable;
```

```SQL
DROP TABLE myTable;
```
