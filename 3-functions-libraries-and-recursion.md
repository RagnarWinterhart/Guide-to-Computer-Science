# Functions
Function are ways of creating resuable and versatile bits of code. They accept input that are called parameters and sometimes return a value. 

Functions are useful because: 
- they help to reduced repeated code
- break programs into easier to understand parts
- make code easier to test

When something goes wrong in a program it is a lot easier to identify a function that is malfunctioning than it is to track down a line of code in a program that doesnt use functions. 


# Libraries
Collections of prewritten code that programs can use to provide useful functions and classes without having to build them from scratch. 

Using libraries is a way to save time and build on things that have already been written, instead of reinventing the wheel.

# Recursion
Recursion is when a function calls itself to solve a problem, doing so breaks the problem down into smaller and smaller parts until it reaches a base case.

Recursive functions have:
- A base case that stops the recursion
- A recursive case the calls the function again with a smaller or simpler form of the problem

Each recursive call creates another function call on the stack, one the base case has been reached each call is resolved in reverse order.
Without a proper base case a function can continue calling itself until the program runs out of stack space. 