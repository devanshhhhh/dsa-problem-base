Link: https://leetcode.com/problems/search-a-2d-matrix-ii/

Approach:
- As the row elements are ascending and column elements are also ascending, we will run a binary search to find the row which has a value larger than target. Then search the answer in the same row, by decreasing columns
- Initialize `row=0`, `column=matrix[0].size()-1`
- Write a binary search, if element is equal to target, return true
- Else if, (target<element), then decrement column
- Else (target>element), then increment row

#matrix 