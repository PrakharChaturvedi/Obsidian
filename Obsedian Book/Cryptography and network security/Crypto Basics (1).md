Book : Halogen
Syllabus: Encoding, encryption, hashing, public key, private key, cryptography, cryptoanalysis, security, safety,  threat, firewall, vulnerability, hacker and *Types of attacks, spoofing and malware attack*.   
# Encoding v/s Encryption v/s Hashing? 
- ==Concept== 
	- *Encryption* : Encryption is a type of encoding technique where the message is encoded using an encryption algorithm so that only authorized persons can access that information.
	- *Encoding* : Encoding is a technique where the data is transformed from one form to another.
	- *Hashing* :  It is a technique where the data is converted to hash using different algorithms present there. (SHA and MD 4 n 5)
- Usage 
	- *Encryption* : For protecting the confidentiality of the data.
	- *Encoding* : For preventing the usability of the data
	- *Hashing* : For checking integrity of the data
- Key 
	- *Encryption* : Appropriate keys are used 
	- *Encoding* : No keys are used 
	- *Hashing* : No keys are used
- Example :
	- *Encryption* : Affine Cipher, Caesar cipher, etc. 
	- *Encoding* : Unicode, Base64, ASCII
	- *Hashing* : SHA256, MD5

# Public vs Private key 
- [>] <font color="#ffc000"> Private key :</font>
	- Key which only sender has access to.
	- The private key mechanism is faster.
	- The private key is to be shared between two parties.
	- Performance testing checks the reliability, scalability, and speed of the system.
	- The private key mechanism is called "symmetric" because a single key is shared between two parties.
- [>] <font color="#ffc000">Public key :</font> 
	- Key which only receiver/everyone has access to.
	- The private key mechanism is slower.
	- The public key can be used by anyone.
	- Load testing checks the sustainability of the system.
	- The public key mechanism is called "asymmetric" because there are two keys for different purposes.

# Cryptography 
- Cryptography is the process of hiding or coding information so that only the person a message was intended for can read it. The art of cryptography has been used to code messages for thousands of years and continues to be used in bank cards, computer passwords, and ecommerce.
- <font color="#ffc000">Importance of cryptography</font> 
	- <font color="#92d050">Privacy and Confidentiality</font>
	- <font color="#92d050">Authentication</font>
		- Cryptography ensures information is not altered while in storage or during transit between the sender and the intended recipient.
	- <font color="#92d050">Nonrepudiation</font> 
		- Cryptography confirms accountability and responsibility from the sender of a message, which means they cannot later deny their intentions when they created or transmitted information.
## Cryptanalysis
-  Cryptanalysis is the study and process of _analyzing and decrypting ciphers, codes, and encrypted text without using the real key_. 

## Security & Safety :
- <font color="#ffc000">Security</font> 
	- We must secure our computers with technology in the same way that we secure the doors to our offices.
- <font color="#ffc000">Safety</font>  
	- We must act in ways that protect us against the risks and threats that come with Internet use. 

## Cyber Security attacks 
-  When there is an unauthorized system/network access by a third party, we term it as a cyber attack. The person who carries out a cyberattack is termed as a hacker/attacker.
- Types: [S B M P P M S]
	- <font color="#ffc000">Spoofing</font>
		- Spoofing is a deceptive technique where an entity, such as an attacker, falsifies information to masquerade as someone or something else. 
		- This can involve manipulating data, identity, or communication sources to deceive and trick individuals, systems, or networks. <font color="#00b050">Common forms of spoofing include email spoofing (misleading email origin), IP spoofing (manipulating source IP address), caller ID spoofing (faking displayed phone numbers), and website spoofing (creating fake websites). </font>
		- Spoofing attacks are often aimed at gaining unauthorized access, stealing sensitive information, or spreading misinformation.
	- <font color="#ffc000">Brute Force Attack</font>
		- Likh h lenge ye toh kam se kam!  
	- <font color="#ffc000">Malware Attacks</font>
		- Malware includes viruses, worms, Trojans, ransomware, spyware, adware, botnets, keyloggers, rootkits, and fileless malware.
		- Viruses replicate in legitimate programs, worms spread autonomously, Trojans deceive users.
		- Ransomware encrypts files, demanding payment; spyware monitors and transmits sensitive data.
		- Adware disrupts with unwanted ads; botnets coordinate large-scale attacks.
		- Keyloggers capture keystrokes, rootkits hide malicious code, and fileless malware operates in system memory.
		- Cybersecurity measures involve antivirus tools, software updates, firewalls, user education, and intrusion detection systems.
	- <font color="#ffc000">Phishing Attacks</font>
		- Deceptive emails or messages imitate trusted entities to trick users into revealing sensitive information.
		- Tactics include urgency and impersonation of banks or government agencies.
		- Phishing may lead to malware installation or direct users to fake websites.
		- Protection involves user education, awareness, and email filters to detect and block phishing attempts.
	- <font color="#ffc000">Password Attacks</font>
		- Preventing password attacks involves using strong, unique passwords, enabling two-factor authentication, avoiding simple and easily guessable passwords, regular password changes, and being cautious of phishing attempts. 
		- Additionally, using password managers can help generate and securely store complex passwords for different accounts. 
	- <font color="#ffc000">Man-in-the-middle</font>
		- The attacker secretly intercepts and possibly alters communication between two parties.
		- It can occur in various forms, such as intercepting Wi-Fi connections, compromising routers, or spoofing websites.
		- The goal is to eavesdrop on sensitive information like login credentials, financial data, or manipulate the communication for malicious purposes.
		- Techniques to prevent MITM attacks include encryption (SSL/TLS), using secure and verified networks, and implementing strong authentication methods like digital certificates.
	- <font color="#ffc000">SQL injection</font>
		- Attackers insert malicious SQL code into input fields or parameters to manipulate a database.
		- Commonly occurs in forms, search boxes, or any user-input areas vulnerable to unfiltered data.
		- Successful SQL injections can lead to unauthorized access, data manipulation, or disclosure of sensitive information.
		- Prevention involves using parameterized queries, input validation, and adopting least privilege principles to limit database access for web applications. Regular security audits are also essential to identify and fix potential vulnerabilities. 
## Basic definitions: 
- <font color="#ffc000">Threats:</font>
	- Is an action or event that might compromise the security.
- <font color="#ffc000">Firewall:</font>
	- It is a software or hardware which is used to filter network traffic based on rules.
- <font color="#ffc000">Vulnerability:</font>
	- Is a weakness, a design problem or implementation error in system that can lead to an unexpected and undesirable event regarding security system. 
- <font color="#ffc000">Hacker:</font>
	- Is a person who tries and exploits a computer system for a reason which can be money, a social cause, fun etc.

