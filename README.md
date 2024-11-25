# AVL Tree Visualization
 AVL Tree Visualization: A dynamic visualization tool to explore AVL tree operations like insertion, deletion, and search, showcasing automatic balancing and highlighting imbalances in real-time. Perfect for learning self-balancing trees and their significance in algorithms.

## Table of Contents

1. [Binary Search Tree (BST) Overview](#1-binary-search-tree-bst-overview)
2. [Need for Self-Balancing Trees](#2-need-for-self-balancing-trees)
3. [AVL Trees Introduction and Imbalance Detection](#3-avl-trees-introduction-and-imbalance-detection)
4. [Sub-Cases of Imbalance in AVL Trees](#4-sub-cases-of-imbalance-in-avl-trees)
5. [Balancing Each Imbalance Case](#5-balancing-each-imbalance-case)
6. [AVL Trees vs. Red-Black Trees](#6-avl-trees-vs-red-black-trees)
7. [How to Use the Visualization](#7-how-to-use-the-visualization)

---

## 1. Binary Search Tree (BST) Overview

A **Binary Search Tree (BST)** is a data structure where each node has at most two children. The left child contains values less than the node, and the right child contains values greater than the node. 

### Time Complexity for Operations:

| **Operation** | **Average Case** | **Worst Case** |
|----------------|------------------|----------------|
| Search         | O(log n)         | O(n)           |
| Insertion      | O(log n)         | O(n)           |
| Deletion       | O(log n)         | O(n)           |

The time complexity depends on the height of the tree. For a skewed BST (e.g., all elements inserted in sorted order), the height can become `n`, making operations inefficient.

---

## 2. Need for Self-Balancing Trees

In unbalanced BSTs, the height can grow to `O(n)`, degrading performance to linear time. **Self-balancing trees** like AVL Trees ensure the height is always `O(log n)`, maintaining efficient operations.

- **Purpose of Balancing**: To keep the tree height minimal, ensuring all operations (search, insert, delete) are efficient.
- Self-balancing mechanisms detect and fix imbalances automatically after insertions or deletions.

---

## 3. AVL Trees Introduction and Imbalance Detection

### Introduction:
**AVL Tree** (named after inventors Adelson-Velsky and Landis) is a self-balancing BST where the difference between the heights of left and right subtrees (the balance factor) is at most 1 for every node.

### Detection of Imbalance:
- The **balance factor** of a node is calculated as:  
  `Balance Factor = Height(left subtree) - Height(right subtree)`
- If the balance factor is not in the range `[-1, 1]`, the tree is imbalanced.

---

## 4. Sub-Cases of Imbalance in AVL Trees

Imbalances can occur in four cases based on the insertion direction:

1. **LL (Left-Left)**: Insertion in the left subtree of the left child.
2. **LR (Left-Right)**: Insertion in the right subtree of the left child.
3. **RR (Right-Right)**: Insertion in the right subtree of the right child.
4. **RL (Right-Left)**: Insertion in the left subtree of the right child.

---

## 5. Balancing Each Imbalance Case

### LL (Left-Left):
- **Cause**: Node inserted in the left subtree of the left child.
- **Solution**: Perform a **Right Rotation**.

### LR (Left-Right):
- **Cause**: Node inserted in the right subtree of the left child.
- **Solution**: Perform a **Left Rotation** on the left child, then a **Right Rotation** on the root.

### RR (Right-Right):
- **Cause**: Node inserted in the right subtree of the right child.
- **Solution**: Perform a **Left Rotation**.

### RL (Right-Left):
- **Cause**: Node inserted in the left subtree of the right child.
- **Solution**: Perform a **Right Rotation** on the right child, then a **Left Rotation** on the root.

---

## 6. AVL Trees vs. Red-Black Trees

### AVL Trees:
- **Strict Balance**: Ensures a height difference of at most 1 between subtrees.
- **Performance**: Better for applications with frequent lookups due to tighter balancing.
- **Memory Overhead**: Stores balance factors for nodes.
- **Use Case**: Use AVL trees for search-heavy applications, e.g., databases.

### Red-Black Trees:
- **Relaxed Balance**: Ensures a maximum height difference of 2.
- **Performance**: Faster insertions and deletions due to less strict balancing.
- **Memory Overhead**: Stores an additional bit per node for color (red or black).
- **Use Case**: Use Red-Black trees for applications with frequent insertions and deletions, e.g., dynamic data structures.

---

## 7. How to Use the Visualization

### Features:
1. **Node Addition**: Add a new node to the AVL tree by entering its value and clicking the **Add** button.
2. **Node Deletion**: Remove a node by entering its value and clicking the **Delete** button.
3. **Search and Highlight**: Search for a node, and it will be highlighted in **red** if found. If not, an alert box notifies that the node is not present.

### Steps:
1. Open the visualization in any modern browser.
2. Use the controls to interact with the AVL tree:
   - Enter values in the input box to add, delete, or search nodes.
   - Observe the tree rebalancing dynamically after operations.
3. Explore the visualization to understand AVL tree behavior and balancing operations.

---

This project provides an educational tool to visualize AVL tree operations and balancing, helping users grasp self-balancing trees and their significance in computer science.
