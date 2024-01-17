Link: https://leetcode.com/problems/middle-of-the-linked-list

Approach:
*\*****(Hare Tortoise algorithm)***:
- Initialize two node pointers slow and fast assigning head pointer to both initially
- Move fast two times and slow one time in each iteration (slow only moves till fast can move two points) 
- while loop running condition: `(fast!=NULL && fast->next!=NULL)`
- After the end of loop, your slow pointer will be pointing at your middle node
- TC: **O(n)**
- SC: **O(1)**

//This is for finding (later) second middle node if the list as two middle nodes
//If you need the fist middle, initialize fast with `head->next` and slow as it is


#lists #leetcode 