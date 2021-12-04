# EMR-Sqoop-RDS

# Table of Contents

● [Project Overview](#overview)<br/>
● [Setting up Cloud9 for EC2](#settingupClou9)<br/>

## Project Overview <a name="overview"></a>

For this project, we're gonna use EC2, Cloud9, EMR, S3 and RDS as follow with their respective brief explanation, in order to undertand a little bit about what each of them can do and why is used for

[__EMR__](https://medium.com/analytics-vidhya/apache-spark-applications-with-amazon-emr-and-s3-services-using-jupyter-notebook-41968a1c2d7) -> Before starting this project, we have to understand what is EMR and why this one is used.

Amazon Elastic MapReduce (EMR) is an Amazon Web Services (AWS) platform for big data processing and analysis using famous open source tools like Apache Spark, Apache Hive, Apache HBase, Apache Flink and Presto. 

EMR provides scalable, flexible and fast computing over petabyte-sized large data.

With EMR usage, one can use [Sqoop](https://www.javatpoint.com/what-is-sqoop)) and its command-line interface application function for transferring data between relational databases and Hadoop. By Using this one Data can be moved into HDFS/hive/hbase from MySQL/ PostgreSQL/Oracle/SQL Server/DB2 and vise versa.

[__RDS__](https://searchaws.techtarget.com/definition/Amazon-Relational-Database-Service-RDS) -> Amazon Relational Database Service (RDS) is a managed SQL database service provided by Amazon Web Services (AWS). Amazon RDS supports an array of database engines to store and organize data. It also helps with relational database management tasks, such as data migration, backup, recovery and patching.

Amazon RDS facilitates the deployment and maintenance of relational databases in the cloud. A cloud administrator uses Amazon RDS to set up, operate, manage and scale a relational instance of a cloud database. Amazon RDS is not itself a database; it is a service used to manage relational databases.

[__S3__](https://medium.com/analytics-vidhya/apache-spark-applications-with-amazon-emr-and-s3-services-using-jupyter-notebook-41968a1c2d7)
Amazon Simple Storage Service (Amazon S3) offers an object storage service for the internet which is designed to store data (up to 5 terabytes single file) from any kind of source with providing scalability, data availability, security, and performance.

[__Cloud9__](https://aws.amazon.com/cloud9/) -> AWS Cloud9 is a cloud-based integrated development environment (IDE) that lets you write, run, and debug your code with just a browser. It includes a code editor, debugger, and terminal. Cloud9 comes prepackaged with essential tools for popular programming languages, including JavaScript, Python, PHP, and more, so you don’t need to install files or configure your development machine to start new projects.

[__EC2__](https://aws.amazon.com/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc) -> Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides secure, resizable compute capacity in the cloud. It is designed to make web-scale cloud computing easier for developers. Amazon EC2’s simple web service interface allows you to obtain and configure capacity with minimal friction. It provides you with complete control of your computing resources and lets you run on Amazon’s proven computing environment.

## Setting up Cloud9 for EC2 <a name="settingupClou9">

More than anything, you'll need to set up Cloud9 [*resolved*]
