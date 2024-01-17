Link: https://www.codingninjas.com/studio/problems/first-negative-in-every-window_759333

Approach:
- Use a queue to store your current window indices (indices so we can track window size easily)
- Process the first window separately:
	- Run a while loop: `while(i<k)`
	- In this insert all the negative element indices 
	- Outside the loop check for answer with if-else
		- `if(!q.empty()) ans.push_back(v[q.front()])`
		- `else v.push_back(0)`
- Now your `i` value should be equal to `k` meaning you have processed `k` elements out of `n`
- Now, process rest of windows in another while loop
	- Run a while loop: `while(i<n)`
	- In this we'll process the current window first in every iteration:  
		- `while(!q.empty() && (i-q.front())>=k) q.pop()`   **OR**  `while(!q.empty() && (q.front()<i-k+1) q.pop()`      //Removes out of window indices from possible answers
		- After this, we insert `i` if `(v[i]<0)`
		- Lastly, we select the answer using the same logic as before
- Return `ans` vector
- TC: **O(n)**
- SC: **O(k)**

#queues #codingninjas #hard #slidingwindow 