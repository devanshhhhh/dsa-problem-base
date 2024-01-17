Link: https://leetcode.com/problems/binary-tree-right-side-view/

Approach:
- Use a map to store `depth` and the first corresponding element 
- Use a recursive function for traversal (NRL) (Reference: [[Basics-Trees]])
- Start with `0` and for left, do `+1`, for right do `+1`
- For each iteration store in map, only if there is no previous entry for certain `depth`
- Push all elements from map to your answer vector and return

Optimization:
//Instead of using a `map` you can pass the `ans` vector and if the `(ans.size()==depth)` push current value (same size indicates no entry for current depth yet as arrays are 0-indexed)


#trees #leetcode 