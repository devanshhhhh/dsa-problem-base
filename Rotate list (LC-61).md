Link: https://leetcode.com/problems/rotate-list/

Approach: 
- Find the length of the list
- Mod the k value with n to find the actual number of rotations
- If `k==0`, return head
- Else find `newLastNode=len-k-1`
- Break the remaining linked list and join it at the head
- Return the new head
- TC: **O(n)**
- SC: **O(1)**

#lists #leetcode 