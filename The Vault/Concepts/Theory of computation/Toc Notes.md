#Concepts 
DFA vs NDFA :-
	- It depends on acceptance of language
	- NDFA is understood as multiple small machines computing at the same time
	- Every DFA is a NDFA while vice versa is false. 
	- There can be multiple endpoints for both 
	- Depends on Lexical analysis : Tells if spells are correct or not in a language. Keyword is correct or not. Example : Python, java, C++, js., etc...
	- Every compiler is based on DFA currently but not on NDFA as it is a theoretical concept.

Topic 2 :- 
-How to convert NFA into DFA steps:-
 - Use the same transition table of NDFA 
 - Number of states increases in DFA if compared to NDFA
 - Starting state is always common :- Refer to copy from now on 

- Two-way automata : 
	- Collection of 8 tuples (Q)


<center>TOC Chapter 2</center>

Question 1 : 
	Write the language and expression for exact length 2.
- Solution : 
	- Regular expression : {aa,ab,ba,bb} 
Question 2 : 
	Write the language and expression for utmost length 2.
	
- Solution :
	- Regular expression: {Epsilon+a+b}{Epsilon+a+b}{Epsilon+a+b}
	 
Question 3 : For languages with utmost 2b's and 1 a's.	
- Solution :
	- Language : Epsilon,a,b,bb,ba,abb,bba,bab
	- RE = Epsilon+a+bb+ba+...........

Question 4: All strings having at least 1 b.
- Solution : 
	- RE = (a+b)* b (a+b)* 

Question 5 : Strings having bbbb as sub string.
- Solution : 
	- RE = (a+b)* bbbb (a+b)*

Question 6 : All strings ending with ab.
- Solution : 
	- RE = (a+b)* ab

Question 7 : All strings begning and ending with a.
- Solution : 
	- RE = a (a+b)* b

Question 8 : Containing a.
- Solution : 
	- RE = (a+b)* a (a+b)*

Question 9 : Staring and ending with different symbols.
- Solutions : 
	- RE = (a+b)* (a+b) and a(a+b)* b + b(a+b)* a

Question 10 : All Strings having 2 b's.
- Solutions : 
	- RE = (a)* b (a)* b (a)*

Question 11 : 