1) [[Book allocation problem (CNJ)]]
2) [[Painter's partition problem (CNJ)]]
3) [[Aggressive cows problem (CNJ)]]
4) [[EKO (SPOJ)]]
6) [[PRATA (SPOJ)]]

Note:
***These are all problems with answer lying in a monotonic search space.***
***All of these problems use contiguous allocations with given conditions.***

Approach:
- Initialize an int variable `ans=-1`
- Select your `start` and `end` values (minimum and maximum answers possible for case)
- Write a binary search
- For every mid value check if the answer is possible by writing a `isPossible()` function
- If answer is correct, update `ans` variable with `mid`
- If you want a better answer, for maximizing answer move to right part of search space `(s=m+1)`, else `(e=m-1)`
- Return the answer 
- TC: **O(n log (sumOfArray))**
- SC: **O(1)**


#searching 