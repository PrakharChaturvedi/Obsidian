#Concepts 
Topics Covered: 
- AES,BLOWFISH, PRESENT
- Public key infrastructure, principle of prime no. , format theorem and Euler's theorem and Chinese remainder theorem.

## Blow fish Algorithm : 
- Youtube Video : https://www.youtube.com/watch?v=ngqtEbxQLBE 
- It is significant faster than DES and provides a good encryption rate with no effective cryptoanalysis t
- technique found till date. 

- It is symmetric block cipher algorithm with:
	- block-size - 64 bits (Input size *[input -> plain text]* )
	- keySize - 32-bits to 448-bits variable size
	- number of subkeys - 18
	- number of rounds - 16
	- number of substitution boxes -  4 *[each having 512 entries of 32-bits each]*
 
- Properties:
	- Fast 
	- Takes less memory 
	- Simple to understand and implement
	- More secured (bcz of variable length key)
### There are 2 steps:
- Key Generation
		 1. Step 1 :  
			- Keys are stored inside of an array
			- k1, k2, k3, k4, k5 ..... kn [1<=n<=14]
			- length of each block = 32 bits [32 x 14 = 448 bits]
		 2. Step 2 : 
			- Initialize an array (p)
			- p1, p2, p3, p4 ...... p18 [Total 18 words]
			- length of each word = 32 bits
		3. Step 3 : 
		     - Initialize S-boxes (4 S-boxes)
			     - S1 = s0, s1, s2 ..... s255 -> 256 bit
			     - S2 = s0, s1, s2 ..... s255 
			     - S3 = s0, s1, s2 ..... s255
			     - S4 = s0, s1, s2 ..... s255
		4. Step 4 :
		     -  Initialize each element of P-array and S-boxes with <font color="#ffc000">hexadecimal values</font>
		5. Step 5 : 
			- P1 = P1 XOR K1
			- P2 = P2 XOR K2
			- ..... P14 XOR K14
			- P15 XOR K1
			- .... P18 XOR K4
		6. Step 6 : 
			- Take ==64 bits plain text== (Initially all bits are 0) 
			- Subkey is generated.
	
- Data Encryption:
	-  Step 1 :
		- 64 bits of plain text is divided into 2 parts : 32 bits each
	- Step 2:
		- 1st 32 bits is XORed with P1 to obtain result X.
		- X is passed into F (function) to get Y.
		- Y is XORed with 2nd 32 bits of plain text. (P2)
	- Step 3 :
		- The result at end is now XORed with P2.
	- Step 4 :
		- Process is repeated upto P18.
		- After P18 both 32 bits are merged together to obtain cipher text.![[Pasted image 20231103010518.png]]
- What happens inside the F : ![[Pasted image 20231103233124.png]]
## Present Algorithm : (Example AES - Optional)
- PRESENT is a light weight symmetric block cipher algorithm based on substitution–permutation network.
- It operates on the plain text 64 bit block, and supports two key lengths of 80 and 128 bit.
- The algorithm requires 31 rounds, each round consists of an exclusive OR (XOR) operation with around key.
![[Pasted image 20231103184911.png]]

## Public key infrastructure (PKI) :
- Standard followed for managing, storing and revoking the digital certificate.
- Follows asymmetric key cryptography.
- It's combination of listed things:
	- Message Digest [Integrity] : No change in content
	- Digital Signature [Authentication, Non-repudiation] : Valid user only use it
	- Encryption Services [Confidentiality] : No third person know about data/message.
- ==Architecture:== (Consists of 4 things)
	- **Public Key Repositories:**
		- Public Key Repositories store and manage public keys and their corresponding certificates. 
		- These repositories make it easier for users to access and retrieve public keys when needed for encryption or authentication purposes.
	- **Certificate Revocation Lists (CRLs):**
		1. Purpose: Communicate revocation status of digital certificates.
		2. Issued by: Certificate Authorities (CAs).
		3. Trigger: Private key compromise or certificate invalidation.
		4. **Function: Published regularly to inform users of certificate validity or revocation.
	- **Registration authority:**
		- RAs act as intermediaries between users or entities and the CAs. They verify the identity of individuals or organizations requesting digital certificates.
		- RAs play a key role in the enrollment process, ensuring that only legitimate entities receive valid certificates. Their function is to validate the information provided during the certificate application.
	- **Certificate Authority:**
		- CAs are a central component of PKI infrastructure. They are responsible for issuing digital certificates that bind public keys to individuals or entities.
		- As play a crucial role in establishing trust within the PKI system, and they are expected to follow stringent security measures to prevent unauthorized issuance of certificates.
## Mathematics of Cryptography
- Positive numbers can be divided into 3 groups :
	- Number 1
	- Primes 
	- Composites
- <font color="#ffc000">Sieve of Eratosthenes </font>
	- Write down all the numbers between 2 and n
	- Cancel all the numbers divisible by 2,3,5,7 in an order.
	- Remaining digits are primes. 
- <font color="#ffc000">Euler’s Function [φ(n)]</font>
	- The function finds the number of integers that are both smaller than n and relative to n.
	- The following helps to find the value of φ(n) :
		1. φ(1) = 0
		2. φ(p) = p-1, if p is a prime number
		3. φ(m x n) = φ(m) x φ(n),  if m and n are relatively prime.
		4. φ(p^e) = pe − pe−1, if p is a prime.
	- Examples :
		- φ(13) [as 13 is prime we directly use the formula]
			- φ(p) = p-1
			- φ(13) = 13-1 = 12
		- φ(10)
			- φ(5 x 2) [Conversion as 10 is a non-prime]
			- φ(5) x φ(2) [according to formula]
			- 4 x 1 = 4
		- φ(240)
			- 240 = 2 x 2 x 2 x 3 x 5
			- φ(240) = φ(2^4 x 5 x 3)
			- φ(2^4) x φ(5) x φ(3)
			- (2^4 - 2^3) x (4) x (2) = 64 
- <font color="#ffc000">Fermat’s Little Theorem</font>
	- If 'p' is a prime and a is an integer such that p does not divide 'a', then: 
		- 4a^(p-1) ≡ 1(mod p)
		- Example 1 : 
			- Given p = 5 and a = 2
			- a^(p-1) ≡ 1(mod p)
			- 2^(5-1) ≡ 1(mod 5) => 2^4 ≡ 1(mod 5)
			- 16 ≡ 1(mod 5) [16 when divided by 5 gives 1]
			- Therefore it is true! 
	- If 'p' is a prime and 'a' is an integer then 
		- a^(p) ≡ a mod p
	- Examples :
		-  Question 1 : Solve 6 ^ 10 mod 11
			- In here 11 is a prime number
			- Then 10 = p-1 => [p = 11]
			- Now using theorem : 6^(10) ≡ 1 (mod 11)
			- 60466176 ≡ 1 (mod 11) [11 when divided by 16477176 gives 1] 
			- Therefore it is true! 
		- Question 2 : Solve 3^12 mod 11
			- In here 11 is a prime number
			- 12 = p-1 => [p = 13]
			- Now using theorem : 3^12 ≡ 1 mod(11)
			- 531441 ≡ 1 mod(11) => 9
			- therefore not true
		- <font color="#00b050">Question 3 : p = 561 , let a = 2</font>
			- 2^(560) ≡ 1 (mod 561)
			- 2^(560) mod 561 ≡ 1
			- 560 to  binary => 1000110000
				- 4,5,9 -> 1 .... 2^4 = 16, 2^5 = 32, 2^9 = 512
				- 2^(560) => 2^(16) x 2^(32) x 2^(512)
				- Law : <font color="#4bacc6">a^x mod n =  (y mod n * z mod n)mod n , if y * z = x </font>
			- 268 which is = 1. Which is composite and theorem fails here!
- <font color="#ffc000">Euler's Theorem </font>
	- Also known as Fermat-Euler theorem
	- it states that x and n are coprime positive integers, 
		- *x^φ(n) ≡ 1 mod n*
		- Example : 
			- let x = 11 and n = 10 both are coprime 
			- 11 ^φ(10) ≡ 1 mod 10
			- 11 ^φ(4) ≡ 1 mod 10
			- 14641 ≡1 mod 10 [Which is true, as 14641 gives 1 when divided by 11]
	- Inverse version of the theorem 
		- If a and n are coprime, then *a^(-1) mod n = a^[φ(n)-1]*
## Generating prime numbers :
- <font color="#00b050">Mersenne formula for prime numbers </font>
	- Mp = 2^p - 1
	- It was later proved wrong where p is a prime number
- <font color="#00b050">Probabilistic Algorithms </font>
	- A probabilistic algorithm does not guarantee the correctness of the result.
	- Probabilistic algorithm returns either a prime or a composite based on the following rules:
		- a) If the integer to be tested is actually a prime, the algorithm definitely returns a prime.
		- b) If the integer to be tested is actually a composite, it returns a composite with probability 1− ε, but it may return a prime with the probability ε.
- <font color="#00b050">Fermat’s test</font>
	- a^(p) - a -> 'p' is prime if this is a multiple of 'p' for all 1<=a < p.
	- Example : 
		- Is 5 prime?
			- 1^5 - 1 = 1 - 1 = 0 [0 is a multiple of 5]
			- 2^5 - 2 = 32 = 2 = 30 [30 is a multiple of 5]
			- 3^5 - 3 = 243 - 3 = 240 [240 is a multiple of 5]
			- 4^5 - 4 = 1024 = 1020 [1020 is a multiple of 5]
		- therefore 5 is a prime number
	- For short method we use formulas : 
		- If n is prime, a^n-1 ≡ 1 mod n
		- If n is composite, it is possible that a^(n-1) ≡ 1 mod n
	- Example : Does the number 561 pass the Fermat test?
		- a = 2
			2 ^ 560 ≡ 1 mod 561 [Remainder 0]
		- As it fails to accept the condition with a = 2 then 561 doesn't pass the Fermat test.
- <font color="#00b050">Miller-Rabin test</font>
	- It is  a probabilistic primality test 
	- It combines the Fermat test and the square root test in a very elegant way to find a strong pseudoprime.
	- Algorithm : 
		- Miller_Rabin_test(n,a)
			{
			// find m and k such that *n-1 = m x 2^k*
			T <- a^(m) mod n 
			if(T+- 1) return "a prime"
			for (i <- 1 to k-1)
			{
				T <- T^2 mod n
				if(T = 1) return "a composite"
				if(T = -1) return "a prime"
			 } 
			 return "a composite"
			}
		- Example : Is 561 prime??
			- Step 1 :
				- n = 561, [n-1  = 2^k x m]
				- 560 = 2^4 x 35 [k =4 and m=35]
			- Step 2 :
				- *a = 2* ; 1< ( a *=2* ) <560 [Condition satisfied]
			- Step 3 :
				- Compute b0 = a^m (mod n)
				- b0 = 2^35 (mod 561) = 263
				- Since b0 is neither +1 or -1 we will have to calculate b1.
			- Step 4 :
				- b1 = b0^2 (mod n)
				- b1 = 263 ^ 2 (mod 561) =  166
				- Since b1 is neither +1 or -1, we will go for b2.
			- Step 5:
				- Process goes on till we get bn = +1/-1
				- In this case we get *b3 = +1 which signifies 561 is composite* 
		- Example : Is 53 prime??
## Chinese remainder theorem :
- It is used to solve a set of congruent equations with one variable but different moduli, which are relatively prime,
	- X ≡ a1 (mod m1)
	- X ≡ a2 (mod m2)
	- .....
	- X ≡ an (mod mn)
	- <font color="#4bacc6">CRT states that the above equations have a unique solution of moduli are relatively prime.</font>
	- Formula : 
	 <font color="#ffc000">X = (a1 x M1 x M1^(-1) + a2 x M2 x M2^(-1) + ..... + an x Mn x Mn^(-1)) Mod M</font>
- Example 1 : Solve the following equations using CRT : 
	- X ≡ 2 (mod 3)
	- X ≡ 3 (mod 5)
	- X ≡ 2 (mod 7)
- Solution 1 : 
	- Therefore, X = (a1 x M1 x M1^(-1) + a2 x M2 x M2^(-1) + a3 x M3 x M3^(-1)) mod M
	- Given : a1=2, a2=3, a3=2, m1=3, m2= 5, m3 =7 [m1,m2,m3 are relatively prime]
	- Value of M's
		- M = m1 x m2 x m3 = 2 x 5 x 7 = 105
		- M1 = M/m1 = 105/3 = 35 [Also can be done by multi. m2 x m3 = 7x5= 35]
		- M2 = M/m2 = 21
		- M3 = M/m3 = 15
		
		- M1 x M1^(-1) = 1 mod m1 
			- 35 x M^(-1) = 1 mod 3
			- 35 x 2 = 1 mod 3 [just start assuming values from 1 to n]
			- [M1^(-1) = 2]
		- M2 x M2^(-1) = 1 mod m2 
			- 21 x M2^(-1) = 1 mod 5
			- 21 x 1 = 1 mod 5
			- [M2^(-1) = 1]
		- M3 x M3^(-1) = 1 mod m3
			- 15 x M3^(-1) = 1 mod 7
			- 15 x 1 = 1 mod 7
			- [M3^(-1) = 1]
	-  Putting values in formula : 
		- X =(a1 x M1 x M1^(-1) + a2 x M2 x M2^(-1) + a3 x M3 x M3^(-1)) mod M
		- X = (2x35x2 + 3x21x1 x 2x15x1) mod 105
		- X = 233 mod 105 = 105 
		- *X = 23*
