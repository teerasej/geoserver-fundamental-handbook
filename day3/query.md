

## แสดงชื่อย่านทั้งหมด

```sql
SELECT name FROM nyc_neighborhoods;
```

## แสดงจำนวนประชากรทั้งหมด

```sql
SELECT Sum(popn_total) AS population
  FROM nyc_census_blocks;
```