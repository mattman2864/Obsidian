#CS 
Memory, or **RAM**, is the part of computer that holds short-term data used for currently active programs on the computer.
## Memory Addresses
Memory addresses are represented by a [[Hexadecimal]] value with an `0x` in from of it. For example, the address for the byte at position `35` in decimal would be `0x23`.
## [[C]] Syntax
In [[C]], you can use various syntax to handle the computer's memory:
- `&` is used to get the address of an object in memory
- `*` is used to go to a given address and return the value
- `%p` is used to format a pointer and print it
For example,
```c
int n = 50;  // n references the int 50
int *p = &n; // p is the address of n
```
- `int *` is the datatype of a pointer (like `pointer p = &n;`)
- `malloc` is used to free up a given amount of memory