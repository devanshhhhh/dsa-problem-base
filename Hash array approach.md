Approach-1:
- Make a hash array
- Traverse the array and record the numbers present (increment hash array index for that element)
- In same traversal, keep checking if any number has more than one occurrence, return index
- If traversed hash array, return -1
- TC: O(n)
- SC: O(n)
- **Can use a bit as hash to reduce SC to O(1)

#arrays 
#hashArray