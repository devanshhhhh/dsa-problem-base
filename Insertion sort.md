Link: https://www.codingninjas.com/studio/problems/insertion-sort_3155179

Approach:
- Assume the first element to be sorted
- Take a pointer as `int i=1`
- Take a int variable temp to store the value, array is being checked for
- Write a while loop for `(i<n)` and store `temp=arr[i]` 
- Take another pointer as `int j=i+1`
- Write a nested loop for `(j>=0)`
- In this `if(arr[j]>temp)`, shift j<sup>th</sup> value to j+1 by copying it, decrement j
- Else  `(arr[j]<=temp)`, break from inner loop
- This will give us the exact position of i<sup>th</th> element as it shifts the elements to next index till it finds a smaller element
- Assign your temp variable value (i<sup>th</th> element) to j+1, `arr[j+1]=temp`
- Increment `i`, return when the outer loop ends
- TC: 
	- Worst: **O(n<sup>2</sup>)**
	- Average: **O(n<sup>2</sup>)
	- Best: **O(n)
- SC: **O(1)**


Other behaviours:
- In-place sorting 
- Stable


#arrays 
#sort 