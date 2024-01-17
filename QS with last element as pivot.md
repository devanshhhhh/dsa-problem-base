*****Slight optimization for `partition()` function***

Approach: 
- Don't use another function for `partition()`, instead use the following approach before the recursive calls in the `quickSort()` function
- Take pivotIndex as e and intialize i and j two pointers as:
	- `int pi=e;`
	- `int i=s-1;`
	- `int j=s+1;`
- Now run a while loop till `(j<pi)`:
	- `if(arr[j]<arr[pi])`
		- `i++; swap(arr[i], arr[j]);` 
	- `j++;`
	*//Pushing `i` at last smaller element and `j` at next to check (similar to modified insertion sort during the loop)* 
- After exiting the loop, increment `(i++)`, so your `i` will now point at the first larger number
- Now `swap(arr[i], arr[pi])`
- Partition is done, and `i` is the `pivotIndex`, make further recursive calls for left and right arrays:
	- `quickSort(arr, s, i-1);`
	- `quickSort(arr, i+1, e);`


#dnc #sort 