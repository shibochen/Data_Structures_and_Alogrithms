# Recursion

A `recursive method` is one that directly or indirectly invokes iteself.
- direct recursion: function calls itself
  - Ex. function A calls function A
- indirect recursion:  a function is called not by itself but by another function that it called.
  - Ex. function A calls function B, function B calls function A.
For a recursive method to terminate, there must be one or more `base cases/stopping condition`

Recursion:
- nontail recursion: There are pending operations on tail position.
- tail recursion: there are no pending operations to be performed on return from a recursive call.

Problem Solving Using Recursion
- The method is implemented using an `if-else` or a `switch` statement that leads to differnt cases.
- One or more bases (the simplest case) are used to stop recursion.
- Every recursive call reduces the original problem, bringing it increasingly closer to a base case until
it becomes that case.
