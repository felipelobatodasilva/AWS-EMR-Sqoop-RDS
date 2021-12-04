# EMR-Sqoop-RDS

[__EMR__](https://medium.com/analytics-vidhya/apache-spark-applications-with-amazon-emr-and-s3-services-using-jupyter-notebook-41968a1c2d7) -> Before starting this project, we have to understand what is EMR and why this one is used.

Amazon Elastic MapReduce (EMR) is an Amazon Web Services (AWS) platform for big data processing and analysis using famous open source tools like Apache Spark, Apache Hive, Apache HBase, Apache Flink and Presto. 

EMR provides scalable, flexible and fast computing over petabyte-sized large data.

[__Sqoop__](https://www.javatpoint.com/what-is-sqoop) -> Sqoop is a command-line interface application for transferring data between relational databases and Hadoop

It supports incremental loads of a single table or a free form SQL query as well as saved jobs which can be run multiple times to import updates made to a database since the last import.Using Sqoop, Data can be moved into HDFS/hive/hbase from MySQL/ PostgreSQL/Oracle/SQL Server/DB2 and vise versa.

[__RDS__](https://searchaws.techtarget.com/definition/Amazon-Relational-Database-Service-RDS) -> Amazon Relational Database Service (RDS) is a managed SQL database service provided by Amazon Web Services (AWS). Amazon RDS supports an array of database engines to store and organize data. It also helps with relational database management tasks, such as data migration, backup, recovery and patching.

Amazon RDS facilitates the deployment and maintenance of relational databases in the cloud. A cloud administrator uses Amazon RDS to set up, operate, manage and scale a relational instance of a cloud database. Amazon RDS is not itself a database; it is a service used to manage relational databases.

# Table of Contents  
● [Setting up EMR](#settingupEMR)<br/>

## Setting up EMR <a name="settingupEMR"></a>

We'll need to set up the EMR environment for Sqoop
