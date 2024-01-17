Link: https://practice.geeksforgeeks.org/problems/maximum-sum-of-non-adjacent-nodes/1

Approach:
- Use a `pair<int, int>` recursive function to return two types of sums
	- `p.first`: including current value
	- `p.second`: excluding current value
- Base condition: `if(!root) return {0, 0};`
- Recursive call for left and right nodes
- For excluding sum we can use the pair retuned by recursive calls:
	- `p.first=left.second+right.second+root->data;`
	 //Including root, excluding right and left
	- `p.second=max(left.first, left.second)+max(right.first, right.second);`
	  //Excluding root, Including right and left
- Return `p` (pair)
- From caller function return max value of pair
- TC: **O(n)**
- SC: **O(n)** for recursive stack

#trees #geeksforgeeks #hard 