Link: https://practice.geeksforgeeks.org/problems/factorials-of-large-numbers2508/1

Approach:
- Initialize a vector with 1 pushed in it, int variable carry with 1
- Take every element till N and multiply with vector, expanding it as required
- Use `(arr[j] * i + carry)`, extract and push digit, update carry
- Use a nested loop for this
- After every inner loop iteration, handle carry with /10 and %10 till carry!=0 because carry could be very large
- After end of both loops, return ans vector
- TC: **O(n)**
- SC: **O(n)** is ans vector is considered, else **O(1)**




#arrays #math #geeksforgeeks #hard