# JavaScript_Specials
A summary of the JavaScript Special Chapter by Ilya Kantor

## Code Structure
Statements are delimited with a semicolon:
``` JavaScript
alert('Hello'); alert('World');
```

Usually, a line-break is also treated as a delimiter, so that would also work:
``` JavaScript
alert('Hello')
alert('World')
```
## Strict mode
To fully enable all features of modern JavaScript, we should start scripts with "use strict".
``` JavaScript
'use strict';
....
```
The directive must be at the top of a script or at the beginning of a function body.
Without "use strict", everything still works, but some features behave in the old-fashion, “compatible” way. 

## Variables

Can be declared using:

let
const (constant, can’t be changed)
var (old-style, will see later)
A variable name can include:

Letters and digits, but the first character may not be a digit.
Characters $ and _ are normal, on par with letters.
Non-Latin alphabets and hieroglyphs are also allowed, but commonly not used.
Variables are dynamically typed. They can store any value:
``` JavaScript
let x = 5;
x = "John";
```

There are 8 data types:

number for both floating-point and integer numbers,
bigint for integer numbers of arbitrary length,
string for strings,
boolean for logical values: true/false,
null – a type with a single value null, meaning “empty” or “does not exist”,
undefined – a type with a single value undefined, meaning “not assigned”,
object and symbol – for complex data structures and unique identifiers, we haven’t learnt them yet.

The typeof operator returns the type for a value, with two exceptions:
```JavaScript
typeof null == "object" // error in the language
typeof function(){} == "function" // functions are treated specially
```

## Interaction 
```JavaScript
prompt(question, [default])
```
Ask a question, and return either what the visitor entered or null if they clicked “cancel”.
```JavaScript
confirm(question)
```
Ask a question and suggest to choose between Ok and Cancel. The choice is returned as true/false.
```JavaScript
alert(message)
```
Output a message.

All these functions are modal, they pause the code execution and prevent the visitor from interacting with the page until they answer.

```JavaScript
let userName = prompt("Your name?", "Alice");
let isTeaWanted = confirm("Do you want some tea?");

alert( "Visitor: " + userName ); // Alice
alert( "Tea wanted: " + isTeaWanted ); // true
```
## Operators
JavaScript supports the following operators:
### Arithmetical
Regular: ``* + - /``, also ``%`` for the remainder and ``**`` for power of a number.

The binary plus ``+`` concatenates strings. And if any of the operands is a string, the other one is converted to string too:
```JavaScript
alert( '1' + 2 ); // '12', string
alert( 1 + '2' ); // '12', string
```
### Assignments
There is a simple assignment: ``a = b`` and combined ones like ``a *= 2``.

### Bitwise
Bitwise operators work with 32-bit integers at the lowest, bit-level: see the docs when they are needed.

### Conditional
The only operator with three parameters: ```JavaScript cond ? resultA : resultB```. If cond is truthy, returns resultA, otherwise resultB.

### Logical operators
Logical AND && and OR || perform short-circuit evaluation and then return the value where it stopped (not necessary true/false). Logical NOT ! converts the operand to boolean type and returns the inverse value.

### Nullish coalescing operator
The ?? operator provides a way to choose a defined value from a list of variables. The result of a ?? b is a unless it’s null/undefined, then b.



