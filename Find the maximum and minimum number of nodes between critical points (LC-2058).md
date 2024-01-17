Link: https://leetcode.com/problems/find-the-minimum-and-maximum-number-of-nodes-between-critical-points/

Approach:
- Find critical points and store their positions (indices) in the vector
- If there are less than two points push -1 and -1 and return
- Else, now calculate the maximum distance by calculation difference for first and last critical points
- For minimum distance, iterate over critical points vector and calculate for all points
- Push minimum and maximum distance and return ans vector
- TC: **O(n)**
- SC: **O(n)**

#lists #leetcode 