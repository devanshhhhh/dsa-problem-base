Link: https://leetcode.com/problems/binary-tree-inorder-traversal/

Approach:
//LNR
- If `(curr->left==NULL)`, add the current node to `ans` vector and move to right `curr=curr->right`
	//L is done, select N and move to R
- Else:           //Exploring L
	- Find a predecessor node inorder (move left then keep going right): `pre=curr->left;`
	- `while(pre->right!=curr && pre->right) pre=pre->right;`   
	 //If `pre->right` is already `curr`, we have already visited this `pre` node an linked it
	 - Now, `if(!pre->right)`     //New `pre` found, so link
		 - `pre->right=curr;`
		 - `pre=pre->left`
	 - Else                                    //Revisited `pre`, so unlink, L is done, select N, move to R
		 - `pre->right=NULL;`
		 - `ans.push_back(curr->data);`
		 - `curr=curr->right`;
 - Return `ans` vector
 - TC: **O(n)**
 - SC: **O(1)**

#trees #hard #leetcode 