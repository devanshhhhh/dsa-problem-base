Link: https://leetcode.com/problems/sort-an-array/

Approach:
- Make a `temp` vector to store your intermediate results: `(vector<int> temp(nums.size(), 0))`
- We are going to write two helper functions:
	- `mergeSort(vector<int> &nums, int s, int e, vector<int> &temp)`
	- `merge(vector<int> &nums, int s, int m, int e, vector<int> &temp)`
- Return `nums/temp` (as needed)

mergeSort()
- Recursive function with base case: `if(s>=e) return;`
- Calculate `m` value 
- Make two recursive calls:
	- `mergeSort(nums, s, m, temp);`
	- `mergeSort(nums, m+1, e, temp);
- After this, call merge on both arrays collectively `merge(nums, s, m, e, temp);`

merge()
- First sorted array is from `(s to m)` and second sorted array is from `(m+1 to e)`
- Merge them in `temp` vector (be careful with `s`)
- Copy updated `temp` from `(s to e)` in the main array (if needed)

- TC: 
	- Worst: **O(nlogn)** 
	- Best: **O(nlogn)** 
	- Average: **O(nlogn)** 
- SC: **O(n)**

Other behaviours:
- Not in-place sorting 
- Stable

Extension: [[In-place MS]]



#dnc #sort 