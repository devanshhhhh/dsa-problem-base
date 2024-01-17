Link: https://leetcode.com/problems/same-tree/

Approach:
- Write a recursive function with base conditions:
	- `if(!p && !q) return true;`                                     //Node match
	  `if((p && !q) || (!p && q)) return false;`           //Node mismatch
- Check for root, if same, recursive calls:
	- `if(p->val!=q->val) return false;`
	- `else`
		- `return sameTree(p->left, q->left) && sameTree(p->right, q->right);`


#trees #leetcode 