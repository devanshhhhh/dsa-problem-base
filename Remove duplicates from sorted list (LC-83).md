Link: https://leetcode.com/problems/remove-duplicates-from-sorted-list/

Approach:
- Return head if `(head=NULL or head->next==NULL)`
- Take a node pointer temp and assign it head
- Run a while loop till `temp->next!=NULL`
- If `temp->val==temp->next->val` use a new node pointer to save that `del=temp->next`
- Connect `temp->next` to the next of pointer that's being deleted `(temp->next=del->next)`
- Delete `del` and continue
- Else if values are different, `temp=temp->next`
- TC: **O(n)**
- SC: **O(1)**

#lists #leetcode 