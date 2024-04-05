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
	- 