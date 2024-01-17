Link: https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/

Approach:
- Maintain an array to store each current level 
- Use `NULL` as delimiter 
- When encountered push `ans` vector to `sol` and clear it
- Keep a level counter as well
- If counter value is odd, reverse `ans` before inserting 
- Else, insert as it is
- Refer to [[Basics-Trees]] (Level order traversal)


#trees #leetcode 