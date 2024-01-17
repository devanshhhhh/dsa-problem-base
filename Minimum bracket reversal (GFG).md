Link: https://practice.geeksforgeeks.org/problems/count-the-reversals0401/1

Approach: 
- If the size of string is odd, return -1 (impossible to create a valid expression of parentheses)
- Else initialize a stack and a count variable and if it's an opening bracket, insert in stack
- If it's a closing bracket, check if the top() of stack is an opening bracket (check empty() before checking top())
- If yes, pop() the opening bracket, else insert the closing bracket
- Once the loop ends, return 0 if stack size is 0 (optional if statement //Avoid)
- Run a while loop till stack is not empty
- Pop() two top chars and compare them, if `ch1==ch2`, count+=1
- Else, count+=2
- Return count after the loop ends
- TC: **O(n)**
- SC: **O(n)**


#stack #geeksforgeeks 