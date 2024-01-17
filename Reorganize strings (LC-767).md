Link: https://leetcode.com/problems/reorganize-string

Approach:
- Take a int `i=0` for a running a while loop
- Run it for `i<(n-1)`, comparing adjacent elements
- If `i+1` and `i` elements are same, assign `swapIndex=i+1`
- Start a loop with `int j=swapIndex+1`, increment j till a new element is found and `j<n`
- After loop check if `(j>n)`, if yes, break else `swap(s[swapIndex], s[j])` and update `i=swapIndex+1`
- Else, `i++`
- Once the loop ends, write this implementation for reverse array as well (return empty string if `j` goes out of bounds in this case)
- Return `s`
- TC: **O(n<sup>2</sup>)**
- SC: **O(1)**

#strings  #leetcode 