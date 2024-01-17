Link: https://www.codingninjas.com/studio/problems/n-queue-using-array_1170053

Approach:
- `Ctor()` data structures:
	- `int* front=new int[n]`         //Stores front element index of n<sup>th</sup> queue
	- `int* rear=new int[n]`           //Stores last element index of n<sup>th</sup> queue
	- `int* q=new int[s]`                //The main array
	- `int* next=new int [s]`         //Stores next index for i<sup>th</sup> index in array
	- `int freespot=0`
	//Initialize appropriately
	
- `enqueue()` flow:
	- `if(freespot==-1) return false;`                           //Overflow 
	- Take `int index=freespot` to insert new element
	- Update `freespot`: `freespot=next[index]`
	- Now, check if n<sup>th</sup> queue is empty (if empty, this will be front element, else we update rear):
		- `if(front[m-1]==-1) front[m-1]=index;`        //Update front if n<sup>th</sup> queue is empty
		- `else next[rear[m-1]]=index;`                         //Link current rear to next rear
	- Update next of new rear as -1: `next[index]=-1;`
	- Now we update rear: `rear[m-1]=index;`                 //Outside if-else to update it in either case
	- Insert the element now: `q[index]=x;`
	- Return true
	
- `dequeue()` flow:
	- `if(front[m-1]==-1) return -1;`                             //Underflow
	- Take `int index=front[m-1]` to pop element
	- Now, update new front: `front[m-1]=next[index];`
	- Update next of index being removed: `next[index]=freespot; `     
	- Now, update `freespot`: `freespot=index;`
	- Store `ans` in variable to return and remove element: `int ans=q[index];  q[index]=-1;` (Optional)
	//Link next `freespot` to this index and make it current `freespot`
- TC: 
- SC: **O(n)**

#queues #hard #codingninjas 