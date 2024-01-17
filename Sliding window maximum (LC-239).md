Link: https://leetcode.com/problems/sliding-window-maximum/

Approach:
- Use a deque to store your current window indices (indices so we can track window size easily)
- Process the first window separately:
	- Run a while loop: `while(i<k)`
	- Now we check if there are any out of window indices and remove them (from the front):
		`while(!q.empty() && i-q.front()>=k){`
                `q.pop_front();`
	- After this we check and remove smaller element from the back (because deque will be filled in descending order):
		`while(!q.empty() && nums[i]>=nums[q.back()]){`
                `q.pop_back();`
	 - Now we push the current index and pick the answer as the front element of deque
- Now your `i` value should be equal to `k` meaning you have processed `k` elements out of `n`
- Now, process rest of windows in another while loop (same as above steps)
- Return `ans` vector
- TC: **O(n)**
- SC: **O(k)**

#queues #leetcode #hard #slidingwindow 