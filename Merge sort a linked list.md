Approach:
- Write a recursive mergeSort function with base case `(if list1==NULL) return list2` and `(if list2==NULL) return list1`
- Find the middle element for each call ([[Middle of the linked list (LC-876)]])
- Once done break from mid and all mergeSort function on both lists
- After that call the merge function to merge sorted lists and return time ([[Merge two sorted lists (LC-21)]])
- TC: **O(n log n)**
- SC: **O(1)**

#lists #leetcode 