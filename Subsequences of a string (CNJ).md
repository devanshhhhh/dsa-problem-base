Link: https://www.codingninjas.com/studio/problems/subsequences-of-string_985087

Approach:
*****Inclusion exclusion approach***
- Write a recursive solver/helper function with parameters input `string str`, `string s` to hold subsequences and `vector<string> ans` and int i (for index pointing)
- Write two recursive calls each passing `solver(ans, str, i, s+str[i])` && `solver(ans, str, i, s)` (one call includes `i` in the substring, one call excludes `i`)
- Base conditions: 
	- `if(i>=s.size()) ans.push_back(s); return;`
//Eliminate empty strings while pushing answers to the vector
- TC: O()
- SC: O()


#recursion #codingninjas 