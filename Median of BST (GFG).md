Link: https://practice.geeksforgeeks.org/problems/median-of-bst/1 

Approach-1:
- Store inorder
- If odd nodes: return `float(v[n/2])`
- Else: return `float(v[n/2]+v[(n/2)-1])/2.0;`

Approach-2:
- Morris traversal: Count nodes
- Morris traversal: Find values for `n/2, (n+1)/2, (n/2)+1` nodes
- If even: return n/2th value
- Else: Add other two and divide by 2


#bst #geeksforgeeks 