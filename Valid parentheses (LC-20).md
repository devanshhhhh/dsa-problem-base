Link: https://leetcode.com/problems/valid-parentheses

Approach:
- If the current character is an opening bracket, push it in stack
- If it's a closing bracket check if stack is empty, if yes, return false
- If stack is not empty, check if the top is the corresponding opening bracket, if yes then pop the top and continue
- Else return false
- If the loop has ended, return true if stack is empty, else false
- TC: **O(n)**
- SC: **O(n)**

#stack #leetcode 