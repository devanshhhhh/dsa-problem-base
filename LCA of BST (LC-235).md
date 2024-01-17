Link: https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/ 

Approach:
- 4 possible cases:
	- p and q both on left: return left recursive call
	- p and q both on right: return right recursive call
	- p and q on different sides: return root(since we are going up to down)


#bst #leetcode 