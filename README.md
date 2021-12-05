# EMR-Sqoop-RDS

# Table of Contents

● [Project Overview](#overview)<br/>
● [Setting up EMR](#settingupEMR)<br/>
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

<!-- [link](https://towardsdatascience.com/creating-aws-ec2-and-connecting-it-with-aws-cloud9-ide-and-aws-s3-a6313aa82ec) -->
More than anything, you'll need to set up Cloud9, but before that is needed to get your access key and Secret Key.

For that, you just need to go throgh AWS Console Management and click on IAM as follows

<img src="https://user-images.githubusercontent.com/69978184/144727778-3933843e-8269-4cff-978f-f27e166f42c7.png" width="800" height="400"/>
  
Then, click on "Users" and choose your username, if you don't have it yet, press add user for its creation.

<img src="https://user-images.githubusercontent.com/69978184/144727827-c4c88404-ccf9-442a-bfb3-d3983c490417.png" width="800" height="400"/>

After creating your username, on the Security Credentials tab click on Create Access Key, in order to download .csv file. Inside this sheet generated you'll find your Access & Secret Key. Keep them stored in stored in a safe place, because you are going to use them later for sure.

<img src="https://user-images.githubusercontent.com/69978184/144727920-4f2c081f-d3d4-4c89-bca7-c52e75ed94ad.png" width="800" height="400"/>
  
Hence, you may need to launch an EC2 instance and for that, follow this step-by-step guide and you'll get your EC2 ready to be used as fast as possible.

As soon as you've finished the EC2 launch process, it is about time to connect it with AWS cloud 9
  
From AWS Management Console, inside the Developer Tools choose Cloud9 and then click on Create Environment button

<img src="https://user-images.githubusercontent.com/69978184/144729559-4337c701-e213-4d4c-8efb-d81314188bc4.png" width="800" height="400"/>
  
https://towardsdatascience.com/how-to-create-and-run-an-emr-cluster-using-aws-cli-3a78977dc7f0
