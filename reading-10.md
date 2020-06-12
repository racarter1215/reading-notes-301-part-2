# Call stack

### It's a mechanism for an interpreter to keep track of its place in a script that calls multiple functions: specifically, what function is currently being run and what functions are called from within that function, etc

##### When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

##### Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.

##### When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

##### If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

# JS Call Stack

### The JavaScript engine is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.

##### The call stack is primarily used for function invocation. Since the call stack is single, function execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.

##### asynchronous js has a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.

##### call stack is a data structure that uses the Last In, First Out principle to temporarily store and manage function invocation (call).

##### When a function is invoked, the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.

##### Manage function invocation (call): The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.

##### A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error|

# JavaScript error messages && debugging

### Types of errors

##### Reference Errors: This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

##### Syntax Errors: this occurs when you have something that cannot be parsed in terms of syntax

##### Range Errors:  an invalid length

##### Type Errors: shows up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

##### Debugging: he easiest and maybe the most common way its to simply console.log() the variables you want to check

##### Using Node.js with Visual Studio Code you can press the debug tab


