Link: https://leetcode.com/problems/reverse-only-letters/

Approach:
- Take two pointers as i=0 and j=s.size()-1
- Start shrinking the array
- If a given characters are in range of english alphabets, swap them and increment i, decrement j
- If i is not valid, i++
- If j is not valid, j--
- Return the string itself after loop ends
- TC: **O(n)**
- SC: **O(1)**

#strings #leetcode 