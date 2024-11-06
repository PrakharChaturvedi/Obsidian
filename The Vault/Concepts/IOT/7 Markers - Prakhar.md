#Concepts 
- Question 1 : Draw and explain IEEE 802.15.4 LR-WPAN Device architecture.
- Solution : 
	- **IEEE 802.15 LR-WPAN Device Architecture**
		- The device comprises a physical layer (PHY), which contains the RF transceiver along with its low-level control mechanism.
		- A MAC sublayer provides access to the physical channel for all types of transfer.
		- The upper layers consist of a network layer, which provides network configuration, manipulation, and message routing.
		- The application layer provides the intended function of a device.
		- An IEEE 802.2 logical link control (LLC) can access the MAC through the service specific convergence sublayer (SSCS).
	- 1. **Physical Layer (PHY):**
	    - Provides two services: PHY data service and PHY management service interfacing to the physical layer management entity (PLME).
	    - Handles transmission and reception of PHY protocol data units (PPDUs) across the physical radio channel.
	    - Services include activation/deactivation of the radio transceiver, energy detection (ED), link quality indication (LQI), channel selection, and clear channel assessment (CCA).
	    - Operates in three frequency bands: 2.4GHz global, 915MHz America, and 868MHz Europe.
	    - Data rates vary per frequency band: 250 kbps at 2.4 GHz, 40 kbps at 915 MHz, and 20 kbps at 868 MHz.
	    - Receiver sensitivities are -85 dBm for 2.4 GHz and -92 dBm for 868/915 MHz.
	    - Supports packet sizes typically ranging from 30-60 bytes for home applications, up to 127 bytes for more demanding applications.
	    - Maximum packet durations vary by frequency band: 4.25 ms for 2.4 GHz, 26.6 ms for 915 MHz, and 53.2 ms for 868 MHz.
	    - Utilizes direct sequence spread spectrum (DSSS) with various modulation techniques based on frequency band.
	2. **Data Link Layer:**
	    - Divided into MAC and LLC sublayers.
	    - MAC provides services such as association/disassociation, acknowledged frame delivery, channel access, frame validation, guaranteed time slot management, and beacon management.
	    - Two services provided to higher layers: MAC data service (accessed through MCPS-SAP) and MAC management services (accessed through MLME-SAP).
	    - Provides interface between SCCS or another LLC and the physical layer.
	    - Confirms successful reception of frames with acknowledgments.
	    - Security options include no security, access control lists, and symmetric key security using AES-128.
	3. **Network Layer:**
	    - Responsible for topology construction, maintenance, naming, and binding services.
	    - Tasks include addressing, routing, and security.
	    - Supports multiple network topologies like star, peer-to-peer, and cluster tree, which are application design choices.
	- ![[Pasted image 20240320215317.png]]

- Question 2 : Architecture reference mode of I05...
- Solution : 
	- Layers of IoT Reference Architecture
		IoT reference architectures typically consist of multiple layers that work together to enable the functioning of an IoT system. While the specific layering may vary based on different frameworks or standards, a commonly used layered structure includes the following:
		- **Perception Layer:**This layer comprises the physical devices or sensors that collect data from the environment or interact with the physical world. These devices can include temperature sensors, motion detectors, cameras, and other IoT−enabled devices.
		- **Network Layer:** The network layer facilitates the connectivity and communication between the IoT devices and the cloud or other data processing components. It includes protocols, gateways, routers, and other networking infrastructure to ensure seamless data transfer and reliable connections.
		- **Data Processing Layer:** This layer involves processing and analyzing the data collected from IoT devices. It may include edge computing devices or cloud−based platforms where data is aggregated, filtered, transformed, and analyzed to derive valuable insights.
		- **Application Layer:** The application layer encompasses the software applications or services that utilize the processed IoT data to provide specific functionalities or address specific use cases. These applications can range from real−time monitoring and control systems to predictive analytics, machine learning algorithms, and automation![[Pasted image 20240320215526.png]]

- Question 3 : What are the security issues in wireless sensor network explain in details.
- Solution : 
	- Wireless sensor networks (WSNs) are vulnerable to various security threats due to their inherent characteristics such as wireless communication, resource constraints, and distributed nature. Here are some of the key security issues in wireless sensor networks:
	1. **Eavesdropping:**
	    - Eavesdropping involves unauthorized users intercepting and monitoring communication between nodes in the network.
	    - Attackers can passively listen to the transmitted data, compromising the confidentiality of the information being transmitted.
	2. **Data Tampering:**
	    - Data tampering involves unauthorized modification of data packets as they are transmitted through the network.
	    - Attackers may alter sensor data, leading to inaccurate or misleading information being sent to the base station or other nodes in the network.
	    - Tampered data can lead to incorrect decision-making and actions based on false information.
	3. **Replay Attacks:**
	    - In replay attacks, attackers capture data packets transmitted over the network and replay them at a later time.
	    - This can lead to various security threats such as unauthorized access, data corruption, or disruption of network operations.
	4. **Node Spoofing:**
	    - Node spoofing involves attackers impersonating legitimate nodes in the network to gain unauthorized access or disrupt network operations.
	    - By spoofing the identity of a node, attackers can inject false data into the network, launch denial-of-service (DoS) attacks, or compromise the integrity of the network.
	5. **Denial-of-Service (DoS) Attacks:**
	    - DoS attacks aim to disrupt the normal functioning of the network by overwhelming nodes or the communication infrastructure with a high volume of traffic.
	    - Attackers may target sensor nodes, base stations, or the communication channels to degrade network performance, exhaust resources, or render the network unusable.
	6. **Physical Attacks:**
	    - Physical attacks involve physically accessing and compromising sensor nodes or the communication infrastructure.
	    - Attackers may tamper with sensor nodes, extract sensitive information, or inject malicious code into the network, posing significant security risks.
	7. **Key Management and Distribution:**
	    - Efficient and secure key management is crucial for ensuring confidentiality, integrity, and authenticity in WSNs.
	    - Challenges include securely distributing keys to sensor nodes, updating keys regularly, and revoking compromised keys without disrupting network operations.
	8. **Limited Resources:**
	    - Sensor nodes typically have limited computational, memory, and energy resources, making it challenging to implement complex security mechanisms.
	    - Security protocols and algorithms must be lightweight and energy-efficient to minimize overhead and conserve resources.
	- Addressing these security issues in wireless sensor networks requires a multi-faceted approach, including the deployment of robust encryption algorithms, authentication mechanisms, intrusion detection systems, and secure routing protocols. Additionally, ongoing research and development efforts are essential to address emerging threats and vulnerabilities in WSNs and ensure the continued security and reliability of these critical infrastructures.


- Question 4 : Draw and explain IPV6 protocol
- Solution : 
	- IPv6 (Internet Protocol version 6) is the latest version of the Internet Protocol (IP) designed to replace IPv4, which is the prevalent version currently used for internet communication. IPv6 was developed to address the limitations of IPv4, particularly the exhaustion of IPv4 addresses due to the exponential growth of internet-connected devices. Here's an explanation of IPv6:
	1. **Expanded Address Space:**
	    - The most notable feature of IPv6 is its significantly larger address space compared to IPv4. IPv6 addresses are 128 bits long, allowing for approximately 3.4 × 10^38 unique addresses.
	    - The expanded address space is essential to accommodate the growing number of internet-connected devices, including smartphones, IoT devices, and other emerging technologies.
	2. **Address Representation:**
	    - IPv6 addresses are represented as eight groups of four hexadecimal digits, separated by colons (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).
	    - To simplify address representation, IPv6 allows for compression of consecutive groups of zeros by replacing them with a double colon (::) once within an address.
	3. **Autoconfiguration:**
	    - IPv6 includes built-in support for stateless address autoconfiguration (SLAAC), allowing devices to automatically configure their IPv6 addresses without the need for a centralized DHCP server.
	    - With SLAAC, devices use information received from routers, such as Router Advertisement (RA) messages, to generate their IPv6 addresses based on prefixes advertised by the router.
	4. **Improved Routing and Efficiency:**
	    - IPv6 simplifies routing by reducing the size of routing tables due to the hierarchical addressing structure and aggregation of address blocks.
	    - IPv6 eliminates the need for Network Address Translation (NAT) in most cases, which improves end-to-end connectivity and simplifies network configuration.
	    - Additionally, IPv6 supports more efficient packet processing by simplifying the header structure and reducing header overhead compared to IPv4.
	5. **Enhanced Security:**
	    - IPv6 includes built-in support for IPsec (IP Security), which provides authentication, integrity, and confidentiality for IPv6 packets at the network layer.
	    - IPsec can be used to secure communication between IPv6-enabled devices, ensuring data privacy and protecting against various network attacks.
	6. **Transition Mechanisms:**
	    - IPv6 incorporates various transition mechanisms to facilitate the coexistence and migration from IPv4 to IPv6 networks.
	    - These transition mechanisms include dual-stack operation (running both IPv4 and IPv6 simultaneously), tunneling (encapsulating IPv6 packets within IPv4 packets for transmission over IPv4 networks), and translation (converting between IPv4 and IPv6 addresses at network boundaries).![[WhatsApp Image 2024-03-20 at 21.20.24_61479122.jpg]]
