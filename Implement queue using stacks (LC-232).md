Link: https://leetcode.com/problems/implement-queue-using-stacks/

Approach:
- Take two stacks (primary and secondary)           //Use primary for storage, secondary for reversals
- Either reverse data while pushing making push **O(n)** TC operation
- Or, you can reverse in pop() and front()             //Slightly more optimized (imo)
- For that, write `pop()` function flow as:
	- `if(!secondary.empty()) `
		- `secondary.pop()` and return that element
	- `else`
		- We transfer elements from primary to secondary (this reverses all elements simulating FIFO if we return from secondary)
		- The `secondary.pop()` and return that element
- `front()` will be the same as `pop()` but without popping           
  //Not using another variable to track `front()` because question allowed only two stacks
- For `empty()`, return `(primary.empty() && secondary.empty())`
- TC: **O(1)** for `push()`, `empty()` and **O(n)** for `pop()`, `front()`
- SC: **O(n)**

#queues #leetcode 