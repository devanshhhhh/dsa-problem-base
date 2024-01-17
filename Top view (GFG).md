Link: https://practice.geeksforgeeks.org/problems/top-view-of-binary-tree/1

Approach:
- Use a map to store horizontal distance and the first corresponding element 
- Use a queue for level order traversal (Reference: [[Basics-Trees]])
- Along with level order store `horizontal_distance` in the queue
- Start with `0` and for left, do `-1`, for right do `+1`
- For each iteration store in map, only if there is no previous entry for certain `horizontal_distance`
- Push all elements from map to your answer vector and return

#trees #geeksforgeeks 