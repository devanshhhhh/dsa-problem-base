Link: https://leetcode.com/problems/car-fleet/

Approach:
- Use a class Car to bind position and speed arrays
- Create a vector for these bundled car objects
- Sort the cars vector using a custom comparator
- Initialize a `stack<float>` and run a for loop calculating the time required for each car to reach the target using `time=(target-position)/speed`
- If stack is empty or `st.top>=time`, `st.pop()` (the car is faster then the next car so they will collide before reaching the target, so they can be grouped in one fleet)
- Else, `st.push(time)`
- Return `st.size()` (number of fleets)
- TC: **O(n log n)**
- SC: **O(n)**

#stack #leetcode #hard 