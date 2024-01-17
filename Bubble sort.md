Link: https://www.codingninjas.com/studio/problems/bubble-sort_980524?source=youtube&campaign=love_babbar_codestudio2&utm_source=youtube&utm_medium=affiliate&utm_campaign=love_babbar_codestudio2

Approach:
- Use a nested loop to traverse the array with two pointers, `i=0`, `j=i+1`
- Update the if `arr[i]>arr[j]`, `swap(arr[i]`, `arr[j])`
- At the end of every pass, greater elements start accumulating at the end of the array
- Also use a swap count and check if there are no swaps in the first pass, it means the array is already sorted so stop if there are no swaps in the first pass
- TC: 
	- Worst: **O(n<sup>2</sup>)** 
	- Best: **O(n)** 
	- Average: **O(n<sup>2</sup>)** 
- SC: **O(1)**

Other behaviours:
- In-place sorting 
- Stable

#arrays 
#sort 