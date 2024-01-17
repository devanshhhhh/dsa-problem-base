Link: https://leetcode.com/problems/maximal-rectangle/

Approach:
- Consider these as histograms
- Convert by adding rows above them (starting with 0<sup>th</sup> row expanding down)
- Do not add if the base element is 0
- Call histogram's max rectangle calculator function on each row, update maxArea
- Helper function: [[Largest rectangle in histogram (LC-84)]] 
- TC: **O(n)**
- SC: **O(n)**


#stack #leetcode 