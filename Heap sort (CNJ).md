Link: https://www.codingninjas.com/studio/problems/heap-sort_1262153 

Approach:
- Heapify `(n/2)-1 to 0` nodes (0-indexed heap)
- Swap first and last, decrement the size, call heapify on remaining array (basically deleting the nodes)
//The nodes will be arranged in reverse order of deletion (use max heap to ascending order and min heap for ascending)


#heaps #codingninjas 