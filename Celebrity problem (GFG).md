Link: https://practice.geeksforgeeks.org/problems/the-celebrity-problem/1

Approach: 
- Push all the persons to stack (i/j) values
- Run a while loop while stack size>1
- Pop two top elements every time(a, b), check if a is a celebrity by comparing to b, if a is possible, push a and continue (b knows a so, b can't be an answer)
- Else, push b (b doesn't know a so, a can't be an answer
- Continue till last element is left
- Check last element left for being the answer (it's row should be all 0) && (it's columns except for its own should be all 1)
- If the check fails anywhere return -1
- If all loops have ended, return that element as answer
- TC: **O(n)**
- SC: **O(n)**

#stack #geeksforgeeks #hard 