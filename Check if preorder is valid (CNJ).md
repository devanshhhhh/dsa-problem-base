Link: https://www.codingninjas.com/studio/problems/check-if-preorder-traversal-is-valid_1164410 

Approach:
- Variation of [[Construct BST from preorder traversal (LC-1008)]] 
- Don't build the tree 
- Use a void function and see if you can reach the end of the array with your traversing index (meaning no breaks in between, valid tree exists)
- Explore only if current index value is valid (increment i only after validation, then recursive calls)
- Base condition: (out of bounds index)
- Return (i== arr.size());
//Read the question to check how to handle duplicate values


#bst #hard #codingninjas 