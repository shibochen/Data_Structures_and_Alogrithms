# Tree Part Two

## AVL Tree

An **AVL Tree** is a balanced binary search tree. In an AVL tree, balance factor of every node is either -1, 0, or + 1.

`Balance factor = heightOfLeftSubtree - heightOfRightSubtree || heightOfRightSubtree - heightOfLeftSubtree`

Every AVL Tree is a binary search tree but every Binary Search Tree need not be AVL Tree.

## AVL Tree Rotations

If the tree becomes imbalanced, rotation operations are used to make it balanced.

`Rotation is the process of moving nodes either to left or to right to make the tree balanced`

There are **four** rotations and they are classified into two types.

Rotaions

1. Single Rotation
    - Left Rotation (LL Rotation)
    - Right Rotaion (RR Rotation)
2. Double Rotation
    - Left Right Rotation (LR Rotation)
    - Right Left Rotation (RL Rotation)

**Note** : LL means a new node is inserted or deleted to the left side of parent's node's left child

```shell
LL Rotation: 1 is on left side of parent's node(3) left child(2)
            3
           /
          2      -------->        2
         /                      /   \
        1                      1     3
```

## Operations on an AVL Tree

The following operations are performed on AVL tree:

1. Search ---- O(log n) time complexity
2. Insertion ---- O(log n) time complexity
3. Deletion ---- O(log n) time complexity

## Red-Black Tree

A **Red-Black Tree** is a variant of Binary Search Tree in which every node is colored either RED or BLACK

## Properties of Red Black Tree

1. Red-Black Tree must be a Binary Search Tree
2. The ROOT node must be colored BLACK.
3. The children of Red colored node must be colored BLACK. (There should not be two consecutive RED nodes).
4. In all the paths of the tree, there should be same number of BLACK colored nodes.
5. Every new node must be inserted with RED color.
6. Every leaf(e.i. NULL node) must be colored BLACK.

If all the properties are not satisfied, perform the following operation to make it Red Black Tree.

1. Recolor
2. Rotation
3. Rotation followed by Recolor