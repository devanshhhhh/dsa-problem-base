Link: https://leetcode.com/problems/flatten-binary-tree-to-linked-list/

Approach:
//Similar to Morris traversal
- Run a while loop will `curr!=NULL`
- If `(curr->left)`:
	- `TreeNode* pre=curr->left`
	 //Go left, then keep going right 
	- `while(pre->right) pre=pre->right;`
	- Once found:
		- Link its right to `curr->right`: `pre->right=curr->right;`      
		 //Link right subtree at tail of left subtree
		- Make `curr->right=curr->left`        
		 //Insert left subtree after root
		- Make `pre->left=NULL;`      //Free-up left links
- Move to curr->right: `curr=curr->right;`


#trees #hard #leetcode 