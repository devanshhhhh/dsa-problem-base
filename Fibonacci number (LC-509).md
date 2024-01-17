Link: https://leetcode.com/problems/fibonacci-number/


Approach: 
- Write a recursive function with base condition: `if(n<=1) return n;` (check constraints for possible invalid n values)
- Recursive call: `return fib(n-2)+fib(n-1)`
- TC: **O(n)**
- SC: **O(n)** if you consider the recursive stack, else **O(1)**

#recursion #leetcode 