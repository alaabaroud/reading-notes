
# The call stack:
 - The call stack is mostly utilized for invoking functions (call). Because the call stack is single, functions are executed one by one, from top to bottom. It denotes a synchronous call stack.

- LIFO means Last In, First Out, It means that when a function returns, the last function pushed onto the stack is the first to be called.

- The call stack keeps track of the position of each stack frame in order to manage function invocation (call). It already knows what function will be run next (and will remove it after execution). The synchronous nature of JavaScript code execution is due to this.

- When a recursive function (one that calls itself) does not have an exit point, a stack overflow occurs. The browser (hosting environment) can only handle a certain number of stack calls before throwing a stack error.
