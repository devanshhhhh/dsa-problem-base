Link: https://leetcode.com/problems/minimum-cost-for-tickets/

Approach:
- Write a void recursive solver/helper function with parameters `(&days, &costs, &minMoney, money=0, coveredDays=0, index=0)`
- Base condition: `if(index>days.size())`  (also update `minMoney` at base condition if `money<minMoney` )
- In the function if `(days[index]>coveredDays)`, make recursive calls for all types of passes and increment `index`:
	- 1-day pass: `solver(days, costs, minMoney, money+costs[0], days[i], index+1);`
	- 7-days pass: `solver(days, costs, minMoney, money+costs[1], days[i]+6, index+1);`
	- 30-days pass: `solver(days, costs, minMoney, money+costs[2], days[i]+29, index+1);`
- Else `(days[i]<=covered)`, recursive call with just index incremented: `solver(days, costs, minMoney, money, covered, index+1);`
- TC: **O(3<sup>n</sup>)**
- SC: O()

//Make sure not to buy new pass on days you're not travelling 

#recursion #leetcode #hard