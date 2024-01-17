Link: https://leetcode.com/problems/check-if-word-is-valid-after-substitutions/

Approach-1:
- If `s[0]!='a'` or `s[s.size()-1]!='c'`, return false (all valid strings will start with a and end with c)
- Initialize a stack and start a for loop
- Write conditions as following:
	- If character is a, push to stack
	- Else if character is b, check if the top of stack is a, if yes, then push b else, return false
	- Else (character is c) check if top is b, if yes, pop b and check top again, if it's a, pop and continue. If conditions fail to match anywhere, return false
- TC: **O(n)**
- SC: **O(n)**

Approach-2:
- Run a while loop to find if string contains substring `"abc"` 
- If yes, delete it and check again, continue till either there is no occurrence or size is less than 3
- Return `s.empty()`
- TC: **O(n<sup>2</sup>)**
- SC: **O(1)**

#stack #leetcode 