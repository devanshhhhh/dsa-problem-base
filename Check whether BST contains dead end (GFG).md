Link: https://practice.geeksforgeeks.org/problems/check-whether-bst-contains-dead-end/1 

Approach:
- Map all BST nodes and check on leaf nodes if (+1) && (-1) values exist in the tree (on the go)
- If yes, then it has a dead end, return true
- Also, mark 0 existing in the map explicitly because 0 cannot be found but it cannot be inserted by rule. Therefore, we need true for (2) only to mark 1 as dead end.


#bst #geeksforgeeks 