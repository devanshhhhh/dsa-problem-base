Link: https://practice.geeksforgeeks.org/problems/count-bst-nodes-that-lie-in-a-given-range/1 

Approach:
- If(root->data<=L && root->Data>=H) count++;      //Valid value selected
- If(root->data>L), then only explore left                      //No valid values in else case (all less than L)
- If(root->data<H), then only explore right                  //No valid values in else case (all greater than H)

#bst #geeksforgeeks 