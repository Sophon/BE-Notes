# INSERTING DATA

### Inserting into table

```SQL
-- strings generally require single quotes
INSERT INTO myTable
VALUES ('Queeny', 13);

-- named column names for ordering
INSERT INTO myTable (name, age)
VALUES ('Alfa', 18);

INSERT INTO myTable (name, age)
VALUES ('Alain', 13),
       ('Belle', 4),
       ('Lilly', 2);
```

```SQL
SELECT * FROM myTable;
```

### Null

- null is absence of value

```SQL
CREATE TABLE nonNull(
    name VARCHAR(50) NOT NULL,
    age INT NOT NULL
);
```

### Default values

```SQL
CREATE TABLE withDefaults(
    name VARCHAR(50),
    age INT,
    breed VARCHAR(50) DEFAULT 'unknown'
);
```

- this doesn't mean the value can't be `null`
    - we can change it to `null`
    - we can insert `null`:

```SQL
INSERT INTO withDefaults(name, age, breed)
VALUES ('Capone', 5, NULL);
```

### Primary keys

- the unique identifier of a row

```SQL
CREATE TABLE uniques(
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT NOT NULL,
)

CREATE TABLE uniques(
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    age INT NOT NULL,
)
```
