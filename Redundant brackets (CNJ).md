Link: https://www.codingninjas.com/studio/problems/redundant-brackets_975473

Approach:
- If character is an opening bracket or an operator, push it in the stack
- If it's a closing bracket, start popping the stack, if you find an operator turn on a bool switch
- If you find an opening bracket in the stack and the switch is on (true), pop it and break the loop, continue the main loop
- Else (if you don't find an opening bracket or if the switch is off) return true
- If all the loops have ended, return false
- TC: **O(n<sup>2</sup>)**
- SC: **O(n)**

#stack #codingninjas 