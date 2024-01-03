### Implementation

```python
class Node:
	def __init__(self, data=None):
		self.data = data
		self.next = None
```

### Examples

```python
# Example usage:
# Create nodes
node1 = Node(1)
node2 = Node(2)
node3 = Node(3)

# Link nodes
node1.next = node2
node2.next = node3

# Access data in nodes
print(node1.data)  # Output: 1
print(node2.data)  # Output: 2
print(node3.data)  # Output: 3

# Traverse linked nodes
current_node = node1
while current_node:
    print(current_node.data)
    current_node = current_node.next
```