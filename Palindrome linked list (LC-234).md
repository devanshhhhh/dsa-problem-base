Link: https://leetcode.com/problems/palindrome-linked-list/

Approach:
- Find the mid point (first one) and divide the linked list in half ([[Middle of the linked list (LC-876)]])
- Reverse the second half of the linked list ([[Reverse a linked list (LC-206)]])
- Compare both halves till `(head!=NULL && mid!=NULL)` 
- Return true if the loop ends, else false will be returned if the vals in nodes are not equal
- TC: **O(n)**
- SC: **O(1)**

 ***(This will handle both odd and even cases because if there is an extra element, it will be on the reversed side and would be at the end, so the first half would hit NULL and the loop will terminate and function will return true)***

#lists #hard #leetcode 