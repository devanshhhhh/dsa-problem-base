Link: https://leetcode.com/problems/convert-sorted-list-to-binary-search-tree/ 

Approach:
- Use a head and tail in main function (head, tail)
- Write another helper function to calculate mid of list between head and tail: use `while(fast!=NULL && fast->next!=NULL)`
- Update for (head, tail) recursive calls:
	- (root->left, head, mid);
	- (root->right, mid->next, tail);

#bst #leetcode 