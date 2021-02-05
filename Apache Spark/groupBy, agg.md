https://stackoverflow.com/questions/41890485/aggregate-function-count-usage-with-groupby-in-spark

Example groupBy, agg

```
import org.apache.spark.sql.functions._ //for count()

new_log_df.cache().withColumn("timePeriod", encodeUDF(col("START_TIME"))) 
  .groupBy("timePeriod")
  .agg(
     mean("DOWNSTREAM_SIZE").alias("Mean"), 
     stddev("DOWNSTREAM_SIZE").alias("Stddev"),
     count(lit(1)).alias("Num Of Records")
   )
  .show(20, false)
```