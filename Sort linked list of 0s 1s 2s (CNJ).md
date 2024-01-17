Link: https://www.codingninjas.com/studio/problems/sort-linked-list-of-0s-1s-2s_1071937

Approach:
- Initialize three lists with -1 stores at the head nodes for(0, 1, 2)
- Make individual lists (all 0s, all 1s, all 2s)
- Remove head nodes of the lists having -1
- Start joining lists:
	- Join 0 and 2 if 1 is NULL (head=zeroHead)
	- Join 0 and 1 if 2 is NULL (head=zeroHead)
	- Join 1 and 2 if 0 is NULL (head=oneHead)
	- And so on (return individual lists if other two are NULL)
	- (You can use int variables to store number of 0s, 1s, 2s)
- TC: **O(n)**
- SC: **O(n)**

#lists #hard #codingninjas 