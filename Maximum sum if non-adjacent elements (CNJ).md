Link: https://www.codingninjas.com/studio/problems/maximum-sum-of-non-adjacent-elements_843261

Approach:
*****Inclusion exclusion approach***
- Write a recursive function with base condition (return if index out of bounds)
- Store the `currAns` at base condition check if `maxAns< currAns`
- If you are including an index element, add it to current sum `(currAns)` and skip next index so, recursive call `(nums, maxSum, currAns+nums[i], i+2)`
- Else (excluding), just increment index so, recursive call `(nums, maxSum, currAns, i+1)`


#recursion #codingninjas 