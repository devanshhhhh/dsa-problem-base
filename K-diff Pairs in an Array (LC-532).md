Link: https://leetcode.com/problems/k-diff-pairs-in-an-array/

Approach:
- Sort the given array
- Initialize a `set<pair<int, int>>` to store unique pairs
- Initialize two int `i=0`,` j=i+1` to check your array
- If difference of elements is equal to target, insert pair in set, increment `i`and `j`
- Else if difference is greater than target, increment `i` to shrink the difference
- Else if difference is lesser than target, increment `j` to increase difference
- If `i==j`, increment `j`
- Return size of set once the loop ends
- TC: **O(n log n)**
- SC: **O(n)** if you count the ans set, else **O(1)**

#searching
