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

## Setting up EMR <a name="settingupEMR"></a>
<!-- [link](https://www.knowledgehut.com/tutorials/aws/hadoop-cluster) -->
To create an EMR cluster go through AWS Console Management and look for EMR on the search field and click on it.
 
<img src="https://user-images.githubusercontent.com/69978184/144752224-b19a9c6b-4c32-4561-ac76-aa45ff7662c9.png" width="800" height="400"/>

Hence, click on "Create cluster" to start the creation of your cluster

<img src="https://user-images.githubusercontent.com/69978184/144752267-17d5f83f-15b6-49af-b817-a3815a0b0f8d.png" width="800" height="400"/>

On the next Screen, it's recommended to click on "Go to advanced options", because all of those softwares available and related to EMR can be selected and installed over there

<img src="https://user-images.githubusercontent.com/69978184/144752616-43605f2d-4647-4596-aa03-e22969c147f1.png" width="800" height="400"/>

<img src="https://user-images.githubusercontent.com/69978184/144752843-920ac58d-ca76-4d8a-9f7a-f49c50d15770.png" width="800" height="400"/>
 
1) For this first step just fill all the specific fields you need to
 
 <img src="https://user-images.githubusercontent.com/69978184/144753005-b9357f4a-2ed9-4a46-bfdb-eb0c1337c945.png" width="800" height="400"/>
 
2) For the second step you'll need to select a node to work with

 <img src="https://user-images.githubusercontent.com/69978184/144753478-f0a36e89-7fd1-4842-99a0-cf5d501344ac.png" width="800" height="400"/>

 <img src="https://user-images.githubusercontent.com/69978184/144753612-11bc3ae4-13eb-4013-a7e6-306893022b0f.png" width="800" height="400"/>

 3) On the third step is where you give the name to your cluster and enable the option Logging inside your S3
 
 <img src="https://user-images.githubusercontent.com/69978184/144753851-b42b2260-0fa8-40c1-acee-595a69d6518a.png" width="800" height="400"/>

 4) On the fourth step you select the EC2 Key Pair created previously
 
 <img src="https://user-images.githubusercontent.com/69978184/144758365-97c91ba7-77f9-4194-954d-06de33dafbc8.png" width="800" height="400"/>

Now you may see that he tried for several times to create this cluster, but it didn't work properly, as shown below
 
 <img src="https://user-images.githubusercontent.com/69978184/144757298-c7e9e9e2-f1b0-4423-bc6a-96d015ca9a75.png" width="800" height="400"/>
 
it happens according to the error, due to lack of available instances, in other words, the number of vCPUs for instance type m5.xlarge exceeds the EC2 service quota for that type.

To fix this issue, you may request a [limit increase](https://aws.amazon.com/es/premiumsupport/knowledge-center/ec2-on-demand-instance-vcpu-increase/) 

With Limits Calculator Section, you may see how much do you need for that

<img src="https://user-images.githubusercontent.com/69978184/144757550-3b616bac-7eba-4a11-b8e0-eb7053e1a512.png" width="600" height="400"/>
 
Then request service limit increase and open chat one of the AWS representative
 
<img src="https://user-images.githubusercontent.com/69978184/144757615-11962ddb-9a06-45f4-bc62-eeee0a23286a.png" width="600" height="400"/>
 
<img src="https://user-images.githubusercontent.com/69978184/144757884-d3342d23-64b3-49fd-a550-59e318e7c7d4.png" width="600" height="400"/>
 
and now, the only thing you can do is just to await! :). Within some day, they're gonna give to you a feedback about your request opened.

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

https://www.youtube.com/watch?v=zqyOOyOlcAk
