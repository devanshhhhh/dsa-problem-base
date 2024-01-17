Link: https://leetcode.com/problems/longest-valid-parentheses

Approach:
- Create an integer stack and push -1 to it 
- Traverse the string and push the current index whenever you find an opening bracket (start of an expression)
- Else (closing bracket), pop from the stack, (if there was no opening bracket, -1 will be popped) 
- After that, check if stack is empty (no opening bracket), push i in that case (next valid expression can start only after i index now)
- Else, stack not empty, update length with currIndex-st.top (i-(-1)) which means there is a valid expression on length i+1
- After this check if length > maxLength, if yes, update maxLength and continue, else, continue
- Return maxLength after the loop ends
- TC: **O(n)**
- SC: **O(n)**


#stack #leetcode #hard  