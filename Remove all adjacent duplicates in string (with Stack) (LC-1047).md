Link: https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string/

Approach:
- Initialize a stack 
- Run a loop and if stack is not empty and top of stack is same as current char, pop() from stack and continue
- Else, insert in stack
- After this loop, run a loop to copy your answer from stack to a string
- Reverse the ans string and return ans (because LIFO)
- TC: **O(n)**
- SC: **O(n)**

#stack #leetcode 