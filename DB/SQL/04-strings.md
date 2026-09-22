# STRINGS

### CONCAT
 
- combines multiple strings into one

```SQL
SELECT CONCAT(first_name_column, last_name_column) AS full_name FROM myTable;
```

```SQL
SELECT CONCAT_WS('separator', first_name_column, last_name_column) AS full_name FROM myTable;
```

### SUBSTRING

```SQL
-- starting at 3 - 'in string'
SELECT SUBSTRING('main string', 3);

-- starting at 1, take 4 chars - 'main'
SELECT SUBSTRING('main string', 1, 4);

-- starting from three places from the end - 'ing'
SELECT SUBSTRING('main string', -3); 
```

### REPLACE

- case **sensitive**

```SQL
SELECT REPLACE('initial', 'old', 'new')
```

### Others

- `REVERSE` - reverses
- `LENGTH`/`CHAR_LENGTH`
  - `LENGTH` bases that off of how many bytes each char is while `CHAR_LENGTH` is true length
  - might matter for things like Chinese letters
- `UPPER`/`LOWER` - lower or upper case
- `INSERT` - at position `pos`, delete `len` chars and then insert the `new_string`

```SQL
-- -> `oreplacementinal string string`
SELECT INSERT('original string', 2, 3, 'replacement')
```

- `LEFT`/`RIGHT` - selects X chars from the left/right
- `REPEAT` - repeats string X times
- `TRIM` - trims leading and trailing spaces; not middle