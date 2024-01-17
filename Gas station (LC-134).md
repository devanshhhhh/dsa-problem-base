Link: https://leetcode.com/problems/gas-station/

Approach: 
- Take three variables
	- `int deficit=0`
	- `int balance=0`
	- `int start=0`
- Run a for loop traversing the array:
	- Keep updating balance: `balance+=gas[i]-cost[i]`
	- If `(balance<0)`, it is deficit so:
		- `deficit+=balance`
		- `balance=0`      //New balance/deficit will be calculated
		- `start=i+1`      //Update starting point
- After the loop, `if(balance+deficit>=0)`, return `start`    //One loop is completed
- Else, return -1
- TC: **O(n)**
- SC: **O(1)**

#queues #leetcode 