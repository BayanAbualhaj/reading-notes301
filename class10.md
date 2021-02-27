# What I learned 

## Call stack

![callstack](https://miro.medium.com/max/798/1*CCHexfHNCNo-f8aw3rbRew.jpeg)

**Call stack** 
is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.

* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.

* **stack overflow** If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

*  Whenever we invoke a function, it is **automatically added to the Call Stack**. Once the function has executed all of its code, it is automatically removed from the Call Stack. Ultimately, the Stack is empty again.

* The browser provides web APIs like:
1. the DOM 
2. AJAX
3. Timers.

function(s) execution, is done, one at a time, from top to bottom. It means the call stack is **synchronous**.

* Manage function invocation (call): The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.

#### The key takeaways from the call stack are:
1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

## JavaScript error messages && debugging


![error](https://d2h0cx97tjks2p.cloudfront.net/blogs/wp-content/uploads/sites/2/2019/08/JavaScript-Debugging-and-Testing.png)

### Error 

* Types of error messages:

1. Reference errors:This is as simple as when you try to use a variable that is not yet declared you get this type os errors.

2. Syntax errors :I know it’s in the name of the errors, but like it says itself, this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.

3. Range errors:Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.

4. Type errors: Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.



### Debugging 

To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5).
If the line you selected was run you will be able to see what has happened before that point and you can try and evaluate the next lines to check if everything is outputting what you are expecting.
The breakpoint can also be achieved by putting a debugger statement in your code in the line you want to break.

### Handling errors

we usually try to catch the errors so we can gracefully fallback to a default state of our application in case of an error (this fallback can be a 404 page which is normally not that graceful but is better than a page to just stop working).

#### Tools to avoid runtime errors

* quokka to evaluate your code as you type

* eslint to make sure your style guide is consistency and it will grab you an error or two along the way and

* For those of you looking to make JS a more strong typed experience you can check out stuff like TypeScript (like I said in a previous article, when learning I rather avoid libraries that abstract the core language so I wouldn’t recommend this last one when starting).

-------
+++++++++++++++++++++


