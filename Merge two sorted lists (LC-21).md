Link: https://leetcode.com/problems/merge-two-sorted-lists/

Approach: 
- Run a while loop till either of the lists becomes NULL
- Compare vals of both node pointers (list1 and list2) in each iteration
- Join the lesser one to your answer list
- Once done, write two separate if conditions loop that add the remaining list to the answer
- Return the ans list
- TC: O(m) where m is the smaller list
- SC: O(1)

#lists #leetcode 