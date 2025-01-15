# Binary Trees and AVL Trees

## Binary Trees

### Definition
A **binary tree** is a hierarchical data structure where each node has at most two children, referred to as the left child and the right child. The topmost node of a binary tree is called the **root**, and each node in the tree contains a value or data.

### Properties
- Each node has at most two children.
- Every node has a left and right child.
- The depth or level of a node is the number of edges from the root to the node.
- The height of the tree is the length of the longest path from the root to a leaf.

### Types of Binary Trees
- **Full Binary Tree**: Every node has either 0 or 2 children.
- **Perfect Binary Tree**: All internal nodes have exactly two children, and all leaf nodes are at the same level.
- **Complete Binary Tree**: All levels are fully filled except possibly for the last level, which is filled from left to right.
- **Degenerate (or pathological) Tree**: Every parent node has only one child, making it essentially a linked list.

### Traversals
There are several methods to traverse a binary tree:
1. **Pre-order**: Visit the root, traverse the left subtree, traverse the right subtree.
2. **In-order**: Traverse the left subtree, visit the root, traverse the right subtree.
3. **Post-order**: Traverse the left subtree, traverse the right subtree, visit the root.
4. **Level-order**: Visit nodes level by level, from left to right.

### Example Binary Tree

    10
   /  \
  5    20
 / \   / \
3   8 15  25



## AVL Trees

### Definition
An **AVL tree** (Adelson-Velsky and Landis tree) is a self-balancing binary search tree, where the difference between the heights of the left and right subtrees of any node is at most 1. This ensures that the tree remains balanced, preventing it from becoming skewed (which could degrade the performance of operations like search, insert, and delete).

### Balance Factor
The **balance factor** of a node is the difference between the heights of its left and right subtrees:
- If the balance factor is 0, the tree is balanced.
- If the balance factor is +1, the left subtree is higher.
- If the balance factor is -1, the right subtree is higher.

### Rotations
To maintain the balance factor between -1 and 1, AVL trees perform rotations when necessary:
1. **Right Rotation (Single Rotation)**: Performed when the left subtree is taller.
2. **Left Rotation (Single Rotation)**: Performed when the right subtree is taller.
3. **Left-Right Rotation (Double Rotation)**: Performed when the left subtree is taller, but the left child of the left subtree is shorter.
4. **Right-Left Rotation (Double Rotation)**: Performed when the right subtree is taller, but the right child of the right subtree is shorter.


### Operations on AVL Trees
- **Insertion**: When inserting a new node, after the insertion, the tree is rebalanced if needed by performing rotations.
- **Deletion**: After deleting a node, the tree may require rebalancing to maintain the AVL property.

### Time Complexity
- **Search**: O(log n)
- **Insertion**: O(log n)
- **Deletion**: O(log n)

### Advantages of AVL Trees
- AVL trees provide fast searching, insertion, and deletion because they maintain a balanced structure.
- By keeping the tree balanced, it guarantees that operations will always take logarithmic time.

### Disadvantages of AVL Trees
- Insertion and deletion can be more complex than with regular binary search trees because of the need to rebalance the tree.
- Rotations during insertion and deletion can add overhead.

---

## Conclusion
Binary trees are a fundamental data structure in computer science, and AVL trees are a specialized form of binary trees that maintain balance for optimal performance. The ability to balance the tree dynamically ensures efficient searching, insertion, and deletion operations, making AVL trees a powerful tool in various applications.

