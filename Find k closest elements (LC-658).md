Link: https://leetcode.com/problems/find-k-closest-elements/

Approach:
- Initialize two int variables to be used as index pointers, `i=0`, `j=arr.size()-1`
- Run a while loop till `k` elements are left and `i<j`
- If abs(difference) of `i` indexed element is less than/equal to abs(difference) of `j` index, decrement `j` (select i<sup>th</sup> element)
- Else,  increment `i` (select j<sup>th</sup> element)
- Once the loop ends, return elements from  i<sup>th</sup> index to j<sup>th</sup> index
- TC: **O(n)**
- SC: **O(1)**

#searching #leetcode 