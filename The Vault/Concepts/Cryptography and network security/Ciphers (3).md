## *Affine Cipher* : 
- It is a monoalphabetic substitution cipher.
- It uses a formula structure of  
	- Formula : 
		- Encryption E(x) = (ax+b) mod 26
		- Decryption D(x) = a^-1 (x-b) mod m
			- a and b => Cipher keys
			- m => size of alphabet (A to Z is 26 characters so easiest way to represent it is [0-25] indexes)
		- Example : For a : E(0)=(5×0+8)mod26=8mod26=8 -> 8 -> "i"
	- *Mod is to find remainder* 
## *Caesar cipher* :
- It is a substitution cipher that shifts letters in a message to make it unreadable if intercepted.
- We just shift letters forward and backwards with respect to indexes. 
	- Example : 
		- Encrypted text : "Zkb glg wkh flsoh fubsw wkh urdg?"
		- Decrypted text : "Why did the chicken cross the road?"
		- Shift : 3.
[[Pasted image 20231014053931.png]]
## *Vengeance cipher* :
- Uses simple form of polyalphabetic substitution.
- The encryption of the original text is done using the Vengeance cipher.
	- The table consists of the alphabets written out 26 times in different rows, each alphabet is then shifted to the left compared to the previous alphabet, corresponding to the 26 possible Caesar Cipher. 
	- Formula : 
		- Encryption Ei = (Pi + Ki) mod 26
		- Decryption Di = (Ei - Ki) mod 26 
	- Example :
		- Plaintext : H - E - L - L - O
			        7 - 4 -11-11-14
		- Key : K - E - Y - K - E 
		            10 -4 -24-10- 4 
	        - Cipher Text : dR - O - V - V - Y
	                        17-14 -21-21-24  
	         ![[Pasted image 20231014054733.png]]
- In row we take H and in column we take K, and repeat it. 
## *Columnar Cipher* : 
- Form of a transposition cipher 
- It involves writing the plain text in rows, and then reading the ciphertext off in columnar one by one.
- Example :  ![[Pasted image 20231012131943.png]]

## *Rail Fence Cipher* :
- It is also known as zig-zag cipher 
- In this cipher the plain text is written downwards and diagonally on successive rails of an imaginary fence.
- When we reach the bottom rail, we traverse upwards moving diagonally, after reaching the top rail, the direction is changed again. Thus the alphabets of the message are written in a zig-zag manner.
- After all alphabets are written, the individual rows are then combined to obtain the cipher text.
- Example : 
![[Pasted image 20231012210556.png]]
- Plain text : <font color="#ffc000">GeeksForGeeks </font>
- Encrypted text : <font color="#ffc000">GSGsEkfrekEoE</font>
- Rails : 3

## *Sbox Cipher* :
- It is a simple modern cipher 
- It can have different numbers of inputs and outputs.
- It can be keyed or keyless, but modern blocks ciphers normally use the keyless approach.
- The function that matches the input to the output may be defined mathematically or by a table.
- Input of 6 bits and output of 4 bits
	- If input bits => m and output bits => n
		- m x n table is made, 2^m words with n bits each.  
- Example 1 :
	- Size : 3 x 2 => 3 input bits and 2 output bits

 --  00  01  10  11 *->* Right most bits
 0 | 00  10  01  11
 1 | 10  00  11 01
  *\>* Left most bits
  
- Example 2 : 
 
| S5 | Middle | 4 | Bits | Inputs | Middle | Four | Bits | Inputs | Middle | Four | Bits | Inputs | Middle | Four | Bits | Inputs | Middle  | Four |
| ---- | ---- | ---- | :--: | :--: | ---- | ---- | :--: | :--: | ---- | ---- | :--: | :--: | ---- | ---- | :--: | :--: | :--: | :--: |
| OUTER | XX | 0001 | 0010 | 0011 | 0100 | 0101 | 0110 | 0111 | 1000 | 1001 | 1010 | 1011 | 1100 | 1101 | 1110 | 1111 |  |  |
| BITS | 0000 | 0001 | 0010 | 1100 | 0100 | 0001 | 0111 | 1010 | 1011 | 0110 | 1000 | 0101 | 0011 | 1111 | 1101 | 0000 | 1110 | 1001 |
| OUTER | 0001 | 1110 | 1011 | 0010 | 1100 | 0100 | 0111 | 1101 | 0001 | 0101 | 0000 | 1111 | 1010 | 0011 | 1001 | 1000 | 0110 |  |
| BITS | 0010 | 0100 | 0010 | 0001 | 1011 | 1010 | 1101 | 0111 | 1000 | 1111 | 1001 | 1100 | 0101 | 0110 | 0011 | 0000 | 1110 |  |
| OUTER | 0011 | 1011 | 1000 | 1100 | 0111 | 0001 | 1110 | 0010 | 1101 | 0110 | 1111 | 0000 | 1001 | 1010 | 0100 | 0101 | 0011 |  |
## *AES Cipher* : (Advance Encryption Standard)

- 128 bit symmetric block cipher (that means 128 bits input and 128 bits output).
- <font color="#ffc000">The key can be 128(10 rounds), 192(12 rounds), 256 bits(14 rounds) </font>
- In AES is addition of ==permutation and substitution== is done to make the conversion more complex and diverse.
- An iterative rather than a Feistal cipher 
	- ==The Feistel cipher is a design model or structure used to build various symmetric block ciphers, such as DES. This design model can have invertible, non-invertible, and self-invertible components. Additionally, the Feistel block cipher uses the same encryption and decryption algorithms.== 
	- Processes data as an entire block of 4 columns and 4 bytes.
	- Operates an entire data block in every round.
- ==Advantages :==
	- Resistance to known attacks
	- Speed and code compactness on many CPU's
	- design simplicity
- ==Key points :==
	- Key expanded into an array of 32-bit words, four words form round key in each round.
	- Has simple structure.
	- only *Add Round Key* uses key.
	- ==Each stage is easily reversible==
	- ==Decryption uses keys in reverse order.== 
- Each round comprises of 4 steps :
	- ==*SubBytes* :== Substitution steps (S-box)
		- Its performed using a lookup table also called the S-box.
		- The result of this step is a 16 byte (4 x 4 ) matrix like before.
	- ==*ShiftRows* :== Row's are shifted in round/linear format at a particular number of time.
		- The first row is not shifted
		- The second row is shifted once to the left.
		- The third row is shifted twice to the left.
		- The fourth row is shifted thrice to the left.
		- <font color="#ffc000">(A left circular shift is performed.)</font>
	- ==*MixColumns* :== 
		- This step is basically a matrix multiplication.
		- Each column is multiplied with a specific matrix and thus the position of each byte in the column is changed as a result.
		- In last round mix-column is not performed while other operations are performed like usual.
	- ==*Add Round Key* :== 
		- Now the resultant output of the previous stage is XOR-ed with the corresponding round key. 
		- Here, the 16 bytes is not considered as a grid but just as 128 bits of data.
	- ==AES structure:==![[Pasted image 20240102233222.png]]
## *DES Algorithm* (Data encryption standard):
- It is a symmetric-key block cipher.
- <font color="#ffc000">It is a block cipher with 56 bit key length. It encrypts data in blocks of 64 bits each, i.e. input (plain text) is 64 bits same as output 64 bits cipher text.</font>
	- Main key : 64 bits
	- Subkey : 56 bits
	- Round key : 48 bits
	- No. of round keys : 16 rounds
- ==Initial Permutation function:==
	- It happens before the first round.
	- This is nothing but jugglery of bit positions of the original plain text block. (For 64 bits arranged in a table)
- ==Subkey Generation:==
	- The 56-bit key is used to generate 16 subkeys, one for each round.
	- The key is subjected to a permutation called the "PC-1" permutation, followed by a split into two 28-bit halves.
	- Each half is individually rotated left by one or two bits (depending on the round), and then combined into a 56-bit subkey using the "PC-2" permutation.
- ==Feistal Network==
	- The 32-bit right half of the data block undergoes an <font color="#ffc000">expansion permutation</font>, expanding it to 48 bits. 
	- This expanded half-block is then XORed with the current round's subkey.
	- The result is passed through a series of <font color="#ffc000">eight S-boxes</font>, each replacing 6 bits with 4 bits based on a specific substitution table.
	- The 32 bit output of S-boxes is then subjected to the straight permutation called the <font color="#ffc000">P-box.</font>
- ==Inverse initial permutation==:
	- Inverse of initial permutation.
	- After completing 16 rounds of the Feistel network, the left and right halves are swapped one last time. 
	- The inverse initial permutation rearranges the bits back to their original order, producing the final 64-bit ciphertext block.
- ==Broad level steps of DES:== ![[Pasted image 20240103003851.png]]

## CIA triad
- Also called **Confidentiality, Integrity, and Availability Triad**.
- ==Confidentiality :==
	- Roughly equivalent to privacy, confidentiality measures are designed to prevent sensitive information from unauthorized access attempts. It's common for data to be classified according to the amount and type of damage that could be done if it fell into the wrong hands. More or less stringent data security measures can then be implemented according to those categories.
- ==Integrity :==
	- The consistency, accuracy and trustworthiness of data must be maintained over its entire lifecycle. Data must not be changed in transit, and steps must be taken to ensure it can't be altered by unauthorized people -- for example, in data breaches.
- ==Availability :==
	- Information should be consistently and readily accessible for authorized parties. This involves properly maintaining hardware and technical infrastructure and systems that hold and display the information.
- ![[Pasted image 20240103203530.png]]
