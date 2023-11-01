- A **stack** is an `ordered list` in which the last element added is the first element *retrieved* or *removed*. `Last-In, First-Out`
- During program execution, the *stack* can be used to *store information* about the parameters and return points for all the methods that are currently executing.
- The methods of the `Stack` class from the `java.util` package are used to implement *stacks* in `Java`.
- The list methods are used to implement *stacks* in `Python`.
- The *two* `2` main stack operations are the following:
	- `Push` - *Adds* an item to the *top of the stack*
	- `Java Version:`
		```java
		Stack stack = new Stack();
		stack.push("Mairo");
		```
	- `Python Version:`
	```python
	stack = []
	stack.append("Berlin");
	```
	- `Pop` - *Removes* an item from the *top of the stack*
	- `Java and Python Version: pop()`
- Other *stack* operations:
	- `Peek` - *Looks* at the item at the *top of the stack* without removing it from the *stack*
		- Method in `Java`: `peek()`
		- Method in `Python`: `stack_name[0]`
	- **Test whether stack is empty**
		- For `Java`, use the `isEmpty()` method.
		- For `Python`, use the `if not` condition, followed by the *stack* name and a colon.
		```python
		stack = []
		if not stack:
			print("Stack is empty.")
		```

###### Stack Applications
- **Finding palindromes**: A **palindrome** is a `string` that reads the same in either direction. *Ex. level, radar, civic*
- **Evaluating a postfix expression**: A normal expression is in infix notation. In a *postfix expression*, the `operands` (variable or number) precede the operators `(symbol)`