# JavaScript: Novice to Ninja, 2nd Edition

## Chapter 1: Hello, JavaScript

### **Programming**

Programming is about making computers do what you want.
A computer program is basically a series of instructions that tell your computer how to perform a task.
The first computers were programmed using punched bards, with a hole representing a 1 and no hole representing 0.

The first computer programs were written in **machine code** and **assembly language**.
These are **low-level programming languages** that are closely associated with a computer's hardware.

**High-level programming langugaes**, on the other hand, allow abstractions to be used that make the code easier for humans to read and write.
Programs are written in a language such as C, C++ or Java, which is then compiled into machine code and executed.
The programs written using these languages are very fast, making high-level languages suited to writing games and professional business software where speed is important.
Most native apps are also written in higher-level languages.

**Scripting languages** are also high-level, but they are interpreted, which means they are translated into machine code at run time.
This often makes them slower than compiled languages, although interpreters are becoming ever more sophisticated, and increasingly blurring the lines between compiled and interpreted languages.

### **JavaScript**

JavaScript is a high-level scripting language that is interpreted and compiled at run time.
This means it requires an engine that's responsible for interpreting a program and running it.
The most common JavaScript engines are found in browsers such as Firefox, Chrome or Safari, although JavaScript can be run without a browser using an engine such as Google V8.
Many modern JavaScript engines use a Just-In-Time(JIT) interpreting process, which considerably speeds up the compilation, making programs run faster.

JavaScript is also a dynamic language, so elements of a program can change while it's running, and it can do lots of things in the background at run time(such as type checking) - things that a compiled langugae like C++ would do at compile time.

### **The History of JavaScript**

Brendan Eich
Borrowed various elements from other languages, including AWK, Java, Perl, Scheme, HyperTalk and Self.
Mocha -> LiveScript -> JavaScript

### **The Browser Wars**

Microsoft won the browser wars and Internet Explorer emerged as the dominant browser. Support for standards also increased, helped largely by the efforts of the Web Standards Project(WaSP).
Developers and browser vendors started to work together and embrace the standards laid out by the World Wide Web Consortium(W3C) and ECMA.

### **Web 2.0**

Ajax(Asynchronous JavaScript and XML) - Jesse James Garrett.

### **Standards**

2008, Google developed the V8 engine to run inside the Chrome browser.

### **HTML5**

HTML5 is the latest HTML specification, though it's actually more of an umbrella term for all the latest technologies that are used on the web.
This includes HTML, CSS3 and lots of APIs that use JavaScript to interact with web pages.

HTML5 was finalized in 2014 and the recommendation for the next version, 5.1 was propsed at the end of 2016.

### **Node.js**

2009, Ryan Dahl developed Node.js, which allowed server-side applications to be written in JavaScript.
Node is based on Google's V8 engine and allows the creation of fast and powerful real-time web applications written exclusively in JavaScript.
It also lead to many applications and JavaScript libraries that don't use the browser at all.

The popularity of Node has lead to an interesting development known as Isomorphic JavaScript.
This involves having the same JavaScript code that can be run either on the client or server side: if a browser is unable to run the code, it can be run on the server and downloaded, or if the server is unavailable, the code can be run on the client.

### **JavaScript Versions**

1996, Netscape, Sun Microsystems, the European Computer Manufacturers Association
This standardized language was called ECMAScript to avoid infringing on Sun's Java trademark.
ECMAScript was used to refer to the specification, and JavaScript was used to refer to the langugae itself.

the implementations of JavaScript can vary from engine to engine.

The working group in charge of maintaining ECMAScript is known as Technical Committee 39, or TC-39.

Version1(1997), Version2(1998), Version3(December,1999), Version4(abandoned), Version5(December, 2009),Version6(June,2015), Version7(June, 2016).
In 2015,TC-39 decided to adopt a new approach and start publishing a new specification every year, with the version named after the year it was published.

### **The Future of JavaScript**

Single Page Application(SPA), Prograssive Web App(PWA), HTML5 games, Windows desktop widgets and Chrome OS applications

### **JavaScript In The Console**

REPL - Read Eval Print Loop, it allows you to write JavaScript in the console then outputs the results.

### **Three Layers of the Web**

It is widely considered best practice to separate the concerns of each layer, so each layer is only responsible for one thing.
Putting them altogether can lead to very complicated pages where all of the code is mixed up together in one file, causing "tag soup" or "code spaghetti".

### **Graceful Degradation and Progressive Enhancement**

**Graceful degradation** is the process of building a website so it works best in a modern browser that uses JavaScript, but still works to a reasonable standard in older browsers, or if JavaScript or some of its features are unavailable.

**Progressive enhancement** is the process of building a web page from the ground up with a base level of functionality, then adding extra enhancements if they are available in the browser.

### **Don't Break the Web**

An important concept in the development of the JavaScript language is that it has to be **backward compatible**.

New versions of JavaScript can't do anything that isn't already possible in previous versions of the language.
All that changes is the notation used to implement a particular feature to make it easier to write.
This is known as _syntactic sugar_, as it allows an existing piece of code to be written in a nicer and more succinct way.

The fact that all versions of JavaScript are backwardly compatible means that we can use _transpilers_ to convert code from one version of JavaScript into another.

## Chapter 2 Programming Basics

### **Comments**

Utilities that can take your comments and produce documentation from them: JSDoc Toolkit, Docco, YUIDoc.

### **JavaScript Grammar**

The syntax used by JavaScript is known as a C-style syntax because of its similarities with the C programming language.

### **Primitive Data Types**

_String_

_Symbol(The symbol primitive data type was only introduced in ES6)_

_Number_

_Boolean_

_Undefined_

_Null_

All non-primitive data types return a type of 'object'

If the variable references a non-primitive data type, such as an array, function or object, then using const will not make it **immutable**.

A core tenet of the JavaScript language is that it has to remain backwardly compatible.

### **Scope**

Scope is an important concept in programming.
It refers to where a constant or variable is accessible by the program.
There are two common scopes that are often referred to in programs: global scope and local scope.

### **Variable Naming**

Variables that start with an underscore generally refer to private properties and methods, so it's best to not follow this convention for your own variable names.

JavaScript's built-in functions use the camel-case notation and this is provavly the best convention to follow when naming the constants and variables in your code.
The most important thing is to be consistent.

### Technically, only objects have properties and methods.

JavaScript overcomes this by creating _wrapper objects_ for primitive data types.
This all happens in the background, so for all intents and purposes it appears that primitive data types also have properties and methods.

### **Symbols**

Symbols were introduced as a new primitive value in ES6.
They can be used to create unique values, which helps to avoid any naming collisions.

The uniqueness of symbols, mean that it's impossible for the names of any properties to clash with each other if they are symbols.

### **Numbers**

ES6 provides a handy method called _Number.isInteger()_ that can be used to check if a number is an integer.

The _toFixed()_ method rounds a number to a fixed number of decimal places. The value is returned as a string, rather than a number.

The _toPrecision()_ method round a number to a fixed number of significant figures that is once again return as a string.

_Infinity_ is a special error value in JavaScript that is used to represent any number that is too big for the language to deal with.

The biggest number that JavaScript can handle is 1.7976931348623157e+308.
The smallest number that JavaScript can deal with is 5e-324.

_NaN_ is an error value that is short for "Not a Number".
It is used when an operation is attempted and the result isn't numerical, like if you try to multiply a string by a number.

typeof NaN => number

### **JavaScript Is Weakly Typed**

JavaScript is known as a **weakly typed** or **loosely typed** language.
This means that you don't need to explicitly specify what data-type a variable is when you declare it.

_parseInt()_ can be used to convert a string representation of a numerical value back into a number.

If a string starts with a number, the _parseInt_ function will use this number and ignore any letters that come afterwards.

### **Undefined**

_undefined_ is the value given to variables that have not been assigned a value.

### **Null**

_null_ means 'no value'.
Both _null_ and _undefined_ are both 'non-value' values, meaning they are similar, but behave slightly differently.

The only strange result produced by hard equality is: NaN === NaN => false.

### **Arrays**

An array is an ordered list of values.
It's prefereable to stick to using array literals.

### **Sets**

A set is a data structure that represents a collection of unique values, so it cannot include any duplicate values.
They are similar in concept to a mathematical set, although they don't contain mathematical set operations.

_Array.from()_ method to convert a set into an array.

A **memory leak** occurs when a program retains references to values that can no longer be accessed in its memory.
This means that memory is being used to store values that are no longer required by the program, effectively wasting system resources.

Most modern programming language, including JavaScript, employ various dynamic memory management techniques as **garbage collection**, which is the process of automatically removing items from memory that are no longer required by the program.
Some languages, such as C++ require the programmer to manually manage memory by removing items from memory once they are finished with.

Only non-primitive data types can be added to weak sets.
Apart from these restrictions, weak sets behave in the same way as regular sets, and have the _has()_, _add()_, and _delete()_ methods that work in the same way.

### **Maps**

**Maps** were another data structure introduced in the ES6 specification.
They are a convenient way of keeping a list of key and value pairs, and are similar to 'hashes', or 'has tables' or 'dictionaries' in other programming languages.

\*Objects are limited to using strings for key values, whereas maps can use any data type as a key.

\*There is no efficient way to find the number of key-value pairs an object has, whereas this is easy to do with maps using the _size_ property.

\*Objects have methods that can be called and prototypes that can be used to create a chain of inheritance, whereas maps are solely focused on the storage and retrieval of key-value pairs.

\*The value of an object's properties can be accessed directly, whereas maps restrict you to using the _get()_ method to retrieve any values.

## Chapter 4 Functions

In JavaScript, functions are considered to be first-class objects.
This means they behave in the same way as all the other primitive data types and objects in the language.
They can be assigned to variables, stored in arrays and can even be returned by another functions.

A ninja programmer should always declare functions using function literals, function declarations or function expressions.

### **Return Values**

All functions return a value, which can be specified using the return statement, which comes after the _return_ keyword.
A function that doesn't explicitly return anything will return _undefined_ by default.

Arrow functions have a number of advantages over other ways of declaring functions:

- They are much less verbose than normal function declarations.

- Single parameters don't need putting into parentheses.

- The body of the function doesn't need placing inside a block if it's only one line.

- The _return_ keyword isn't required if the return statement is the only statement in the body of the function.

- They don't bind their own value of _this_ to the function.

Arrow functions make perfect candidates for short, anonymous functions.

### **Function Hoisting**

Hoisting is the JavaScript interpreter's action of moving all variable and function declarations to the top of the current scope, regardless of where they are defined.

### **Variable Hoisting**

Variable declarations that use the _var_ keyword are automatically moved to the top of the current scope.
Variable assignment is not hoisted.

A function expression is hoisted in a similar way to variables.

### **Callbacks**

A function that is passed as an argument to another is known as a callback.

## Chapter 5 Objects

An object in JavaScript is a self-contained set of related values and functions.
They act as a collection of named properties that map to any JavaScript value such as strings, numbers, booleans, arrays and functions.
If a property's value is a function, it is known as a method.

All objects are mutable at any time when a program is running.
This means that its properties and methods can be changed or removed, and new properties and methods can be added to the object, even if it was delcared using _const_.

ES6 provided a shorthand method of creating objects if a property key is the same as a variable name that the property value is assigned to.

Bracket notation has a few advantages to access object:

- it's the only way to access nonstandard property and method names that don't follow the variable naming rules.

- it also let you evaluate an expression and ust it as the property key.

If you try to access a property that doesn't exist, _undefined_ will be returned.

### **Computed Properties**

The ability to create objects with computed property keys was introduced in ES6.

Each symbol has a unique value, which means that using them as property keys avoids any naming clashes if you mistakenly use the same value for two different property keys.

### **Checking if Properties or Methods Exist**

- The _in_ operator can bed used to check whether an object has a particular property.

- Check to see if the property or method doesn't return _undefined_.

- To use the _hasOwnProperty()_ method.

### **Finding all the Properties of an Object**

The _Object.keys()_ method will return an array of all the keys of any object that is provided as an argument.

ES2017 also adds some the _Object.values()_ that works in the same way, but returns an array of all the object's value.

_Object.entries()_ is also part of ES2017 and returns an array of key-value pairs.
These key-value pairs are returned in arrays.

The keyword _this_ refers to the object that it is within.
It can be used inside methods to gain access to th object's properties.

### **Namespacing**

A solution is to use the **object literal pattern** to create a namespace for groups of related functions.
This is done by creating an object literal that serves as the namespace, then adding any values as properties of that object, and any functions as methods.

### **JSON**

JavaScript Object Notation, or JSON, was invented by Douglas Crockford in 2001.
It is an extremely popular lightweight data-storage format that is used by a large number of services for data serialization and configuration.

JSON is a string representation of the object literal notation that we have just seen.
There are, however, a couple of key differences:

- Property names must be double-quoted.

- Permitted values are double-quoted strings, numbers, true, false, null, arrays and objects.

- Functions are not permitted values.

### **The _RegExp_ Object**

A regular expression(or RegExp, for short) is a pattern that can be used to search strings for matches to the pattern.

Character Groups

Groups of characters can be placed together inside square brackets.
This character group represents any one of the characters inside the brackets.

A sequence of characters can also be represented by placing a dash [-] between the first and last characters.

If a \^ character is placed at the start of the sequence of characters with the brackets, it negates the sequence.

Regular Expression Properties

Regular expressions are objects, and have the following properties:

- The _global_ property makes the pattern return all matches. By default, the pattern only looks for the first occurrence of a match.

- The _ignoreCase_ property makes the pattern case-insensitive. By default, they are case sensitive.

- The _multiline_ property makes the pattern multiline. By default, a pattern will stop at the end of a line.

The following flags can be placed after a regular expression literal to change the default properties:

- **g** sets the _global_ property to true

- **i** sets the _ignoreCase_ property to true

- **m** sets the _multiline_ property to true

Special Characters

- **.** matches any character, except line breaks

- **\w** matches any word character, and is equivalent to **[A-Za-z0-9_]**

- **\W** matches any non-word character, and is equivalent to **[\^A-Za-z0-9_]**

- **\d** matches any digit character, and is equivalent to **[0-9]**

- **\D** matches any non-digit character, and is equivalent to **[\^0-9]**

- **\s** matches any whitespace character, and is equivalent to **[ \t\r\n\f]**

- **\S** matches any non-whitespace character, and is equivalent to **[^ \t\r\n\f]**

Modifiers

Modifiers can be placed after a token to deal with multiple occurrences of that token:

- **?** makes the preceding token in the regular expression optional

- _\*_ matches one or more occurrences of the preceding token.

- **+** matches one or more occurrences of the preceding token.

- **{n}** matches n occurrences of the preceding token.

- **{n,}** matches at least n occurrences of the pattern.

- **{,m}** matches at most m occurrences of the preceding token.

- **{n,m}** matches at least n and at most m occurrences of the preceding token.

- **^** marks the position immediately before the first character in the string.

- **\$** marks the position immediately after the last character in the string.

Greedy and Lazy Modifiers

All the modifiers above are **greedy**, which means they will match the longest possible string.
They can be made into **lazy** modifiers that match the shortest possible string by adding an extra '?' after the modifier.

## Chapter 6 The Document Object Model

The Document Object Model(DOM) allows you to access elements of a web page and enable interaction with the page by adding and removing elements, changing the order, content and attributes of elements, and even altering how they are styled.

All nodes have a numerical code to signify what type they are.

| Code |   Type    |
| ---- | :-------: |
| 1    |  element  |
| 2    | attribute |
| 3    |   text    |
| 4    |  comment  |
| 5    |   body    |

To stop any malicious content being added to a page using _*innerHTML*_, any code contained within _`<script>`_ tags is not executed.

## Chapter 7 Events

### **Stopping Default Behavior**

_`preventDefault()`_ is a method of the _event_ object that can be used inside the callback function to stop the default behavior happening.

### **Event Propagation**

Event propagation is the order that the events fire on each element. There are two forms of event propagation: bubbling and capturing.

Bubbling is when the event fires on the element clicked on first, then bubbles up the document tree, firing an event on each parent element until it reaches the root node.

Capturing starts by firing an event on the root element, then propagates downwards, firing an event on each child element until it reaches the target element that was clicked on.

The capturing model was originally implemented by Netscape and the bubbling model was implemented in Microsoft browsers.

`event.stopPropagation()` method will stop bubbling.

## Chapter 8 Forms

### **Forms**

Forms are made up of a _`<form>`_ element that contains form controls such as input fields, select menus and buttons.

### **Form Properties and Methods**

Form objects have a number of useful properties and methods that can be used to interact with the form.

- `form.submit()` method will submit the form automatically.
  Submitting a form using this method won't trigger the from _submit_ event.

- `form.reset()` method will reset all the form controls back to their initial values specified in the HTML.

- `form.action` property can be used to set the `action` attribute of a form, so it's sent to a different URL to be processed on the server.

### **Form Events**

- The `focus` event occurs when an element is focused on.

- The `blur` event occurs when the user moves the focus away from the form element.

- The `change` event occurs when the user moves the focus away from the form element after changing it.

### **Form Validation**

Form validation is the process of checking whether a user has entered the information into a form correctly.

Examples of the types of validation that occur include ensuring that:

- A required field is completed.

- An email address is valid.

- A number is entered when numerical data is required.

- A password is at least a minimum number of characters.

It is advisable to use both client-side and server-side validation.
JavaScript validation should be used to enhance the user experience when filling in a form by giving feedback about any errors before it's submitted.

## Chapter 9 The Window Object

### The Browser Object Model

The Browser Object Model(or BOM for short) is a collection of properties and methods that contain information about the browser and computer screen.

In browser environment, the global object is the _window_ object.

ES6 made `parseInt()` and `isNaN()` methods of the `Number` object.

### **Browser Information**

- The `window` object has a `navigator` property that returns a reference to the `Navigator` object.
  The `Navigator` object contains information about the browser being used.
  Its `userAgent` property will return information about the browser and operating system being used.
  Don't rely on this information though, as it can be modified by a user to masquerade as a different browser.

- The `window.location` property is an object that contains information about the URL of the current page.

- The `protocol` property returns a string describing the protocol used(such as `http`, `https`, `pop2`, `ftp` etc.).

- The `host` property returns a string describing the domain of the current URL and the port number.

- The `hostname` property returns a string describing the domain of the current URL.

- The `port` property returns a string describing the port number, although it will return an empty string if the port is not explicitly stated in the URL.

- The `pathname` property returns a string of the path that follows the domain.

- The `search` property returns a string that starts with a "?" followed by the query string parameters.
  It returns an empty string if there are no query string parameters.

- The `hash` property returns a string that starts with a "#" followed by the fragment identifier.
  It returns a empty string if there is no fragment identifier.

- The `origin` property returns a string that shows the protocol and domain where the current page originated from.
  This property is read-only.

The `window.location` object also has the following methods:

- The `reload()` method can be used to force a reload of the current page.
  If it's given a parameter of `true`, it will force the browser to reload the page fromt he server, instead of using a cached page.

- The `assign()` method can be used to load another resource from a URL provided as a parameter.

### **The Browser History**

The `window.history` property can be used to access information about any previously visited pages in the current browser session.

The `window.history.length` property shows how many pages have been visited before arriving at the current page.

The `window.history.go()` method can be used to go to a specific page, where 0 is the current page.

The `window.history.forward()` and `window.history.back()` method can be used to navigate forwards and backwards by one page respectively.

### **Controlling Windows**

The `window.open()` can be used to open a new window.

The `close()` method can be used to close a window.

The `window.moveTo()` method can be used to move a window. This takes two parameters that are the X and Y coordinates of the screen that the window is to be moved to.

The `window.resizeTo()` method can be used to resize a window.

### **Screen Information**

The `window.screen` object contains inforamtion about the screen the browser is displayed on.

The `availHeight` and `availWidth` can be used to find the height and width of the screen, excluding any operating system menus.

The `colorDepth` property can be used to find the color bit depth of the user's monitor.

The Screen object has more uses for mobile devices.
It also allows you to do things like turn off the device's screen, detect a change in its orientation or lock it in a specific orientation.

### **Cookies**

Cookies are small files that are saved locally on a user's computer.
They were invented by Netscape as a way of getting round HTTP being a stateless protocol.
This means that a browser does not remember anything from one request to another.
Cookies can be used to sidestep this problem by storing information that can then be retrieved between requests.

A restriction of cookies is that they can only be read by a web page from the same domain that set them.
This is to stop sites being able to access information about users, such as other sites they have visited.
Cookies are also limited to storing up to 4KB of data, although 20 cookies are allowed per domain, which can add up to quite a lot of data.

Cookies can be used for personlizing a user's browsing experience, storing user preferences, keeping track of user choices, authentication and tracking users.
Cookies are still useful for retaining state information(such as if a user is logged in) because they're passed between the client and server on every HTTP request.

Cookies take the form of a text file that contain a list of name/value pairs separated by semicolons.

- Creating Cookies

Use `document.cookie`

The `document.cookie` property acts like a special type of string.
Assigning another cookie to it won't overwrite the entire property, it will just append it to the end of the string.

- Changing Cookie Values

A cookie's value can be changed by reassigning it to `document.cookie` using the same name but a different value.

- Reading Cookies

enter `document.cookie`;

- Cookie Expiry Dates

Cookies are session cookies by default.
They are deleted once a browser session is finished(when the user closes the browser tab or window).
Cookies can be made persistent - that is, lasting beyond the browser session - by adding ";expires=date" to the end of the cookie when it's set, where `date` is a date value in the UTC String format `Day, DD-Mon-YYYY HH:MM:SS GMT`.
An alternative is to set the `max-age` value.

- The Path and Domain of Cookies

By default, cookies can only be read by pages inside the same directory and domain as the file was set.
This is for security reasons so that access to the cookie is limited.

The path can be changed so that any page in the root directory can read the cookie.
It's done by adding the string "; path=/" to the end of the cookie when it is set.

- Secure Cookies

Adding the string "; secure" to the end of a cookie will ensure it's only transmitted over a secure HTTPS network.

- Deleting Cookies

To remove a cookie, you need to set it to expire at a time in the past.

### **Timing Functions**

`setTimeout()`

The `window.setTimeout()` method accepts a callback to a function as its first parameter and a number of milliseconds as its second parameter.

The mehtod returns an integer. This is an ID used to reference taht particular timeout.

It can also cancel the timeout using the `window.clearTimeout()`.

`setInterval()`

The `window.setInterval()` method works in a similar way to `window.setTimeout()`, except that it will repeatedly invoke the callback function after every given number of milliseconds.

To stop this, we can use `window.clearInterval()` method.

### **Animation**

`requestAnimationFrame`

This method of the `window` object works in much the same way as the `window.setInterval()` method, although it has a number of improvements to optimize its performance.
This will return a unique ID that can be employed to stop the animation using the `window.cancelAnimationFrame()` method.

## Chapter 10 Testing and Debugging

### **Errors, Exceptions, and Warnings**

Errors are usually caused by one of the following:

- System error - there's a problem with the system or external devices with which the program is interacting.

- Programmer error - the program contains incorrect syntax or faulty logic; it could even be as simple as a typo.

- User error - the user has entered data incorrectly, which the program is unable to handle.

### **Exceptions**

An exception is an error that produces a return value that can then be used by the program to deal with the error.

### **Stack Traces**

An exception will also produce a stack trace.
This is a sequence of functions or method calls that lead to the point where the error occurred.

### **Warnings**

A warning can occur if there's an error in the code that isn't enough to cause the program to crash.

When a runtime error occurs in the browser, the HTML will still appear, but the JavaScript code will stop working in the background.
If the warning occurs, the JavaScript will continue to run.

### **The Importance of Testing and Debugging**

Strict Mode

Strict mode encourages a better quality of JavaScript to be written that befits a ninja programmer, so its use is recommended.

The recommended way to invoke strict mode is to place all your code into a self-invoking function.

ES6 introduced JavaScript modules.
These are self-contained pieces of code that in strict mode by default, so the `'use strict'` declaration is not required.

Feature Detection

The recommended way to determine browser support for a feature is to use feature detection.
This is done using an _if_ statement to check whether an object or method exists before trying to actually call the method.

Modernizr is a library that offers an easy way to implement feature detection and Can I Use? is another useful resource for checking which feature are currently supported in different browsers.

The "old-school" way of checking for browser support was known as **browser sniffing**.

Debugging in the Browser

The Trusty Alert

The most basic form of debugging is to use teh `alert()` method to show a dialog at certain points in the code.

Using the Console

It's not officially part of the ECMAScript specification, but is well supported in all the major browsers and Node.js.

The `console.trace()` method will log an interactive stack trace in the console.
This will show the functions that were called in the lead up to an exception occurring while the code is running.

Debugging Tools

Most modern browsers also have a debugging tool that allows you to set **breakpoints** in your code that will pause it at certain points.

One of the most useful commands is the _**debugger**_ keyword.

Error Objects

An `error` object can be created by the host environment when an exception occurs, or it can be created in the code using a constructor function.

There are 7 more error objects used for specific errors:

- _`EvalError`_ is not used in teh current ECMAScript specification and only retained for backwards compatibility.
  It was used to identify errors when using the global `eval()` function.

- _`RangeError`_ is thrown when a number is outside an allowable range of values.

- _`ReferenceError`_ is thrown when a reference is made to an item that doesn't exist.

- _`SyntaxError`_ is thrown when there's an error in the code's syntax.

- _`TypeError`_ is thrown when there's an error in the type of value used.

- _`URIError`_ is thrown when there's a problem encoding or decoding the URI.

- _`InternalError`_ is a non-standard error that is thrown when an error occurs in the JavaScript engine.
  A common cause of this too much recursion.

Throwing Exceptions

It's possible to throw your own exceptions using the `throw` statement.
It is best practice to throw an `error` object.
This can then be caught in a `catch` block.

Exception Handling

It is possible to handle exceptions gracefully by catching the error.
Any errors can be hidden from users, but still identified.

`try`, `catch`, and `finally`

The code inside the `catch` block will only run if an exception is thrown inside the `try` block.
The error object is automatically passed as a parameter to the `catch` block.
This allows us to query the error name, message and stack properties, and deal with it appropriately.
A `finally` block can be added after a `catch` block.
This will always be executed after the `try` or `catch` block, regardless of whether an exception occurred or not.
It is useful if you want some code to run in both cases.

Test-driven Development

**Test-driven development**(TDD) is the process of writing tests before any actual code.
Obviously these tests will initially fail, because there is no code to test.
The next step is to write some code to make the tests pass.
After this, the code is refactored to make it faster, more readable, and remove any repetition.

This process should be followed in small piecemeal chunks every time a new feature is implemented, resulting in the following workflow:

1. Write tests(that initially fail)

2. Write code to pass the tests

3. Refactor the code

4. Test refactored code

5. Write more tests for new features

This is often reffered to as the "red-green-refactor" cycle of TDD, as failing tests usually show up as red, and tests that pass show as green.

## Chapter 11 Further Functions

### **Function Properties and Methods**

The fact that functions are first-class objects means they can have properties and methods themselves.
All functions have a `length` property that returns the number of parameters the function has.

Call and Apply Methods

The `call()` method can be used to set the value of `this` inside a function to an object that is provided as the first argument.

The `apply()` method works in the same way, except the arguments of the function are provided as an array, even if there is only one argument.

Memorization

A useful feature of this is that it provides result caching, or **memoization**.
If a function takes some time to compute a return value, we can save the result in a `cache` property.

### **Immediately Invoked Function Expressions**

An anonymous function that is invoked as soon as it's defined.

IIFEs are a useful way of performing a task while keeping any variables wrapped up within the scope of the function.
This means the global namespace is not polluted with lots of variable names.

### **Temporary Variables**

Placing any code that uses the temporary variable inside an IIFE will ensure it's only available while the IIFE is invoked, then it will disappear.
This technique is not needed to swap the values of two variables in ES6, as destructuring can be used.

### **Initialization Code**

An IIFE can be used to set up any initialization code that there'll be no need for again.
An IIFE will be invoked once, and can set up any variables, objects and event handlers when the page loads.

### **Creating Self-contained Code Blocks**

An IIFE can be used to enclose a block of code inside its own private scope so it doesn't interfere with any other part of the program.
Using IIFEs in this way means code can be added or removed separately.

### **Functions that Define and Rewrite Themselves**

If any properties have previously been set on the function, these will be lost when the function redefines itself.

This is called the _Lazy Definition Pattern_ and is often when some initialization code is required the first time it's invoked.

### **Init-Time Branching**

This technique can be used with the feature detection to create functions that rewrite themselves, known as init-time branching.
This enables the functions to work more effectively in the browser, and avoid checking for features every time they're invoked.

This can be a useful pattern to initialize functions the first time they're called, optimizing them for the browser being used.

### **Recursive Functions**

A recursive function is one that invokes itself until a certain condition is met.
It's a useful tool to use when iterative processes are involved.

### **Callbacks**

They're functions passed to other functions as arguments and then invoked inside the function they are passed to.

Event-driven Asynchronous Programming

Callbacks can be used to facilitate event-driven asynchronous programming.
JavaScript is a single-threaded environment, which means only one piece of code will ever be processed at a time.
A callback can be created that's invoked when the event happens.
This means that the code is able to run out of order, or asynchronously.
By using callbacks, we ensure that waiting for these tasks to complete doesn't hold up the execution of other parts of the program.
Once the task has been completed, the callback will be invoked before returning to the rest of the program.

We would have expected the callback to have been invoked immediately, but a callback always has to wait for the current execution stack to complete before it's invoked.

### **Callback Hell**

Callback hell is the term used to refer to tangled mess of code, and it's such a common issue that it even has its own website!

Error-first Callbacks

In this coding pattern, callbacks have 2 arguments.
The first is the error argument, which is an error object provided if something goes wrong when completing the operation.
The second argument is any data returned by the operation that can be used in the body of the callback.

### **Promises**

A promise represents the future result of an asynchronous operation.
Promise don't do anything that can't already achieved using callbacks, but they help simplify the process, and avoid the convoluted code that can result from using multiple callbacks.

The Promise Life Cycle

When a promise is created, it calls an asynchronous operation and is then said to be _pending_.
It remains in this state while the operation is taking place.
At this stage, the promise is said to be _unsettled_.
Once the operation has completed, the promise is said to have been _settled_.
A settled promise can result in 2 different outcomes:

- Resolved - the asynchronous operation was completed successfully.

- Rejected - the asynchronous operation didn't work as expected, wasn't successfully completed or resulted in an error.

Both these outcomes will return any relevant data, and you can take the appropriate action based on the outcome of the promise.

Chaining Multiple Promises

Promises come into their own when multiple asynchronous tasks are required to be carried out one after the other.
If each function that performs an asynchronous operation returns a promise, we can chain the `then()` methods together to form a sequential piece of code that's easy to read.
Each promise will only begin once the previous promise has been settled.

Async Functions

Async functions are proceded by the `async` keyword and allow you to write asynchronous code as if it was synchronous.
This is achieved by using the `await` operator before an asynchronous function.
This will wrap the return value of the function in a promise that can then be assigned to a variable.
The next line of code is not executed until the promise is resolved.

Generalized Functions

Callbacks can be used to build more generalized functions.
Instead of having lots of specific functions, one function can be written that accepts a callback.

Functions That Return Functions

Functions can return a function.

Closures

Function Scope

A closure is a reference to a variable that was created inside the scope of another function, but is then kept alive and used in another part of the program.

One of the key principles in creating closures is that an 'inner' function, which is declared inside another function, has full access to all of the variables declared inside the scope of the function in which it's declared(the 'outer' function).
This means that whenever a function is defined inside another function, the inner function will have access to any variables that are declared in the ourt function's scope.

Generators

ES6 introduced support for generators. These are special functions used to produce iterators that maintain the state of a value.

To define a generator function, an asterisk symbol(_\*_) is placed after the function declaration.
Calling a generator function doesn't actually run any of the code in the function; it returns a _Generator_ object that can be used to create an iterator that implements a _next()_ method that returns a value every time the _next()_ method is called.

### **Functional Programming**

JavaScript has always supported functional-style programming due to functions being first-class objects.
The ability to pass functions as arguments, return them from other functions, and use anonymous functions and closures, are all fundamental elements of functional programming that JavaScript excels at.

Functional programming is a programming paradigm. Other examples of programming paradigms include object oriented programming and procedural programming.
JavaScript is a multi-paradigm language, meaning that it can be used to program in a variety of paradigms(and sometimes a mash-up of them!).
This flexibility is an attractive feature of the language, but it also makes it harder to adopt a particular coding style as the principles are not enforced by the language.

### **Pure Functions**

A key aspect of functional programming is its use of pure functions.
A pure function is a function that adheres to the following rules:

1. The return value of a pure function should only depend on the values provided as arguments.
   It doesn't rely on values from somewhere else in the program.

2. There are no side-effects.
   A pure function doesn't change any values or data elsewhere in the program.
   It only makes non-destructive data transformations and returns new values, rather than altering any of the underlying data.

3. Referential transparency.
   Given the same arguments, a pure function will always return the same result.

In order to follow these rules, any pure function must have:

- At least one argument; otherwise the return value must depend on something other than the arguments of the function, breaking the first rule.

- A return value; otherwise there's no point in the function(unless it has changed something else in the program - in which case, it's broken the 'no side-effec

Pure functions help to make functional programming code more concise and predictable than in other programming styles.
Referential transparency makes pure functions easy to test as they can be relied on to return the same values when the same arguments are provided.
Another benefit is that any return values can be cached, since they're always the same.
The absence of any side-effects tends to reduce the amounts of bugs that can creep into your code, because there are no surprise dependencies as they only rely on any values provided as arguments.

Functional progarmming uses pure functions as the building blocks of a program.
The functions perform a series of operations without changing the state of any data.
Each function forms an abstraction that should perform a single task, while encapsulating the details of its implementation inside the body of the function.
This means that a program becomes a sequence of expressions based on the return values of pure functions.
The emphasis is placed on using **function composition** to combine pure functions together to complete more complex tasks.

### **Higher-Order Functions**

Higher-order functions are functions that accept another function as an argument, or return another function as a result, or both.

Closure are used extensively in higher-order functions as they allow us to create a generic function that can be used to then return more specific functions based on its arguments.
This is done by creating a closure around a function's arguments that keeps them 'alive' in a return function.

When a higher-order function returns another function, we can use a neat trick to create an anonymous return function and immediately invoke it with a value instead by using double parentheses.
