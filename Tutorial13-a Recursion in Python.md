# Python Recursion 

Recursion is a technique in programming where a function calls itself repeatedly until a certain condition is met. 
Here is an example of a recursive function in Python:

```Python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)
```

In this example, the factorial function takes an integer n as input and returns the factorial of that number.
The factorial of a non-negative integer n is the product of all positive integers less than or equal to n.

The factorial function uses recursion to calculate the factorial. If n is equal to 0, the function returns 1,
which is the base case. If n is not equal to 0, the function calls itself with n-1 as the argument. This continues 
until n is equal to 0, at which point the function returns 1.
