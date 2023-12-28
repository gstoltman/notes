### Implementation

```python
def binary_search(ordered_list, search_value):
	first = 0
	last = len(ordered_list) - 1

	while first <= last:
		middle = (first + last) // 2
		if search_value == ordered_list[middle]:
			return True
		elif search_value <= ordered_list[middle]:
			last = middle - 1
		else:
			first = middle + 1
	return False
```

### Implementation using recursion

```python
def binary_search_recursive(ordered_list, search_value):
	if len(ordered_list) == 0:
		return False
	else:
		middle = len(ordered_list) // 2
		if search_value == ordered_list[middle]:
			return True
		elif search_value < ordered_list[middle]:
			return binary_search_recursive(ordered_list[:middle], search_value)
		else:
			return binary_search_recursive(ordered_list[middle+1:], search_value)
			
```
