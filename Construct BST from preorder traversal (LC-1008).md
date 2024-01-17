Link: https://leetcode.com/problems/construct-binary-search-tree-from-preorder-traversal/ 

Approach:
- Pick an index and increment it (passed by reference) for next call
- Make a node with the current index
- Recursive calls for left=(preorder, i, min, root->val);
- Recursive calls for right=(preorder, i, root->val, max);
- Return root
- Base conditions: Invalid index or Invalid bst value `if (i>=preorder.size() || preorder[i]>=max || preorder[i]<=min) return NULL;`

#bst #leetcode 