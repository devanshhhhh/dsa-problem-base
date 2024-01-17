Link: https://leetcode.com/problems/construct-binary-tree-from-inorder-and-postorder-traversal/

Variation of [[Construct a binary tree from preorder and inorder traversal (LC-105)]] 


Changes:
- Travel backward in `postorder` to find `root` for each iteration
- Populate `right` subtree first (first recursive call will be for `right`, then `left`)


#trees #leetcode #hard 