### Implementation

```python
class TreeNode:
	def __init__(self, data, left=None, right=None):
		self.data = data
		self.left_child = left
		self.right_child = right
```
```python
class BinaryTree:
	def __init__(self):
	    self.root = None

    def insert(self, key):
        if self.root is None:
            self.root = Node(key)
        else:
            self._insert_recursive(key, self.root)

    def _insert_recursive(self, key, current_node):
        if key < current_node.key:
            if current_node.left is None:
                current_node.left = Node(key)
            else:
                self._insert_recursive(key, current_node.left)
        elif key > current_node.key:
            if current_node.right is None:
                current_node.right = Node(key)
            else:
                self._insert_recursive(key, current_node.right)
        else:
            # Duplicate keys are not allowed in this example
            print("Key already exists in the tree.")

    def inorder_traversal(self, node):
        if node:
            self.inorder_traversal(node.left)
            print(node.key, end=" ")
            self.inorder_traversal(node.right)
```
```