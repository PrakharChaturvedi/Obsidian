#Concepts 
+- Lab of EC2
- Virtualization : 
## 22/03/24
- Module 3 : 
	- Amazon EC2 (Elastic Compute Cloud)
		- Steps :
			- Choose AMI
			- Instance type
			- Network Settings
			- IAM Role
			- User Data
			- Storage options
			- Tags
			- Security group
			- Key pair
	- Elastic block storage v/s EC2 instance store.

- Tags
	- A tag is a label that you can assign o an AWS resource.
		- It exists outside of the instances guest OS.
	- Create rules that specify the sources and which ports that network communications can use.
		- Specify the port number and the protocol, such as Transmission Control Protocol (TCP), User datagram Protocol (UDP),  or internet control message protocol (ICMP).
		- Specify the source that is allowed to use.

- Key Pair 
	- At instance launch, you specify an existing key pair or create a new key pair.
	- A key pair consists of -
		- A public key that AWS store.
		- A private key file that you store.



## Docker 
- Define :
	- Docker is an open source platform that helps a user to package an application and its dependencies into a Docker Container for the development and deployment of software. 
- Flow :
	- Developer -> Docker Container -> Tester
- Types of machine layer :
	- Standard Machine (Layered)  :
		(1) |App A| |App B| |App C|
		(2) |       Bins/ Libs            | 
		(3) |        Host OS             |
		(4) |      Infrastructure     |
	-  Virtual Machine Architecture:
		- [[[Notes 1]]]
	- Docker Container : ![[Pasted image 20240405110302.png]]

- Note : Tester uses software called JBoss for java applications. Then application is uploaded to cloud. As JBoss was unable to work on all the VM's, we had to install it every time for a new Machine (Its a problem which is time and resource consuming).
- ECS : Elastic container Service 
	- A highly scalable, fast, container management service.
	- ECS cluster options:
		- AWS Fargate
		- AWS EC2
	- Kubernetes : open source, software for container architecture.
- ECR : Elastic Container Registry 
	- ...


## AWS Lambda 
- It is a example of PAAS architecture.
- In here we do not manage the server it is managed by AWS, we just have to mage the code part (Client End).
- It is a serverless compute service.
- We just have to pay for the compute time used. 
	- Upload code -> Code compute (Run your code on a schedule or in response to events) -> Code runs (only when it is triggered) -> Pay only for the compute time that you use. 
- Benefits :
	- Pay-per-use.
	- Supports multiple programming language.
	- Completely automated administrator.
- Schedule-based lambda function example :
	- Stop instance of example :
		- Time based cloud watch event -> Lambda function triggered -> EC2 instance stopped.
	- Start instance of example :
		- Time based CloudWatch event -> Lambda function triggered -> EC2 instance starts. 
- Steps :
	- AWS Console Active
	- Services
	- Console

## AWS Elastic Beanstalk
- Serverless
- PAAS with a difference that it is just an easy way to get web applications ip and running from AWS Lambda.
- Managed services :
	- Deployment
		- Java
		- .Net
		- Node
		- Express
		- Microsoft SQL server 
	- Load balancing 
	- Automatic scaling
	- Health monitoring
	- etc....

## Module overview :
- Amazon RDS - DIL
- Amazon DynamoDB - DIL
- Amazon Redshift - DIL
- Amazon Aurora - DIL (5x faster than SQL) 
## Demos 
- Amazon RDS console
- Amazon DynamoDB console
- 

## 12/04/2024
## Amazon EBS
- Enables you to create individual storage volumes and attach them to an Amazon EC2 instance.
- Snapshots
- Data transfer
- 


