***Important terms:***
- **Node**: Data and links
- **Root**: Topmost node (start point)
- **Parent**: 1 level up connected node
- **Child**: 1 level down connected node
- **Ancestor**: Nodes connected going up till root node
- **Descendant**: Nodes connected going down till leaf node
- **Sibling**: Same parent's child nodes are siblings
- **Leaf node**: Node with no child nodes (last node)


***Types:***
- **Binary trees**: Only children up to 2 (0, 1, 2)
	- **Perfect (fully) binary tree:** All nodes except leaf nodes have both (left and right) children
	- **Complete binary tree:** Nodes filled from left to right
	- **Balanced binary tree:** Height difference between corresponding left and right subtrees should not be more than 1
- **n-ary trees**: n children possible for each node
- **Skew trees**: Trees with all nodes on only one side (either)
- **Sum tree:** A tree where every node contains sum of values of nodes in left and right subtrees in the original tree


***buildTree():***
- Read input in a `temp` variable
- Call the constructor on `temp` variable and create a new node `n`
- Recursive call for left nodes: `n->left=buildTree();`
- Recursive call for right nodes: `n->right=buildTree();`
- Base condition: `if(temp==-1) return NULL;`

***Traversals:***  
//L: Left node
//N: Current node
//R: Right node

1) **Level Order Traversal**
	- Use a queue to write this
	- Handle first node outside while loop
	- After each level insert `NULL` in queue to mark a level end (outside loop for root)
	- Run a while loop: `while(!q.empty())`
		- Store front in temp and pop front: `Node* temp=q.fornt(); q.pop();`
		- `if (temp==NULL)`
			- Insert a new line
			- `if(!q.empty()) q.push(NULL)`      //Level marking
			- `continue;`
		- `(temp!=NULL)`
			- `if(temp->left!=NULL) q.push(temp->left);`
			- `if(temp->right!=NULL) q.push(temp->right);`
2) **In-order Traversal** 
	  //Follow order LNR
	- Base condition: `if(!root) return NULL;`
	- Recursive call for left: `root->left->inOrderReversal();`       //L
	- Print value of current node: `cout<<root->val;`                      //N
	- Recursive call for right: `root->right->inOrderReversal();`   //R
3) **Pre-order Traversal**
	  //Follow order NLR
	- Base condition: `if(!root) return NULL;`
	- Print value of current node: `cout<<root->val;`                       //N
	- Recursive call for left: `root->left->inOrderReversal();`        //L
	- Recursive call for right: `root->right->inOrderReversal();`    //R
4) **Post-order Traversal**
 	  //Follow order LRN
	- Base condition: `if(!root) return NULL;`
	-  Recursive call for left: `root->left->inOrderReversal();`        //L
	- Recursive call for right: `root->right->inOrderReversal();`     //R
	- Print value of current node: `cout<<root->val;`                        //N


***Height of tree/ Maximum depth:***
- No. of nodes in the farthest path from root node to leaf node
- If the question says edges, calculate accordingly

#trees 