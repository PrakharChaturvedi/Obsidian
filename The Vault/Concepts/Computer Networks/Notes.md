#Concepts 
## Modems and routers
- Modem : 
	- Modulator-demodulator or a modem, it is used to change digital signal into analog signal so that they can be transmitted over the telephone line.
	- The opposite process also occurs when data is received : analog signal is converted into digital signals for use by computers or another devices. 
- Routers : 
	- A router is a device that connects two or more packets-switched networks or subnetworks. 
	- It serves two primary functions : managing traffic between networks by forwarding data packets to their intended IP addresses, and allowing multiple devices to use the same Internet connection. 

##  Protocols : 
- A network protocol is a mechanism or set of procedures that enables devices to communicate back and forth across the internet. In order to communicate together, two devices must support the same protocol or a gateway will need to be used to translate the communication. 
- There are three main types of network protocols you need to be aware of : 
	- Network Management protocols : 
		- For setting out policies designed to monitor, manage and maintain a network.
		- Examples : Include SNMP, FTP, POP 3 and Telnet.
	- Network Communication protocols : 
		- A group of protocols used to establish rules and formatting for exchange data across  a network. 
		- Types : TCP, UDP, IP, HTTP, IRC, BGP and ARP.
	- Network Security protocols : 
		- Security protocols that use security measures such as cryptography and encryption to protect data.
		- Example : SFTP, SSL and HTTPS.
## Network communication protocols 
- **Transmission Control Protocol (TCP)**
	- It is a protocol that converts data into packets so that it can be sent between a server and a client. Organizations use TCP to transfer content such as files, text, images and emails because it guarantees that the packets will be delivered accurately and in the correct order. 
	- It's worth nothing that TCP will establish a connection between the origin and the destination devices before attempting to transfer data. This three-say handshake is outlined briefly below : 
		- The client or web browser sends the destination server a Synchronize Sequence Number (SYN).
		- The destination server sends an acknowledgement message known as SYN-ACK.
		- The origin device receives the SYN-ACK message and generates an ACK acknowledgement message, which finalizes the connection.
- **User Datagram Protocol (UDP)**
	- UDP is communication protocol that's designed to send packets from one device to another on a network. Many organizations use UDP as an alternative to TCP because if offers higher transfer speeds. 
	- While this increase in speed comes at the cost of accuracy, UDP better supports video/audio streaming services, online  games or voice-over-internet-protocol (VoIP) calls, which can handle some degree of data loss.
	- Another key difference between the two is that UDP won't attempt to establish a connection before sending packets on to the destination. At the same time, it also doesn't guarantee the delivery of data to the other device.
- **File Transfer Protocol (FTP)**
	- FTP is a network protocol that's used to transfer files from one device to another over an unencrypted TCP/IP connections. With FTP, a client user can load up a web browser or FTP client such as FileZilla or FTP Voyager and send up to 2 GB at once.
	- Many organizations use FTP because of  its ability to send large files or lots of files at once in a way that's fast and efficient. Unfortunately, this efficiency comes at the cost of security as FTP transmits all data in plain text.
	- For this reason, many organizations opt to use a secure version of FTP called File Transfer Protocol Secure Sockets Layer (FTPS), which functions the same but uses SSL encryption to obscure the transferred data. 
- **Hypertext Transfer Protocol (HTTP)** 
	- HTTP is a communication protocol that enables systems to communicate on the World Wide Web. With HTTP, a client will send a hypertext message request to a web server asking for access to the resources needed to load a web page.
	- The server hosting the content will then respond and enable the client to load all the necessary text, images and videos featured on the page. HTTP's request-response cycle is outlined briefly below : 
		- The client sends an HTTP  request message to the web server to request access to the web page content.
		- The web server processes the request message. 
		- The web server sends a response message that includes the requested content or web page. 
		- The client receives the message and loads the content in the web browser for the end user to view. 
	- There is also an encryption version of HTTP called HTTPS, which uses SSL/TLS encryption to encrypt requests and responses so they can't be accessed by third parties. 

## OSI model  
- Open system inter-connection model. It's standard for communication between servers.
- Their are 7 layers in OSI model : 
	- **Application Layer**
		- The topmost layer where end-user software interacts with the network. It provides network services directly to applications such as email, file transfer, and web browsing. This layer contains the applications.
		- Examples: HTTP, FTP, SMTP, DNS, POP3, IMAP.
	- **Presentation Layer**
		- 
	- **Session Layer**
	- **Transport Layer**
	- **Network Layer**
	- **Data-Link Layer**
	- **Physical Layer**