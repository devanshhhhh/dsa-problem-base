Link: https://leetcode.com/problems/perfect-squares/

Approach: 
*****Inclusion exclusion approach***
- Write a recursive function with base cases:
	- `if(n==0)` check if `nums` less than `minNums`, if yes, update and return else, just return
	- `if(n<(i*i))` checking if we can subtract i<sup>th</sup> square 
- Then three recursive calls:
	- Include `i` and move to next: `solver(n-(i*i), minNums, nums+1, i+1)`
	- Exclude `i` and move to next: `solver(n, minNums, nums, i+1)`
	- Include `i` and but don't move to next: `solver(n-(i*i), minNums, nums+1, i)`
- TC: **O(3<sup>n</sup>)**
- SC: **O(3<sup>n</sup>)** if we consider recursive stack, else **O(1)**


#recursion #leetcode 