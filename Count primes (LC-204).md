Link: https://leetcode.com/problems/count-primes/

Approach:
*****Sieve of Eratosthenes*** 
- Take a bool vector of size `(n+1)` initialized with 1, each index representing a number till n 
- Mark 0 and 1 indices as false 
- Run a for loop `for(i=2; i<n; i++)` 
- In this, check if `v[i]==true`, if no, continue
- Else if (true), `primesCount++`
- Now enter another nested for loop `for(j=i+i; j<n; j=j+i)`
- In this mark all j indices as false in vector `v[j]=false` (eliminating all multiples of `i` for checking)
- Return `primeCount` at the end of all loops
- TC: **O(nlog(logn))**
- SC: **O(n)**

#leetcode #math 