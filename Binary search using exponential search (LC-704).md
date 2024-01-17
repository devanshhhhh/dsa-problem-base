Link: https://leetcode.com/problems/binary-search/

Approach:
- Take a int variable `i=0` 
- Use a while loop till `arr[n]<=target`, increment `i` with `i=i*2`
- Once the loop ends, run a binary search from `i/2` to `min(n-1, i)`
- TC: **O(log n)**
- SC: **O(1)**

***Use the same approach for unbounded binary search***

#searching #leetcode 