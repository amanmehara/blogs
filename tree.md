## Binary Tree
A binary tree \\(T\\) is a structure defined on a finite set of nodes that either
* contains no nodes, or
* is composed of three disjoint set of nodes: a root node, a binary tree called its left subtree, and a binary tree called its right subtree.

The binary tree that contains no nodes is called the empty tree or null tree, sometimes denoted NIL.

## Binary Search Tree
The keys in a binary search tree are always stored in such a way as to satisfy the binary-search-tree property:
Let \\(x\\) be a node in a binary search tree. If \\(y\\) is a node in the left subtree of \\(x\\), then \\(y.key \geq x.key\\). If \\(y\\) is a node in the right subtree of \\(x\\), then \\(y.key \leq x.key\\).

### Theorem 1
If \\(x\\) is the root of an \\(n\\)-node subtree, then the call INORDER-TREE-WALK(\\(x\\)) takes \\(\Theta(n)\\) time.

### Theorem 2
We can implement the dynamic-set operations SEARCH, MINIMUM, MAXIMUM, SUCCESSOR, and PREDECESSOR so that each one runs in \\(O(h)\\) time on a binary search tree of height \\(h\\).

### Theorem 3
We can implement the dynamic-set operations INSERT and DELETE so that each one runs in \\(O(h)\\) time on a binary search tree of height \\(h\\).

### Theorem 4
The expected height of a randomly built binary search tree on \\(n\\) distinct keys is \\(O(\lg{n})\\).

## Red-Black Tree
A red-black tree is a binary search tree with one extra bit of storage per node: its color, which can be either RED or BLACK.
A red-black tree is a binary tree that satisfies the following red-black properties:
* Every node is either red or black.
* The root is black.
* Every leaf (NIL) is black.
* If a node is red, then both its children are black.
* For each node, all simple paths from the node to descendant leaves contain the same number of black nodes.

### Lemma 1
A red-black tree with \\(n\\) internal nodes has height at most \\(2 \lg{(n+1)}\\).

## References
1. Introduction to Algorithms, MIT Press
