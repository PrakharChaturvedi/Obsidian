## AWS Platform and infrastructure
- Diagram : ![[Pasted image 20240428122014.png]]
- Amazon Web Services provides highly scalable computing infrastructure that enables organizations around the world to requisition compute power, storage, and other on-demand services in the cloud.  These services are available on demand so a customer doesn’t need to think about controlling them or maintaining them.  Customers access the services when they need them and pay for only what they use.  One of the primary benefits of the AWS cloud is that it enables companies of all sizes to focus on the differentiating factors of their business as opposed to the infrastructure required to run it.
- **Region :**  
	- It is a physical location in the world which consist of availability zones. 
	- Examples : US EAST (N. Virginia), EU (Ireland), US EAST (Ohio). 
	- AWS has **33 regions**.
	- Each region is completely independent.
	- Every Region is physically isolated from and independent of every other Region in terms of location, power, water supply, etc.
	- This level of isolation is critical for workloads with compliance requirements where guarantees must be made that user data does not leave a particular geographic region. The presence of AWS Regions worldwide is also important for workloads that are latency-sensitive and need to be located near users in a particular geographic area.
	- Inside each Region, you will find two or more availability zones with each zone hosted in separate data centers from another zone.
- **Availability Zones :** 
	- Consists of one or more discreate data centers, each with redundant power, networking and connectivity, housed in separate data facilities. 
	- AWS has **58 availability zones**. 
	- Each zone is completely isolated. 
- **Edge locations :** 
	- These locations are strategically positioned points in the AWS network optimized for low-latency content delivery, ensuring that data reaches users swiftly. 
	- In contrast, AWS regions are larger geographic areas with multiple Availability Zones.   


## Compute server types :
 - **EC2** (Amazon Elastic compute cloud)
	 - <font color="#ffc000">Virtual Computing Environment</font>: Offers web service interfaces to launch instances with various operating systems and configurations.
	- <font color="#ffc000">Launch and Manage Instances</font>:
	    - <font color="#00b050">Select an AMI</font> : Choose from pre-configured Amazon Machine Images (AMIs) or create your own with your applications, data, and settings.
	    - <font color="#00b050">Configure Security and Network Access</font> : Set up permissions and access controls for your instances.
	    - <font color="#00b050">Choose Instance Type</font> :  Select from a range of instance types and sizes depending on your needs.
	    - <font color="#00b050">Start, Terminate, and Monitor Instances</font> : Manage your instances using web service APIs or management tools.
	- <font color="#ffc000">Flexible Deployment</font>:
	    - <font color="#00b050">Multiple Locations</font> : Option to deploy in multiple regions for redundancy and latency optimization.
	    - <font color="#00b050">Static IP Endpoints</font> : Utilize static IP addresses for consistent endpoint connections.
	    - <font color="#00b050">Persistent Block Storage</font> : Attach durable storage to your instances for data persistence.
	- <font color="#ffc000">Pay for Usage</font>: Only pay for resources consumed, such as instance-hours and data transfer.
	- <font color="#ffc000">Variety of Instance Types</font>:
	    - Offers 14 types of instances ranging from Micro to High I/O and Cluster Compute instances.
	    - Instance types are categorized based on configuration and use case, including High Memory for databases, High CPU for computational workloads, and standard instances for general purposes like web tier frontend.
	- <font color="#ffc000">Flexible Configurations</font>: Customize instances to fit your specific workload and application needs.

 - **AMI** (Amazon Machine Image)
	 - Here is a summary of Amazon EC2 in bullet points:
		- <font color="#ffc000">Virtual Computing Environment</font>: Offers a true virtual environment with web service interfaces for managing instances.
		- <font color="#ffc000">Launch Instances</font>: 
			- <font color="#00b050">Select an AMI</font>: Choose a pre-configured Amazon Machine Image or create a custom AMI with your applications and data.
			- <font color="#00b050">Configure Security</font>: Manage network access and permissions for your instance.
		- <font color="#ffc000">Manage Instances</font>: 
			- **Choose Instance Type**: Select from a range of types based on your needs.
			- **Start, Terminate, and Monitor**: Control your instances using web service APIs or management tools.
	- <font color="#ffc000">Deployment Options</font>:
		- <font color="#00b050">Multiple Locations</font>: Deploy in different regions for redundancy and low latency.
		- <font color="#00b050">Static IP Endpoints</font>: Utilize static IP addresses for consistent connectivity.
		- **Persistent Storage**: Attach block storage to your instances for data persistence.
	- <font color="#ffc000">Cost-Efficiency</font>: Pay for only the resources consumed, such as instance-hours and data transfer.

- **Auto Scaling** 
	 - Auto-scaling in AWS dynamically adjusts the number of Amazon EC2 instances in your application based on demand. It ensures optimal resource usage and cost-effectiveness by automatically scaling out to handle increased demand and scaling in to reduce capacity when demand decreases. 
	 - Users can set scaling policies based on metrics such as CPU utilization, network traffic, or custom metrics. This feature enhances application performance and availability while minimizing costs. Auto-scaling supports different strategies, including maintaining a fixed number of instances or scaling based on scheduled events.

## Cloud Storage
- **S3** (Simple Storage Service)
	- Amazon Simple Storage Service (S3) is a scalable, durable, and secure object storage service provided by Amazon Web Services (AWS). It allows you to store and retrieve any amount of data, at any time, from anywhere on the web. S3 is designed for durability and availability, ensuring that your data is protected and accessible when you need it.
	- It's a bucket = folder, can store unlimited objects of size => 1B to 5 TB; no bucket size limit.
	- **Features** : Scalability, durability, security, accessibility, storage classes, cost-efficient.
	- Is accessed through HTTP/HTTPS 
- **EBS** (Elastic Block Store)
	- Amazon Elastic Block Store (EBS) is a scalable block storage service provided by Amazon Web Services (AWS). It offers persistent storage volumes for use with Amazon EC2 instances. EBS provides high-performance, durable storage that can be dynamically provisioned and managed to meet the storage needs of your applications.
	- Storage Volumes = Virtual Disks, it's built to be used with AWS EC2 instance - create, attach, backup, restore and delete. These volumes behave like unformatted block devices for Linux and windows instances.
	- **Features** : Persistent storage, scalability, performance, snapshots, security and integration with EC2.
	- Can use to create RAID configuration for a server
- **Glacier**
	- Amazon Glacier is an extremely low-cost storage service that provides secure and durable storage for data archiving and backup. In order to keep costs low, Amazon Glacier is optimized for data that is infrequently accessed and for which retrieval times of several hours are suitable.
	- **Low-Cost Archival Storage**: Provides secure and durable storage optimized for data that is infrequently accessed, with retrieval times of several hours.
	- **Cost-Effective**: Storage costs as low as $0.01 per gigabyte per month, offering significant savings compared to on-premises solutions.
	- **Data Storage and Organization**:
		- **Archives**: Store data as archives, which can be a single file or a combination of files.
		- **Vaults**: Organize archives into vaults for better data management and access control.
	- **Data Retrieval**:
		- **Initiate Jobs**: Retrieve data from Glacier by initiating a job, which typically completes in 3 to 5 hours.
	- **APIs and Monitoring**:
		- **Use APIs**: Utilize AWS Management Console or Amazon Glacier APIs to create vaults, upload, and retrieve archives.
		- **Monitor Jobs**: Track the status of jobs using APIs and optionally receive notifications via Amazon SNS when jobs complete.
	- **Pay for Usage**: Monthly billing is based on the amount of data stored and transferred.
- **Storage Gateway**
	- Amazon Storage Gateway is a hybrid cloud storage service provided by Amazon Web Services (AWS) that connects on-premises environments with cloud storage, allowing businesses to leverage the scalability and cost-effectiveness of the cloud while maintaining local performance and latency. 
	- Storage Gateway offers three types of gateways to meet different storage needs: 
		- **File Gateway**: Translates on-premises file-based data to object storage in Amazon S3, providing a local file share while storing data in S3.
		- **Volume Gateway**: Offers block storage volumes that are backed by Amazon S3, either as cached volumes (storing data locally and in the cloud) or stored volumes (keeping full data copies on-premises and in the cloud).
		- **Tape Gateway**: Provides a virtual tape library interface that enables businesses to move tape backups to the cloud, using Amazon S3 and Amazon S3 Glacier for data archiving.
	- Storage gateway service connects an on-premise software appliance with cloud-based storage.
	- Use case : 
		- Backup/Restore on-premise data.
		- Setting up test/dev environments with production data.
		- Migrating applications to the cloud. 
		- On-premise DR/COOP to AWS.

## IAM (Identity and access management)
- AWS IAM enables you to securely control access to AWS services and resources for your users. IAM enables you to create and manage users in AWS, and it also enables you to grant access to AWS resources for users managed outside of AWS in your corporate directory. IAM offers greater security, flexibility, and control when using AWS.
- IAM enables identity federation between your corporate directory and AWS services. This enables you to use your existing corporate identities to grant secure and direct access to AWS resources, such as Amazon S3 buckets, without creating a new AWS identity for those users. 
- Allows customers to 
	- Create users
	- Assign individual passwords, access keys, multi-factor authentication devices.
	- Grant fine-grained permissions
	- Optimally grant them access to the AWS console.
	- Organize users in groups.


## Database 
- **DynamoDB**
	- **Managed NoSQL Database**: Amazon DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability.
	- **High Performance**: Offers low-latency, high-throughput read and write operations for applications.
	- **Automatic Scaling**: Supports on-demand and provisioned capacity modes for automatic scaling of throughput and storage.
	- **Security**: Provides data encryption at rest and in transit, and integrates with AWS Identity and Access Management (IAM) for access control.
	- **Backup and Recovery**: Offers point-in-time recovery and continuous backups for data protection.
	- **Global Tables**: Allows you to create globally distributed tables for low-latency access across multiple regions.
- **ElasticCache**
	- **Managed In-Memory Data Store**: Amazon ElastiCache is a managed service that provides in-memory caching and data storage using Redis or Memcached.
    - **High Performance**: Delivers sub-millisecond latency, ideal for accelerating application performance.
    - **Scalable**: Automatically scales the data store according to demand.
    - **Data Persistence**: Supports persistence and backup options for Redis clusters.
    - **Security**: Offers data encryption, VPC support, and integration with IAM for secure access.
- **RDS**
	- **Managed Relational Database**: Amazon Relational Database Service (RDS) is a managed service that offers various relational database engines, such as MySQL, PostgreSQL, SQL Server, Oracle, and MariaDB.
	- **Automated Management**: Handles tasks such as backups, patching, and monitoring automatically.
	- **Scalability**: Supports read replicas and automatic scaling for enhanced performance.
	- **High Availability**: Provides multi-AZ deployments for improved availability and durability.
	- **Security**: Offers data encryption at rest and in transit, and integrates with IAM for access control.
- **SimpleDB**
	- **NoSQL Database**: Amazon SimpleDB is a NoSQL database service designed for simpler data storage and retrieval with a focus on ease of use.
	- **Schema-Free**: Allows you to store data in a flexible, schema-free format.
	- **Querying and Indexing**: Supports simple querying and automatic indexing for quick data retrieval.
	- **Scalability**: Automatically scales to handle varying data loads.
	- **Cost-Effective**: Offers a pay-as-you-go pricing model based on usage.
- **Redshift**
	- **Data Warehousing**: Amazon Redshift is a managed data warehousing service designed for analytics and business intelligence.
	- **Scalable**: Provides scalable data storage and query processing capabilities.
	- **High Performance**: Delivers fast query performance using columnar storage and parallel processing.
	- **Data Integration**: Supports data loading from various sources, such as S3, DynamoDB, and on-premises databases.
	- **Security**: Offers data encryption, VPC support, and integration with IAM for secure access.
	- **Cost-Effective**: Offers different pricing options, including on-demand and reserved instances, for cost-effective usage.

## Amazon CloudFront 
- It is a web service for content delivery. It integrates with other amazon web services to give developers and business and easy way  to distribute content to end users with low latency, high data transfer speeds, and no commitments.
- Supports download, streaming, live streaming, and dynamic content.
- Use cases : 
	- Video and rich media, online gaming, Interactive agencies, software downloads, static websites.
	- Static web content that must be delivered to global user base at highest bandwidth/ lower latency / lowest cost.

## Application Services 
- **SNS** (Simple Notification Service):
    - **Messaging Service**: Amazon SNS is a fully managed pub/sub messaging service that enables you to send messages to a variety of endpoints.
    - **Message Delivery**: Supports multiple delivery protocols, including SMS, email, and HTTP.
    - **Flexible Messaging**: Allows you to create topics and subscribe endpoints to receive notifications.
    - **Integration**: Easily integrates with other AWS services for automation and alerts.
    - **Scalability**: Handles high-throughput messaging and scales with demand.
    - **Security**: Provides access control through AWS Identity and Access Management (IAM).
- **SQL** (Structured Query Language):
    - **Database Language**: SQL is a programming language used for managing and querying relational databases.
    - **Data Manipulation**: Allows you to insert, update, delete, and retrieve data from tables.
    - **Data Definition**: Supports creating, altering, and dropping database schema objects like tables and indexes.
    - **Standardized**: Widely adopted language for interacting with databases across various platforms.
    - **Efficient Querying**: Provides optimized querying capabilities for large datasets.
    - **Compatibility**: Works with different relational database management systems.
- **SWF** (Simple Workflow Service):
    - **Workflow Management**: Amazon SWF is a fully managed workflow service for coordinating tasks and processes across distributed applications.
    - **Task Orchestration**: Manages and coordinates individual tasks and their dependencies.
    - **Durability and Reliability**: Ensures tasks are completed and retried in case of failures.
    - **Flexible**: Supports complex workflows and diverse use cases.
    - **Visibility**: Provides visibility into workflow executions and state tracking.
    - **Integration**: Easily integrates with other AWS services and on-premises systems.
- **CloudSearch**:
    - **Managed Search Service**: Amazon CloudSearch is a managed search service for quickly and easily setting up and managing search domains.
    - **Search Features**: Offers full-text search, faceted search, and filtering capabilities.
    - **Scalability**: Automatically scales to handle varying search loads.
    - **Ease of Use**: Simple to set up and manage through the AWS Management Console.
    - **Integration**: Supports data indexing from various data sources, such as S3 and DynamoDB.
    - **Analytics**: Provides insights into search usage and performance.
- **SES** (Simple Email Service):
    - **Email Sending Service**: Amazon SES is a managed service for sending and receiving email.
    - **Reliable Delivery**: Offers high deliverability rates and compliance with email best practices.
    - **Scalable**: Handles large volumes of email with ease.
    - **Multiple Use Cases**: Supports transactional emails, marketing campaigns, and more.
    - **Integration**: Easily integrates with other AWS services and applications.
    - **Cost-Effective**: Offers competitive pricing based on email usage.

## EMR (Amazon Elastic MapReduce)
- Amazon Elastic MapReduce (Amazon EMR) is a web service for processing vast amounts of data using a hosted Hadoop framework.
- It utilizes Amazon EC2 and Amazon S3 for scalable, web-scale infrastructure.
- EMR allows instant provisioning of capacity for data-intensive tasks such as data mining, web indexing, and scientific simulations.
- Users can focus on data analysis without the need for complex Hadoop cluster setup or management.
- Supports various applications, including machine learning, data warehousing, and financial analysis.
- Integrates with Cloudera, Hive, and Karmasphere Studio, as well as other libraries such as MapR and Matlab.

## Networking 
- **ELB** (Elastic load balancing)
	- Elastic Load Balancing helps ensure your application remains highly available and responsive to users by managing traffic and providing resilience in case of instance failures.
	- **Traffic Distribution**: Automatically distributes incoming application traffic across multiple Amazon EC2 instances for balanced workload management.
	- **Fault Tolerance**: Enhances fault tolerance by routing traffic only to healthy instances and bypassing unhealthy ones.
	- **Auto-Scaling**: Seamlessly scales load balancing capacity in response to changes in incoming application traffic.
	- **Health Monitoring**: Continuously monitors the health of instances and reroutes traffic as needed to maintain optimal performance.
	- **Availability Zone Flexibility**: Can operate within a single Availability Zone or across multiple zones for greater consistency and resilience.
	- **VPC Compatibility**: Can be used within an Amazon Virtual Private Cloud (VPC) to distribute traffic between different application tiers.
- **Route 53**
	- 
- **VPC** 