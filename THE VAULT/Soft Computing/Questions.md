### Fuzzy Sets terminologies :
- <font color="#ffc000">Core :</font> The **core** of a fuzzy set 𝐴 is the set of all elements 𝑥 in the universe of discourse 𝑋 where the membership function 𝜇𝐴(𝑥) is equal to 1. In other words, it consists of all elements that fully belong to the fuzzy set.
- <font color="#ffc000">Support :</font> The **support** of a fuzzy set 𝐴 is the set of all elements 𝑥x in the universe of discourse 𝑋 where the membership function 𝜇𝐴(𝑥) is greater than 0. It includes all elements that have a non-zero degree of membership in the fuzzy set.
- <font color="#ffc000">Singleton Set :</font> A **singleton set** in the context of fuzzy sets is a fuzzy set where only one element has a non-zero membership value, and that value is typically 1.
- <font color="#ffc000">Band Width :</font> The **band width** of a fuzzy set refers to the range of values in the universe of discourse over which the membership function is non-zero. It essentially describes the spread or width of the fuzzy set.
- <font color="#ffc000">Cross-over Points :</font> **Cross-over points** are the values of 𝑥x in the universe of discourse where the membership function 𝜇𝐴(𝑥)μA​(x) is equal to 0.5. These points indicate where the membership grade of the fuzzy set transitions from being less than 0.5 to greater than 0.5, or vice versa.
- <font color="#ffc000">Convexity :</font> A fuzzy set 𝐴A is **convex** if for any two elements 𝑥1x1​ and 𝑥2x2​ in the universe of discourse 𝑋X, and for any 𝜆∈[0,1]λ∈[0,1], the membership function satisfies :
	-> 𝜇𝐴 (𝜆𝑥1 + (1−𝜆) 𝑥2) *≥* min⁡(𝜇𝐴(𝑥1) , 𝜇𝐴(𝑥2)) 
	This means that the membership grade of any point between 𝑥1 and 𝑥2​ should not be less than the minimum membership grade of 𝑥1​ and 𝑥2.
- <font color="#ffc000">Normality :</font> A fuzzy set 𝐴 is **normal** if there is at least one element in the universe of discourse 𝑋X whose membership grade is 1. In other words, the maximum membership grade in the fuzzy set is 1.

### Consider the Following membership Functions: 
- A = {(x1, 0.3). (x2, 0.5), (x3,1), (x4,0.8),(x5,0.1)} 
- B = {(x1, 0.5). (x2, 0.2). (x3,0.7), (x4,0.4), (x5,0.6)}
- Perform the following Fuzzy Operations on these fuzzy sets:
	a. Algebraic sum [uA(x) + uB(x) - uA(x) * uB(x)]
	b. Algebraic difference []
	c. Bounded sum [uA(x) (+) uB(x) = min { 1, uA(x) + uB(x) }]
	d. Union [uAUB(x) = max { uA(x), uB(x) }]
	e. Algebraic product [uA.B(x) = uA(x) * uB(x )]
	f. Bounded difference [uA(x) (-) uB(x) = max { 1, uA(x) + uB(x) }]
	g. Cartesian product [uAxB(x,y) = min { uA(x), uB(x) }]
![[WhatsApp Image 2024-02-21 at 13.07.58_f0ced6d4.jpg]]