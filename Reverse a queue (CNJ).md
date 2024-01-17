Link: https://www.codingninjas.com/studio/problems/reversing-queue_1170046?leftPanelTab=2

Approach-1:
- Write a recursive function with base case: `if(q.empty) return;`
- Initialize a `int temp=q.front();` and `q.pop();`
- Recursive call: `reverse(q);`
- While returning, push back temp: `q.push(temp);`
- TC: **O(n)**
- SC: **O(n)** for recursive stack

Approach-2:
- Use a stack/vector to store elements and then re-insert
- TC: **O(n)**
- SC: **O(n)**

#queues #codingninjas 