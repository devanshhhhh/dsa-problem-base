Link: https://leetcode.com/problems/find-duplicate-subtrees/

Approach:
- We can identify if two maps are identical by encoding their representations 
- To do this use an `unorderd_map<string, int>` to map `[encoding]=occurrence`
- For encoding use a recursive function that returns `string`
- Base condition: `if(!root) return "N";`
- Now, (NLR) preorder:
	- string n=to_string(root->data);            //N
	- string l=solver(root->left, mp, ans);      //L
	- string r=solver(root->right, mp, ans);   //R
	- string node=n+","+l+","+r;                   //Final encoding
- Check in map and add to answer now
	- `if(mp.find(node)!=mp.end())`        //Found in map
		- `if(mp[node]==1)`
			//This is second occurrence so include parent (root)
			- `ans.push_back(root);`
		- `mp[node]++;`                             //Won't operate on same duplicate multiple times
	- `else`                                                   //New entry
		- `mp[node]=1;`
- Return `node`
- Return `ans` vector from caller function
- TC: **O(n)**
- SC: **O(n)**

#trees #leetcode #hard 