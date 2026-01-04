# What is Hadoop?
Apache Hadoop is a framework used to store and process very large data across many machines(cluster).
Clusters are combination of machines.

# Why Hadoop?
* In Traditional system, there were many failures such as:
	* When Data is too big
	* One Machine crashes
	* Storage is expensive

* Hadoop was introduced to solve this by using:
	* Distributed storage
	* Fault Tolerance
	* Parallel Processing

* Hadoop Core Components:

|Component	|Meaning	|Purpose|
|-----------|-----------|-------|
|HDFS|	Hadoop Distributed File System|	Storage|
|YARN|	Yet Another Resource Negotiator	|Resource management|
|MapReduce|	Programming model	|Batch processing|

# In Modern Systems:
* Spark replaces MapReduce
* Hive replaces raw MapReduce SQL

# What is HDFS?
HDFS is Hadoop's distributed file system. A file is split into blocks and stored on multiple machines.
For example:
* Machine 1 (Data Nodes) =  1 TB, 16 Core, 16 GBRAM
* Machine 2 (Data Nodes) =  1 TB, 16 Core, 16 GBRAM
* Machine 3 (Data Nodes) =  1 TB, 16 Core, 16 GBRAM
* Machine 4 (Data Nodes) =  1 TB, 16 Core, 16 GBRAM

If we have a cluster as c = upload customer.txt on c then it will store on any of those machines above. Master (Name Node) does that operation for you.
Note: If NameNode crashes then we will lose everything and actual data is never stored on  NameNode.

# HDFS Architecture
|Node|	Role|
|----|------|
|NameNode|	Master – stores metadata|
|DataNode|	Workers – store actual data|
|Secondary NameNode|	Backup metadata (not real backup)|

<img width="1280" height="694" alt="image" src="https://github.com/user-attachments/assets/34c7626d-0658-4ac3-b959-c92d2d987b3c" />

* Metadate means:
	* File name
	* File path
	* Block locations
	* Replication info

# HDFS Block and Replication
* Block Size:
	* Default: 128MB
	* Files which are greater than block size still uses 1 block.
* Replication Factor:
	* Default: 3
 	* Each block stored on 3 different DataNodes.
* Why?
	* Fault Tolerance
 	* High Availability

# Hadoop Cluster
* What  is a Cluster?
* A group of machines working together as one-system
  
	|Type|	Description|
	|----|-------------|
	|Single Node|	Practice / local|
	|Multi Node	|Production|

# HDFS vs Local File System

|Feature|	Local FS|	HDFS|
|-------|-----------|-------|
|Storage|	Single machine|	Distributed|
|Fault tolerance|	❌|	✅|
|Handles big data|	❌|	✅|
|Replication|	❌|	✅|

# Big Data
<img width="1280" height="563" alt="image" src="https://github.com/user-attachments/assets/5f85c384-e809-4365-9d02-bbbf4682ca43" />

* Structured Data: Row and Column based Data
<img width="1280" height="410" alt="image" src="https://github.com/user-attachments/assets/7537a66c-57e7-4259-b761-d3937662f627" />

* Semi-Structured Data
<img width="1280" height="646" alt="image" src="https://github.com/user-attachments/assets/168a2519-b1a3-47ea-b52b-68f2a90a27e9" />

* Unstructured Data
<img width="1280" height="690" alt="image" src="https://github.com/user-attachments/assets/9de0a287-06b2-4f02-86f8-f76d3ce38836" />
