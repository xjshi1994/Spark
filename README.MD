# Spark
## DataFrame
### 1. What is DataFrame
>> DataFram is RDDS full of records with detailed schema
### 2. How to start
* 1. create sparkSession
* 2. '''scala
	import org.apache.spark.sql.SparkSession
	val spark = SparkSession
	.builder()
	.appName("My App")
	.getOrCreate()'''
* 3. Example of creating dataFrame
	* (1a) create dataframe from RDD, schema reflectively inferred  
	'''java
	val tupleRDD = .....// assume RDD[(int, String, String)]    
	val tupleDF = tupleRDD.toDF("bid", "bookname", "publishDate")  
	// if you have an RDD containing sonme kind of class instance  
	case class Person(id: Int, name: String, city: String)  
	val peopleRDD = ....  
	val peopleDF = peopleRDD.toDF  
	'''
	* (1b) create dataframe existing RDD, schema explicitly specified


