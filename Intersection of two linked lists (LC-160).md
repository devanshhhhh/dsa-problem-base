Link: https://leetcode.com/problems/intersection-of-two-linked-lists/

Approach:
- Traverse both the linked lists till at least one of them becomes NULL
- Once done, you will find small and big linked lists, find the gap by traversing the other one
- Now, traverse the linked lists from head again but give the bigger one a headstart of gap nodes
- In all the loops keep checking if both the nodes ever become equal, if yes, return the node and stop
- If all the loops have ended, return NULL
- TC: **O(n)**
- SC: **O(1)**

***(Write generalized code for either of the linked lists being larger, use a bool switch for the same)***


#lists #hard #leetcode 