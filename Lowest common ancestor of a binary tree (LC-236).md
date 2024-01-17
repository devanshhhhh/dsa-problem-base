Link: https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/

Approach:
- Write a recursive function with base condition: `if(!root) return NULL;`
- Answer based base condition: `if(root==p || root==q) return root;`
- Check for left: `TreeNode* left=ancestors(root->left, p, q);`
- Check for right: `TreeNode* right=ancestors(root->right, p, q);`
- Now conditions for picking answer:
	- `if(left && right) return root; `              //Current node is an ancestor to both
	- `else if(left && !right) return left;`     //One node if found in the left subtree (current ancestor)
	- `else return right;`                                    //One node if found in the right subtree (current ancestor)


#trees #leetcode 