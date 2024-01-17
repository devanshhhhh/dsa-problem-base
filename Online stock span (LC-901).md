Link: https://leetcode.com/problems/online-stock-span/

Approach-1: 
- Take a `stack<pair<int, int>>` where `p.first=price` && `p.second=span`
- For the `next(int price)` function, initialize an `int span=1`
- Run a while loop till stack is not empty and stack's top element's price is not more than current price
- In each iteration add the span of the top element to current span and pop the top
- After exiting the loop `push({price, span})`
- Return `span`
- TC: **O(n)**
- SC: **O(n)**

*****Basically, you are compressing and storing the span of monotonic elements to save iterating all the `n` elements*** 



Approach-2:
- Use a single element stack to store the prices, for each span calculation, call a recursive function that pops, checks and restores all the elements
- TC: **O(n<sup>2</sup>)**
- SC: **O(n)**

*****TLE** 

#stack #leetcode 