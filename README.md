# AWS-DEVOPS
<pre>

from pyspark.sql import SparkSession

# Create Spark session
spark = SparkSession.builder \
    .appName("CSV to Parquet") \
    .getOrCreate()

# Read CSV
df = spark.read.csv("data.csv", header=True, inferSchema=True)

# Show data
df.show()

# Convert to Parquet
df.write.parquet("data.parquet", mode="overwrite")

spark.stop()
</pre>
