Link: https://leetcode.com/problems/reverse-nodes-in-k-group/

Approach: 
- Calculate the length of the linked list ([[Length of a linked list (Self)]])
- If `(len<k)`, return head
- Else initialize and int count=0 and run a while loop till `(count<k)`
- Reverse linked list in this while loop ([[Reverse a linked list (LC-206)]])
- After exiting if forward!=NULL write a recursive call `head->next=reverseKGroup(forward, k)` (head will be the new tail after reversing k nodes)
- Return prev (head of the new linked list)
- SC: **O(n)**
- TC: **O(1)**

#lists #leetcode #hard 