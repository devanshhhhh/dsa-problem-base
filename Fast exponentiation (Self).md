Link: https://www.codingninjas.com/studio/problems/modular-exponentiation_1082146

Approach:
*****Binary exponentiation*** 
- Write a recursive function
- Base condition: `if(B==0) return 1`
- Then initialize an int `res=power(A, B/2)`
- Write a conditional statement, `if(A==even) return res*res`
- Else `(A==odd) return res*res*A` 
- TC: **O(log B)**
- SC: **O(log B)** if we consider recursive stack

#math #self 