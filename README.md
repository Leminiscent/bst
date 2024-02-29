# BST

This Python module provides a basic implementation of a Binary Search Tree (BST). A Binary Search Tree is a node-based binary tree data structure which has the following properties:

- The left subtree of a node contains only nodes with keys less than the node's key.
- The right subtree of a node contains only nodes with keys greater than the node's key.
- Both the left and right subtrees must also be binary search trees.

## Features

- **Insertion**: Adds a new node with a unique key to the BST.
- **Search**: Finds a node with a specified key in the BST.
- **Deletion**: Removes a node with a specified key from the BST.
- **Inorder Traversal**: Traverses the BST in an inorder manner and returns a list of node keys.

## Classes and Methods

### `TreeNode`

This class represents a node in the binary search tree.

#### Attributes

- `key`: The value or data contained in the node.
- `left`: Reference to the left child node.
- `right`: Reference to the right child node.

### `BinarySearchTree`

This class represents the binary search tree.

#### Methods

- `insert(key)`: Inserts a new key into the BST.
- `search(key)`: Searches for a node with the specified key in the BST.
- `delete(key)`: Deletes a node with the specified key from the BST.
- `inorder_traversal()`: Returns a list of keys in the BST obtained via an inorder traversal.

## Usage

To use this BST implementation, create an instance of `BinarySearchTree` and utilize its methods to perform operations on the tree.

Example:

```python
bst = BinarySearchTree()
nodes = [50, 30, 20, 40, 70, 60, 80]

for node in nodes:
    bst.insert(node)

print("Inorder traversal:", bst.inorder_traversal())
print("Search for 40:", bst.search(40))

bst.delete(40)

print("Inorder traversal after deleting 40:", bst.inorder_traversal())
print("Search for 40:", bst.search(40))
```

This will output:

```python
Inorder traversal: [20, 30, 40, 50, 60, 70, 80]
Search for 40: <__main__.TreeNode object at 0x...>
Inorder traversal after deleting 40: [20, 30, 50, 60, 70, 80]
Search for 40: None
```

## Note

This implementation does not handle duplicate keys. If a key already exists in the BST, the insertion method will ignore the new key.
