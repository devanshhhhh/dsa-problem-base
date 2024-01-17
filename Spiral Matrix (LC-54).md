Link: https://leetcode.com/problems/spiral-matrix/

Approach: 
- Find total elements=(m*\n)
- Print first row, (startingRow++)
- Print last column, (endingColumn--)
- Print last row, (endingRow--)
- Print first column, (startingColumn++)
- Repeat this while count<\total
- TC: **O(n<sup>2</sup>)**
-  SC: **O(n<sup>2</sup>)**

#matrix #leetcode 