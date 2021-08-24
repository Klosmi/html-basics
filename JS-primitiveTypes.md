# **[JS: Primitive Types](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)**

- basic building blocks, basic types of information that we can store.

<br>

- [**number**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#number)
- [**boolean**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#boolean-)
- [**string**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#string-)
- **null**
- **undefined**
- symbol
- BigInt

<br>

#### [**REPL**](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) : read → evaluate → print → loop

<br>

## **[Number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)**

- only **1** type of number exists in JS, this can be:
  - positive and negative numbers
  - whole number (intigers)
  - decimal numbers

<br>

- [**math operations**](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math#arithmetic_operators) :   
  arithmetic operators are the basic operators that we use to do sums in JavaScript:
  - __\+__  Addition
  - __\-__  Subtraction
  - __\*__  Multiplication
  - __\/__  Division
  - __\%__  Modulo or Remainder *(8 % 3 → returns 2)*
  - __\**__ Exponent *(5 ** 2 → 25)*

<br>

  > **PEMDAS** (order of operations):  
     **P**arentheses first   
     **E**xponents (ie Powers and Square Roots, etc.)   
     **M**ultiplication and    
     **D**ivision    
     **A**ddition and   
     **S**ubtraction    

<br>

 - [**NaN**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/NaN) (Not A Number):   
  it is considered a numeric value (number), but it represents something that is not a number.

    - 0/0 → NaN *(because it's impossible to assign a value to it, 0 / 0 is meaningless)*
    - 1 + NaN → NaN

<br>

  **[typeof](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof)** :    
  the typeof operator returns a string indicating the type of the unevaluated operand.
  - eg.:
     ```
     typeof 4 //"number"

     typeof NaN //"number"
     ```
  
  <br>

  - [__assignment operators__](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#assignment_operators)

    - [__`+=`__ (addition assignment)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Addition_assignment) 
    eg.:
      ```
      x += y    // x = x + y
      ```
      __++__  →  increments by `1` 
        eg.:
        ```
        let x = 1
        x++   // x = x + 1
        ```

    - [__`-=`__ (subtraction assignment)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Subtraction_assignment)    
    eg.:
      ```
      x -= y    // x = x - y
      ```
      __--__  →  decremnts by `1` 
        eg.:
        ```
        let x = 1
        x--   // x = x - 1
        ```

    - [__`*=`__ (multiplication assignment)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Multiplication_assignment)

    - [__`/=`__ (division assignment)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Division_assignment)

    - [__`%=`__ (remainder assignment)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Remainder_assignment)

    - [__`**=`__ (exponentiation assignment)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Exponentiation_assignment)

<br>

## **[Boolean](https://developer.mozilla.org/en-US/docs/Glossary/Boolean)** :   
There are two options for a __boolean value__, `true` or `false`.

- booleans are to store yes or no values (true or false value)

- eg.:
  ```
  let isLoggedIn = true;
  let gameOver = false;
  const skyIsBlue = true;
  ```

<br>

## [String](https://developer.mozilla.org/en-US/docs/Glossary/string) :   
  A string is textural information, *a string of characters.*

  - represent text
  - `"must be wrapped in quotes"`.        
  `"double"` or `'single'` quotes, both work, but be consistent with them. Except a quote in a string, like:    
  `'The dog said "Hello master!"'`

    - eg.:
      ```
      let name = "Jane Doe";    // it's a string
      let numberString = "42";  // it's a string
      let emptyString = ""      // it's a string (an empty string)
      ```

- **[index](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods#retrieving_a_specific_string_character)** :

  - strings are indexed. So each character has a corresponding index __(a positional number)__.   
  In other words:   
  **every character in a string has a corresponding number associated with it**. It is a positional number, **starting from `0`**.

  - `[]` square brackets with number `[0]`, this is the 1st index of the character.   

    eg.: the second character of the word *'dog'*
      ```
      let animal = "dog"
      animal[1]           // "o"

      animal[42]         // undifenied
      ```

- **[length](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods#finding_the_length_of_a_string)** property :    
  the `length` property of a string object contains the length of the string.   
  **It gives the number of characters.**
    - chain on `.length`   
    eg.:
      ```
      let animal = "dog";
      animal.length;    // 3 characters
      ```
  
 - __concatenation__ :    
   concatenating together strings to get a new string.   
    eg.:
    ```
    "hello" + "hello";   //"hellohello"    
    ```
    eg.:
    ```
    let greeting = "Hello";
    let user =  "Gamer";

    welcome + user;  //HelloGamer

    //or add a space between

    let helloUser = greeting + " " + user;  //Hello Gamer
    ```
- **you can't change a string❗️**
    eg.: the `let name = 'John';` with capital __J__. If I make the __J__ lowercase __j__, it will be a new string. They take a different place in the memory.
    ```
    let name = 'John'; // place in the memory A
    name = 'john';     // place in the memory B
    ```

- **[type coercion](https://developer.mozilla.org/en-US/docs/Glossary/Type_coercion)**:   
  you can add `number` to a string: because JavaScript tries and coerce different types to a common type.
  It makes the number string, because the other way around would not work (makes the string into number?).

a common type. 
  eg.:
  ```
  let result = 1 + "hello";  //"1hello"
  ```
---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
