Link: https://leetcode.com/problems/search-a-2d-matrix/


Approach-1:
- Initialize `start=0` and `end=(rows*cols)-1`
- Run a binary search with rows as `mid/col` and columns as `mid%col`
- TC: **O(log(m*\n))**
- SC: **O(1)**

Approach-2:
- Apply binary search just in last column values of all rows
- If target is found, return true 
- Else, store the row that has last column value less than target
- Increment rowToSearch by 1
- After that, check if the rowToSearch is valid, if not, return false
- If valid, apply binary search on all column values of that row
- TC: **O(log(m*\n))**
- SC: **O(1)**

#matrix 