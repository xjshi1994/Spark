# Spark
## DataFrame
### 1. What is DataFrame
>> DataFram is RDDS full of records with detailed schema
### 2. How to start
>> 1. create sparkSession
>> 2.
 '''scala
	import org.apache.spark.sql.SparkSession
	val spark = SparkSession
	.builder()
	.appName("My App")
	.getOrCreate()
'''
