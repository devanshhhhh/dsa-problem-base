Link: https://leetcode.com/problems/reverse-linked-list

Approach:
- if head is NULL or head is the only component, return head
- Assign two node pointers curr and prev
- Assign head to curr
- Run a while loop till curr!=NULL 
- In the loop, take a forward node pointer to store the remaining linked list (`forward=curr->next`)
- Assign `curr->next=prev` (curr now points to prev)
- Update new `prev=curr` (next node will pointy to this)
- Assign forward to curr and continue(`curr=forward`) and continue
- Return prev (head of reversed linked list)
- SC: **O(n)**
- TC: **O(1)**

#lists #leetcode 