Link: https://practice.geeksforgeeks.org/problems/gcd-of-two-numbers3459/1

Approach: 
*****Extended Euclidean Theorem***
- Write a recursive function
- Base conditions 
	- `if(A==0) return B`
	- `if(B==0) return A`
- Recursive calls
	- `if(A>B) return gcd(A-B, A)`
	- `else return gcd(B-A, B)`
- TC: **O(log(min(A, B)))**
- SC: **O(1)**


#math #geeksforgeeks 