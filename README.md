# Big Data

This repository contains all assignments for the course "Big Data" (NWI-IBC036) given at the Radboud University.

**Outline**

* Assignments
	* Using a blend of **Docker**, **github**, and **Spark Notebook**
	* Blog posts on “scripted” assignments (4 or 5 in total)
	* Free-format final assignment
		* **Plan**: on a large Hadoop cluster (SurfSara? Q4)
		* Analyze the [CommonCrawl](https://commoncrawl.org/) (A crawl archive of ~225TB in size and more than 2.85 billion web pages)
	* Final presentation: “Showcase Portfolio”

**Grading**

* Midterm Exam: 40%
* Assignments: pass/fail
* Final Exam: 30%
* Final Project: 30%



## Lecture 1

* Big Data: Petabytes of data which are hard to process in terms of volume, velocity and variety (The three V's)
	* **Volume**: We measure more and more; the resulting data is very large already, and it grows faster and faster
	* **Velocity**: The analysis may take too long for appropriate reaction to measurement
	* **Variety**: The data comes in many variants, structured and unstructured
* Why Big Data?
	* We can analyse (and differentiate) to the **level of the individual**
	* We are less likely to miss **rare events**, e.g., those that occur one out of ten million times	
	* We can better account for the **real-time nature of the data**
* Map-reduce: https://en.wikipedia.org/wiki/MapReduce
	* A MapReduce framework (or system) is usually composed of three operations (or steps):
		* **Map**: each worker node applies the map function to the local data, and writes the output to a temporary storage. A master node ensures that only one copy of redundant input data is processed.
		* **Shuffle**: worker nodes redistribute data based on the output keys (produced by the map function), such that all data belonging to one key is located on the same worker node.
		* **Reduce**: worker nodes now process each group of output data, per key, in parallel.
* Implementations of MapReduce
	* [Apache Hadoop](https://en.wikipedia.org/wiki/Apache_Hadoop): Mostly uses data from a persistent storage such as a database and therefor supports larger amounts of data than Spark
	* [Apache Spark](https://spark.apache.org/): Mostly uses data from volatile storage such as RAM
	* [Apache CouchDB](https://en.wikipedia.org/wiki/Apache_CouchDB)
	* [Disco Project](http://discoproject.org/)
	* [Infinispan](https://en.wikipedia.org/wiki/Infinispan)
	* [Riak](https://en.wikipedia.org/wiki/Riak)
* [Spark vs. Hadoop MapReduce: Which big data framework to choose](https://www.scnsoft.com/blog/spark-vs-hadoop-mapreduce)
	* "To make the comparison fair, here we will contrast Spark with Hadoop MapReduce, as both are responsible for data processing. In fact, the key difference between them lies in the approach to processing: Spark can do it in-memory, while Hadoop MapReduce has to read from and write to a disk. As a result, the speed of processing differs significantly – Spark may be up to 100 times faster. However, the volume of data processed also differs: Hadoop MapReduce is able to work with far larger data sets than Spark."
* [How Does Spark Use MapReduce?](https://dzone.com/articles/how-does-spark-use-mapreduce)






