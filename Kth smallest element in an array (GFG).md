Link: https://practice.geeksforgeeks.org/problems/kth-smallest-element5635/1 

Approach-1:
//Build a max heap to hold exactly k smallest elements and return top() at the end as it is the kth smallest (largest of the smallest)
- Build a max heap
- Push till (i<k)
- Once (i>=k) push only if the top() element is greater than the current element (pop() the top element first)        //This ensures we remove current kth smallest and update with smaller value
- Return top() once the loop ends
- TC: **O(n logn)**
- SC: **O(k)**

Approach-2:
- Use a max heap or sort and return kth index
- TC: **O(n logn)**
- SC: **O(n)**

#heaps #geeksforgeeks 