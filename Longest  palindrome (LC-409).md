Link: https://leetcode.com/problems/longest-palindrome

Approach: 
- Make an hash array and record occurrences
- Take a bool variable `check` and set it to false 
- Iterate through the array and if `hash[i]` is even, add it to the answer
- If the `hash[i]` is odd, check if it's `1`, if it's `1` and `check` variable if set to false, add it to answer and assign true to check variable (it includes 1 odd element to be in the middle of the palindrome)
- Else if it's not `1`, add `(hash[i]-1)` to answer (it includes all even occurrences)
- Also, put the condition to check for including one odd occurrences in the else block of odd variables `(hash[i]!=1)` incase there is no single occurrences but other odd occurrences 
- TC: **O(n)**
- SC: **O(1)** as hash array is of constant size (128)

#strings #leetcode 