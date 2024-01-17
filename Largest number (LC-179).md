Link: https://leetcode.com/problems/largest-number/

Approach:
- Convert the given nums vector from int to string
- Sort the string vector with a custom comparator that returns `a+b>b+a`  Ex-*(3, 30: 330>303)*
- Use a loop to concatenate this sorted vector to the ans string
- Check if the 0<sup>th</sup> index is '0', if yes, return "0" (0 is the largest number in that array)
- Else return ans

#strings #leetcode 