Link:  https://leetcode.com/problems/remove-nth-node-from-end-of-list/


Approach-1: 
*\*****(Hare Tortoise algorithm)***:
- Take a dummy node and connect it before head
- Initialize two pointers fast and slow as head
- Move fast forward n times `(fast=fast->next)`
- Now take a prev pointer and initialize it with dummy `(prev=dummy)`
- Run a while loop that runs till `(fast->next!=NULL)`
- Move fast and slow one step at a time and store slow in prev (before increment)
- Once the loop ends, `(prev->next)` or `(slow)` will be the node to be deleted 
- Delete the node to be deleted
- Also update head with `head=dummy->next`
- Remove and delete dummy node
- Return head
- TC: **O(n)** single pass
- SC: **O(1)**


Approach-2: 
- Write a recursive function having `(headNode, currNode, n, count)
- Base case: `if(currNode==NULL) return currNode;`
- This function calls itself if `(currNode->next!=NULL)` with `curr->next=deleter(head, curr->next, n, count)`
- After the recursive call increment count (incrementing time at return time)
- Return `currNode` `if(count>n)`
- After check `if(n==count)` (checking count at return time)
- If yes, delete the `currNode` and return it's next (handle deleting the `headNode` differently by checking if `(currNode==headNode)`)
- Return `currNode` at the end
- TC: **O(n)**
- SC: **O(1)**

#lists #leetcode 