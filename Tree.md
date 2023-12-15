#CS 
A tree is a hierarchical [[Data Structure]].
![[Pasted image 20230920130033.png]]
## Binary Tree
A binary tree is a tree where each node has no more than 2 children.
## Binary Search Tree
A binary search tree is a binary tree where the nodes are sorted. The left child will always be less than the parent and the right node will always be greater than the parent. Binary search trees make searching for a specific item extremely quick, with a complexity of $O(\log n)$.
## Traversing Orders
- Inorder: Left -> Root -> Right
- Preorder: Root -> Left -> Right
- Postorder: Left -> Right -> Root
## Insertion
Follow tree until no edge found, and insert new node
## [[Algorithmic Complexity]]
Unbalanced Search complexity: $O(n)$
Balanced Search complexity: $O(\log n)$