Link: https://leetcode.com/problems/wildcard-matching/

Approach:
- Take two index pointer `si` and `pi` for s and p each (declare default arguments initialized as 0)
- Write conditions for matching
	- `if(s[si]==p[pi]  ||  p[pi]=='?')` consume p char with s char and move ahead so, recursive call `return(s, p, si+1, pi+1)`
	- `if(s[i]=='*')`, we can't be sure of how many characters of s should be consumed with `'*'`, so we run two recursive calls splitting tree of solutions, `bool a=return(s, p, si, pi+1)` and `bool b=return(s, p, si+1, pi)`, we return true if either of them are true (`return a||b`)
- Base conditions:
	- return true if both the s and p strings are over
	- if s is over but p is remaining, check if all remaining p string chars are `'*'` , if yes, they can be consumed for no character so return true, else false
	- return false at the end of the function (s not over, p over)


#recursion #leetcode #hard 