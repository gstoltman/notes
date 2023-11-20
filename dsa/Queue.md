### Implementation

```python
class Node:
	def __init__(self, data=None):
		self.data = data
		self.next = None
```

```python
class Queue:
	def __init__(self):
		self.front = None
		self.rear = None

    def is_empty(self):
        return self.front is None

    def enqueue(self, data):
        new_node = Node(data)
        if self.is_empty():
            self.front = self.rear = new_node
        else:
            self.rear.next_node = new_node
            self.rear = new_node

    def dequeue(self):
        if not self.is_empty():
            removed_data = self.front.data
            self.front = self.front.next_node
            if self.front is None:
                self.rear = None
            return removed_data
        else:
            print("Queue is empty")
            return None

    def peek(self):
        if not self.is_empty():
            return self.front.data
        else:
            print("Queue is empty")
            return None

    def size(self):
        current_node = self.front
        count = 0
        while current_node:
            count += 1
            current_node = current_node.next_node
        return count
```