Link: https://www.codingninjas.com/studio/problems/common-elements-in-three-sorted-arrays_1113130

Approach-1:
- Take three pointers, i, j,k for arrays A, B, C
- Run them in a single while loop which terminates if any array ends
- In this if all three pointers are at same element, check if it is present in answer array
- If it's not present, push it to ans array and increment i, j, k
- else if A value is less than B, increment A's pointer (i)
- else if B value is less than C, increment B's pointer (j)
- else C value is least, increment C pointer (k)
- Once  the loop ends, return the ans vector
- TC: **O(n)**
- SC: **O(n)** if ans vector is considered, else **O(1)**

Approach-2:
- If any of the arrays are empty, return empty array as answer
- Find max element of all the arrays
- Create and fill respective hash arrays (in single loop traversal)
- Check if all the hash arrays have the given element (in single loop traversal), if yes then push that to ans vector
- Once  the loop ends, return the ans vector
- **TLE expected 
- **Works only for positive elements but can work with unsorted arrays too
- TC: **O(n)**
- SC: **O(n)** 


#arrays #codingninjas #hard