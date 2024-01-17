Link: https://leetcode.com/problems/car-fleet-ii/

Approach:
- A car will only collide if the next car is moving slower than it
- Start from the back of the array as they are sorted by position
- Initialize a stack of int type to store car indices and a vector of double to store collision times
- In a for loop from the back of the array, run a while loop that pops the stack till it's either empty or there is a slower moving car ahead
- The car on the top of the stack would be colliding after the loop (if stack is empty, it moves to next iteration, dodging the collision time while loop)
- Now, run a while loop till stack is not empty 
- Calculate a collision time with proper type casting using formula (distance/speed): `(p2-p1)/(s1-s2)` as the car 2 is moving faster
- Now check if the collision time of the `car[st.top()]` is either -1 or more than current collision time
- If yes, store the collision time in i<sup>th</sup> index and push the i to stack to move to next iteration
- Else pop the top of the stack till you either find a valid colliding car or stack is empty, then push i to stack and move to next iteration
- TC: **O(n)**
- SC: **O(n)**

#stack #leetcode #hard 