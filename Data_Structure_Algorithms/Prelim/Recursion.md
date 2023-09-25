#### Recursion
- is a process where a `function` calls itself once or multiple time to solve a problem.
- Any function that calls itself is `recursive`.
- A `recursive algorithm` must:
	1. Have a base case - A `base case` is the condition that allows the algorithm to stop recurring.
	2. Change its state and move toward the base case - A `change of state` means that some data that the algorithm is using is modified.
	3. Call itself, `recursively`.

##### Three recursion occurrences
- **Direct Recursion** - Recursion that involves a method directly calling itself.
```java
public class Test {
	public static void main(String[] args) {
		int number = 3;
		func(number);
	}
	
	/* Recursion function */
	static void func(int num) {
		if (num > 0) {
			System.out.print(num+" ");
			func(num - 1); // Last statement in the function
		}
	}
}
```

- **Indirect Recursion** - Occurs when a method invokes another method, eventually resulting in the original method being invoked again.
```java
public class Test {
	public static void main(String[] args) {
		funcA(20);
	}

	
	static void funcA(int number) {
		if (number > 0) {
			System.out.print(" "+number);
			funcB(number - 1); // func(A) is calling func(B)
		}
	}

	static void funcB(int number) {
		if (number > 1) {
			System.out.print(" "+number);
			funcA(number / 2); // func(B) is calling func(A)
		}
	}
}
```

- **Infinite Recursion** - A recursive function fails to stop recursion.
```java
public class Test {
	public static void main(String[] args) {
		int number = 10; // Initial value of number
		foo(number);
	}

	static void foo(int number) {
		if (number == 0)  // Base condition is never met here
			return;

		System.out.print(number+" "); // Print the current value of number
		foo(number); // Call itself recursively
	}
}
```

##### Recursion vs Iteration
- **Iteration** - A process of repeating a ==set of instructions==. This is also known as `looping`.

| **Recursion** | **Iteration** |
| --------- | --------- |
| It terminates when a base case is reached. | It terminates when a condition is proven to be false. |
| Each recursive call requires extra memory space. | Each iteration does not require extra memory space |
| An infinite recursion may cause the program to run out of memory and may result in stack overflow | An infinite loop could loop forever since there is no extra memory being created. |
| Solutions to some problems are easier to formulate recursively. | Iterative solutions to a problem may not always be as obvious as a recursive solution. |

##### Types of Recursion
- **Linear Recursion** - The function calls itself `once` each time it is invoked. `Ex.` **finding the factorial**
```python
def factorial(n):
	if n == 0:
		return 1
	else:
		return n * factorial(n - 1)

n = int(input("Enter a number to compute the factorial: "))
print("The factorial of "+str(n) + " is "+str(factorial(n)) +".")
```
 
```java
import java.util.Scanner;

public class factorial {
	public static void main(String[] args) {
		Scanner read = new Scanner(System.in);
		System.out.print("Enter a number to compute the factorial: ");
		int number = read.nextInt();

		System.out.println("The factorial of "+number+" is "+compute(number));
		read.close();
	}

	public static int compute(int number) {
		if (number == 0) {
			return 1;
		} else {
			return number * compute(number - 1);
		}
	}
}
```
###### Output
	> java factorial.java
	> Enter a number to compute the factorial: 6
	> The factorial of 6 is 720
	> 
	> python factorial.py
	> Enter a number to compute the factorial: 6
	> The factorial of 6 is 720


- **Tail Recursion** - The function makes a recursive call as its very `last` operation. `Ex.` finding the greatest common divisor of two (2) non-zero integers.
```python
def find_gcd(num1, num2):
	if num1 % num2 == 0:
		return num2
	return find_gcd(num2, num1 % num2)

num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))
print("The GCD of "+str(num1)+" and "+str(num2)+" is "+str(find_gcd(num1, num2)))
```

```java
import java.util.Scanner;

public class find_gcd {
	public static void main(String[] args) {
		Scanner read = new Scanner(System.in);
		System.out.print("Enter the first number: ");
		int num1 = read.nextInt();

		System.out.print("\nEnter the second number: ");
		int num2 = read.nextInt();

		System.out.printf("The GCD of %d and %d is %d\n", num1, num2, find_gcd(num1, num2));
		read.close();
	}

	public static int find_gcd(int num1, int num2) {
		if (num1 % num2 == 0) {
			return num2;
		}
		return find_gcd(num2, num1 % num2);
	}
}
```
###### Output:
	> python gcd.py
	> Enter the first number: 40
	> Enter the second number: 35
	> The GCD of 40 and 35 is 5
	> 
	> java find_gcd.java
	> Enter the first number: 40
	> Enter the second number: 35
	> The GCD of 40 and 35 is 5


- **Binary Recursion** - The function call itself `twice` in the run of the function. `Ex.` Fibonacci series
```python
def fib(num):
	if num <= 1:
		return num
	return fib(num - 1) + fib(num - 2)

num = int(input("Enter a number higher than 0: "))
for i in range(num):
	print(fib(i))
```

```java
import java.util.Scanner;

public class fib {
	public static void main(String[] args) {
		Scanner read = new Scanner(System.in);

		System.out.print("Enter a number higher than 0: ");
		int num1 = read.nextInt();

		for(int i = 0; i < num1; ++i) {
			System.out.println(fib(i));
		}
		read.close();
	}

	public static int fib(int num) {
		if (num <= 1) {
			return num;
		}
		return fib(num - 1) + fib(num - 2);
	}
}
```

###### Output:
	> python fib.py
	> Enter a number higher than 0: 6
	> 0
	> 1
	> 1
	> 2
	> 3
	> 5
	> 
	> java fib.java
	> Enter a number higher than 0: 6
	> 0
	> 1
	> 1
	> 2
	> 3
	> 5


- **Mutual Recursion** - The function works in a `pair` or a group. `Ex.` determining whether an integer is even or odd
```python
def is_even(num):
	if num == 0;
		return True
	else:
		return is_odd(num - 1)

def is_odd(num):
	if num == 0:
		return False
	else:
		return is_even(num - 1)

num = int(input("Enter a number: "))
if is_even(num):
	print(str(num)+" is an even number.")
else:
	print(str(num)+" is an odd number.")
```

```java
import java.util.Scanner;

public class even_odd {
	public static void main(String[] args) {
		Scanner read = new Scanner(System.in);

		System.out.print("Enter a number: ");
		int num = read.nextInt();

		System.out.printf(is_even(num)? "%d is an even number\n" :
			"%d is an odd number\n", num);

		read.close();
	}

	public static boolean is_even(int num) {
		if (num == 0) {
			return true;
		}
		return is_odd(num - 1);
	}

	public static boolean is_odd(int num) {
		if (num == 0) {
			return false;
		}
		return is_even(num - 1);
	}
}
```
###### Output:
	> python even_odd.py
	> Enter a number: 7
	> 7 is an odd number
	> 
	> java even_odd.java
	> Enter a number: 10
	> 10 is an even number