Link: https://leetcode.com/problems/diameter-of-binary-tree/

Approach:
- Use the `maxDepth()` helper method: 
- Answer can lie in `left subtree`, `right subtree` or `across`
- So, write a recursive function with base condition: `if(!root) return 0;`
- Calculate for across: `int cross=maxDepth(root->left)+maxDepth(root->right);`
- Recursive call for left: `int left=diameter(root->left);`
- Recursive call for right: `int right=diameter(root->right);`
- Return `max(cross, max(left, right));`
- TC: **O(n<sup>2</sup>)**

Approach-2:
//Optimizing approach-1
- Instead of calling `diameter()` for each node, check condition at each recursive call and update accordingly
- Take a global variable to your solution class to store and update answer and initialize it to `0`
	- `int maxD=0;`
- Now after your recursive calls for left and right subtrees, you check if current diameter is greater and update answer:
	-  `int currD=left+right`:
	- `maxD=max(maxD, currD);`
- Now you just have to call `maxDepth()` from your main `diameter()` function and you can return `maxD` variable as answer
- TC: **O(n)**

#trees #leetcode 