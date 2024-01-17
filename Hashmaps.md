- Hashing is implemented using a bucket array.
- STL header files: `<unordered_map>`, `<map>`
- **Hash function:**
	- One-way function that maps a key value to a numeric value
	- Two components:
		- *Hash code:* Logic to calculate the numeric value
		- *Compression function:* If hash code returns a value that's out of bounds, it converts the value to fir in the range (mod)

- **Collision:**
	- When two key values passed in a hash function give the same numeric value
	- Impossible to avoid it completely, so it is minimized

- **Collision handling:**
	- Achieved by (Open hashing) making a linked list at the colliding value and storing possible keys

- **Linear probing:**
	- Free spots to store new entries are searched at every next filled spot
	- F(i)=i

- **Quadratic probing:**
	- Free spots to store new entries are searched at every square value of current filled index
	- F(i)=i<sup>2</sup>

- **Load factor:**
	- Ratio of (filled spots in a map memory : free spots in a map memory)
	- n/b<0.7 (for highest efficiency)

#maps