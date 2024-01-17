Link: https://www.codingninjas.com/studio/problems/bst-to-sorted-dll_1263694 

Approach:
- Initialize `head` node for `NULL`
- Pass it by reference
- Go all the way right
- Process node at return
	- root->right=head;                 //Update further link 
	- if(head) head->left=NULL;    //Update left link to NULL
	- head=root;                            //Update head as current node
- Go left and process
- Return head from main()

#bst #hard #codingninjas 