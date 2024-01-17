Link: https://leetcode.com/problems/validate-binary-search-tree/

Approach:
- Use a range to validate every node (min, max), if validates:
	- Update min and max for left recursive call as (min, root->val)
	- Update min and max for right recursive call as (root->val, max)
	- Return left && right

#bst #leetcode 