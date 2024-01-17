Link: https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string/description/

Approach:
- Run a while loop iterating over the array
- Take an ans string
- If ans is empty push the current character
- If ans is not empty compare if the last character of ans matches current one
- If they match pop_back ans else, insert current character
- TC: **O(n)**
- SC: **O(n)** is ans string is considered, else **O(1)**

#strings #leetcode 