Link: https://leetcode.com/problems/balanced-binary-tree/

Approach-1:
- You need to calculate height for each node (Helper function: [[Maximum depth of a binary tree (LC-104)]])
- Calculate heights for left and right subtrees:
	- `int left=maxDepth(root->left);`
	- `int right=maxDepth(root->right);`
- Check `if (abs(right-left)<2)`:
	- `return balanced(root->left) && balanced(root->right)`
- Else
	- `return false;`
- Base condition: 
	- `if(!root) return false;`
- TC: **O(n<sup>2</sup>)**

Approach-2:
//Optimizing approach-1
- Instead of calling `isBalanced()` for each node, check condition at each recursive call and update accordingly
- Take a global variable to your solution class to store and update answer and initialize it to `true`
	- `bool balanced=true;`
- Now after your recursive calls for left and right subtrees, check the condition and update answer:
	-  `if (balanced && abs(right-left)>1)`:
		- `balanced=false;`
- Now you just have to call `maxDepth()` from your main `isBalanced()` function and you can return `balanced` variable as answer
- TC: **O(n)**

#trees #leetcode 