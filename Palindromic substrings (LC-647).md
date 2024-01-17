Link: https://leetcode.com/problems/palindromic-substrings/

Approach-1:
- Run a for loop to get the pointers
- Write  a check function that tries placing i, j and expanding on both sides
- If i<sup>th</sup> and j<sup>th</sup> element are same, it's a palindromic substring
- For odd strings start i and j at same index
- For even strings start at i and i+1
- TC: **O(n<sup>2</sup>)**
- SC: **O(1)**

Approach-2:
- Run nested while loops making all substrings
- Write a function to check palindromes
- Check all substrings
- TC: **O(n<sup>3</sup>)**
- SC: **O(1)**

#strings #hard #leetcode 