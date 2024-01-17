Link: https://leetcode.com/problems/flatten-a-multilevel-doubly-linked-list/

Approach: 
- Traverse through the linked list and pass them in expand function 
- The expand function checks if the node's child pointer is not NULL, if not NULL, it expands (inserts the child level in current level between current and next nodes) and returns
- Continue the traversal (If a list has multiple levels, it will be handled because the nodes will be visited again after expansion in the main loop)
- TC: **O(n)**
- SC: **O(1)**

#lists #leetcode 