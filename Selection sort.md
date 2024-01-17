Link: https://www.codingninjas.com/studio/problems/selection-sort_981162?source=youtube&campaign=love_babbar_codestudio2&utm_source=youtube&utm_medium=affiliate&utm_campaign=love_babbar_codestudio2

Approach:
- Initialize a int min variable with `arr[0]`
- Use a nested loop to traverse the array with two pointers, `i=0`, `j=i+1`
- Update the min value if `arr[j]` is lesser than it
- At the end of every inner loop swap `arr[i]`, `arr[j]`
- TC: 
	- Worst: **O(n<sup>2</sup>)** 
	- Best: **O(n<sup>2</sup>)** 
	- Average: **O(n<sup>2</sup>)** 
- SC: **O(1)**

Other behaviours:
- In-place sorting 
- Not stable


#arrays #sort 