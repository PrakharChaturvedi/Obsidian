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
 - **EC2**
	 - 
 - **Amazon Machine Image**
 - **Auto Scaling**