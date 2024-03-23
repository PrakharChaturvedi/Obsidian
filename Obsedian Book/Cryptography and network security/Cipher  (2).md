# *What is Cipher? 
- Also called <font color="#ffc000">encryption algorithms</font>, are about systems for encrypting and decrypting data. A cipher converts the original message, called plain text into cipher text using a key to determine how it is done. 

- *Types of ciphers : 
	- [>] Substitution cipher
		- <font color="#ffc000">Concept</font><font color="#ffc000"> :</font>
			- Any character of plain text from the given fixed set of characters is substituted by some other character from the same set depending on a key. 
			- For example with a shift of 1, A would be replaced by B, B would become C, and so on.
				- Then ABCDEF => BCDEFG.
		
	- [>] Transposition cipher
		- <font color="#ffc000">Concept :</font> 
			- Unlike substitution ciphers that replace letters with other letters, transposition ciphers keep the letters the same, but rearrange their order according to a specific algorithm. 
			- For Example in a *simple columnar transposition cipher*, a message might be read horizontally but would be written vertically to produce the ciphertext.
			 ![[Pasted image 20230921130054.png]]
		
	- [>] Columnar cipher 
		- <font color="#ffc000">Concept :</font> 
			- Form of a transposition cipher 
			- It involves writing the plain text in rows, and then reading the ciphertext off in columnar one by one.
  
	- [>] <font color="#9360ea">Polygraphic cipher</font>
		- <font color="#ffc000">Concept : </font>
			- Substituting one letter for another letter, a Polygraphic cipher performs substitutions with two or more groups of letters.
			- For example : 
				- Hill cipher 
				- https://www.geeksforgeeks.org/hill-cipher
	
	- [>] Permutation cipher
		- <font color="#ffc000">Concept :</font>
			- The Permutation Cipher is another form of Transposition Cipher. It is similar to *Columnar Transposition* in some ways, in that the columns are written in the same way, including how the keyword is used. 
			- However, the *Permutation Cipher* acts on blocks of letters (the lengths of the keyword), rather than the whole ciphertext.
			- In theory, any *transposition cipher* can be viewed as permutation cipher where e is equal to the length of the plaintext
			
	- [>] Private-key cipher 
		- <font color="#ffc000">Concept : </font> 
			- In this cipher, the sender and receiver must have a pre-shared key. The shared key is kept secret from all other parties and is used for encryption, as well as decryption.
		- Also known as **"Symmetric Key Algorithm"**
		
	- [>] Public-key cipher
		- <font color="#ffc000">Concept :</font> 
			- In this cipher, two different keys -- public key and private key -- are used for encryption and decryption. The sender uses the public key to perform the encryption, but the private key is kept secret from the receiver.
		- Also know as **"Asymmetric key cipher"**


## Substitution vs Columnar Cipher
|S.NO|Substitution Cipher Technique|Transposition Cipher Technique|
|---|---|---|
|1.|In substitution Cipher Technique, plain text characters are replaced with other characters, numbers and symbols.|In transposition Cipher Technique, plain text characters are rearranged with respect to the position.|
|2.|Substitution Cipher’s forms are: Mono alphabetic substitution cipher and poly alphabetic substitution cipher.|Transposition Cipher’s forms are: Key-less transposition cipher and keyed transposition cipher.|
|3.|In substitution Cipher Technique, character’s identity is changed while its position remains unchanged.|While in transposition Cipher Technique, The position of the character is changed but character’s identity is not changed.|
|4.|In substitution Cipher Technique, The letter with low frequency can detect plain text.|While in transposition Cipher Technique, The Keys which are nearer to correct key can disclose plain text.|
|5.|The example of substitution Cipher is Caesar Cipher, monoalphabetic cipher, and polyalphabetic cipher.|The example of transposition Cipher is Rail Fence Cipher, columnar transposition cipher, and route cipher.|
|6.|Involves replacing plaintext letters or groups of letters with ciphertext letters or groups of letters according to a specific algorithm or key.|Involves rearranging the order of the plaintext letters or groups of letters according to a specific algorithm or key.|
|7.|The frequency distribution of the plaintext letters is typically obscured, but patterns can still be detected with statistical analysis.|The frequency distribution of the plaintext letters remains the same, but the order is scrambled, making it difficult to detect patterns with statistical analysis.|
|8.|Vulnerable to frequency analysis attacks, where the most commonly used letters or letter combinations in the language can be identified and used to deduce the key.|Less vulnerable to frequency analysis attacks, but still susceptible to attacks such as brute force and known plaintext attacks.|
|9.|Relatively easy to understand and implement, making it suitable for simple applications.|Can be more difficult to implement and understand, but can be more secure than substitution ciphers for certain applications.|

# *More about on ciphers
- These ciphers are taught in classes 
	- Refer to VSCode Crypto vault for *java codes*   
- <font color="#ffc000">Exam potential Ciphers</font> 
	- [f] *Affine cipher* 
	- [f] *Vengeance cipher*    
	- [f] *Caesar cipher 
	- [f] *Columnar cipher* 
	- [f] *Rail Fence cipher* 
	- [f] One-time pad 
	- [f] *SBox cipher* 
	- [f] *DES* 
	- [f] *AES* 