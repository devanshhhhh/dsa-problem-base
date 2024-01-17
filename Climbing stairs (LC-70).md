Link: https://leetcode.com/problems/climbing-stairs/

Approach-1 (Brute-Force):
*****Inclusion exclusion approach***
- Write a recursive solver/helper function with parameters n and ans variable
- Write two recursive calls each passing (n-1) && (n-2) (meaning taking 1 step and 2 steps respectively and for each further n resultant value)
- Base conditions: 
	- `if(n==0) ans++; return;`
	- `if(n<0) return;`
- TC: 
- SC:

#recursion #leetcode 