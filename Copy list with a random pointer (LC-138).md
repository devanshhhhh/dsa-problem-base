Link: https://leetcode.com/problems/copy-list-with-random-pointer/

Approach:
- Insert the new nodes just after the node itself
- For random pointer run another loop from the head 
- If random pointer of a node is not NULL, `temp->next->random=temp->random->next`
- After this, detach the old and new linked lists and return a new one (be careful and use a temporary pointer to store cloned node while changing links)
- TC: **O(n)**
- SC: **O(1)**

#lists #hard #leetcode 