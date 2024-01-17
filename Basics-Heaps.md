**Properties followed:**
- *Complete BT:* 
	- All levels filled except last (strictly left to right)
- A type of *heap property* (ex- min heap, max heap etc.)

**Construct heap:**
- *Using arrays:*
	- *1-indexing:*
		- Parent=i
		- Left child=2i
		- Right child=2i+1
	- *0-indexing:*
		- Parent=i
		- Left child=2i+1
		- Right child=2i+2
	- If index=i, parent=i/2 

**Deletion in heap:**
- Only root values (1st) can be deleted
- Swap first and last values (nodes)
- Decrease size (delete last value)
- Heapify the new root value

**Heapify:**
- Check if left or right child has a larger value (or smaller depending on type of heap)
- Pick the largest and swap, recursive call for new index (largest)

**Build heap:**
- No need to heapify leaf nodes:
	- 0-indexed CBT: `n/2 to n` are leaf so call for `(n/2)-1 to 0`
	- 1-indexed CBT: `(n/2)+1 to n` are leaf so call for `n/2 to 0`
- TC: **O(n)**

#heaps 