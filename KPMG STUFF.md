
## AZURE Tools and Services : 
#### Core Computing and Hosting :-
- **_Azure Virtual Machine (VMs)_**
    - **Use when:** You need full control (OS, runtime, configs), or want to lift-and-shift an app.
    - **Why it’s great:**
        - Run any OS or app
        - Pay only when running
        - Insanely flexible for dev/testing/prod
        - Scalable and suitable for almost any workload
- **_Azure App Service_**
    - **Use when:** You want to deploy web apps/APIs without dealing with servers.
    - **Why it’s great:**
        - Deploy code in minutes
        - Auto-scaling built in
        - Perfect for MERN, .NET, Java, Python, Node
        - Zero infrastructure management
- **_Azure Kubernetes Service (AKS)_**
    - **Use when:** You’re running microservices or containerized apps at scale.
    - **Why it’s great:**
        - Easiest way to run containers at scale
        - Handles updates, scaling, clusters
        - Ideal for microservices
        - Azure manages underlying cluster setup and operations
- **_Azure Functions_**
    - **Use when:** You want tiny serverless code that runs on events (cron, API hits, DB triggers).
    - **Why it’s great:**
        - Pay only for execution time
        - Zero server setup
        - Great for cron jobs, webhooks, background tasks
        - No infrastructure to maintain
#### STORAGE & DATABASES :-
- **_Azure Blob Storage_**
    - **Use when:** Storing images, videos, logs, backups, documents.
    - **Why it’s great:**
        - Super cheap
        - Highly durable
        - Great for media-heavy apps
        - High performance and globally scalable
- **_Azure SQL Database_**
    - **Use when:** You need a relational database (OLTP) without maintaining a server.
    - **Why it’s great:**
        - No server setup
        - Auto-backup, auto-patching
        - Scales blindly fast
        - Fully managed and secure
- **_Cosmos DB_**
    - **Use when:** You want blazing-fast NoSQL with global replication.
    - **Why it’s great:**
        - Millisecond response times
        - 99.999% uptime
        - Supports MongoDB, SQL-like queries, Graph, Cassandra
        - Low latency + multi-region replication
#### DATA MOVEMENT & ANALYTICS :-
- **_Azure Data Factory (ADF)_**
	- **Use when:** You need ETL/ELT pipelines between databases, files, APIs, SaaS tools.
    - **Why it’s great:**
        - Connects databases, files, cloud apps
        - Visual drag-drop interface
        - Great for ETL/ELT workflows
        - Tons of built-in connectors
- **_Azure Synapse Analytics_**
    - **Use when:** You need data warehousing, analytics, reporting, or want to combine big data + SQL analytics in one platform.
    - **Why it’s great:**
        - Combines SQL pools, Apache Spark, data pipelines, and analytics in one workspace
        - Ideal for large-scale analytics and BI
        - Handles massive datasets with high performance
        - Integrates deeply with ADF, Power BI, and Azure Storage
#### DEVOPS & AUTOMATION :-
- **_Azure DevOps_**
    - **Use when:** You need CI/CD, repos, boards, pipelines.
    - **Why it’s great:**
        - Best pipelines for enterprise
        - Solid repo + test management
        - Works with any language
        - End-to-end DevOps platform
- **_GitHub Actions (Azure-Friendly)_**
    - **Use when:** You want CI/CD directly in GitHub, especially if your code already lives there.
    - **Why it’s great:**
        - Simple YAML-based workflows
        - Massive community actions and templates
        - Deep integration with Azure for deployments
        - Great for lightweight, flexible CI/CD
- **_Azure Logic Apps_**
    - **Use when:** You want no-code automation (send emails, connect apps, schedule workflows).
    - **Why it’s great:**
        - No-code automation
        - Connects with 400+ apps (Salesforce, Slack, Gmail, SAP)
        - Great for enterprise workflows
        - Easy drag-and-drop interface
#### MONITORING & SECURITY :-
- **_Azure Monitor + Log Analytics_**    
    - **Use when:** You want logs, metrics, alerts, dashboards.
    - **Why it’s great:**
        - Alerts when things break
        - Visual dashboards
        - Works with any Azure service
        - Central monitoring + log querying at scale
- **_Azure API Management (APIM)_**
    - **Use when:** You need an API gateway, rate limiting, authentication, and API documentation.
    - **Why it’s great:**
        - Add rate limits, keys, policies
        - API gateway + documentation in one
        - Perfect for microservices + client apps
        - Secure, scalable, and enterprise-ready
- **_Microsoft Sentinel_**
    - **Use when:** You need security monitoring + detecting suspicious events.
    - **Why it’s great:**
        - Real-time threat alerts
        - Uses AI to detect abnormal behavior
        - Good for enterprise security teams
        - SIEM + SOAR in one powerful platform

#### Bonus Azur Point
- If you need to create an enterprise level application one can go for :-

| Backbone        | DevOps         | Monitoring and logs  | Automation | Security                    |
| --------------- | -------------- | -------------------- | ---------- | --------------------------- |
| AKS             | Azure Devops   | Azure Monitor        | Logic Apps | Entra ID (Identification)   |
| Apps Service    | Github Actions | Application Insights | Functions  | Sentinel (Threat Detection) |
| Blob Storage    |                |                      |            |                             |
| SQL DB + Cosmos |                |                      |            |                             |
| API Management  |                |                      |            |                             |


## SDLC Methodologies 
- SDLC is a structured process used to design, develop, test, and deploy software systems.
- How it works (general phases):
	- **Requirement Analysis** – gather user/business needs
	- **System Design** – create architecture and design documents
	- **Implementation (Coding)** – developers write code
	- **Testing** – QA team tests the software
	- **Deployment** – release software to users
	- **Maintenance** – fix issues, update, improve features
- Types :
	- ***Agile Methodology***
		- Agile is an iterative and incremental SDLC approach focusing on delivering small, usable software pieces quickly with continuous customer involvement.
		- **How it works:**
			- Work is divided into **small iterations (2–4 weeks)**
			- Requirements evolve continuously
			- Frequent feedback from stakeholders
			- Focus on adaptability and customer satisfaction
	- ***Scrum***
		- A structured Agile framework using fixed-length “**Sprints**.”
		- **How it works:**
			- **Sprint Planning** → select work for the sprint
			- **Daily Scrum** → 15-minute daily sync-up
			- **Sprint Work** → developers build features
			- **Sprint Review** → show completed work to stakeholders
			- **Sprint Retrospective** → reflect and improve
		- **Key Roles:**
			- **Product Owner** (defines requirements)
			- **Scrum Master** (removes blockers, ensures process)
			- **Development Team**
	- ***Kanban***
		- A visual flow-based Agile method focusing on continuous delivery.
		- Work items move through a **Kanban board** (To Do → In Progress → Done)
		- Limits on WIP (**Work in Progress**) to avoid overload
		- No fixed iterations
		- Continuous improvement and flow optimization
	- ***Waterfall Model***
		- A linear, sequential SDLC model where each phase must finish before the next begins.
		- **How it works:**
			1. Requirements
			2. Design
			3. Implementation
			4. Testing
			5. Deployment
			6. Maintenance
		- Features 
			- Rigid and structured
			- Good for projects with stable requirements
			- Difficult to change later
	- ***Spiral Model***
		- A risk-driven development model combining iterative development and Waterfall principles.
		- **How it works (4 phases repeated in spirals/loops):**
			1. **Planning** – requirements like in Waterfall
			2. **Risk Analysis** – identify and mitigate risks
			3. **Engineering** – development and testing
			4. **Evaluation** – customer reviews outcome
		- Each loop results in a more complete version of the software. Ideal for **large, high-risk projects**.
	- ***DevOps Model***
		- An approach combining **development (Dev)** and **operations (Ops)** to enable continuous integration, delivery, deployment, and monitoring.
		- **How it works:**
			- **Continuous Integration (CI)** – merge code frequently, automatic builds/tests
			- **Continuous Delivery/Deployment (CD)** – automate release pipelines
			- **Infrastructure as Code (IaC)** – automate infrastructure setup
			- **Monitoring & Feedback** – real-time performance analysis
			- **Collaboration Between Dev & Ops** – shared pipelines and processes
		- Focus: **automation, speed, reliability**.
	- ***XP (Extreme Programming)*** 
		- An Agile methodology emphasizing **software quality** and **rapid, frequent releases**.
		- **How it works:**
			- **Short iterations**
			- **Pair programming**
			- **Test-Driven Development (TDD)**
			- **Continuous integration**
			- **Refactoring**
			- **Small, frequent releases**
			- **Close customer collaboration**
		- Goal: produce high-quality code with fewer defects.
	- ***V-Model (Validation & Verification Model)***
		- An extension of the Waterfall model where testing is planned alongside development in a V-shape.
		- **How it works:**  
			- Left side = **Verification**  
			- Right side = **Validation**
		- **Verification (Development):**
			1. Requirements
			2. System Design
			3. Architecture Design
			4. Module Design
		- ***Validation (Testing):***
			- User Acceptance Testing ↔ Requirements
			- System Testing ↔ System Design
			- Integration Testing ↔ Architecture
			- Unit Testing ↔ Module Level
		- Testing is linked directly to its corresponding development stage.

| Model         | Works As                         | Best For                                |
| ------------- | -------------------------------- | --------------------------------------- |
| **Waterfall** | Linear & sequential              | Stable requirements                     |
| **Agile**     | Iterative, incremental           | Changing requirements                   |
| **Scrum**     | Iteration-based sprints          | Team collaboration                      |
| **Kanban**    | Continuous flow                  | Support/maintenance work                |
| **Spiral**    | Risk-driven iterations           | Large, risky projects                   |
| **DevOps**    | Automated CI/CD + Ops            | Rapid deployment                        |
| **XP**        | Code-quality focused Agile       | High-quality fast releases              |
| **V-Model**   | Testing aligned with development | Critical systems (healthcare, aviation) |

## Networking Protocols 
- Networking protocols are basically the **rules of communication** between computers. Imagine two devices trying to talk protocols decide _how they speak, what language, how loud, how often,_ everything. They ensure data actually reaches the right place, in the right format, without getting messed up.
- Types of API's :
	- ***HTTP (Hypertext Transfer Protocol)***
		- The protocol that powers the web — used when you open websites.
		- Your browser sends an HTTP request to a server → the server sends back HTML/CSS/JS → your browser displays it.  
		- It’s **stateless**, meaning each request is fresh; the server doesn’t remember you.
	- ***HTTPS***
		- HTTP but encrypted.
		- Uses **SSL/TLS** certificate to create a secure tunnel. Everything sent between browser and server is scrambled so hackers can't read it.
	- ***TCP (Transmission Control Protocol)***
		- A reliable, connection-based protocol used for accurate data transmission.
		- **How it works:**
			- Sets up a 3-way handshake (SYN → SYN-ACK → ACK)
				- SYN : Synchronize, ACK : Acknowledge 
			- Breaks data into packets
			- Ensures every packet is delivered (retransmits if needed)	
		- Used for apps that need accuracy (web, email, files). Guarantees no packet loss.  
	- ***UDP (User Datagram Protocol)***
		- A fast, connectionless protocol.
		- No handshake, no checking — it just throws packets and hopes they arrive.  
		- Speed > accuracy.
		- Used in : 
			- Gaming
			- Video streaming
			- Live calls (Zoom, WhatsApp)
	- ***FTP (File Transfer Protocol)***
		- Used for transferring files over a network.
		- Client → Server
		- You authenticate → browse files → upload/download.
		- **Why it matters:**
			- Simple file management
			- Works even with large files
			- Still used in DevOps, hosting
	- ***SFTP (Secure File Transfer Protocol)***
		- Secure version of FTP.
		- Runs through SSH → fully encrypted.
		- Used for :
			- Safe for enterprise file transfers
			- No chance of data leaks
			- Standard for server-to-server automation
	- ***SSH (Secure Shell)***
		- A secure way to access remote servers.
		- Creates an encrypted terminal session over the internet.
		- Developers use it to manage Linux servers
		- Super secure
		- Base of DevOps tooling
	- ***DNS (Domain Name System)***
		- The “phonebook” of the internet.
		- When you type google.com → DNS converts it to an IP address (e.g., 142.251.42.238).
	- ***SMTP (Simple Mail Transfer Protocol)***
		- Used to send emails.
		- Your mail server → SMTP server → recipient’s mail server.
		- **Why it matters:**
			- Backbone of email systems
			- Used in notifications, OTPs, etc.
	- ***DHCP (Dynamic Host Configuration Protocol)***
		- Automatically assigns IP addresses to devices.
		- When you connect to WiFi → DHCP gives you IP, gateway, DNS.
		- Zero manual setup
		- Network management becomes easy
		- Used in every LAN/WiFi
	- ***ARP (Address Resolution Protocol)***
		- Maps IP address → MAC address.
		- Your device broadcasts “Who has 192.168.1.4?”. The owner responds with its MAC address.
		- Devices find each other in LAN
		- Core of packet routing
	- ***WebSockets***
		- Used for real-time continuous communication.
		- Keeps a single open connection between client and server → instant updates.
		- Used in:
			- Live chats
			- Stock tickers
			- Multiplayer games
			- Real-time dashboards


## API's
- **Application Programming Interface**
- Think of it as a **menu** that a service exposes.
- You order through the API → the server performs the action → sends back a response. APIs let two applications talk to each other without knowing internal details.
- **How it works?**
	- Client sends request (HTTP request GET/POST)
	- Server processes the request
	- Server sends response
	- Client displays the info
- **Types :**
	- **REST APIs**
		- REST APIs use a client-server model to enable communication between different systems over the internet. A client, such as a web or mobile app, sends a request to a server for a specific resource, identified by a URL.
		- They utilize standard HTTP methods (like GET, POST, PUT, and DELETE) to specify the desired action on a resource. The server then responds with a representation of the resource's current state, most commonly formatted as JSON.
		- A key principle of REST is statelessness, meaning the server does not store client information between requests. This makes REST APIs highly scalable and lightweight, as each request contains all the necessary information for the server to process it.
	- **SOAP**
		- SOAP is a protocol for exchanging structured information in web services, relying on XML as its message format.
		- It is highly standardized, strictly typed, and platform-agnostic, but its reliance on XML can make its messages larger and more verbose compared to other methods.
	- **GraphQL**
		- GraphQL is a query language for APIs that allows clients to request exactly the data they need in a single network request, preventing over-fetching or under-fetching of data.
		- It operates over a single endpoint, using a strong type system to define a schema that specifies the data and services available, which improves error handling and validation.
	- **WebSocket**
		- WebSocket provides a persistent, full-duplex communication channel over a single TCP connection, allowing for real-time, bidirectional data exchange between a client and a server.
		- Unlike HTTP's request-response cycle, it maintains an open connection, reducing overhead and latency for applications that require continuous, low-latency updates, such as chat or live sports tickers.
	- **gRPC**
		- gRPC is a high-performance RPC framework that allows a client application to call a method on a server application as if it were a local object.
		- It uses HTTP/2 for transport and Protocol Buffers for efficient binary serialization, making it ideal for low-latency, internal microservice communication where performance is critical.