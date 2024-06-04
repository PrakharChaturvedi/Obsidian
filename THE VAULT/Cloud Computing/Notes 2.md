- **Virtualization** : 
	- Virtualization refers to the creation of a virtual resource such as a server, desktop, operating system,  file, storage or network.
	- Virtualization provides a platform for optimizing complex IT resources in a scalable manner (efficiently growing), which is ideal for delivering services.
	- Characteristics of virtual machine : 
		- Partitioning
		- Isolation 
		- Encapsulation : Encapsulation in virtual machines is like packing up a whole computer system into a single box. This box contains everything the computer needs to run - like its operating system and all the software it uses. This makes it easy to move the virtual machine around and use it on different computers without causing any problems for the main computer.
	- Benefits : 
		1. Easy setup of new systems.
		2. No need to invest in additional hardware for testing and debugging setups.
		3. Quick recovery from system corruption.
		4. Easy relocation and migration of systems.
		5. Seamless transition to more powerful hardware using snapshots.
		6. Simplified remote management, reducing the need for physical access to data centers.
		7. Ability to run multiple operating systems simultaneously on one server.

- **Hypervisor** : 
	- A hypervisor is like a virtual landlord for computers. It's software that creates and runs virtual machines on a physical computer. Just like a landlord manages different apartments in a building, a hypervisor manages multiple virtual machines on a single physical computer. 
	- It helps these virtual machines share the resources of the physical computer, like its CPU, memory, and storage, without interfering with each other. So, the hypervisor acts as a mediator, making sure everything runs smoothly in the virtual world.
	- Types :
		- Native hypervisor
			- Think of this like a direct manager for virtual machines. It runs directly on the computer's hardware, no extra software needed. It's like having a boss who manages everything from the ground up.
		- Hosted hypervisor
			- This one works like a manager who needs an assistant. It runs on top of a regular operating system (the assistant), and then it creates and manages virtual machines. It's like having a manager who relies on someone else for support.
		- Embedded hypervisor
			- Integrated into a processor on a separate chip. Using this type of hypervisor, a service provider gains performance improvements.


- **Containers** :
	- A container is like a virtual box for software. It wraps up an application and all its dependencies into a package, making it easy to run anywhere. Unlike virtual machines, containers share the same operating system kernel, which makes them lightweight and quick to start.
	- Advantages : 
		- **Lightweight:** Containers consume fewer resources compared to VMs.
		- **Faster Deployment:** Containers start quickly, enabling rapid deployment and scaling.
		- **Portability:** Containers can run consistently across different environments.
		- **Isolation:** Provides application-level isolation, ensuring one container doesn't affect others.
		- **Scalability:** Easy to scale containers horizontally or vertically to meet demand.
		- **Efficiency:** Allows for efficient resource utilization due to sharing the host OS kernel.
	- Disadvantages :
		- **Security Concerns:** Containers share the host OS kernel, raising security risks if not properly configured.
		- **Limited Isolation:** Containers provide less isolation than VMs, potentially leading to conflicts between applications.
		- **Complex Networking:** Networking between containers can be complex, requiring additional setup.
		- **Persistence:** Containers are typically ephemeral, meaning data inside a container may not persist unless specifically managed.
		- **Tooling Overhead:** Requires additional tooling for managing containers effectively, which may add complexity to the infrastructure.

- **SLA (Service Level Agreement)** :
	- An SLA is a contract between a service provider (either internal or external) and the end user that  defines the level of service expected from the service provider.
	- A service level agreement (SLA) serves as both a blueprint and warranty for cloud computing.
	- Every company that buys any service from a cloud service provider must either accept a standard  service level agreement (SLA) from the provider or negotiate such an agreement.
	- SLA includes :
		- Response times
		- Availability on any given day
		- Overall uptime target
		- Agreed-on response times and procedures in the event a service goes down.

- **VPC (Virtual Private Cloud)** :
	- Hybrid cloud mechanism which has private cloud within public cloud provider’s infrastructure.
	- VPC managed by public cloud provider -> gives a section of it to the pvt user.
	- VPC are specifically for those who want to benefit from cloud yet have some concerns about privacy,  security and loss of control over proprietary data.
	- Example : Amazon VPC and Google app engine.
	- Advantages :
		- Bandwidth efficiency
		- Application performance
		- Security 

- **IaaS Networking** :
	- In Infrastructure as a Service (IaaS) networking, cloud resources are virtualized, including network resources. This is achieved through virtual switches, which divide a physical network into logical partitions. Virtual networks resemble LANs and can be segmented into automatically routed subnets.
	- Virtual LANs (VLANs) extend an enterprise's private network and can be accessed via encrypted Virtual Private Network (VPN) connections. A hypervisor enables sharing a single physical network interface among multiple virtual machines, each equipped with one or more virtual network interfaces. This setup optimizes resource utilization and facilitates flexible networking configurations in the cloud environment.
	- Storage : 
		- In Infrastructure as a Service (IaaS) storage, complexity arises from creating resource pools that include virtualized storage, tied together with orchestration to meet cloud requirements like VM mobility and instant snapshots.
	Storage services are categorized based on how they're consumed:
	1. **File Storage:** Offers shared file systems using protocols like NFS or SMB/CIFS for accessing shared folders.
	2. **Block Storage:** Provides fixed-size raw storage volumes treated as independent disk drives, commonly used in SAN, iSCSI, or local disks. These volumes are formatted with file systems like FAT32, NTFS, EXT3, or EXT4.
	3. **Object Storage:** Stores data along with metadata, accessed directly through APIs or HTTP/HTTPS. It's ideal for unstructured data like photos, videos, and log files, offering data replication across data centers and simple web service interfaces for access, ensuring data integrity and availability.
	- IaaS Security issues :
		- Data Leakage Protection and Usage Monitoring
		- End-to-End Logging and Reporting
	- IaaS Security : 
		- Authentication and authorization
		- Infrastructure hardening
		- End-to-End encryption
	- Cloud data protection :
		- Data Integrity
		- Storage management
		- Infrastructure security
	- Cloud pricing :
		- On-demand pricing
		- Reserved instances
		- Spot pricing 
		- Prepared VM access
		- Recurring resource pooling
		- Prepared Consumption
	- Benefits :
		- Cost saving.
		- Scalability and Flexibility.
		- Faster time to market.
		- Support for DR, BC and high availability.
		- Focus on business growth.
	- Examples :
		- Amazon EC2
		- Windows Azure
		- EBS
		- Google compute engine

- **PaaS (Platform as a service)** :
	- Complete development and deployment environment in the cloud with  resources that enable you to deliver everything from simple cloud-based apps to sophisticated, cloud-enabled  enterprise applications.
	- You purchase the resources you need from a cloud service provider on a pay-as-you-go basis and access them over a secure Internet connection.
	- Benefits :
		- Software developers
		- Web developers
		- Businesses
	- Infrastructure includes :
		1. Infrastructure such as servers, storage and networking
		2. Middleware (such as IIS, Tomcat, Caching Services)
		3. Development tools
		4. Business Intelligence (BI) services
		5. Database management systems (SQL Server, Oracle, MySQL)
		6. Runtime (JRE and .NET Framework)
	- Examples :
		- NetSuite
		- Window Azure
		- AWS Elastic Beanstalk
		- Google app engine
	- Risks :
		1. **Lack of Control Over Virtual Machines**:
		   - Users have no control over the underlying virtual machines processing their data, potentially limiting customization and performance optimization.
		2. **Limited Flexibility Compared to IaaS**:
		   - PaaS solutions offer less flexibility than Infrastructure as a Service (IaaS), restricting the ability to create and delete multiple virtual machines simultaneously and limiting resource management options.
		3. **Predefined Programming Model**:
		   - PaaS platforms enforce a predefined programming model, leading to vendor lock-in issues as users are constrained to using only the languages and frameworks provided by the platform.
		4. **Difficulty in Migration**:
		   - Migration to the cloud can be challenging, especially if existing code or applications are not supported by the PaaS provider, potentially requiring significant reengineering efforts.


- IaaS vs PaaS![[Pasted image 20240321205824.png]]

- **SaaS (Software as a Service)** :
	- Software as a service (SaaS) allows users to connect to and use cloud-based apps over the Internet. Common  examples are email, calendaring, and office tools such as Microsoft Office 365.
	- Software as a Service (SaaS) offers a complete software solution on a pay-as-you-go basis from a cloud service provider. Users access the application over the Internet, typically through a web browser, with all infrastructure, middleware, software, and data hosted in the provider's data center. 
	- The provider manages hardware, software, availability, and security, allowing organizations to quickly deploy applications with minimal upfront costs.
	- **SaaS Benefits:**
		- Enhanced business agility with anytime, anywhere access.
		- Operational continuity during natural disasters.
		- Resource sharing across time zones or geopolitical zones.
		- Support for sustainable initiatives like remote work and reduced environmental impact.
	- **SaaS Risks:**
		1. **Usage Risk:**
		    - Varies based on the criticality of functions and sensitivity of data stored.
		2. **Data Security Risk:**
		    - Concerns about how the service provider handles data, including encryption, storage controls, and access management.
		3. **SaaS Provider Operational Risk:**
		    - Reliability issues such as uptime SLA, support availability, compliance, and disaster recovery strategies.
		4. **SaaS Provider Application Risk:**
		    - Inherent risks within the application, including authentication, authorization, development practices, and vulnerability management.
	- **Traditional Software vs SaaS:**
		- **Traditional Software:**
			- Capital expense for purchase.
			- Operating expenses for installation, updates, and maintenance.
			- Involves multiple steps for acquisition, installation, patching, and updating.
		- **SaaS:**
			- Prebuilt products with provided functionality.
			- Consumed as-is without significant customization.
			- Simplified management with licensing and reliance on provider for maintenance.
	- Examples :
		- SalesForce.com
		- Office 365
		- Zoho 
		- Google G Suite


- ***Evaluation of SAAS*** 
	- <u>User Perspective :</u>
		- 1. **Security Standards:**
		    - Assess the SaaS provider's security processes and standards to ensure compliance with organizational security requirements.
		    - Collaborate with the vendor to establish a Service Level Agreement (SLA) for security, including penalties for service failures.
		    - Verify disaster recovery, backup, and restore processes.
		2. **Flexibility and Customization:**
		    - Evaluate the provider's flexibility in adjusting subscription plans, adding or dropping features, and managing seats.
		    - Ensure the ability to cancel subscriptions without penalties and assess the ease of customizing the application to meet organizational needs.
		    - Consider data portability and the process for retrieving data upon subscription cancellation.
		3. **SLA Performance History:**
		    - Examine the provider's track record in meeting SLA commitments to gauge reliability.
		    - Prioritize providers with a history of consistently meeting or exceeding SLA requirements.
		4. **Business Viability and Future Outlook:**
		    - Assess the long-term viability of the SaaS provider, aiming for a stable business partner.
		    - Look into the provider's experience in delivering SaaS solutions, financial stability, and predicted growth trajectory.
	- <u>Vendor Perspective :</u>
		- 1. **Financial Concerns:**
		    - Adaptation to a subscription-based revenue model necessitates a focus on customer retention to ensure consistent cash flow, given the lower switching costs for customers in the cloud model.
		2. **Compliance Management:**
		    - Ensure compliance with national and global regulations to meet legal requirements and maintain trust with customers.
		3. **Operational Efficiency:**
		    - Maintain 24/7 operability and implement robust business continuity plans to minimize downtime and ensure uninterrupted service delivery.
		    - Implement high-caliber data management and security protocols to safeguard customer data.
		4. **Configuration and Customization Policies:**
		    - Leverage economies of scale offered by SaaS deployment, such as multitenancy, to enhance profitability.
		    - Establish policies governing the degree of software tailoring allowed to meet individual client needs while maintaining operational efficiency.

- **Load Balancing*** :
	- Load balancing optimizes resource utilization, throughput, latency, response time, and prevents system overload by distributing service requests across available resources.
	- **Load Balanced Network Resources:**
	    - Network interfaces and services (e.g., DNS, FTP, HTTP).
	    - Intelligent switches for connections.
	    - Computer system processing assignments.
	    - Storage resources.
	    - Access to application instances.
	- **Benefits:**
	    - Provides redundancy for reliability through managed redirection.
	    - Enhances fault tolerance when coupled with failover mechanisms.
	    - Essential for server farms, computer clusters, and high availability applications.
	- **Load Balancing Mechanisms:**
	    - Utilizes scheduling algorithms such as round robin, weighted round robin, fastest response time, least connections, and weighted least connections.
	    - Assigns service direction based on incoming requests.
	- **Session Persistence:**
	    - Ensures subsequent traffic related to a session is routed to the same resource for continuity.
	    - Achieved through session tickets, client-side cookies, or URL modification.
	    - Session data can be stored in databases and replicated across multiple load balancers.
	- **Optimal Method:**
	    - Session cookies stored on the client have minimal overhead for load balancers, allowing independent resource selection.

- **Advanced Load Balancing:**
	- **Workload Management:**
	  - Load balancers analyze resource utilization, response time, queue length, connection latency, and other factors to assign tasks efficiently.
	- **Health Monitoring:**
	  - Continuously polls resources for health status and can activate standby servers when needed (priority activation).
	- **Asymmetric Loading:**
	  - Balances workload based on a resource's capacity, allowing for optimized resource utilization.
	- **Traffic Optimization:**
	  - Performs HTTP traffic compression to reduce bandwidth usage and improve response times.
	  - Utilizes TCP offload and buffering to enhance network performance.
	- **Security Features:**
	  - Implements security measures such as authentication and access control to protect against unauthorized access.
	- **Packet Shaping:**
	  - Utilizes content filtering and priority queuing to shape network traffic, ensuring optimal performance for critical applications.

- **Application Delivery Controller (ADC):**
	- **Functionality:**
		- Combines load balancing and application server capabilities.
		- Placed between a firewall/router and a server farm to provide web services.
	- **Virtual IP Address (VIP) Mapping:**
		- Assigned a VIP that maps to a pool of servers based on application-specific criteria.
	- **Network and Application Layer Device:**
		- Operates at both network and application layers, providing comprehensive traffic management.
	- **Aliases:**
		- Also known as a content switch, multilayer switch, or web switch, reflecting its varied functionalities.

- **Type 1 and Type 2 Virtual Machines:**
	- **Type 1 Hypervisor (Bare Metal Hypervisor):**
		 - Runs directly on the physical hardware of the host system.
		 - Manages guest operating systems directly, without relying on a host OS.
		 - Offers high performance and efficiency.
		- Examples include VMware ESXi, Microsoft Hyper-V, and Xen.
	- **Type 2 Hypervisor (Hosted Hypervisor):**
		 - Runs on top of a conventional operating system.
		 - Relies on a host operating system for resource management.
		  - Typically used for development, testing, and desktop virtualization.
		  - Examples include VMware Workstation, Oracle VirtualBox, and Parallels Desktop.
	- **Key Differences:**
		- **Installation:**
			- Type 1 hypervisors are installed directly on hardware, while Type 2 hypervisors are installed on top of a host operating system.
		- **Performance:**
			- Type 1 hypervisors generally offer better performance and efficiency since they bypass the host OS.
		- **Use Cases:**
			- Type 1 hypervisors are preferred for server virtualization and enterprise environments due to their performance and scalability.
			- Type 2 hypervisors are suitable for desktop virtualization, development, and testing scenarios where performance is less critical.

- **VMware vSphere:**
	- **Definition:**
	    - VMware vSphere is a management infrastructure framework that virtualizes system, storage, and networking hardware to create cloud computing infrastructures.
	- **Components:**
	    - **vCompute:** Aggregates servers into a pool for assignment.
	    - **vStorage:** Aggregates storage resources into a pool for assignment.
	    - **vNetwork:** Creates and manages virtual network interfaces.
	    - **Application Services:** Includes features like High Availability (HA) and Fault Tolerance.
	    - **vCenter Server:** A provisioning, management, and monitoring console for VMware cloud infrastructures.
	- **Functionality:**
	    - Provides a set of services for applications to access cloud resources efficiently.
	    - Enables aggregation and management of server, storage, and network resources.
	    - Offers features like HA and Fault Tolerance for enhanced reliability and availability.

- DaaS (Data as a Service) 
	- DaaS is similar to software as a service, or SaaS, a cloud computing strategy that involves delivering applications to end-users over the network, rather than having them run applications locally on their devices.
	- DaaS outsources most data storage, integration, and processing operations to the cloud.
	- Examples :
		- Urban Mapping, a geography data service, provides data for customers to embed into their own websites and applications.
		- Xignite is a company that makes financial data available to customers.
		- D&B Hoovers provides customers with business data on various organizations
	- Benefits :
		- Minimal setup time
		- Improved functionality
		- Greater flexibility
		- Cost saving
		- Automated maintenance
		- Smaller staff requirements
	- Challenges :
		- **Challenges of DaaS (Desktop as a Service):**
			1. **Security Risks:**
			   - Moving data to cloud infrastructure and transferring it over the network can expose organizations to security threats. Encryption for data in transit helps mitigate these risks.
			2. **Compliance Complexity:**
			   - Compliance challenges may arise when sensitive data is moved to the cloud. Organizations must ensure they meet specific compliance requirements, potentially requiring hosting DaaS on servers located in specific countries.
			3. **Limited Tool Options:**
			   - DaaS platforms may restrict users to a set of tools hosted on or compatible with the platform, limiting flexibility. Choosing a DaaS solution with broader tool compatibility helps address this challenge.
			4. **Data Transfer Time:**
			   - Transferring large volumes of data to a DaaS platform can be time-consuming due to bandwidth limitations. Data compression and edge computing strategies can help accelerate transfer speeds when bandwidth is limited.

- NoSQL as a Service 
	- NoSQL databases enable you to store data with flexible schema and a variety of data models. These databases are relatively easy for developers to use, and have the high performance and functionality needed for modern applications.
	- NoSQL AWS databases can hold large volumes of data while still providing low latency.	
	- As part of AWS database offerings, there are six types of NoSQL databases you can select from along with a variety of managed and self-managed database services. These database services are designed to support your cloud-native workloads and smoothly integrate with existing AWS resources. ![[Pasted image 20240321225821.png]]

