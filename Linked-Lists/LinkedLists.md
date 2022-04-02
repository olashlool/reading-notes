# Linked Lists

### Type Data Structure
- Linear Data Structure
	- Array
	- Linked List
	- Stack
	- Queue
- Non-Linear Data Structure
	- Tree
	- Graphs
	
## LINKED LIST VS ARRAY
### WHAT IS ARRAY?
> An Array is a data structure containing a number of data values (All of Which are of same type)

#### PROPERTIES OF ARRAY
- Fixed Size
- All of Which are of same type
- contiguous memory locations
- Difficulty of insertion/deletion
- Fast Access  O(1)

### WHAT IS LINKED LIST?
> in which the elements are not stored at contiguous memory locations.

#### PROPERTIES OF LINKED LIST
-  Dynamic Size
-  Not contiguous memory locations
-  Ease of insertion/deletion
- Extra memory space
-  Slow Access  O(n)

### Types of LINKED LIST:
- Single-Linked list
- Doubly-Linked list

#### REPRESENTATION OF LINKED LIST
- Head
- Tail
- Node 

#### REPRESENTATION OF NODE
- Data
- Pointer to the next node

## Terminology

1. ##### Linked List: A data structure that contains nodes that links/points to the next node
2. ##### Singly: there is only one reference, and the reference points to the Next node
3. ##### Doubly: there being two (double) references within the node, for Next and Previous
4. ##### Node: items or data in the linked list
5. ##### Next: property contains the reference to the next node.
6. ##### Head: is a reference of type Node to the first node in a linked-list
7. ##### Current: is a reference of type Node to the node that is currently being looked


### What’s a Linked List, Anyway? [Part 1]
[Resource](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)
- Linked Lists are linear data structures meaning you have to traverse every node to get to the value you want to access or add in most cases.
- The difference between Linked Lists and arrays is the way it handles memory.
    - Linked Lists can be stored anywhere in memory as they will always point to the next and/or previous node in their list.
    - Arrays require a block of contiguous memory of the size required to be available in memory.

### What’s a Linked List, Anyway? [Part 2]
[Resource](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)
- Adding new items to the list is simple with linked lists because there is no need to pre-allocate memory.
- Once a new item is added to the list, you just need to rearrange the pointers
- The advantage of linked lists is the dynamic memory management and the speed at which you can add or remove elements.
- The disadvantage of linkedlists is that it is slow to search for a specific item in the list.

