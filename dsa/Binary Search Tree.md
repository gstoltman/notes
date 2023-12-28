### Implementation

```python
class TreeNode:
	def __init__(self, data, left=None, right=None):
		self.data = data
		self.left_child = left
		self.right_child = right
```

```python
class BinarySearchTree:
	def __init__(self):
		self.root = None

	def insert(self, data):
		new_node = TreeNode(data)
		if self.root == None:
			self.root = new_node
			return
		else:
			current_node = self.root
			while True:
				if data < current_node.data:
					if current_node.left_child == None:
						current_node.left_child = new_node
						return
					else:
						current_node = current_node.left_child
				elif:
					if current_node.right_child == None:
						current_node.right_child = new_node
						return
					else:
						current_node = current_node.right_child

	def find_min(self):
		current_node = self.root
		while current_node.left_child:
			current_node = current_node.left_child
		return current_node.data
```