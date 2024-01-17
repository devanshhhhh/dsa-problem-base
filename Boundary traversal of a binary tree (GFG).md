Link: https://practice.geeksforgeeks.org/problems/boundary-traversal-of-binary-tree/1

Approach:
- Print the left boundary nodes first:
	- Base conditions
		- Return if node is null or if it is a leaf node (skip leaf nodes)
	- Flow:
		-  Print current
		- If (root->left) printLeft(root->left);
		- Else printLeft(root->right); 
		//Makes sure you stay in left most boundary
- Print all leaf nodes
	- Base conditions
		- Return if node is null or if it is a leaf node (print in second base condition ie, leaf nodes)
	- Flow
		- printLeaf(root->left);
		- printLeaf(root->right); 
-  Print the right boundary nodes first:
	- Base conditions
		- Return if node is null or if it is a leaf node (skip leaf nodes)
	- Flow:
		- If (root->right) printRight(root->right);
		- Else printRight(root->left); 
		- Print current                //Tail recursion for inverse output
		 //Makes sure you stay in right most boundary
- Handle root separately in main function to skip printing it multiple times (left and right)

#trees #geeksforgeeks 