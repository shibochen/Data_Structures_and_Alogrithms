# Tree

A `tree` is a non-linear data structure which organizes data in hierarchical structure.

## Tree Terminology

- **Root** : The root node is the topmost node in the tree hierarchy.
- **Edge** : The connecting link between any two nodes. If we have **N** number of nodes then we can have a maximum of **N-1** number fo links.
- **Parent Node** : The node is predecessor of any node
- **Child Node** : The node is descendant of any node
- **Sibling Node** : nodes belong to same parent
- **Leaf Node** : The node does not have a child
- **Internal Nodes** : The node has at least one child
- **External Nodes** : The node does not have a child
- **Degree**
  - **Degree of the Node** : The total number of children of a node
  - **Degree of the Tree** : The highest degree of a node among all the nodes
- **Level Number** : Each node of the tree is assigned a level number in such as way that each node is present at one level higher than its parent. Root node of the tree is always present at level 0.
- **Height**
  - **Height of the Node** : The total number of edges from leaf node to a particular node in the largest path
  - **Height of the Tree** : The height of the root node
- **Depth**
  - **Depth of the Node** : The total number of edges from root node to a particular node.
  - **Depth of the Tree** : The total number of edges from root to leaf in the longest path
- **Path** : The sequence of nodes and edges between two nodes
- **Length of a Path** : The total number of nodes in that path
- **Sub Tree** : Every child node will form a subtree on its parent node

## Binary Tree

- A **binary tree** is a special type of tree data structure in which every node can have a maximum of 2 children.
- A Binary Tree node contains following parts:

    1. Data
    2. Pointer to left child
    3. Pointer to right child

## Types of Binary Tree

1. **Full Binary Tree** - A binary tree in which every node has either two or zero number of children
2. **Complete Binary Tree** - A Binary Tree is complete Binary Tree if all levels are completely filled except possibly the last level and last level has all keys as left as possible
3. **Perfect Binary Tree** - A Binary Tree is Perfect Binary Tree in which all internal nodes have two children and all leaves are at the same level.
4. **Balance Binary Tree** - A Binary Tree is balanced if the height of left and right children of every node differ by either -1, 0 or +1.

## Binary Tree Traversal

- Breadth First Traversal (BFS)
- Depth First Traversals (DFS)
  - Preorder Traversal (Root-Left-Right)
  - Inorder Traversal (Left-Root-Right)
  - Postorder Traversal (Left-Right-Root)
- Implementation of BFS
  - recursion
  - iteration (using Queue)
- Implementation of DFS
  - recursion
  - iteration (using Stack)
  
## Binary Search Tree

- A **Binary Search Tree** is a binary tree in which every node contains only smaller values in its left substree and only larger values in its right subtree

Reference

- [Tree Traversal](https://www.geeksforgeeks.org/tree-traversals-inorder-preorder-and-postorder/)
- [树的遍历](https://www.cnblogs.com/harrygogo/p/4599097.html)
