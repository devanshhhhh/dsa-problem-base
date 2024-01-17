Link: https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/

Approach:
- As `preorder` follows (NLR) and `inorder` follows (LNR), we can:
	- We can deduce that root index will always be `preorder[0]`
	- We can decide left and right subtrees based off `root` element's position in `inorder`
	- We can use recursive calls to build subtrees

- Write a recursive function with parameters:
	- `inorder array`                  (&)
	- `preorder array`                (&)
	- `preorder index`                (&)
	- `start of subtree (inorder)`
	- `end of subtree (inorder)`
	- A helper function: `linearSearch()`     //Check optimization (end of document)

- Base conditions:
	- `preIndex>size`
	- `start>end`
	- Return `NULL`

- Flow for function:
	- Pick the `root` element: `int rootElement=preorder[preorderIndex++];` 
		//Preorder incremented for next iteration
	- Make the `root` node: `TreeNode* root=new TreeNode(rootElement);`
	- Find the `root` element in `inorder`: `int pos=linearSearch(inorder, rootElement);`
	- Recursive call for left subtree and right subtree:
		- `root->left=builder(preorder, inorder, preIndex, s, pos-1);`
		- `root->right=builder(preorder, inorder, preIndex, pos+1, e);`
	- Return `root`

- Optimization: Use an `unordered_map` to avoid linear searching again and again

#trees #hard #leetcode 