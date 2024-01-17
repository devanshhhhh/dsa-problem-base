Link: https://leetcode.com/problems/largest-rectangle-in-histogram

Approach: 
- Helper function 1: [[Find the next smaller element going forward in array(right side) (Self)]] 
- Helper function 2: [[Find the next smaller element going backward in array (left side) (Self)]] 

*\***Use indices to be stored not the actual elements to calculate expandable width for a histogram***
*\****In the nextSmaller results function, replace -1 with size of the array to adjust output for calculation of width***

- Using nextSmaller and prevSmaller, find the closest adjacent smaller histograms to the i<sup>th</sup> histogram, explaining where you can expand and where you cannot
- Using formula, `next[i]-prev[i]-1`,  find the width, length would be height of histogram
- Calculate the area for each one and update the maxArea variable accordingly
- Return maxArea after end of the loop
- TC: **O(n)**
- SC: **O(n)**

#stack #leetcode #hard