#CS
Arrays are a data structure which includes a collection of items stored consecutively in memory. An array can consist of any data type, such as [[Integer]]s or [[Char]]s, though every item in the array must be of the same type. An array must also have a fixed size, defined on initialization.

An example of arrays in C++:
```cpp
int numbers[3] = {10, 59, 11};
string cars[3] = {"BMW", "Volvo", "Ford"};
char types[3] = {'A', 'G', 'U'};
```
# Array Operations
## Accessing an Element
Consider the following array:
```c
int numbers[] = [5, 9, 1, 6, 2, 1, 3];
```
The complexity of reading an element from the array `numbers` would be constant, or $O(1)$. This is because the computer can almost instantly recall any item from memory at any index.
## Inserting/Deleting an Element
Consider the same array `numbers`:
```c
int numbers[] = [5, 9, 1, 6, 2, 1, 3];
```
The [[Algorithmic Complexity]] of inserting an item into an array at a specific index would be linear, or $O(n)$. This is because the computer must first push all elements after the index to the right, then it must insert the given item at the given index. Similarly, the algorithmic complexity of removing an element is also $O(n)$.
## Updating an Element
Consider the same array `numbers`:
```c
int numbers[] = [5, 9, 1, 6, 2, 1, 3];
```
The algorithmic complexity of updating an element at an index is $O(1)$, because the computer can simply replace the item at the given index with a given item.
## Traversing the Array
Consider the same array `numbers`:
```c
int numbers[] = [5, 9, 1, 6, 2, 1, 3];
```
The algorithmic complexity of traversing the array would of course be $O(n)$, as the computer must go through each element individually.