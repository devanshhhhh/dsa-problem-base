Link: https://leetcode.com/problems/integer-to-english-words/

Approach:
- Use a `vector<pair<int, string>>` to store English words (Multiples of 10, 1-9, 11-19)
- Write a recursive function that returns a string
- Base condition: `if(num==0) return "Zero"`
- Run a for loop traversing the vector with following conditions:
	- `if(num>=it.first)` store, `b=it.second` in a string b and recursive call for string a, `a=(num/it.first)`  (Here b stores the max value like "hundred", "million" etc. and a will store "how much hundreds or millions etc.")
	- After this `if(num%it.first!=0)`, another recursive call to handle rest of the number string c, `c=(num%it.first)`
	- At last return `a+b+c` (within the loop)
//Insert empty space character after a result and before c result

#recursion #hard #leetcode 