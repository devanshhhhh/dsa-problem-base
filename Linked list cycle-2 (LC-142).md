Link: https://leetcode.com/problems/linked-list-cycle-ii/

Variation of [[Linked list cycle (LC-141)]] 

Approach:
*\*****(Hare Tortoise algorithm)***:
- In the loop to find if a cycle exists, keep checking if  `(slow==fast)`, break if this condition is true
- Write a check so find if the loop was terminated on its own or by the condition check (return NULL if the condition did not break the loop)
- Else (if condition broke the loop) assign head to slow pointer and start moving both fast and slow pointer by a step till they meet again
- Return slow/fast when they point to the same node this time
- TC: **O(n)**
- SC: **O(1)**

#lists #leetcode #hard