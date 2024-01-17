Link: https://leetcode.com/problems/find-the-duplicate-number/

Data structure:  [[Arrays]]

Approach-1:
- Make a hash array
- Traverse the array and record the numbers present
- Traverse hash array, if any number has more than one occurrence, return index
- If traversed hash array, return -1
- TC: O(n)
- SC: O(n)
- **Can use a bit as hash to reduce SC to O(1)

Approach-2:
- Traverse the array and compare i<sup>th</sup> element with all remaining elements.
- Use nested loops for same
- TC: O(n<sup>2</sup>)
- SC: O(1)

#arrays