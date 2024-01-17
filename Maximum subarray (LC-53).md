Link: https://leetcode.com/problems/maximum-subarray/

Approach-1:
- Take two variables:
	- `int tempSum=0;`
	- `int sum=INT_MIN;`
- Run a for loop traversing the array and add the current index to `tempSum`
- After that, in the loop:
	- `if(tempSum>sum) sum=tempSum;`         //Updating max sum
	- `if(tempSum<0) tempSum=0;`                //Excludes negative numbers
- TC: **O(n)**
- SC: **O(1)**


Approach-2:
*****DnC based***
- Write a recursive function with base condition: `if(s>=e) return nums[s];
- Calculate mid and make recursive calls for left and right arrays:
	- `int leftSum=sumer(nums, s, m);`
	- `int rightSum=sumer(nums, m+1, e);`
- Now initialize two variables to store border sums:
	- `int maxLeftBorderSum=INT_MIN;`
	- `int maxRightBorderSum=INT_MIN;`
- Now calculate `leftBorderSum` and `rightBorderSum` traversing array in respective directions and update `maxLeftBorderSum` and `maxRightBorderSum` within the loops
- Your `crossBorderSum` will be:  `int crossBorderSum=maxLeftBorderSum + maxRightBorderSum;`
- Return the maximum out of left, right and cross border sums
- TC: **O(nlogn)**
- SC: **O(1)**

#dnc 