Link: https://leetcode.com/problems/minimum-time-difference/description/

Approach:
- Convert all string to integer values of minutes
- Sort the minutes vector
- Find differences between the adjacent elements to find the minimum difference
- ***Edge case handling:*** Time is circular so subtract last element from first one, adding 1440 (total minutes in a day) to the first element
- TC: **O(n log n)**
- SC: **O(n)**

#strings #hard #leetcode 