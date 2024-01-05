#CS 
A linked list is a [[Data Structure]] consisting of a linear collection of items where each item points to the next element in memory. It is different from an [[Array]] because the values are not stored sequentially, and elements can be inserted and removed. Each [[Node]] contains a value and a pointer:
![[Pasted image 20230920110202.png]]
The last element in a list points to `NULL` (`0x0` in memory). The head points to the first node.
## Modifying a Linked List
### Inserting an Element: $O(1)$
#### Inserting at Start
1. Create Node
2. Point node to previous first element
3. Point head to new node
#### Inserting in Middle
1. Create node and point to element before which to insert
2. Redirect previous element to new node
#### Inserting as End
1. Create node
2. redirect last element to new node
3. Point new node to `NULL`
### Deleting an Element $O(1)$
#### Deleting at Start
1. Redirect head to second element
#### Deleting at Middle
1. Take node before node to be deleted and point it to node after node to be deleted
#### Deleting at End
1. Second to last element point to `NULL`
## Other [[Algorithmic Complexity|Algorithmic Complexities]]
Traversing the list is $O(n)$.
Accessing an element of the list is $O(n)$.
## Linked List vs Array
Linked lists are faster than arrays but use more memory:

|            | Array  | LL  |
| ---------- | ------ | --- |
| **Ram**        | 1x     | >2x |
| **Complexity** | $O(n)$ | $O(1)$    |
