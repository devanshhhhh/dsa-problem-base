Link: https://www.codingninjas.com/studio/problems/quick-sort_983625

Approach:
- We take a `pivotIndex` in each iteration and rearrange the array such that all the elements on its left are smaller or equal and all the elements on its right are greater (`pivotIndex` is placed at its sorted position)
- Then we recursively call the `quickSort()` on the eft side and right side
- This is done using two helper/solver functions *(actual sorting is done by `partition()`):*
	- `void quickSort(vector<int> &arr, int s, int e)`
	- `int partition (vector<int> &arr, int s, int e)`

quickSort()
- Recursive function with base condition: `if(s>=e) return;`
- Initialize an `int pivot` which store the pivot index returned by the `partition` function: `int pivot=partition(arr, s, e);`
- Now call `quickSort` recursively on left and right side of array
	- `quickSort(arr, s, pivot-1);`
	- `quickSort(arr, pivot+1, e);`

partition()
- First pick the pivot element and store the element in `pivotElement` variable(can pick any element but picking `middleIndex` is considered best practice)
- Now run loop to find elements greater than `pivotElement` (start loop from `s` and run till `e`)
- Now find `pivotIndex`: `int pivotIndex=s+greaterElements;`
- `Swap(arr[pivotIndex], arr[currIndexOfPivotElement])`
- Now run a while loop till (index in currArrayRange): 
	- `i=s; int j=e; while(i<pivotIndex && j>pivotIndex)`
	- In this, `while(arr[i]<=pivot) i++;`
	- In this, `while(arr[j]>pivot) j--;`
	- After this check inside loop `if(i<pivotIndex && j>pivotIndex) swap(arr[i++], arr[j--]);
- Return `pivotIndex` once the loop exits

- TC: 
	- Worst: **O(n<sup>2</sup>)** 
	- Best: **O(nlogn)** 
	- Average: **O(nlogn)** 
- SC: **O(1)**

Other behaviours:
- In-place sorting 
- Not stable

Extension: [[QS with last element as pivot]]


#dnc #sort 