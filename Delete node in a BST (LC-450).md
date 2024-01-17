Link: https://leetcode.com/problems/delete-node-in-a-bst/

Approach:
- Find the node on the go using preorder approach
- Whenever found, delete node(4 cases):
	- No left child but right child: Return right child
	- No right child but left child: Return left child
	- No child nodes: Return NULL
	- Both nodes:
		- Find inorder successor (min of right subtree) || inorder predecessor (max of left subtree)
		- Swap current root value with this
		- Recursive call in the chosen direction to delete the predecessor or successor (whichever used)
- TC: **O(n)**
- SC: **O(H)**

#bst #leetcode 