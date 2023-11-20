### Implementation

```python
class Node:
	def __init__(self, data=None):
		self.data = data
		self.next = None
```

```python
class LinkedList:
	def __init__(self):
		self.head = None

	def is_empty(self):
		self.head = None

	def append(self, data):
		new_node = Node(data)
		if self.is_empty():
			self.head = new_node
		else:
			current_node = self.head
			while current_node.next_node:
				current_node = current_node.next_node
			current_node.next_node = new_node

	def prepend(self, data):
		new_node = Node(data)
		new_node.next_node = self.head
		self.head = new_node

    def display(self):
        current_node = self.head
        while current_node:
            print(current_node.data, end=" -> ")
            current_node = current_node.next_node
        print("None")
```
### Examples
```python
my_linked_list = LinkedList()

my_linked_list.append(1)
my_linked_list.append(2)
my_linked_list.append(3)

my_linked_list.prepend(0)

my_linked_list.display()
```