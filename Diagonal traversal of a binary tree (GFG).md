Link: https://practice.geeksforgeeks.org/problems/diagonal-traversal-of-binary-tree/1

Approach-1:
- Calculate horizontal distance and insert elements corresponding to it in an ordered map
- Use a recursive function for the same
- Increment distance for left nodes, nothing for right
- Add all the vectors in order to the answer vector from the map

Approach-2:
//Optimized saving space for map and inserts in map
- Use a queue like in the level order traversal (Refer: [[Basics-Trees]])
- Every time you take temp from `temp` from the queue, run a while loop:
	- `while(temp)`
		- `ans.push_back(temp->data);`                     //Add element to answer
		- `if(temp->left) q.push(temp->left);`       //Process left diagonal later
		- `temp=temp->right;`                                     //Go to right nodes till right!=NULL
- TC: **O(n)**  //visiting each node once
- SC: **O(n)**

#trees #geeksforgeeks 