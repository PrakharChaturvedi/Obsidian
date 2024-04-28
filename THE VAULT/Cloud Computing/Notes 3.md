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
	- **Features** : Scala

- **SBS** (Elastic Block Store)

- **Glacier** 

- Storage Gateway