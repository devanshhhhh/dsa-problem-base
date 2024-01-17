Link: https://practice.geeksforgeeks.org/problems/sum-tree/1

Approach:
- Use a helper sum function returning `root->val+sum(root->left)+sum(root->right)`
- Write a recursive function with base case if `!root` or `isLeafNode()` return true
- Check if sum of left and right subtree `sums==root->val`:
	- `if(root->val==sum(root->left)+sum(root->right))`
- If yes, recursive calls for left and right and return their `&&`
	- `return isSumTree(root->left) && isSumTree(root->right);`
- Else, return false


#trees #geeksforgeeks #hard 