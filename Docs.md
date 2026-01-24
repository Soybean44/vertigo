# Documentation

For simple terminology, a line in vertigo is a vertical sequence of characters. 

## The Stack
In vertigo any immediate is placed onto the stack. As of right now the stack only supports integers and strings.
```
2"
4H
;i
 ;
```

This pushes the integer 24 and then the string "Hi" onto the stack. 

## The `;` character

The `;` character is used to indicate the end of a statement. When the compiler encounters a `;` it will do one of two things depending on what is on the statement type. If it is an immediate (integer or string) it will push it onto the stack. If it is an operation it will execute that operation.

If there is nothing on the statement when a `;` is encountered it will be ignored. And if there is anything after the `;` on the same line it will also be ignored. This effectively makes `;` a comment indicator as well.

## Operations
As of right now the rest of vertigo is operations. There is no way to define variables or functions yet. Most of these are self explanatory, they pop the required number of arguments off the stack and push the result back onto the stack. Here is a list of all the operations:

- `+` : Pops two integers off the stack, adds them, and pushes the result back onto the stack.
- `-` : Pops two integers off the stack, subtracts the second from the first, and pushes the result back onto the stack.
- `*` : Pops two integers off the stack, multiplies them, and pushes the result back onto the stack.
- `/` : Pops two integers off the stack, divides the first by the second, and pushes the result back onto the stack.
- `print` : Pops a value off the stack and prints it to the console, can handle strings or integers.
- `dup` : Pops a value off the stack and pushes it back twice, effectively duplicating the top value on the stack.
- `flip` : Pops two values off the stack and pushes them back in reverse order, effectively swapping the top two values on the stack.
- `pop` : Pops a value off the stack and discards it.
- `loop` : Marks the start of a loop block.
- `end` : Marks the end of a loop block. Pops an integer off the stack and loops back to the matching `loop` statement if it is not 0. If the number is non-zero it will push the number back onto the stack before looping.


