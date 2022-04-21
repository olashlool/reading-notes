# Reading 15: Tree

## What is a Tree?

Trees are branching data structure. They are often visualized top down from a single root node that has a left child and a right child. Both of these children nodes can have their own left and right children. This pattern can continue on indefinitely until a massive tree-like structure is formed (albeit visualized upside down). Traditionally trees only have right and left children. Since there are two it is referred to as a binary tree.

## Tree Terminology

- Node - A node is the individual item/data that makes up the data structure
- Root - The root is the first/top Node in the tree
- Left Child - The node that is positioned to the left of a root or node
- Right Child - The node that is positioned to the right of a root or node
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not contain any children
- Height - The height of a tree is determined by the number of edges from the root to the bottommost node

## Traversals

Since there is a top down recursive pattern inherent to trees, the traversal algorithms are also recursive. Here are some basic patterns:

## Depth First

- PreOrder - Root, Left child, Right child
- InOrder - Left child, Root, Right child
- PostOrder - Left child, Right child, Root

## Breadth First

- BreadthFirst - Root downward, row by row (of depth), left to right.

## Adding a Node

Trees don't have a strictly defined order so a new node could really be attached anywhere. Traditionally it is acceptable to find the first node that doesn't have two children and slot in there. This can be done using any breadth first traversal.

## Big O Traversals

Searching through a tree only requires one look at each node, so it has a time and space efficiency of O(n). The same goes for insertion. If its insertion is strictly breadth first, then then it is O(w) where w is the largest width of the tree. In an ideal situation where every node has two child nodes, then the width would be 2^(height - 1) where height is log n where n is the total number of nodes and log is base two.

## Binary Search Tree

These type of trees actually have some inherent order where nodes with values smaller than the nodes are placed to the left and greater values are placed to the right. This recursive pattern results in an ordered tree where a value can quickly be found by comparing it to the node its at and go left or right depending if it is less than or greater than its value, respectively.

## Big O Searches

Searching and insertions have a complexity of O(h) where h is height. In an ideal tree, the height is again calculated as log(n) where log is naturally base two. Because of its organized pattern, a search only require O(1) space.
