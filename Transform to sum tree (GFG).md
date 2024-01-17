Link: https://practice.geeksforgeeks.org/problems/d7e0ce338b11f0be36877d9c35cc8dfad6636957/1

Approach:
- Write a recursive function with base condition: `if(!root) return 0;`
- Store the current node value: `int old=root->data;`
- Now for current node value make recursive calls for left and right subtrees
	- `root->data=toSumTree(root->left)+toSumTree(root->right);`
- Return `old+root->data`         //Older node value needs to be added to parent node


#trees #geeksforgeeks 