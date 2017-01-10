# select multiple columns and rows from dual

```sql
          SELECT 1 AS value, 'one' as name FROM dual
UNION ALL SELECT 2, 'two' FROM dual
UNION ALL SELECT 3, 'three' FROM dual;
```

This can be used in a query with actual tables like this

```sql
SELECT astext.text
FROM numbers,
     (
      SELECT 1 AS value, 'one' as text FROM dual
      UNION ALL SELECT 2, 'two' FROM dual
      UNION ALL SELECT 3, 'three' FROM dual
     ) astext 
WHERE numbers.value = astext.value
  
```
