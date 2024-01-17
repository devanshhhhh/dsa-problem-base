Link: https://www.codingninjas.com/studio/problems/interleave-the-first-half-of-the-queue-with-the-second-half_1169450

Approach:
- Copy the first half of elements in a new queue and remove from original
- Now in the original queue, start by inserting one element from the first half and one from the second half (keep removing inserted elements from respective queues)
- If you have odd length queues, check `if(n&1)`, then insert one more element from the second queue manually
- TC: **O(n)**
- SC: **O(n)**

//You can also use a vector if the question allows

#queues #codingninjas 