Link: https://www.codingninjas.com/studio/problems/reverse-first-k-elements-of-queue_982771

Approach:
- Use a stack `st` to store first `k` elements
- Then take an `ans` queue and push the elements in stack to `ans`
- Now, push the rest of the queue as it is
- Return the `ans`
- TC: **O(n)**
- SC: **O(n)**

//You can avoid using an extra queue and make changes in the given queue, follow this flow for same:
- Take `int n=q.size()` (initially)
- Insert `k` reverse elements at  back
- Now, `while (j<(n-k))`:
	- Insert front element at back: `q.push(q.front())`
	- Remove from front of queue: `q.pop()`


//Handle edge cases properly (check constraints)

#queues #codingninjas 