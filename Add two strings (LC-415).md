Link: https://leetcode.com/problems/add-strings/

Approach: 
- Initialize int variable sum=0, carry=0 and a string ans
- Get the backs of both vectors
- Pop the back elements of both vectors
- Subtract '0' or 48 and store then in int variables n1, n2
- Sum=n1+n2+carry
- If sum<10, push it to ans string with +'0' or +48 and continue
- If sum>10, get digit by sum%10 and update carry with sum/10
- Push it to ans string with +'0' or +48
- Run this in while loop till either of the vectors is empty
- Write while loops for both vectors which run if either of them are not empty (similar algo)
- Handle the last carry with if statement
- Return reverse(ans)
- TC: **O(n)**
- SC: **O(n)** if ans string is considered, else **O(1)**


#strings #leetcode 