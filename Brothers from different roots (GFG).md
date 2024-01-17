Link:

Approach:
- Traverse one tree inorder, other in reverse inorder using iterative approach in an intine while loop
- Break if either stack gets empty (cannot make a pair with one tree value only)
- Pick and check if values make sum during traversal in each iteration:
	- If (sum<target): Maximize sum (pop inorder tree stack)
	- If (sum>target): Minimize sum (pop reverse inorder tree stack)
	- If(sum = = target): Pop both stacks

//You can do the same using two vectors to store inorders (as it is and reverse) 

#bst #geeksforgeeks #hard