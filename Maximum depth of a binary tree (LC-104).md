Link: https://leetcode.com/problems/maximum-depth-of-binary-tree/

Approach: 
- Base condition: `if(root==NULL) return 0;
- Recursive call for left: `int left=maxDept(root->left);`
- Recursive call for right: `int right=maxDept(root->right);`
- Return `max(left, right)+1;`
- TC: 
- SC: 

#trees #leetcode 