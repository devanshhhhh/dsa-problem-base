Link: https://leetcode.com/problems/decode-string/

Approach:
- Initialize a stack of strings and push all the characters as strings
- When you find a closing bracket, start decoding it
- Run a while loop adding all elements that are popped from the stack before finding an opening bracket (this string will be repeated)
- Ignore the opening bracket
- Do the same process for finding the numeric string and use stoi after reversing the string to find the integer number
- Repeat the found string for given numeric value
- Push the string on top of the stack and continue
- Once done all your answer strings are in the stack
- Pop and concatenate strings till stack is not empty
- Reverse the concatenated answer and return 
- TC: **O(n)**
- SC: **O(n)**

#stack #hard #leetcode 