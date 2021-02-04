
https://stackoverflow.com/questions/54167792/spark-filter-string-column-by-contains-one-of-list-of-strings



```
val rePattern = interestingThings.mkString("|")
```

```
df.filter(col("foo").rlike(rePattern)
```

