Link: https://leetcode.com/problems/isomorphic-strings

Approach: 
- Use two maps and map all characters to each other using a while loop
- If the characters are unmapped, map them
- If already mapped, check if the mapping is for each other only
- If yes, the continue, else return false
- If loop has ended return true
- TC: **O(n)**
- SC: **O(n)**

#strings #hard #leetcode 