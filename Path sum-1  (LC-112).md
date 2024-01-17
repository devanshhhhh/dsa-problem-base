Link: https://leetcode.com/problems/path-sum/

Approach:
- Write a recursive function with base condition: `if(!root) return false;`
- Another base case for picking answer:
	- `if(target==sum+root->val && !root->left && !root->right) return true;`
	//We will only pick answer if the sum value becomes target at a leaf node
- Recursive calls to explore left and right nodes:
	- `bool left=hasPathSum(root->left, targetSum, sum+root->val);`
	- `bool right=hasPathSum(root->right, targetSum, sum+root->val);`
	- Return true if either is true: `return (left||right);`

#trees #leetcode 