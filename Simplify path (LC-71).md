Link: https://leetcode.com/problems/simplify-path/

Approach:
- Pre-defined rules:
	- `/..` means go back a directory
	- `/` marks the end and beginning of directories
	- `/.` means stay in the same directory
	- `/` are to be ignored (problem statement)
- Take a `stack<string>` to store directories going forward in the path string
- Run a while loop till you iterate to the end of the path string
- In each iteration, make a substring of the directory given (select character including first `'/'` upto but not including next `'/'`) 
- Compare the substring with above pre-defined rules, push the substring if it's not `/..`, else pop if it is `/..`
- Ignore in other cases
- After the loop, convert the answer stored in stack to string (try using a recursive function)
- TC: **O(n)**
- SC: **O(n)**

#stack #leetcode 