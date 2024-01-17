Link: https://leetcode.com/problems/best-time-to-buy-and-sell-stock/

Approach:
- Initialize a minPrice variable with INT_MAX
- If you find a price lower than minPrice, update minPrice
- Then calculate profit for i<sup>th</sup> day and if profit > maxProfit (maxProfit=profit)
- Recursive call for next day (index)
- Base case: 
	- Index out of bounds

#recursion #leetcode 