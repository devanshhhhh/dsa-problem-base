Link: https://www.codingninjas.com/studio/problems/first-unique-character-in-a-string_893404?leftPanelTab=2

Approach:
- Take three structures:
	- `queue<char> q`                          //Stores and lookup first character
	- `vector<int> hash(26, 0)`        //Stores frequency of characters
	- `vector<char> ans`                    //Stores answer
- Now run a while loop traversing over the array and for each iteration:
	- Increment the frequency for `s[i]`
	- Push in queue `s[i]`
	- Run another while loop: `while(!q.empty() && hash[q.front()-'a']>1) q.pop()`;
		//This pops all the elements in queue till it finds a unique one
	- After the inner loop, check `if(q.empty())`, if yes then continue, else push `q.front()` to `ans` vector
- TC: **O(n)**
- SC: **O(n)**

#queues #codingninjas #hard #slidingwindow 