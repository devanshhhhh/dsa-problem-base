Link: https://practice.geeksforgeeks.org/problems/largest-bst/1 

Approach:
- Define data and appropriate ctors with int size, minimum, maximum, and bool flag for validity
- Recursive calls for left, right, then process node
//These min and max values indicate max and min value of the tree upto that node and won't be used to test current node but the upper node
- `curr->size=1+left->size+right->size;`
- `curr->maximum=max(root->data, right->maximum);`
- `curr->minimum=min(root->data, left->minimum);`
- `curr->valid=left->valid && right->valid && (root->data<right->minimum && root->data>left->maximum);`
- `if(curr->valid) ans=max(ans, curr->size);`
- Return `curr`
- Return `ans` from main()
- TC: **O(n)**
- SC: **O(H)**

#bst #hard #geeksforgeeks 