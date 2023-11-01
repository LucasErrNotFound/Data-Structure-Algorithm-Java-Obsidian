- A `queue` is an *ordered list* in which the *first element added is the first element retrieved or removed* `(First-In, First-Out)`.
- The first element in the queue in known as the `head` of the *queue*.
- The methods of the `Queue` interface from the `java.util` package are used to implement *queues* in `Java`. Since interfaces cannot be instantiated, `LinkedList` is used to *instantiate* a `Queue` object.
- The methods of `collections.deque` are used to implement *queues* in `Python`. The *import* statement shall be `from collections import deque`.
- The list methods can also be used to implement *queues* in `Python`.
- The *two* `2` main *queue* operations are the following:
	- `Enqueue` - *Adds* an item into the *queue*
	- Method in `Java:
	```java
	Queue queue = new LinkedList();
	queue.offer("Kuya Rome");
```
	- Method in `Python:`
	```python
	queue = deque([])
	queue.append("Kuya Rome")
```

	- `Dequeue` - *Removes* the `head` of the *queue*
	- Method in `Java:` `poll()`
	- Method in `Python:` `popleft()`

- Other *queue* operations:
	- `Peek` - *Retrieves* the `head` of the *queue*
		- Method in `Java:` `peek()`
		- Method in `Python:` `queue_name[0]`
	- **Test whether queue is empty**
		- For `Java`, use the `isEmpty()` method.
		- For `Python`, use the `if not` condition, followed by the queue name and a colon.
		```python
		queue = deque([])
		if not queue:
			print("Queue is empty")
```

###### Other Queue Methods
- `Java` methods `offer()`, `poll()`, and `peek()` do not throw exceptions. The methods `add()`, `remove()`, and `element()` perform the same tasks but throw exceptions.
- Other methods that can be used for both *queues* and *lists* are the following:
 
| `Function` | `Java` | `Python` |
| --- | --- | --- |
| *Delete all elements* | `clear()` | `clear()` |
| *Copy all elements* | `clone()` | `copy()` |
| *Reverse the elements* | `Collections.reverse()` | `reverse()` |