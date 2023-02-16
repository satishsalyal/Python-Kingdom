# Python Recursion 

Recursion is a technique in programming where a function calls itself repeatedly until a certain condition is met. 

# Syntax:
  
    def func(): <--
                  |
                  | (recursive call)
                  |
        func() ----


Here is an __example__ of a recursive function in Python:

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

### Advantages of using recursion

* A complicated function can be split down into smaller sub-problems utilizing recursion.
* Sequence creation is simpler through recursion than utilizing any nested iteration.
* Recursive functions render the code look simple and effective.

### Disadvantages of using recursion

* A lot of memory and time is taken through recursive calls which makes it expensive for use.
* Recursive functions are challenging to debug.
* The reasoning behind recursion can sometimes be tough to think through
