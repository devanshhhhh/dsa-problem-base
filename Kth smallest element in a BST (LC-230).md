Link: https://leetcode.com/problems/kth-smallest-element-in-a-bst/ 

Approach:
- Use (LNR) inorder traversal sequence and process nodes in the middle (returning from left (min value), starting at root if there is no left):
	- `k--;`
	- `if(k==0) k=-1; ans= root->val; return;`

#bst #leetcode 