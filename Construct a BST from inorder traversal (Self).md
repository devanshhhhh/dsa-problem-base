Approach:
- Pass (s, e, vector), calculate mid, make root and recursive calls on left and right:
	- `root->left=solver(s, m-1, arr);`
	- `root->right=solver(m+1, e, arr);`

#bst 