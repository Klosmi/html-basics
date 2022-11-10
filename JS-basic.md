__[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)__

---

# **[JS: Primitive Types](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)**

- basic building blocks, basic types of information that we can store.

<br>

- [**number**](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#number)
- [**boolean**](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#boolean-)
- [**string**](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#string-)
- [**null**](https://github.com/Klosmi/html-basics/blob/master/JS-basic.mdd#null-)
- [**undefined**](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#undefined)
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
   concatenating together strings to get a new string. Smushes two strings together (without space).   
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
<br>

## **[Null](https://developer.mozilla.org/en-US/docs/Glossary/Null)** :
- Intentional absence, lack of any value.   
- Must be assigned
- eg.:
  *For a logged in user, we initially set it to 0*
  ```
  let loggedInUser =  null;   // explicitly indicitas there's nothing there
  ```

<br>

## **[Undefined](https://developer.mozilla.org/en-US/docs/Glossary/undefined)**
- Variables that do not have an assigned value.
- eg.:   
  *I don't give a value to a variable*
  ``` 
    let variable;   // undifenied = it is not defined
  ```

<br>

__The difference between null and undifined__:   
  - **null** is what you set explicitly.    
  - **undefined** is what you run into (accidentally) because that something is *not defined*

<br>

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---

# **[JS: Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#declarations)**
  - varables are like __labels for values__:
    - we can store a value and give it a name so that we can:
      - refer back to it later
      - use that value to do things
      - change it laters

<br>

 To define a variable, we should use let, const, or var (though var isn't recommended these days anymore).      
 **We only use those keywords when first declaring the variable (the first time we tell javaScript it exists).**     
 *For example:      
      <br>
      `let numberOfEggs = 12;`    
  Then if we want to change the value of a variable, we reference the variable name WITHOUT let/const/var like:    
  <br>  
   `numberOfEggs = 10;`   
  It is possible defining a variable without let/const/var in JavaScript, but you should never do it. JS will treat your variable as a global variable*.  
  
- **basic syntax**:   
  -  #### [**let**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)  :    
    let statement declares a block-scoped local variable, optionally initializing it to a value.

    <br>

    -  **let** year = 2021;   
        eg.:
        ```
        let numChickens = 4;
        let numRoosters = 1;

        let totalChickens = numChickens + numRoosters   //5;
        ```

  <br>
  
  -  #### [**const**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)  :    
    `const` works like let __except__ you cannot change the value! They **cannot be reassigned**.
    We use `const` to store things we know that will not change.

    <br>

    -  **const** num = 7;   
        eg.:
        ```
        let num = 7;
        num = 20;   // ERROR!

        const days= 30;
        days = days + 1 //TypeError: Assignment to constant variable.
        ```

  <br>
    
  -  #### [**var**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)  :    
    it's the __old__ variable keyword. We don't use it anymore (although it still works).

    <br>

- **Variables can CHANGE TYPES**
    - in the "regular" JS variables can chage types, but in TypeScript (a fancier JS) it cannot change types (it has to remain).   
    - eg.:
    *we can change a numeric variable to a boolean.*   
      ```
      let numPeople = 42;    // Number
      numPeople = false;    //Changed to boolean
      numPeople = 99;      //Back to number    
      ```

<br>

- **[Variable naming conventions](https://developer.mozilla.org/en-US/docs/Glossary/Identifier)**: 
  - __rules__:
    - can't start with numbers
    - can't contain space
    - camelCase : `let daysOfTheYear = 365;`s

  - __best practice__:
    - start with a lowercase letter (although uppercase works, but don't do that)
    - it can start with an `_` (underscore) : `let _age_ = 10;`, but no usually used.
    - the name should represent what it contians (meaningful names).
    - generally avoid 1 letter variables.
    - for booleans is a good practice to start the nameing with `is`.    
    Like `let isGameOver = false;`
    
    <br>
  
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---

# **[JS: Methods](https://developer.mozilla.org/en-US/docs/Glossary/Method)** ([string](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#string-) methods):
  - __methods__ are built-in __ACTIONS__ that we can perform with individual __strings__.   

  - __every string has a set of methods__
  - every string can do the same thing as another string:    
  eg.:   
  the *"hello" string* can do the same as the *"goodbye" string*    
  - methods help to: search within a string
  - methods help to: replace part of a string
  - methods help to: chane the casing of a string
  - etc.

  - __the syntax:__   
    - `thing.method()`;   
    eg.:
      ```
      const message = "Hello, it is a nice day!";
      const bigMessage = message.toUpperCase(); // "HELLO, IT IS A NICE DAY!"
      ```
<br>

  - another, more __[general definition of methods](https://en.wikipedia.org/wiki/Method_(computer_programming))__:   
  __Data is represented as properties__ of the object, and __behaviors are represented as methods__. For example, a Window object could have __methods such as open and close__, while __its state__ (whether it is open or closed at any given point in time) would be __a property__.

<br>

 - __[list of string methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#)__

    - [thing.toUpperCase()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)
    - [thing.toLowerCase()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)
    - [thing.trim()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/Trim):   
    eg.:   
    *trim a space beginning of a string*
      ``` 
      const input = "    Hi, my name is...";
      input.trim()    // "Hi, my name is ..."
      ```
    - [thing.indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf) :     
    __first occurrence__ of the specified value
    - [thing.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice) :    
    it extracts a portion of a string and returns it as a new string, __without modifying the original string__   
    eg.:   
    *pass in a begin index and an optional end index*
    ```
      const joke = "I love this joke!";
      joke.slice(2, 11);   // "love this"
      joke;                // "I love this joke!" → So the original variable is unchaged
    ```
    - [thing.replace](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replace) :   
    pass in two arguments: the first is what want to replace, the second is what we want to replace it with.
    eg.:
       ```
      const joke = "I love this joke!";
      joke.replace("love", "hate");     // "I hate this joke!" 
      joke;                // "I love this joke!" → So the original variable is unchaged  
      ```
    - [thing.replaceAll()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/replaceAll) :   
    returns a new string with all matches of a pattern replaced by a replacement.   
    eg.:
      ```
      let pangram = "The quick brown fox jumps over the lazy dog. If the dog reacted, was it really lazy?";
      pangram.replaceAll("dog", "monkey");    // "The quick brown fox jumps over the lazy monkey. If the monkey reacted, was it really lazy?"
      ```
    - [thing.repeat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) :    
    it constructs and returns a new string which contains the specified number of copies (repeats) of the string on which it was called.

    - [thing.concat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/concat)

<br>

  - **chain methods:**
    `thing.toUpperCase().trim();` → *makes the string uppercase and trim the space from the beginning or the end.*

 ## [arguments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments) :
  arguments are __inputs that we can pass into the method to modify how they behave__.   
  - __thing.method(arg)__

  - we pass arguments inside of the parentheses `(value)`   
  eg.:   
  *pass the argument into the `indexOf()` method*
    ```
    const animal = "tigerwolf";
    animal.indexOf("tiger");  // 0 → tiger start at index 0
    animal.indexOf("wolf");   // 5
    animal.indexOf("x");      // -1 → because it is not found
    ```

<br>

- 💡 the difference between __method__ and __property__:
    - property has no `()` after. Eg.: `"hello".length";`

    - method has `()` after. Eg.: `thing.toUppercase();`

    - __properties are like nouns__ where __methods are like verbs__    
    __methods perform a function__   

    - __properties can't perform an action__   

    - __the only value that a method has is the one that is returned after it finishes performing the action__ 
    - __method is just an action we can call upon later__

<br>

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---


# [__JS: Template literals__ (Template strings)](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)
  Template literals are strings that allow embedded expressions, which will be evaluated and then turned into a resulting string.    

  In other words: template literals allow us to create strings where we can embed an expression inside the string and that expression will be evaluated and turned into a string.


  - kindof replaces concatenation.
  - using back-ticks __\` \`__ and __$__ and curlybraces __{}__ 👉
      __\`String ${expression to evaluate}\`__


  - eg.:      
    *Instead of this long concatenation:*
      ```
      let blackSheep = 3;
      let whiteSheep = 4;

        "I counted " + blackSheep + whiteSheep    // "I counted 7 sheep."
      ```
    *I can write this. Where:*    
    **`${3 + 4}` will be evaluated and replace with a string.**
      ```
        `I counted ${3 + 4} sheep.`;   // "I counted 7 sheep."
      ```                                         
  - another example:   
    *concatenation*
    ```
    let product = "pizza";
    let amount = 3;
    let price = 10;

    "I ordered " + amount + " " + product + "s" + for + price*amount + "€"."   // "I ordered 3 pizzas for 30€."
    ```
    *temaplate literals*
    ```
    let product = "pizza";
    let amount = 3;
    let price = 10;

    `I ordered ${amount} ${pizza}s for ${price*amount}€.` // "I ordered 3 pizzas for 30€."
    ```

<br>

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---


# **[JS: Math Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)**

- **contains properties and methods for mathematical constants and functions.** (It’s not a function object.)

- (an object is a collection of properties and methods.)

- Math's [properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math#static_properties) and [methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math#static_methods) :

  (here below these are mainly methods):

    - [`Math.PI`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/PI) → 3.141592653589793

    - [`Math.round(3.7)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/round)  → 4

    - [`Math.abs(-434)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/abs) → 434

    - [`Math.pow(2,4)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/pow)  → 16

    - [`Math.floor(3.999)`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)  → 3

    - [**Random Numbers** 👉 `Math.random()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)
      - built in method
      - gives a random decimal between 0 and 1 (non-inclusive)
      - eg.:
        ```
        Math.random() // 0.02169928868605231
        Math.random() // 0.17593062488380706
        Math.random() // 0.07464813343445598
        ```
      - how to get a random number to get __integers__?
        -   a multy step process
        - eg.:    
        **a random number between 1 - 10**
        ```
        const step1 = Math.random();      // 0.252811726254621
        
        const step2 = step1 * 10;         // 2.52811726254621
        
        const step3 = Math.floor(step2);  // 2
        
        // because it starts from 0, I add 1
        const step4 = step3 + 1;          // 3 

        // in 1 line:
        Math.floor(Math.random() * 10) + 1;
        ```

  <br>  
  
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---


# **[JS: Comparison Operators](http://www-lia.deis.unibo.it/materiale/JS/developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators.html)**
**comparing two values: the left and the right.**
 - **booleans**: it can be true or false
 - we can compare letters (their value based on their [Unicode](https://unicode-table.com/en/))

 - **`>`**   greater than    
   **`<`**   less than   
   **`>=`**  greater than or equal to   
   **`<=`**  less than or equal to   
   **`==`**  equality  
   **`!=`**  non equality   
   **`===`** strict equality   
   **`!==`** strict non-equality   

- **`>`**   
  - eg.:    
    comparing the left to the right value → *boolean*
    ```
    1 > 3;       // false  
    1 < 3;       // true
    -1 < -1;     // false
    'a' > 'A';   // true
    '@' > 'a';   // false because unicode U+0040 > U+0061
    ```
- **`>=`**  greater than or equal to 
  - eg.:    
    comparing the left to the right value → *boolean*
    ```
    1 >= 3;      // false  
    1 <= 10;    // true 
    -1 =< -1;   // true 
    'a' >= 'b';  // false
    ```

- **`==`** double equals
  - checks for equality of value, but not equality of type.

  - it coerces both values to the same type and then compares them, it can lead to unexpected results!

  - so it does not care about type❗️
  
  - eg.:
    ```
    1 == 1;   // true
    ```
    But
    ```
    // It doesn't care about the type:

    1 == '1';           // true
    'c' == 'b';         // false
    0 == '';            // true  
    true == false;      // false 
    0 == false;         // true
    null == undefined;  // true    
    ```
    *So, it converts them to the same type and then compares!*

- **`===`** strict equality or tripple equals
  - checks for equality of __value and type__, so it cares about type!

  - always use tripple equals when you're comparing things to see if they're equal. 

    - eg.:
      ```
      1 === '1';          // false
      0 == false;         // false
      
      ```
      
<br>

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---


# [The `console.` method](https://developer.mozilla.org/en-US/docs/Web/API/console)

  - all the [`console` methods](https://developer.mozilla.org/en-US/docs/Web/API/console#methods)

  - eg.:
    ```
    console.log("Hello!");`
    ```
     __prints__ out "Hello!" to the console. 

<br> 

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---

# [The `alert()` method](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics#functions)  
  - print out, but in a pop-up window (not in the console)
  - shows a message
  - eg.:
    ```
    alert("Hey!");
    ```
<br>

# [The `prompt`](https://javascript.info/alert-prompt-confirm#prompt)
  - shows a message asking the user to input text. It returns the text or, if Cancel button or Esc is clicked, null.

  - it's useful for `input`s

  - it gives us a string

  - eg.:
    ```
    prompt("please enter a number");
    ```
<br>

---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
   


# **[JS: Conditional statement - if • else if • else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)**
- the code is either true or false

- the condition between the `{ }` runs, executes only of the condition (`if (something === something)`) is true

#### `if` statement

- eg.:
  ```
  let rating = 3;

  if (rating === 3) {
    console.log("You are my hero!")'
  }
  ```

- if the code is false, it does not run, but what is before and after will still run.
  - eg.:
    the app.js file
    ```
    console.log("Before the conditional")   // runs
      
      if (1 + 1 === 3) {
        console.log("In the condition");    // doesn't run
      }

      console.log("After the conditional")  // runs
    ```

<br>

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---

#### `if` + `else if` statement

basically it is: if the `if` part is false, than *otherwise*.

- you can chain them together, so you can have as many `else if` as you need.

- eg.:
  ```
  let rating = 2;

  if (rating === 3) {
    console.log("Hi!");
  }
  else if (rating === 2) {
    console.log("Bye!");
  }
  ```

- eg.:   
  if one of the condition is true, it runs and the rest will be skipped. 
  ```
  const age = 8;

  if (age > 5) {
    console.log("Free");   // this line runs because it's true , it doesn't go to the else if line
  } else if (age > 13 ){
    console.log("5$");
  } else if (age < 65 ){
    console.log("5$");
  }
  ```

<br>

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---

#### `else` statement

basically it is the `everything else`.   

It's the last piece of the entire conditional,  we don't specify any condition (we don't have parentheses).   
It's going to run as **the last thing** if nothing else matched first (always the last statement).


 eg.:
 ```
  const days = prompt("enter a day!");

  if (days === 'Monday') { 
    console.log("1st day of the week");
  } else if (days === 'Tuesday') {
  console.log("2md day of the week"); 
  } else if (days === 'Wednesday') {
  console.log("3rd day of the week"); 
  } else if (days === 'Thursday') {
  console.log("4th day of the week");
  } else if (days === 'Friday') {
  console.log("5th day of the week");
  } else  {
  console.log("who cares, it's weekend");
  }
```

#### Nesting conditionals

- eg.:
  ```
  const password = prompt("please enter a new password");

  //password must be 5 characters
  if (password.length >= 5) {
      // password not inlcude space
      // this is the nested part
      if (password.indexOf(" ") === -1) {
        console.log("super");
      } else {
        console.log("please don't use spaces")
      }
  } else {
    console.log("password too short");
  }
  ```
  
  
<br>  

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---
  
# [`switch` statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch) 

it is another control flow statement, it can replace several statements.

- not used often, but still.

- keyword: __`swittch`__ and __`case`__ and __`break`__ and __`default`__*(it works like the `else`)*

- `switch` works like  whenever there is a match, the `switch` starts executing the code until it hits a `break`.   
`default`: if nothing else matched.

- eg.:
    ```
    const day = prompt("Enter a number");

    switch(day) {
      case 1:
        console.log('Monday');
        break;
      case 2: 
        console.log("Tuesday");
        break;
      case 3: 
        console.log("Wednesday");
        break;
      case 4: 
        console.log("Thursday");
        break;
      case 5: 
        console.log("Friday");
        break;
      case 6:
      case 7:   
        console.log("Weekend");
        break;
      default:
        console.log("Something like weekend!!!!");
    }
    ```
  
 <br>
 
[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---
  
  
# **[Truthy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy)** and **[Falsy](https://developer.mozilla.org/en-US/docs/Glossary/Falsy)** values

A truthy value is a value that is considered true when encountered in a Boolean context.   
**All values are truthy unless they are defined as falsy** (i.e., except for false, 0, -0, 0n, "", null, undefined, and NaN).

- Falsy values:
  - false
  - 0
  - "" (empty string)
  - null
  - undefined
  - NaN

- Everything else is truthy!

- eg.:   
  Truthy   
  since everything is truthy except when falsy, when you write something to the input, is going to be true.
  ```
  const userInput = prompt("Enter smthing");

  if (userInput) {
    console.log("Truthy!");
  } else {
    console.log("Falsy");
  }
  ```

- eg.:   
  Falsy
  ```
  if (0) {  // null, NaN, undefined also Falsy
    console.log("Truthy!");
  } else {
    console.log("Falsy");
  }
  ```
 
<br> 

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---

# [Logical operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators#binary_logical_operators) 

#### **[AND `&&`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_AND)**

- __join__ an expression on the left and an expression on the right
- `&&`
- true is when the *left* && *right* is true (so the whole thing is true).

  - true  &&  true  = true
  - true  &&  false = false
  - false &&  true  = false
  - false &&  false = false   

<br>

- eg.:   
  && true
  ```
  1 < 4  && 1 === 1;    // true
  ```

- eg.:
  *A password checker. The password has to be greater than 10 characters, long or equal to and does not contain any space.*
  ```
  const password = prompt("Enter pw");

  if (password.length >= 10 && password.indexOf(' ') === -1)  {
    console.log("Valid password");
  } else {
    console.log("Wrong password");
  }
  ```
#### **[OR `||`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_OR)**

- true if either the left or the right is true or both are true. So when 1 side is true, its all true.
- `||`  (pipe character)
  - true  &&  true  = true
  - true  &&  false = true
  - false &&  true  = true
  - false &&  false = false   

<br>

- eg.:   
  || true
  ```
  1 === 1 || 2 > 7  // true
  ```

<br>

__The order:__   
-  `&&` __runs first__ always, so `&&` is before than the `||`❗️

<br>

`&&` and `||` together
- eg.:
  ```
  const age = prompt("Enter your age");

  if (age >= 0 && age < 5 || age >= 65) {
    console.log("free");
  } else if (age >= 5 && age < 10) {
    console.log("$10");
  } else if (age >= 10 && age < 65) {
    console.log("$20");
  } else {
    console.log("there's no age like that");
  }
  ```

#### **[NOT `!`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Logical_NOT)**

- `!`expression returns true if expression is false

- `!` (bang)

- it negates the value, so if something is false, than it turns to true.

- eg.:
  False
  ```
  !('a' === 'a');  // false

  !null   // true, because null is inherently false
  ```

- eg.:
  *When you don't give a name it's false*
  ```
  const name = prompt("Enter your name");

  if (!name) {
    console.log('ooops');        
    name = prompt("Write it again");
  } else {
    console.log('Hi');
  }
  ```
  
<br>

---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)


# [Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) :
 it's a data structure. (A data structure is a collection of data.)
 - Arrays allow us to group data together  
 - A __collection of values__, and an __ordered collection of values__

 - `let variable = [first, second, third];` *(ordered values from left to right)*

 - arrays are indexed  *(starts from 0)*, so every element has an associated number.
    - eg.:
      ```
      let days = ["Monday", "Tuesday", "Wednesday"];

      days[1];    // Tuesday
      ```

 #### **array indexes**

- we can chain the indexes:
  - eg.:   
    To get the letter `y` of Monday
    ```
    let days = ["Monday", "Tuesday", "Wednesday"];

    days[0][5]      //  y
    ```

- update an array
  - eg.:
    ```
      let days = ["Monday", "Tuesday", "Wednesday"];

      days.length;    // 3

      days[3] = "Thursday";

      // The outcome:
      // let days = ["Monday", "Tuesday", "Wednesday", "Thursday"];
    ```

#### __[array methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#common_operations)__

- __[`push()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)__    
  add an element to the end of the array
  - `something.push("item")`  *in the parenthesis we add what we push*
  - eg.:
    ```
    let letters = ["a", "b", "c"];

    letters.push("d");

    // the result:
    //letters = ["a", "b", "c", "d"];
    ```
  - the new length of the array (so the array has changed)

  - we can push multiple things on an array
    ```
    let letters = ["a", "b", "c", "d"];

    letters.push("e", "f");

    // the result:
    //letters = ["a", "b", "c", "d", "e", "f"];
    ```

<br>

- __[`pop()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)__    
  remove an element from the end of the array
  - `something.pop()` *it does not require any argument, the parenthesis stays empty*
  - it gives element to us and it removes it from the array 
    - eg.:
      ```
      let letters = ["a", "b", "c"];

      letters.pop();
      "c"     // it gives the "c" and removes it from the array

      // the result:
      //letters = ["a", "b"];
      ```

  - I can capture the removed element into a variable
    - eg.:   
        *remove from the `letters = ["a", "b", "c"];` array the last element and give it to a `newVariable`.*
        ```
        let newVariable = letters.pop();

        // the result is that the new variable has the "c"
        // newVariable = "c"
        ```
  - stack (add in the end and remove from the end)

<br>

- __[`shift()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)__
  - removes from the beginning (yes, not the unshift removes, but the shift!)

    - eg.:
      ```
      let letters = ["a", "b", "c"];

      letters.shift();

      // returns:
      // "a"
      ```
  - we can save it to a variable
    - eg.:
      ```
      let letters = ["a", "b", "c"];

      let newVariable = letters.shift();

      // returns:
      // newVariable = "a"
      ```

<br>

- __[`unshift()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)__   
  with this method we can **add** a new element to the beginning of an array.

  - eg.:   
    *in the `()` we write the element that we want to add to the beginning of the array.* 
    ```
    let letters = ["a", "b", "c"];

    letters.unshift("Z");   // element what we add!

    // returns:
    // ["Z", "a", "b", "c"]
    ```

<br>

- __[`concat()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)__    
 it is used to **merge arrays**. 
 It concatenates arrays and gives a **new** array.

  - We call `concat()` on one of the arrays and then we pass in a second array to concatenate with that initial array. That creates a new third array.
    - eg.:
      ```
      let arrayA = ['a', 'b', 'c'];
      let arrayB = ['d', 'e', 'f'];
      let arrayAB = arrayA.concat(arrayB);

      // returns:
      // arrayAB = ["a", "b", "c", "d", "e", "f"]
      ```

<br>

- __[`includes()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes)__ 
  returns **true or false**. It tel us if an array includes a certain value.

  - eg.:   
    *does `arrayA` includes `'b'` ?*
    ```
    let arrayA = ['a', 'b', 'c'];
    arrayA.includes('b');

    // returns:
    // true
    ```

<br>

- __[`indexOf()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)__ 
   returns the **first index** at which a given element can be found in the array. 

   - it shows us the **first time** that element occurs

   -  when element is not found, it gives `-1`


     - eg.:   
    *what is the index of `'b'` in the `arrayA` ?*
    ```
    let arrayA = ['a', 'b', 'c', 'b'];
    arrayA.indexOf('b');

    // it only gives the first match❗️
    // returns:
    // 1
    ```

    - eg.:
    *what is the index of `'Y'` in the `arrayA` ?*   
    *When element is not found, it gives `-1`*
    ```
    let arrayA = ['a', 'b', 'c'];
    arrayA.indexOf('Y');

    // returns:
    // -1
    ```
    
<br>

- __[`reverse()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reverse)__ 
   it **reverses an array**, it does it in *place*.    
   It means it is a **destructive method**: it changes the original array❗️

   - use it with empty parentheses

    - eg.:   
      ```
      let arrayA = ['a', 'b', 'c'];
      arrayA.reverse();

      // it overwrites the original array:
      // console.log(`arrayA`);
      // arrayA = ['c', 'b', 'a'];
      ```
  
<br>

- __[`slice()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)__ 
  it gives a **copy** of a portion of an array, a **slice of an array**.

  - the original array will not be modified. 

  - the array object is selected from *start* to *end*, where start and end represent the index of items in that array.

  - start and end are optional. If I don't specify them (leaving the parenthesis empty) it gives a copy of the whole array.
    - eg.:
      ```
      let letters = ['a','b','c','d','e','f'];
      letters.slice()

      // returns the copy of the whole array
      // ['a','b','c','d','e','f']
      ```

  - start is inlcuded, the end is not included, it just goes *upto* the index.

    - eg.:
      ```
      let letters = ['a','b','c','d','e','f'];
      letters.slice(2, 4)      // goes from the index of 2 upto 4 (not inlcuding the end indeox of 4❗️)
  

      // returns:
      // ['c', 'd']
      ```
 

  - eg.:   
      *only specified the start index*   
      Array with 6 elements, and I want the first 3.
      ```
      let letters = ['a','b','c','d','e','f'];
      letters.slice(3)      // goes from the index of 3

      // returns:
      // ['d', 'e', 'f']
      ```

  - giving a negative index, it starts from the end of the array
    - eg.:
      ```
      let letters = ['a','b','c','d','e','f'];
      letters.slice(-3)      // start from the end of the array

      // result: it gives the last 3 elements
      // ['d','e','f']
      ```
  
<br>

- __[`splice()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)__    
  it changes the contents of an array by **removing or replacing** existing elements and/or adding new elements in place.    
  (Destructive method, doesn't make a copy.)

  - splice is sort of *joining* something to something else.

  - we have to specify:   
    - where to start   
    -  how many things to delete   
    - optionally, what to insert

  - eg.:   
    *delete the 'blue'*
    ```
    let colors = ['red', 'green', 'blue', 'yellow', 'purple', 'pink'];

    colors.splice(2, 1);
    
    // result: 
    // output: ['red', 'green', 'yellow', 'purple', 'pink']

    ```

  - eg.:   
    *insert 'magenta' between 'purple' and 'pink'*
    ```
    let colors = ['red', 'green', 'yellow', 'purple', 'pink'];

    colors.splice(4,0,'magenta')    
    
    //0 means delete nothing. I want to insert 'magenta' after the 4rd index

    //result:
    // ['red', 'green', 'yellow', 'purple', 'magenta', 'pink']
    ```

💡 Usually it is not efficient to update the middle of an array, rather try to update the end of an array if it is possible.

<br>


- __[`sort()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)__    
   it **sorts the elements** of an array in place and returns the sorted array.

   - destructive method

   - the default sort order is ascending❗️   
    But, it is built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values. 



   - eg.:
      * we expect that it will sort ascending, but becuase it uses the 1st digit, the result is different*
      ```
      let numbers = [1, 42, 7000, -5, 6, 0];
      numbers.sort();

      // result: 
      // [-5, 0, 1, 42, 6, 7000]
      ```

<br>

 __[Compare Arrays](https://www.geeksforgeeks.org/how-to-compare-two-arrays-in-javascript/)__ 

  - reference in the memory is like an address

  - in arrays, when we use `==` or `===` it only compares the  **references** in memory and not the content. That's why:   
      - eg.:  
      ```
      ['a', 'b'] === ['a', 'b'];    // FALSE❗️
      ```
  - `['a', 'b']` has a different reference number compared to `['a', 'b']` 

  - if we link the arrays, they share the same reference
    - eg.:   
      *`otherNumbers` array point to the `numbers` array's, so __they are linked__*
      ```
      let numbers = [1, 2, 3];

      let otherNumbers = numbers;

      // now compare them

      numbers === otherNumbers    // true

      // if I make a change on one the other will change too❗️
      otherNumbers.pop();   // [1, 2]

      numbers               // [1, 2]
      ```

  - the values can change as long as the reference remains the same. So we can use __`const variableName`__.
    - eg.:
      *if I change the content of `const number`, it doesn't affect the reference, it remains the same.*
      ```
      const number = [1, 2];  
      number.push(3)          // [1, 2, 3] → same reference as before, [1, 2]. const number reference remains.
      ```

  - reassignemnt causes error
    - eg.:
      ```
      const number = 1;
      number = 2;       // error: Uncaught TypeError: Assignment to constant variable.
      ```

<br>

 __[Multidimensional Arrays](https://www.javascripttutorial.net/javascript-multidimensional-array/) (nested arrays)__ 

  - arrays can store other arrays, that's the nested array
    - eg.:
      ```
      const nestedArray = [
        ['a', 'b'],
        [10, 30, 50],
        ['green', 'yellow']
      ]
      ```
      How to acces the number `30` ?   
      We have to go through 2 levels:
      ```
      nestedArray[1]    // gives the second line [10, 30, 50]
      nestedArray[1][1] // gives the second element of the second arrays → number 30
      ```

<br>

---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)      


# [JS: Object Literals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics) :
 Object's are collections of properties.    
 Objects are data stractures, where the data is stored in __key value__ pairs, in other words __properties__.

 - __property__ : 2 peices of information: a `key` and a `value`.    
 Value is the right side of the __`:`__ (colon).
    - eg.:
      ```
      const objectLiteral = { key : 'value', key2 : 'value2' }
      ```

 - it's about *labeling* the information

 - we can use custome `keys` to access data (not indexes)

 - using __`{}`__ when declaring

 - the order doesn't matter

 -  we can have different types of objectd

 - eg.:   
    *a key value pairs.*
    ```
    const days = {
      sunnyDays : 120,
      coldDays : [180, 30, 'Z'],
      rainyDays : false,
      niceDays : 'weekends'
    }
    ```

<br>

## [dot notation](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#dot_notation) 

-  using `[]` square brackets and quotation marks `["value"]` after the varibale which store the property.   

    - eg.:
        ```
        const name = {firstName : "John",  lastName : "Doe"}

        name["lastName"]      //  "Doe"
        ```

- other way is using __dot.notation__ syntax, using a __`.`__
    - eg.:
        ```
        const name = {firstName : "John",  lastName : "Doe"}

        name.lastName      //  "Doe"
        ```
  
- 💡 all the keys are converted into strings (except symbols) 
  - eg.:   
    *so number as a key, boolean as a key, etc. are all strings, not numbers, booleans, etc.*
    ```
    const days = { 
      1 : "Monday", 
      null : "Friday", 
      true : "Sunday",
      favourite : "Saturday" }

    days[null]        // "Friday"
    days["null"]      // "Friday"
    days[1]           // "Monday"
    days["1"]         // "Monday"
    days[favourite]   // ReferenceError, it expects a variable
    days["favourite"] // "Saturday" 
    ```

  -  if we are using something dynamic like a __variable as a key__ in an object, we use the __square brackets__.   
  Variable as a key using dot notiation doesn't work.

<br>

## [modifying objects](https://dev.to/sanchithasr/how-to-add-modify-and-delete-javascript-object-literal-properties-49cd) 

  __adding__ or __updating__ new information. 

  - eg.:   
      to change a key's value
      ```
      const dogs = { smalldog : "small", bigdog: "big" }

      dogs.smalldog = "verysmall";  
      dogs['bigdog'] = "quitebig";  
      
      // result: 
      // { smalldog : "verysmall", bigdog: "quitebig" }
      ```
      to add an extra element:
      ```
      const dogs = { smalldog : "verysmall", bigdog: "quitebig" }

      dogs['tinydog'] = "tiny";
      dogs.megadog = "huge";

      // result: 
      // { smalldog : "verysmall", bigdog: "quitebig", tinydog : "tiny", megadog : "huge"}
      ```

<br>

## [nesting arrays and objects](https://hackernoon.com/accessing-nested-objects-in-javascript-f02f1bd6387f)   
  - have an array with objects
  - have objects with objects
  - combination of arrays and objects

  - eg.:   
    *An __array__ (or list) __of objects__*
    ```
    const blog = [
    {user: "John", text: "Helooo", likes: 3},
    {user: "Doe", text: "Yasss", likes: 5}
    ]
    ```
  - eg.:   
    *An __object which stores an array and an object__*
    ```
    const museums = {
      name : 'National Gallery',
      type : 'fine art'
      attractions : 
        ['images', 'sculptures', 'ceramics'], //  ← array
      ticketPrice: 
        { children : 2, adult : 6 }           //  ← object
    }
    ```
  
  - accessing the elements:
    - array containing objects:
       ```
      const blog = [
        {user: "John", text: "Helooo", likes: 3},
        {user: "Doe", text: "Yasss", likes: 5}
        ]

        // accessing:
        blog[0].text    // gives → 'Hellooo!'
        blog[0]['text']    // gives → 'Hellooo!'
      ```

  *remember:    
    - object are key value pairs { key : 'value'}   
    - arrays are list of things ['a', 'b', 'c']*

<br>

---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
   
# [JS: Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration) :
the aim of looping is to repeat some functionality.
- loops allow us to repeat code
- there are several types of loops:
  - __[for](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#for-loop)__
    - [looping arrays](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#looping-arrays)
    - [nested loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#nested-loops)
  - __[while](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#while-loop)__
  - __[for... of](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#for--of)__
  - __[for... in](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#for--in)__
  - __[Object methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#special-object-methods)__:    
      [Object.keys()](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#objectkeys) • [Object.values()](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#objectvalues) • [Object.entries()](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#objectentries)

## [for loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)
   
__for loop__ expression is this:
  ```
  for (  
    [intiailExpression];
    [condition];
    [incrementExpression];
  )
  ```
  
  - for loops are preferred for a set number of iteration 

  - so eg.:   
    *Print all the numbers from `1` to `10`*
    ```
    for (let i = 1; i <= 10; i++) {
      console.log(i);
    }
    ```
    the code syntax:

    start at 1      →   `let i = 1;`   
    stop at 10      →   `i <= 10;`   
    add 1 each time →   `i++` 

<br>
     
  1. __initial expression__ :    
    making a new variable __`let i`__. It only exists for the purpose of the loop (counter variable).

  2. __condition or conditional expression__ :   
    middle part is a boolean expression __`i < 10`__. As long as it is `true`, (while it is true) the loop is running. So how long the loop should run.

  3. __increment expression__ :   
    the value of `i` is updated __`i++`__
    (you can also do like divide, multiply or subtract)



  - eg.:   
    *when we want __even numbers__ printed out (i += 2)*
    ```
    for(let i = 0; i <= 20; i += 2) {
      console.log(i)
    }
    ```
    *to skip the 0 at the __starting point: (let i = 2)__*
     ```
    for(let i = 2; i <= 20; i += 2) {
      console.log(i)
    }
    ```
    *to have __odd number__, give 1 at the starting point: (let i = 1)*
     ```
    for(let i = 1; i <= 20; i += 2) {
      console.log(i)
    }
    ```
    *__count down__ to 0*
     ```
    for(let i = 100; i >= 0; i -= 10) {
      console.log(i)
    }
    ```
    *__multiply__*
     ```
    for(let i = 10; i <= 1000; i *= 10) {
      console.log(i)
    }

    // prints out: 10, 100, 1000 
    ```

    *__infinite loop__ (take care it nover stops, your mrowser run out of memory)*
       ```
    for(let i = 10; i >= 0; i++) {
      console.log(i)
    }
    ```

<br>

- when writing a loop always make sure that how your loop will end, to avoid infinite loops.

<br>

[👆go up to Loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-loops-)


### [looping arrays](https://www.codecademy.com/courses/introduction-to-javascript/lessons/loops/exercises/for-loops-with-arrays)
It is basically iterating over an array.
We use a for loop to create a number, which can be used to refer an element's index in the array.

  - eg.:   
    *looping over an array, using 'i' as an __index__ to acces the element from the array*   
    
    *Here we are iterating __from the beginning to the end of the array.__*
    ```
    const foods = ['hamburger', 'hotdog', 'soup'];

    for (let i = 0; i < foods.length; i++) {
      console.log(i, foods[i]);
    }  

    // result: 
    // number(i)  ,  (foods[i])
    //  0            'hamburger' 
    //  1            'hotdog' 
    //  2            'soup'
    ```
    *Here we are iterating __from the end to the beginning of the array.__*   

    *Se we turn it around, and start with the 
    highest index number and __- 1__, because we start from 0 index*
    ```
    const foods = ['hamburger', 'hotdog', 'soup'];

    for (let i = foods.length - 1; i >= 0; i--) {
      console.log(i, foods[i]);
    }

    // result: 
    // number(i)  ,  (foods[i])
    //  2            'soup' 
    //  1            'hotdog' 
    //  0            'hamburger'
    ```

<br>

[👆go up to Loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-loops-)

### [nested loops](https://www.codecademy.com/courses/introduction-to-javascript/lessons/loops/exercises/for-loops-iii)   
we are talking about nested loop, when __a loop is inside of another loop__

- every iteration of the outer loop, the inner loop is going to have its own full cycle, as many times as the outer loop runs.   
If outer loop has 3, the inner loop runs 3 times its own full cycle.

- eg.:
  ```
  let greeting = 'Hi';

  for (let i = 0; i <= 2; i++) {
    console.log("Outer loop:", i);

    for (let j = 0; j < greeting.length;  j++) {
      console.log(' Inner loop:' , greeting[j] )
    }
  }

  // Outer loop: 0 
  //   Inner loop: H 
  //   Inner loop: i 
  // Outer loop: 1 
  //   Inner loop: H 
  //   Inner loop: i 
  // Outer loop: 2 
  //   Inner loop: H 
  //   Inner loop: i
  ```

  - eg.:   
    *with string template literal :* __\`${i}`__
    ```
    for(let i = 1; i <= 2; i++) {
      console.log(`i is: ${i}`);
      for (let j = 1; j < 4; j++) {
        console.log(`    j is: ${j}`)
      }
    }

    // i is: 1 
    //   j is: 1 
    //   j is: 2 
    //   j is: 3 
    // i is: 2 
    //   j is: 1 
    //   j is: 2 
    //   j is: 3
    ```

- Nested loops are very useful when we are dealing with nested arrays.
  - eg.:  
  *I want to print out each name.*   
  *The first loop just prints out the 3 arrays*   

    ```
    const names = [
      ['John', 'Alexandra', 'Erika'],
      ['Joe', 'Eve', 'Kevin', 'Wilma'],
    ]

    for (let i = 0; i < names.length; i++) {
      console.log(names[i]);
    }
    // [ "John", "Alexandra", "Erika" ]
    // [ "Joe", "Eve", "Kevin", "Wilma" ]
    ```
    *The second, nested loop can access the nested arrays*   
    *I have to save the first loop's results into a variable, like `const row`. It contains the arrays.*   
    *We use the `const row` variable for the nested loop, so we can iterate over the `row`, and get the names from each array.*
    ```
    for (let i = 0; i < names.length; i++) {
      const row = names[i]; 
                      // variable created
      console.log(`ARRAY #${i + 1}`)        // it shows the number of the ARRAY. We add +1, so it doesn't start from ARRAY #0.

      for (let j =0; j < row.length; j++) {
        console.log(row[j]);                // prints out the names
      }
    }
    // ARRAY #1 - [i]
    //    John      - [j]
    //    Alexandra - [j] 
    //    Erika     - [j] 
    // ARRAY #2 - [i]
    //    Joe       - [j]
    //    Eve       - [j]
    //    Kevin     - [j]
    //    Wilma     - [j] 
    ```
    
<br>

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-loops-)

<br>

## [while loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)   
  one syntax: __`while`__ and then inside of the parentheses, a __(single condition)__.
  - while loops contue running as long as the test condition is true.
  - the addition, subtract, multiply, etc. operation are in the loop's body!
  - while loops are preferred __when we don't know how many times we are going to iterate__    
  *(eg.: in games. The game contiues until somebody wins, because we don't know how many time we have to iterate.)*

  - eg.:
      ```
      let num = 0;

      while (num <= 5) {
        console.log(num);
        num++;
      }

      // 0 1 2 3 4 5
      ```

  - eg.:   
    *a more useful example for while loops. A password: as long as the user doesn't find the password, the program keeps asking you.*
    ```
    const pw = "PassworD";

    let guess = prompt("Hello user! Guess your password");

    while(guess !== pw) {
      guess = print("The password is incorrect, try again")
    }
    console.log("Your password is correct")      // it only runs, when the user entered "PassworD" correctly.
    ```
    

  <br>

  - what is the [__`break`__](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/break) statement?    
    - the `break` terminates the current loop, stops the execution of the current loop immediately.   Then code just resumes __running after the loop__.

    - eg.:   
        *The program would go and print out numbers until reaches 100, but the break stop at 50.*
        ```
       if (let i = 0; i < 100; i++) {
          console.log(i);
          if (i === 50) break;
        }
        ```

    - eg.:   
        *The program is always true, until there is a break (so infinite loop until breaks).*   
        *So, here, it repeats the user's input, until the user writes quit, which makes running the `break` and the program stops.*
        ```
        let input = prompt("Write here:" );

        while (true) {
          input = prompt(input);
          if(input === "quit") {
            break;
          }
        } 

        console.log("You quit the program.")
        ```     
    - eg.:   
      *with for loop*
      ```
      for ( let i = 0; i < 1000; i++ ) {
        console.log(i);
        if (i === 100) break;
      }
      ```
<br> 

[👆go up to Loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-loops-)

## [for...  of](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of)
iterates over arrays and other iterable objects. 

- it is a shorter, newer and easier way to iterate than with for loop.

- eg.:   
  *for... of*
  ```
  const array1 = ['a', 'b', 'c'];

  for (const element of array1) {
      console.log(element);
  }

    //  "a"
    //  "b"
    //  "c"
  ```

  *with for loop takes more typing*
  ```
  for (let i = 0; i < array1.length; i++) {
    console.log(array1[i]);
  }

  //  "a"
  //  "b"
  //  "c"
  ```
  *nested arrays*
  ```
  const nestedArray = [
    ['a', 'b', 'c'],
    ['A', 'B', 'C']
  ];

  for (let row of nestedArray) {
    for (let letter of row) {
      console.log(letter);
    }
  }
  //  "a"
  //  "b"
  //  "c"
  //  "A"
  //  "B"
  //  "C"
  ```

- when you do need an __index__ it is better to use a for loop❗️ O

- with `for...of`__ you __can't__ iterate over a __{ key-value } pair__, it gives an error.

<br>

[👆go up to Loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-loops-)

## [for...  in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)
iterates __over__ an object, so all enumerable properties of an object that are keyed by strings.

- it only gives us the key

- eg.:
    ```
    const object = { a: 1, b: 2, c: 3 };

    for (const property in object) {
      console.log(property);
    }
    // it only gives us the key
    // "a"
    // "b"
    // "c"
    ```
    *to get the value*
    ```
    const object = { a: 1, b: 2, c: 3 };

    for (const property in object) {
      console.log(`${property}  : ${object[property]}`);
    }

    // key : value
    // "a : 1"
    // "b : 2"
    // "c : 3"
    ```
  
<br>

[👆go up to Loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-loops-)

## __special Object methods__:
  ### __[`Object.keys()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)__
  __method__ returns an array of a given object's own enumerable property __names__, iterated in the same order that a normal loop would.   
  So it give the key of key-value pairs.

  - eg.:
    ```
    const object = {
      a: 'somestring',
      b: 42,
      c: false
    };

    console.log(Object.keys(object));

    // ["a", "b", "c"]
    ```

  ### __[`Object.values()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/values)__
__method__ returns an array of a given object's own enumerable property __values__, in the same order as that provided by a for...in loop.   
So this method gives the values of a key-value pairs.

- eg.:
  ```
  const object = {
  a: 'somestring',
  b: 42,
  c: false
  };

  console.log(Object.values(object));

  // ["somestring", "42", "false"]
  ```

  ### __[`Object.entries()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/entries)__
  method returns an array of a given object's own enumerable string-keyed property __[key, value]__ pairs.   
  So it gives back the nested array's key-value pairs.

 - eg.:
    ```
    const object = {
    a: 'somestring',
    b: 42
    };

    console.log(Object.entries(object));

    // Array [ "a", "somestring" ]
    // Array [ "b", 42 ]
    ```

<br>


#### __using `Object.something()`methods with `for...of`__

- eg.:    
  *to get the average of the values*
  ```
  const dollars = {
    a : 20,
    b : 42,
    c : 50,
    d : 100 
  }

  let total = 0;
  for (average of Object.values(dollars)){
    total += average;
  }
  console.log(total / Object.values(dollars).length)

  // result 53
  // note, that {value-pairs} objects don't have length, not like [arrays].

  ```
  
[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Loops](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-loops-)
  
<br>

# [JS: Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions) :   

__Functions are reusable pieces of code__, chunks of code, they __have a name__ to them and __we can use them execute them at a later point__.   
*(Not all functions have names)*

- reusable chunks of code, so we can use a function any time once we defined a function. 

- modular:  we can pass in some sort of input that will impact the output.

- 2 steps: (1.) 🛠 __define__ and then (2.) ⏯ __call__ 

- *💡 It's a good habit, that when we have some functionality that could stand alone,  so a distinct thing (something that does something) to move it into a separate function.* 


- __[defining a function](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#defining-a-function)__   
  __[arguments](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#arguments)__   
  __[return](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#return)__   
  __[scope](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#scope-)__   
  __[function expressions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#function-expressions-)__   
  __[higher order functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#higher-order-functions-)__   
  __[returning functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#returning-functions-)__   
  __[defining methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#defining-methods-)__   
  __[the `this`keyword](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#this-)__   

<br>

## [Defining a function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#defining_functions) 

**Define:**
```
function functionName() {  
  
  // the code does something  

}
```

**Execute:**
```
functionName(); 
```

<br>

- eg.:   
  *defining a function and then executing it*
  ```
  function greetingsLoudly() {
    console.log("Hello!");
    console.log("Bonjour!");
    console.log("Bye!");
  }

  greetingsLoudly();

  // "Hello!"
  // "Bonjour!"
  // "Bye!"
  ```

- *[hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting) allows functions to be safely used in code before they are declared.   
  (Execute the function before you define it.)*

- __every method is a function__

<br>

## [Arguments](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments)
basically they are __INPUT to a function__.   

```
function functionName("PARAMETER") { 
    do something 
}

functionName("ARGUMENT");
```

Terminology:

- [Argument](https://developer.mozilla.org/en-US/docs/Glossary/Argument) is the value of the function. So, when you call the function, the value is called argument. 

- [Parameter](https://developer.mozilla.org/en-US/docs/Glossary/Parameter) is when we call the function and we pass a value in.   
So the parameter is just a placeholder (a variable) that we define to use inside of the function definition.

```
function example(parameter) {
  console.log(parameter);
}

example("argument");
```

- eg.:
  ```
  function greet(name)  {
    console.log(`Hello ${name}`);
  }

  greet("John Doe");

  // "Hello John Doe"
  ```

- if an expected argument is not provided, it has a value "undefined"

  - eg.:
    *no argument passed in but expected*
    ```
    function greet(name)  {
      console.log(`Hello ${name}`);
    }

    greet();

    // "Hello undefined"
    ```

<br>

- __Multiple arguments__ :    
we can define functions that expect more than one argument.  
  
  - in this case we have to tell the function, how many arguments we'll use.
  
  - separate the parameters & arguements by a __comma__.

  - __order counts__:    
  *(from left to right)* the first parameter gets the first argument, the second parameter gets the second argument, etc.

  - they can be different types: one parameter is a string, the other is a boolean, etc.

  - eg.:   
    *multiple arguments*
    ```
    function greetings(firstName, lastName)  {
      console.log(`Hello ${firstName} ${lastName}!`);
    }

    greetings("John", "Doe");

    // "Hello John Doe!"
    ```

  - eg.:   
    *multiple arguments with different types: string and number*
    ```
    function repeat(string, number)  {
      let empty = "";
      for(let i = 0; i < number; i++) {
          empty += string                  //string + "" + string + "" + string ...etc.
      };
      console.log(empty);
    }

    repeat("Hello!", 3);

    // Hello!Hello!Hello!
    ```

  - We can ignore arguments, buy not passing them in, because JavaScript doesn't care. __Until that argument is used in the code__. In this case the code that could cause an error.

    - eg.:   
      *ignored an argument that is in the parameter, but that argument is used → error*
      ```
      function repeat(string, number)  {
        console.log(string, number);    // 2 arguments will needed
      }

      repeat("Hello!");                 //  we give 1 argument, instead of two!

      // Uncaught ReferenceError: number is not defined!
      ```
    - eg.:   
      *ignored an argument that is in the parameter, no error*
      ```
      function repeat(string, number)  {
          console.log(string);          //  1 argument will do it
      }

      repeat("Hello!");

      // "Hello!"                       // 1 paramater
      // undefined                      //  the 2nd is undefined, but it's not an error message
      ```
<br>

## [Return](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/return)
  - We can store the output (values) of a function.


- eg.:   
  *with __RETURN__ we can __store__ variables!*
  ```
  function add(num1, num2) {
    return num1 + num2;
  }

  const total = add(2, 4);

  // call total
  // result: total gives 6!

  ```
- eg.:   
  *__But__ we __can not store__ in a variable num1 and num2 without the __reutrn__*
  ```
  function add(num1, num2) {
    console.log(num1 + num2);
  }

  add(2, 4);
  // 6

  let total =  add(2, 4);
  // 6  
  
  total;
  // but only calling "total" we get undefined!!!
  ```

- To write functions that have an __output__ (that's not just console.log()), but something that we can save, we need to use the __return__ key word❗️❗️❗️ 
  - eg.:
    *If we save the Math.random() function into a varibale (rand), it captures the output of that function.*
    ```
    let rand = Math.random();
    
    rand = 0.9936277568240952;
    ```
    *If we write a function and we want to capture its output, that's when we have to use __return__*
    ```
    function something(x, y) {
      return x + y;
    }
    
    let variable = something(2,4);
    
    let;
    // 6 - because variable now holds that value, thanks to the return key word in the function.
    ```

- The __return__ statement __stops the execution of a function__ ❗️❗️❗️   
So the line which comes after the return will be never executed.
  - eg.:   
    *return stops the execution of a function*
    ```
    function add(num1, num2) {
      return num1 + num2;
      console.log("Hello numbers!");      // this line will be never executed (unreachable code)
    }

    add(10, 20);

    // only result is: 30
    ```

- We can only return a __single value__ (only one thing)!   
*It can be an array `[1, 2, 3, 4]`, because it's a single value.*

- *Built-in-functions return values, eg. `Math.random()` returns a vlue.*    
*So you can store it in a variable. (`let x = Math.random()`)*

---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-functions-)


<br>

## [Scope](https://developer.mozilla.org/en-US/docs/Glossary/Scope) : 

A __scope__ is a location where a variable is defined, and it specifies where we have access to that variable.   
So basically it is the __visibility of the variable__.

 - __where we define a variable__ in JavaScript __impacts where we have access to it__.

 - eg.:
   *to see where the the variable `totalMails` deifned*   
   *defined with in the function*
   ```
   function receivedMails() {
      let totalMails = 10;
      console.log(totalMails);
   }

   receivedMails();

   // result: 10
   ```
   *defined outside of the function - ReferenceError  - because the __variable__ exists in the function, it is __scoped to that function__. So we don't have acces to it. It is like a little bubble.*
   ```
   function receivedMails() {
      let totalMails = 10;
   }
      console.log(totalMails);

   receivedMails();

   // result: ReferenceError: totalMails is not defined!
   ```
   /*using a global variable: outside of the function, and we update inside of the function, that makes a new variable. First we get zero and then six.*    
   ```
   let totalMails = 0;

   function receivedMails() {
    totalMails = 10;
   }
    
   console.log(totalMails);
   receivedMails();
   console.log(totalMails);

   // result: 0 
   // result: 10
   ```
  -  not very common practice to update a __global variable__  within a function.

  - usually in our functions we have our own internal variables.


 ### __[Function Scope](https://medium.com/nerd-for-tech/function-scope-block-scope-in-js-d29c8e7cd216)__   
  When a variable is declared inside a function, it is only accessible within that function and cannot be used outside that function.

  - eg.:   
    *function scope - the __variable__ (greeting) __is scoped to the__ (sayHello) __function__*

      ```
      function sayHello(){
        let greeting =  "Hello!";

        greeting                  // "Hello!"
      }

      greeting;                   // NOT DEFINED! - outside of the function

      ```
  
  - if there is a variable defined with the same name in the function, then we will reference that variable first.
    - eg.:
      ```
      let food = "pizza";

      function dinner() {
        let food = "quiche";
        console.log(food)
      }

      console.log(food)         // "pizza" - outside of the function
      dinner();                 // "quiche" - inside of the function, redefines the "let food" variable. 
      ```

<br>

 ### __[Block Scope](https://medium.com/nerd-for-tech/function-scope-block-scope-in-js-d29c8e7cd216)__   
  A variable when declared inside of a conditional or inside a loop, they are accessible within that condition or loop.   
  
  -  The variables declared inside the curly braces are called as within block scope.

  -  block refers to almost any time we see curly braces except for a function. 

  - block includes conditionals and loops.

  - eg.:   
    *variable declared outside and another inside of a if conditional*
    ```
    let diameter = 10;

    if (diameter > 2) {
      const square = 5;
      let str  = "Hello!";
    }

    console.log(diameter);        // 10
    console.log(str);             // Reference Error: str is NOT DEFINED!
    ```

  - the before, when `var` was used. The `var` variables are scoped to functions, but they are not scoped too blocks.

  - using `let` or `const` the variables are block scoped *(one of the main reasons that `let` and `const` were introduced)*.

<br>

### __[Lexical Scoping](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures#lexical_scoping)__
  An inner function __nested__ inside of a parent function, and the inner function has access to the variables defined in the scope of that outer function.

  - eg.:   
    *lexical scoping: nested function*
    ```
    function outer() {
      let hero = "Spiderman";

      function inner() {
        let callHero = `Hello ${hero}!`
        console.log(callHero);
      }
      inner();                   // executing the innerfunction inside of the outer function
    }


    outer();                     // executing the outer function


    // result: "Hello Spiderman!"
    ```

---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-functions-)

<br>

## [Function Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/function) : 
An other way of defining a function is that __storing a function in a variable__.

- a function expression is this:
  ```
  const variable = function (x, y) {
      return x + y;
  }

  variable(1, 2);      // 3
  ```

- eg.:   
  *storing a function in a variable, it has no name. The variable has a name `const square`❗️*
  ```
  const square = function(num) {
    return num + num;
  }

  square(10);         // 20
  ```


- a function statement
  eg.:   
  *a function statement, which has a name `add`❗️*
  ```
  function add(x, y) {
    return x + y;
  }

  add(2+4);           // 6
  ```

- using a function expression is the same as using any other function (executing or naming is the same).

- functions are values (in JavaSCript), meaning you can store them, you can pass them, etc.

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-functions-)

<br>

## [Higher Order Functions](https://medium.com/javascript-scene/higher-order-functions-composing-software-5365cf2cbe99) : 
are functions that operate on, work with other functions.

- they can accept other __functions as arguments__, and do something with them.
- they can __return a function__.

<br> 

- 💡 remember: a function is just a value.

<br>

- eg.:   
  *__functions as arguments__. So, a function is passed in (here I named `func`).*  
  *(you can call `func` anything else).*
  ```
  function waving(func) {
    func();
    func();
    func();
  }

  function greeting() {
    console.log("Hello!");
  }

  waving(greeting);         // pass a function as an argument!

  // "Hello!"
  // "Hello!"
  // "Hello!"
  ```
  
  *If I try to pass a number or a string, it gives an __error__, because it tries to execute it.*
  ```
  function waving(func) {
    func();
    func();
    func();
  }

  waving(10);           // TypeError: func is not a function!
  ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-functions-)

<br>

## [Returning Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/return#returning_a_function) : 
they are returning a function as a value from within a function.

- eg.:   
  *this function creates random messages.*   
  ```
  function sayHi(){
    const rand = Math.random();
      if (rand > 0.5) {
          return function () {
              console.log("Hello!");
          }
      } else {
          return function () {
              console.log("Good day!");
          }
      }
  }

  sayHi();            // just calling the function, I don't call the inner function

  // result is a function, just the return value: 
  // f () { console.log("Good day!"); } or { console.log("Hello!"); }
  ```
  *If I want __to use the return value, I have to capture the function which contains the return value into a variable__.*   
  ```
  const greetings = sayHi();    // now the greeting variable holds a function...

  greetings();                   //... and I can execute that function.
  greetings();
  greetings();

  // "Good day!"
  // "Hello!"
  // "Hello!"
  ```
  *Let see what happened in the code above:*
  1. *The outer function returns one of the 2 inner functions, but the inner function is never called to be executed.*   
  2. *So __to make the return function executed, we have to reach them__: by __calling the inner function__ in the way that __applying the parenthesis `()` after the variable__ `greetings` (so it becomes `greetings()` )*
  3. *There are 2 ways:*    
      *I.*     
      *save the result of the higher-order function to a variable, and then call that variable:  
      `sayHi()()`*  
      *II.*    
      *`greetings = sayHi()`*      
        *`greetings()`*

- So, we can say: a __higher-order function returns another function__, but if that returned function isn't called yet, we still have to do it manually, by __adding the parentheses `()`__ (it's how we immediately call a function)❗️

<br>

- A __[factory function](https://www.codecademy.com/courses/introduction-to-javascript/lessons/advanced-objects/exercises/factory-functions)__: is a function that __returns an object and can be reused to make multiple object instances__ 
Factory functions can also have parameters allowing us to customize the object that gets returned.

- eg.:   
  *An other example, where our __function generates a function__ (based on an input)*   
  *This function can show if the number I give is between `min` and `max` (eg. `5` is between `1` and `10`).*   

  *Short explanation:*    
  1. *we're using the `between()` function, that accepts 2 parameters `(min, max)`, but it returns another function, that accepts `1` single parameter `(num)`.*   
  2. *When we call `between()`, it is returned the following:*    
  *`return function (num) {`    
    `return num > min && num < max;`     
    `}`*    
  *This function accepts a single parameter`(num)`*
  ```
  function between(min, max) {
    return function(num) {
      return num > min && num < max;
    }
  }

  between(1, 10);

  // returns a function:  
  // f () (num) { return num >= min && num <= max; }

  // but if I save between(min, max) into a variable:

  const test = between(1, 10);        

  test(5); 
  // true

  test(30);
  // false
  ```

  *Detailed, step-by-step explanation:*
  ```
  • function between(min, max) {
  •   return function(num) {
  •     return num > min && num < max;
  •   }
  • }

    // we save the between(min, max) into a variable:
  • const test = between(1, 10);
  

    // it translates to this:
  • test = return function(num) {
  •     return num > 1 && num < 10;
  •   }
    
    // to call this inner function (now saved to the 'const test' variable,   
    // we need to pass 1 single argument, in the paranthesis right after the variable's name:
  • test(5)

    // Another way to have the same calculation is: // to call both functions at the same time, using multiple parentheses pairs, each pair to one function:
  • test = between(1, 10)(5);
  ```
 ---
 
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-functions-)

<br>

## [Defining Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects#defining_methods) : 
We can add functions as properties on objects. __We call them methods!__   

 __A method is a function that has been placed as a [property](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-object-literals-) on an object__ ❗️: we put a dot __`.`__ infront of its name (like we did with built in methods).
 
- *object’s method (a function that belongs to an object)* 

- built in methods, like string methods, array methods, etc.
  - eg.:
    ```
    "ahoj!".toUpperCase();

    // AHOJ!
    ```

- What is the __difference between a method and a function__?
  - A method is simply a **function that has been placed as a property on an object**.

  - Every method is a function, but not every function is a method.

- We can add a function as a property value (key : value pairs).   
    - eg.:   
      *We made an object: math*  
      *We access 3 functions, each of them is a __method__.*    
      *(also they are objects, math object literals)*  
      *So __method: is a function that's been added as a property on some object__.*  
      *We need to call them*
      ```
      const math = {

        multiply : function(x, y) {
              return x * y;
        },
        
        divide : function(x, y) {
              return x / y;
        },

        square : function(x) {
              return x * x;
        }
      }

      // calling the method on the 'math' object:

      math.square(2);

      // gives 4
      ```

- We can use a function as the value in a property, in an object. 
   - eg.:  
    *Create a `counting` object* 
      ```
      const counting = {
        square : function(num) {
          return num * num;
        },
        cube : function(num) {
          return num ** 3;
        }
      }

      counting.cube(2);

      // 8
      ```
 - __Shorthand__ way of adding methods: leaving out the `function` keyword and the colon `:`.
    - eg.:
      ```
      const counting = {
        square(num) {         // → square : function(num)
          return num * num;
        },
        cube(num) {           // → cube : function(num)
          return num ** 3;
        }
      }

      counting.cube(2);

      // 8
      ```

<br>

💡 Reminder: __an [object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects#objects_overview) is a standalone entity, with properties and type.__    
Like a cup: a cup is an object, with properties:       
a cup has a color,    
a cup has design, weight, a material it is made of, etc. 

---

<br>

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#js-functions-)



## __[this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)__ :  
 `this` keyword is used when we want to access other properties on the same object.

 - most common situation to use `this`: we typically use inside of an object in a method.
 - the value of [`this`](https://alligator.io/js/this-keyword/#four-rules) differs depending on how a function is invoked (how it is called), so we can’t know the value of `this` just by looking at the function itself, but we need to know the context in which the function is invoked.
 - So, the `this` references the object that is executing the current function.  
 - If a function is part of an object, it is called a method → If the function is a method in an object, `this` references that object itself.   
   Otherwise, if that function is a regular function, so it's not part of an object, `this` references the global object, the `window`. 

 - eg.:   
    *creating an object `person`, it has a method `fullname()`*   
    *`this` refers to the `person` object.*   
    ```
    const person = {
      first : "John",             // property
      last  : "Doe",              // property
      fullname()  {               // method
        return `${this.first} ${this.last}`
      }
    }

    person.fullname();    // "John Doe"
    person.last;          // "Doe"

    person.last = "Smith" 
    person.fullname();    // "John Smith"
    ```
    *if I try to acces last name without the `this`, it gives an error*
    ```
    const person = {
      first : "John",            
      last  : "Doe",              
      fullname()  {               
        return last;
      }
    }

    person.fullname;
    // ReferenceError: last is not defined
    ```

- when we are in a method and we write `this` dot `.` property, it __refers to the object__ that the method is defined on.   
The `this` refers to what is on its left side.

<br>

- So the value of `this` __can change__ ❗️
- the value of `this` depends on the invocation context of the function it is used in, so it depends on __how we call the function__.

  - eg.:   
    *make a `dog2` variable which refers to the `dog.woof()` method*   
    *the `this` will change, and will refer to the top level element in JS, the `window`*
    ```
    1.    const dog = {
    2.        name : 'Bulldog',
    3.        color : 'grey',
    4.        woof() {
    5.           console.log(`${this.name} says woof woof!`);
    6.           console.log("this is:", this);
    7.        }
    8.    }
    9.  
    10.   dog.woof();
    11.   //(at line 5. result ↓:)
    12.   // Bulldog says woof woof!
    13.   //(at line 6. result: ↓) 
    14.   // this is: {name: 'Bulldog', color: 'grey', woof: ƒ}       
    15. 
    16.   const dog2 = dog.woof;      // I capture dog.woof method in another variable. 
    17.                               // Note: we just give the function definition when used without parenthesis❗️
    18.   
    19.   dog2();                     // it is a function.
    20.   // [blank] says woof woof!
    21.   // this is: Window {window: Window, self: Window, document: document, name: '', location: Location, …}
    ```
  - when we call the `dog2()` the `this` is not pointing to the `dog` object, therefore it doesn't know what `this` means. That's why it is `[[blank] says woof woof!`.     
If we assign `dog.woof()`with parenthesis to the `const dog2`global variable, the function is immediately executed, but we don't want that, since we want to control when to call it. Therefore we reassign the `dog.woof` without paranthesise to `const dog2`, because we want to control when to call it, by using `dog2()` later.

  - when I call (invoke) `dog.woof()` it is a method. `woof()`refers to the object to the left (`dog`). __When I run `dog2()`, which is the same function as `dog.woof`, only it is invoked differently__ therefore the `this` is not referring to the `dog`, but instead to the `window` top level object.    
So, if we call the the `woof` method on the `dog` object then the `this` keyword will point to that `dog` object. However, by reassigning the function reference to a global variable like `dog2`, when we call it with parentheses we are actually calling the function from the global (window) object, so the `this` keyword will indeed point to that global window object (even though we assigned the function from the object originally - still, the value of the `this` keyword will be determined based on which object we call the function from, and that changed when we assigned it to a global variable).

- `this` the [`Window`](https://developer.mozilla.org/en-US/docs/Web/API/Window) is a special object, it is the top level object, the main object in JS. All the functions lives inside of it.

- just type `window;` into the browser's console, and you'll what the the window object contains.

- when I create a method, it is added to the window object.
    - eg.:   
      *by creating `hello` method, it is added to the `window` object automatically. I can call it `window.hello`.*
      ```
      function hello() {
        console.log("Hello hello!");
      }

      window.hello;
      // ƒ hello() {
        console.log("Hello hello!");
        }
      ```
  
  💡 We use the function without using the parenthesis when we ant to make a copy of it.    
  `dog2 = dog.woof;`
  
  💡 What does invoke mean?   
   JavaScript Function Invocation is used to __executes the function code__ and it is common to use the term “call a function” instead of “invoke a function”. __The code inside a function is executed when the function is invoked__.   
   ([calling vs invoking](https://stackoverflow.com/questions/50884893/calling-vs-invoking-a-function): it is more a semantic, subtle difference).    
*When you call a function, you are directly telling it to run. When you invoke a function, you are letting something to run it.*

- to sum up: the __value of this differs depending on how a function is invoked (the call site), so we can’t know the value of this just by looking at the function itself, but we need to know the context in which the function is invoked__.

- [MDN's explanation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this#this_in_function_contexts), very helpful. 

- further reading about __[`this`](https://www.javascripttutorial.net/javascript-this/)__ and __[`this`](https://alligator.io/js/this-keyword/)__


---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
   
<br>

# __[Callback functions](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function) & [Array Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#instance_methods)__ :  
__Array methods accept a function as its arguments.__   
 So a __[callback](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)__ is a function passed as an argument to another function, this technique allows __a function to call another function__.

- __[forEach](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#foreach)__   
  __[Map](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#map)__   
  __[Arrow Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#arrow-functions)__   
  __[setTimeout](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#settimeout)__   
  __[setInterval](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#setinterval)__ & __[clearInterval](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#clearinterval)__         
  __[Filter](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#filter)__   
  __[Every](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#every
)__ & __[Some](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#some
)__   
  __[Reduce](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#reduce)__   
  __[`this` in arrow functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#this-in-arrow-functions)__   


## __[forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)__   
__accepts a callback function__.
__It runs a function__, (so run some code) __once per item in some array__.   
So we pass in a function, and that function will be called once per item, where each item is going to be passed into the function automatically.

- eg.: 

  *We want to print out all the numbers.*   
  
  *A __common way__ to do `forEach` is to __define the function as an anonymus function expression, in the forEach__*  
  *We also need a parameter, here `num`*

  *The way it works: I call for each on every element, so `forEach` executes the print once per element: it passes `1` to print, then `2` to print then `3`, etc.*
    ```
    const numbers = [1, 2, 3, 4 ];

    numbers.forEach(function(num) { 
      console.log(num); 
    });

    // 1 // 2 // 3 // 4
    ```

  *This is the __uncommon way__, where we define a function above the forEach*.
    ```
    const numbers = [1, 2, 3, 4];

    function print(element) {
      console.log(element)
    } 

    numbers.forEach(print);  

    // 1 // 2 // 3 // 4
    ```

- but __[`for...of`]()__ ❗️❗️❗️ is as efficient (and easier, shorter way) for doing something once per element.
  - eg.:   
    *using the `for...of`*
    ```
    const numbers = [1, 2, 3, 4];

    for(let num of numbers) {
      console.log(num);
    }

    // 1 // 2 // 3 // 4
    ```

- eg.:   
  *printing out even numbers*
  ```
  const numbers = [1, 2, 3, 4, 5, 6];

  numbers.forEach(function(num) {
    if (num % 2 === 0) {
        console.log(num);
  });

  // 2
  // 4
  // 6
  ```

- eg.:   
  *pizzeria ratings, 1 to 10 stars*
  ```
  const pizzeria = [
    {
        name: "Joe's Pizza",
        stars: 1
    },
    {
        name: "Marios's Pizza",
        stars: 5
    },
    {
        name: "Cecilia's Pizza",
        stars: 9
    }
  ];

  pizzeria.forEach(function(pizza) {
      console.log(`${pizza.name} ${pizza.stars} / 10`);
  });

  // Joe's Pizza 1 / 10
  // Marios's Pizza 5 / 10
  // Cecilia's Pizza 9 / 10
  ```

  💡 nowadays we use __`for...of`__  rather than `forEach`.

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br>

## __[Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)__   
creates a new array with the results of calling a callback on every element in the array.

- it is also a __callback function__ and it also __runs that function once per element in the array__, like the `forEach`.
But `Map` is __then generates a new array using__ the result, using __the return value of that callback__.    

- ❗️ it __doesn't change__ the array; it __creates a new__ one❗️

- `something.map(callback)`

*(to map an array from one state to another)*

- eg.:   
  *The return value, which is coming back from callback function `Map`, is taking and adding into a new array. The new array returns and then I can save it under a new variable (const doubles).*
  *Here, I double every intiger*
  ```
  const numbers = [1, 2, 3, 4,];

  const doubles = numbers.map(function(num) {  // it calls the function on every number (goes to parameter every "num")
    return num * 2;                            // each number is * 2, then return to a new array which is stored in the new variable "doubles"
  });

  doubles;
  // [2, 4, 6, 8]

  ```
  *a not common way to do it*
  ```
  const numbers = [1, 2, 3, 4,];

  function doubles(num) { 
    return num * 2; 
  };

  numbers.map(doubles);

  // [2, 4, 6, 8]
  ```

- eg.:   
  *with an object of key-value pairs*
  *create an array just for the pizzeria names*
  ```
  const pizzeria = [
    {
        name: "Joe's Pizza",
        stars: 1
    },
    {
        name: "Marios's Pizza",
        stars: 5
    },
    {
        name: "Cecilia's Pizza",
        stars: 9
    }
  ];

  const restos = pizzeria.map(function(pizza){
      return pizza.name;
  });

  restos;
  // ["Joe's Pizza", "Marios's Pizza", "Cecilia's Pizza"]
  ```

- `map` is usually used when we need a portion of a data, or we want to transform every element into a new array.

<br>

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br>

## __[Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)__

It allows us to write functions without the keyword function.

- it is called in short [*the fat arrow*](https://www.freecodecamp.org/news/learn-es6-the-dope-way-part-ii-arrow-functions-and-the-this-keyword-381ac7a32881/) (and in Ruby may known as the *hash rocket* ) 

- syntactically compact alternative to a regular function expression, so the point is to make things shorter.

- a *traditional function* vs. an *arrow function*:   
    __*traditional function*__   
    *(normally this function requires a name)*   
   ```
   function (a){
      return a + 100;
    };

   ``` 
 
   *__arrow function__*      
   *function word removed, arrow `=>` placed between `(a)` the argument and `{` the opening body bracket*
   ```
   (a) => {
      return a + 100;
   }
   ```

- arrow functions are all anonymys. __You can not name them, but we can store them in a variable__.

  -  eg.:    
     *we store the arrow function which has 1 parameter in the "const square" variable*
      ```
      const square = ( x ) => {   
        return x * x   
      };
      ```
     *we store the arrow function, wich has 2 parameters in the "const sum" variable*
      ```   
      const sum = ( x, y ) =>   
          return x + y  
      }  
      ```
- arrow function has parenthesis with the parameters

- we can't declare a function on its own like: 
    ```
    function(x,y){ 
      return x + y 
   }
   ``` 
  __we have to give a function statement__ (a name) like: 
  ```
  function name (x,y) { 
    return x + y
  };
  ```

- for a __single__ argument we don't need the parenthesis (for multiple arguments, we need!).
  - eg.:   
    ```
    const variable = x => { 
      return x + x
    } 
    ```

- we can't declare an arrow function on its own , like `(x,y) => { }`. So __we have to save it in a variable__. (💡 If we don't save it to a variable, once we create an array (or any other content), it's [discarded](https://javascript.info/garbage-collection).
  - eg.:
    ```
    const variable = (x,y) => { 
      return x + y
    }
    ```

- arrow function __without arguments__, we have to use the empty parenthesis: 
  - eg.:   
  *dice rolling*
    ```
    const dice = () => { 
      return Math.floor(Math.random() * 6) + 1; 
    }
    ```

- we can make arrow fucntion even more compact by using the __implicit return__ ❗️So we __leave out the `return` keyword__.   
*It only works with arrow function (doesn't work with a typical function expression).*   
To return without return __replace the curlybraces `{ }`with parenthesis `( )`__ !

  - eg.:   
    ```
    const variable = (x) => (
      x * x
    )

    variable(5);
    // 25
    ```

- it can be even shorter, a one liner, by leaving out completely the parenthesis.  Good for short codes. 
*If the return is long, maybe don't use it on one line, to make it readable.*
  - eg.:   
    ```
    const variable = (x, y) => x + y
    
    variable(2, 4);
    // 6
    ```

- ❗️ __implicit returns only work, when there is only 1 statement in the budy of the function!!!__

<br>

- eg.:    
  *arrow function exercise, using map*
  ```
  const pizzeria = [
    {
        name: "Joe's Pizza",
        stars: 1
    },
    {
        name: "Marios's Pizza",
        stars: 5
    },
    {
        name: "Cecilia's Pizza",
        stars: 9
    }
  ];

  const restos = pizzeria.map((pizza) => {
      return `${pizza.name} - ${pizza.stars}`
  });

  // we can leave out the parameters parenthsis, and the return (see the ())

    const restos = pizzeria.map(pizza => (
     `${pizza.name} - ${pizza.stars}`
  ));

  // make it to a 1 line
    const restos = pizzeria.map(pizza => `${pizza.name} - ${pizza.stars}`);

  restos;
  //  ["Joe's Pizza - 1", "Marios's Pizza - 5", "Cecilia's Pizza - 9"]
  ```
  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br>

  ## __[setTimeout](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout)__ 
  it sets a timer which executes a function or specified piece of code once the timer expires.

   it expects to __pass 2 arguments__: 
  1. a callback 
  2. a number of milliseconds to delay the execution of the function

  eg.:   
  *setTimeout: after 3 seconds, it executes the function. We have to pass in a callback:*      
  *Otherwise, if we just passed in `console.log`, that is going to execute it immediately.*      
  *So the goal is to make the browser wait 3 seconds.*
  ```
  setTimeout(() => {
    console.log("Hello!")       // 1st argument
  }, 3000);                     // 2nd argument

  // wait 3 seconds, then:
  // "Hello!"
  ``` 
  *Another example: first it runs "Hello there!", than immediately the "Bye!", and then the `setTimeout` "are you still there?". Instead of "Hello!", "Are you still there?", "Bye!"*
  ```
  console.log("Hello!");

    setTimeout(() => {
    console.log("Are you still there?")    
  }, 3000);

  console.log("Bye!");
  ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br>

## __[setInterval](https://developer.mozilla.org/en-US/docs/Web/API/setInterval)__    
it calls a callback function every X time. So, we can repeat something with the `setInterval`.

- eg.:
  *`setInterval` a `Math.random`. Every 2 seconds prints out a random number. So it continues to call that function ever 2 seconds.*
  ```
  setInterval(() => {
    console.log(Math.random())
  }, 2000);                     // 2000 milliseconds
  ```

  How to stop it? Use the `clearInterval()`

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br>

  ## __[`clearInterval`](https://developer.mozilla.org/en-US/docs/Web/API/clearInterval)__
  it cancels a timed, repeating action which was previously established by a call to `setInterval()`.

  - We have to __save the value of the `setInterval` into a variable__. Doing this, it returns the ID of corresponding interval we set up.   
  So, if we have several different `setInterval`s we can specify which one we want to stop.

  - eg.:   
  *Save the s'setInterval' into a variable (id)*
  ```
  const variable = setInterval(() => {
    console.log(Math.random())
  }, 2000);

  variable;             // calling the variable, which has the setInterval, which starts to print every 2 seconds
  // 0.8287249162601189
  //0.13595591599851664
  // 0.5061340888408574

  clearInterval(variable); 
  
  // variable stops
  ```
  
---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br>  

## __[`filter`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)__   
  creates a new array with all the elements that pass the test implemented by the provided function.   
  So when we want to __filter out or make a subset in a new array__.

  - eg.:   
  *We want to pull out just the the odd numbers into their own array.*   
  *So, we pass in a callback and this callback needs to return true or false, (boolean function).*
  *If that callback returns true for any element, that element will be added to the filtered array*
  *Otherwise, it's ignored*
```
const nums = [6, 5, 4, 3, 2, 1];
const odds = nums.filter(n => {
  return n % 2 === 1;         // the callback return tru or false
                              // if true, 'n' is added to the filtered array
});

odds;
// [5, 3, 1]
```

*Another example: filter out to a new array the pizzerias which score is equal or bigger than 5*
  ```
  const pizzeria = [
    {
        name: "Joe's Pizza",
        stars: 1
    },
    {
        name: "Marios's Pizza",
        stars: 5
    },
    {
        name: "Cecilia's Pizza",
        stars: 9
    }
  ];

  const goodRestos = pizzeria.filter( p => {
      return p.stars >= 5
  });

  goodRestos;
  // [{name: "Marios's Pizza", stars: 5}, {name: "Cecilia's Pizza", stars: 9}]     // array of objects    
  ```
    
*the same code with a 1 liner*
  ```
  const goodRestos = pizzeria.filter( p => p.stars >= 5);
  ```
*if we want to have the titles of the pizzerias, not the whole array of objects, we can combine methods, `filer` and `map`.*
```
  const pizzeria = [
    {
        name: "Joe's Pizza",
        stars: 1
    },
    {
        name: "Marios's Pizza",
        stars: 5
    },
    {
        name: "Cecilia's Pizza",
        stars: 9
    }
  ];

const goodRestos = pizzeria.filter( p => p.stars >= 5);
// 0: [{name: "Marios's Pizza", stars: 5},
// 1: {name: "Cecilia's Pizza", stars: 9}]

const restoNames = goodRestos.map( n => n.name);
// ["Marios's Pizza", "Cecilia's Pizza"]
```
*we can do the codes above in one singe lines: chain them together*
```
const goodRestos = pizzeria.filter( p => p.stars >= 5).map(n => n.name);

goodResots;
//["Marios's Pizza", "Cecilia's Pizza"]
```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br> 

## __[every](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)__
The `every()` method __tests whether ALL elements in the array pass the the provided function__ (the test). It __returns a Boolean value__.

So, if every element passed into that function returns true, then the entire every function call returns true.

- eg.:
  *check if EVERY goals reach 50. If all the goals are equal or greater than 50, returns TRUE*
  ```
  const goals = [80, 100, 50, 40, 77];

  goals.every(points => points >= 50)         // each element from points array is passed into the callback ***every(callback)***, callback should return true/false.
  // result is FALSE, because one of the goals is less than 50.
  ```
- eg.:   
  *a function (evens) which accepts a single array of numbers, returns true if the numbers are even and false of odd.*
  ```
  function evens(num){
      (num.every( (x) => (x % 2 === 0) ) ) 
      {
        return true;
      } 
    }

    evens([2, 4, 6, 8]);
    // true

    evens([3, 6, 8]);
    // false


    //******* shorter version! ******//
      
    function allEvens(num){
      return (num.every( x => x % 2 === 0))
    }

    evens([2, 4, 6, 8]);
    // true
    evens([3, 6, 8]);
    // false
  ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br> 

## __[some](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)__  
Similiar to every, but __returns TRUE if SOME of the array elements pass the test function__.

- eg.:   
  **check if SOME of the goals reach 50. If some of the goals are equal or greater than 50, returns TRUE**
  ```
  const goals = [80, 100, 50, 40, 77];

  goals.some(points => points >= 50)         // at least 1 element has to be >= 50.
  // result is TRUE, because 4 out of 5 of the goals is greater than 50.
  ```

- eg.:   
  *let see if any of the houses is built after 1920*  
  ```
  const buildings = [
    {
      name : "House1",
      year: 1990
    },
    {
      name : "House2",
      year: 1909
    },
    {
      name : "House3",
      year: 1870
    }
  ];

  buildings.some(house => house.year > 1920)

  // true - because 1 of the elements passes the test
  ```
---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br> 

## __[reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)__   
  executes a reducer function on each element of the array, resulting in a single value.   
  So its main goal is to take some array and reduce it down to a single value.

  - eg.:   
   *The __accumulator__ it __holds the sum__.*   
  *The __currentValue__ represents each element from the array*
    ```
    [1, 3, 5, 7].reduce((accumulator, currentValue) => {
      return accumulator + currentValue;
    });

    // first callback: 1 + 3 = 4
    // second callack: 4 + 5 = 9
    // third callback: 9 + 7 = 16
    ```
 
 - eg.:   
   *figure out the total (not using for.. of, but would be easier)*    
   *here accumulator is named as total*

    ```
    const prices = [1.99, 4.50, 19.99];

    const totalPrice = prices.reduce((total, num) => {
      return total + num
    })

    totalPrice;
    // 26.479999999999997
    ```

- `reduce()` can be use to find maximum or minimum values.

- eg.:    
  *find the min. price of the array*   
  *what we are accumulating is the minimum value through the array*
  ```
  const prices = [1.99, 4.50, 19.99];

  const minPrice = prices.reduce((min, currentNum) => {
    if (currentNum < min) {
      return currentNum;
    }
    return min;
  });

  minPrice;
  // 1.99
  ```

- eg.:    
  *find the newest house*
  ```
  const houses = [
      {
        name : "House1",
        year: 1990
      },
      {
        name : "House2",
        year: 2013
      },
      {
        name : "House3",
        year: 1870
      }
  ];

  const newestHouse = houses.reduce((newHouse, currentHouse) => {
    if (currentHouse.year > newHouse.year) {
          return currentHouse;
    }
      return newHouse;            
  });

  newestHouse;
  //{name: 'House2', year: 2013}
  ```

- we can specify a starting point for the `accumulator` parameter, by adding a __2nd argument__ to the `current value`.
  - eg.:
    *adding a 2nd argument `100` to `current` as a starting point*
    ```
    const evens = [2, 4, 6, 8];

    evens.reduce((accumulater, current) => 
    accumulater + current, 100);
    
    // 120        - because [2, 4, 6, 8] = 20 + 100
    ```

💡 [further reading about `reduce`](https://www.freecodecamp.org/news/reduce-f47a7da511a9/)   
💡 [another reading about `reduce`](https://www.digitalocean.com/community/tutorials/js-finally-understand-reduce)

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br> 

## __[`this`](https://www.freecodecamp.org/news/learn-es6-the-dope-way-part-ii-arrow-functions-and-the-this-keyword-381ac7a32881/)__ in __[arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this#arrow_functions)__

`this` of an arrow function vs `this` of a traditional function.

- __`this` in a normal method refers to the object in which it is contained__.

- __`this` in an arrow function refers (be scoped to) only the function in which it is created__.

- eg.:   
  *__regular function:__*   
  *`person` is the value of the `this.name` when we call the `person.hello()`.*
  ```
  const person = {
    name: "Joe",
    hello : function() {
      console.log("Hey", this.name, "hello!")
    }
  }

  person.hello();
  // Hey Joe hello!
  ```
  *__arrow function:__*   
  *the value of `this` has not changed (not set) when we call the `person.hello()`.*        
  *`this` is set to the `window` object, so it seems that `hello` method is defined on its own, not inside of the `person` object.*      
  *That is why, it doesn't matter how we call the function.*  
  *So, we are not getting a new value for `this` (because its value is that global value, the `window` object).*
  ```
  const person = {
    name: "Joe",
    hello : () => {
      console.log("Hey", this.name, "hello!")
    }
  }

  person.hello();
  //Hey  hello!
  ```

<br>

- So, if we use `this` inside the arrow function, it will refer to the global environment which is the `window`. 
If we put the arrow function inside of a normal function, the `this` will refer to the function's scope.

- eg.:   
  *a traditional function with `this` - returning the first and last name*
  ```
  const person = {
    first : "John",
    last : "Doe",
    fullName : function () {
     return `${this.first} ${this.last}` 
    }
  }

  person.fullName();
  // 'John Doe'
  ```
  __*`this` with arrow function*__
  ```
  const name = {
    first : "John",
    last : "Doe",
    fullName : () => {
     return `${this.first} ${this.last}` 
    }
  }

  name.fullName();
  // 'undefined undefined'
  ```

- In arrow functions, JavaScript sets the `this` lexically.  
  It means that the __arrow function does not create its own execution context__ but __inherits the `this` from the outer function where the arrow function is defined__ ❗️.    
  Since an arrow function does not create its own execution context, defining a method using an arrow function will cause an error.    

   - So `this` does not [bind](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_objects/Function/bind#examples) to the object’s method or the object itself.
  - in this example, it means `this` refers to the *window object*.

- to __define a method we shouldn't use  an arrow function__ (give undefined)!

<br>

- 💡 __when `this` make sense in an arrow function__
  - eg.:   
  *we add a `setTimeout` method in to our person object, under the fullName method*
  ```
  const person = {
    first : "John",
    last : "Doe",
    fullName : () => {
     return `${this.first} ${this.last}` 
    },
    timeName : function() {
      setTimeout( () => {
          console.log(this);
          console.log(this.fullName())
      }, 3000)                  // we waint 3 sec, before condsle.log(this.fullName())
    }
  }

  person.timeName();        // wait 3 seconds
  // {first: 'John', last: 'Doe', fullName: ƒ, timeName: ƒ}
  // undefined undefined
  ```
 - the `setTimeout()` is a window object, and that's why it's important to use arrow functions in that case. 
 - Because if it were a normal function, than `this` inside that normal function *would point to the window object*, since __normal functions use the execution context__ (in this case, the context is the window), so `this.fullName` returns undefined. 
 - With an *arrow function*, the __`this` would correctly point to the scope of the outer function__ (timeName) instead of using the window context of the `setTimeout()` function, and `this.fullName` wouldn't be undefined.    
See explanation [here](https://www.youtube.com/watch?v=thXp0_py9X4) at 17:25 (this example is based on that).

 - in other words: the outer function (`timeName`) is the block/scope where we're defining the `setTimeout` method, and an arrow function nested in that `timeName` function will inherit its context.   
When we use the `this` inside `timeName`, we're referring to the `person` object (the object to the left when the method is called, as in `person.timeName`), so we would apply the same thing to the `this` inside the `setTimeout` as well.   
When JavaScript code is interpreted, each function creates an __execution context__, to scope any variables and arguments inside the block created by that function. So with that, the arrow function is part of the execution context created for `timeName`. 
 - when we use `this` inside of an arrow function, we're going one level back in terms of scope.

  <br>

  *the same example: but we use a regular function, and we have an error*
  ```
  const person = {
    first : "John",
    last : "Doe",
    fullName : () => {
     return `${this.first} ${this.last}` 
    },
    timeName : function() {
      setTimeout(function() {
          console.log(this);
          console.log(this.fullName())
      }, 3000)                  // we waint 3 sec, before condsle.log(this.fullName())
    }
  }

  person.timeName();        // wait 3 seconds
  // Window {window: Window, self: Window, document: document, name: '', …}
  // TypeError: this.fullName is not a function
  ```

  - gives an error, because of the [execution context](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#about-the-execution-context-): here `setTimeout()` is a method on the `window` object (`window.setTimeout`), and `this` refers to that `window` object.

- to conclude:    
  *A method:*    
  is a function directly inside of an object.

  *A function:*    
  is either standalone or inside of a method.

  *Non-Arrow Functions:*   
  When `this` is used inside of an object’s method the `this` keyword is bound to the object. Yet when it is inside of a function, either stand alone or within another method, it will always refer to the `window` / global object.

  *Arrow Functions*   
  The `this` keyword inherits the execution context from the outer function where the arrow function is defined, i.e. it gets the same scope as it's parent's scope.

💡 recap for the scoping:
  - eg.:   
  *to understand the scoping with `this`*
    ```
    const thing1 = {
      thing2 : {
          thing3 : () => {
              console.log(this)
            }
        }
    }
  
    thing1.thing2.thing3();
    // Window ...
    ```
    `thing2` is a property of the `thing1` object, and the scope of that property is still the `thing1` object. When we use the arrow function, it will refer to the parent scope of the `thing1` object, which is indeed the `Window` object.


##### [about the execution context](https://dev.to/thee_divide/fast-guide-to-execution-context-execution-stack-in-javascript-3eij) :   
  - As soon as we're starting to write our code, we create an [execution context](https://www.youtube.com/watch?v=exrc_rLj5iw): it is the process of going through our code line by line (known as the thread of execution), and the memory which we store any variables, functions, the stuff, to get declared. This two (going through the code and the memory) together is an execution context, a space where to execute the code.
  - The [execution context](https://stackoverflow.com/questions/9384758/what-is-the-execution-context-in-javascript-exactly) is the wrapper around your existing code; which contains __code that you have not written__, __but is generated by the JS Engine__.   
  - An Execution Context is created each time you run your .js file/app. The first step in this creation phase is Hoisting. The JS Engine reserves space or set's up memory for all the variables and functions defined in your code. These are then accessed when your code is executed line-by-line.
---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Callback functions & Array Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-functions--array-methods-)

<br> 

# __[Other JS Features](https://www.digitalocean.com/community/tutorials/understanding-destructuring-rest-parameters-and-spread-syntax-in-javascript)__   
- [default parameters](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#default-parameters-)      
  [spread syntax](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#spread-syntax-)   
  [rest parameters](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#rest-parameters)   
  [destructuring assignment](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#destructuring-assignment)

## __[Default parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters)__ :  
`Default function` parameters allow named parameters to be initialized with default values if no value or undefined is passed.    
Basically when we don't use a parameter, we can give it a default value.

- eg.:   
  *a roll die method with `Math.random` times, a number of sides*
  ```
  function rollDie(sides) {
    return Math.floor(Math.random() * sides) + 1
  }

  rollDie(6);     // expecting a number from 1 to 6
  // 2 // 5 

  rollDie();
  // NaN          // we didn`t pass any value, so it's NaN, nothung multiply number is NaN
  ```

- The way to avoid `NaN` when we don't pass value to the function, is we give a __`default param`__ 
- we add an __`=`__ sign to the parameters in the function. 
-eg.:     
  *We set __`b = 1`__, so the default value of `b` is `1`*
  ```
  function multiply(a, b = 1) {
    return a * b;
  }

  multiply(7);     // 7  →  7 * 1
  multiply(7, 3);  // 21 →  7 * 3
  ```
  If we leav out the `b`, the `b` is set to `1`, so its defaul value is `1`.

- eg.:   
  *so the first example with `default param`*
    ```
  function rollDie(sides = 6) {
    return Math.floor(Math.random() * sides) + 1
  }

  rollDie(6);     // expecting a number from 1 to 6
  // 2 // 5 

  rollDie();      // sides = 6 
  // 2 // 4
  ```

- __the order is very important__ ❗️

  - eg.:  
    *we pass two parameters*
    ```
    function greeting( greet, name ) {
      console.log(`${greet} ${name}`);
    }

    greeting("Hi there!", "John");
    // Hi there! John

    greeting("John");           // I pass only 1 argument
    // John undefined           // it doesn't know the order, John is the 2nd normally
    ```
    *The default parameters should come second or third or, etc. They need to come after any parameters that are not default.*
    ```
    function greeting( name, greet = "Hello!" ) {
      console.log(`${greet} ${name}`);
    }

    greeting("John");
    // Hello! John
    ```
    *we can use multiple default parameters*
    ```
    function greeting(greet = "Hello!", name, question = "How are you?"  ) {
      console.log(`${greet} ${name} ${question}`);
    }

    greeting("John");
    // Hello! John How are you?

    greeting("Bonjour", "John", "comment tu vas?");
    // Bonjour John comment tu vas?
    ```


---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS Other Features](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#other-js-features)

<br> 

## __[Spread Syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)__ :  
Spread syntax looks liek this: __`...`__ .   
It allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected.  

- The keyword is expanding, so spread (*taking something and spreading it out*).  

- its 3 dots: __`...`__

- spread in:     
   __[function call](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#spread-in-function-calls)      
   [array literlas](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#spread-in-array-literals)   
   [object literals](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#spread-in-object-literals)__

#### __[Spread in Function Calls](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_function_calls)__ 

Spreading an iterable (array, string, etc.) into a Function Call (a list of arguments)

- eg.:   
  *`Math.max` and `Math.min` static functions expect multiple arguments. They return  `NaN` if any parameter isn't a number and can't be converted into a number.*
  ```
  Math.min(3, 5, 9, 1);         // these numbers are separate arguments
  // 1

  Math.max(3, 5, 9, 1);         // these numbers are separate arguments
  // 9

  const nums = [3, 5, 9, 1];

  Math.min(nums)

  // NaN          // because we passed a single array full of numbers, not multiple sperate arguments
  ```
  *so we are going to use the __spread syntax__, and by that, we're separating the `nums` into separate arguments, so the functions can use it.*
  ```
  const nums = [3, 5, 9, 1];

  Math.max(...nums);           // num array spreaded out into separate arguments: 3, 5, 9, 1
  // 9
  ```
  *the __`...`__ syntax doesn't change `nums`*   
 
- eg.:   
  *using `console.log`, and printing out `nums`. Then using the separate syntax, see the difference: __each element from `nums` array passed in as a separate argument__ to the `console.log`.*
  ```
  const nums = [3, 5, 9, 1];

  console.log(nums);
  // [3, 5, 9, 1]                 // the array itself is printed

  console.log(...nums);
  // 3 5 9 1                      // numbers are separated by spaces
  ```

- we can use the __spread__ for any other iterable (which we can use the `for..of`)
  - eg.:   
    *spread on a string: it spreads each character into individual arguments*
    ```
    console.log("HELLO");
    // HELLO

    console.log(..."HELLO");        // it equals to this: console.log("H", "E", "L", "L", "O") ← separate arguments
    // H E L L O
    ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Spread Syntax](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#spread-syntax-)

<br>

 #### __[Spread in Array Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_array_literals)__     
 How can we spread an iterable into arrays.
 Basically spreading an array into an other array.

 - eg.:   
  *We have 2 arrays, and we want to contain all the arrays into a variable. Using spread, we create a copy of the arrays.*
  ```
  const cities = ["London", "Paris", "Budapest"];
  const countries = ["India", "China"];

  const places = [...cities]
  // ['London', 'Paris', 'Budapest']      // → a copy of const cities


  // to prove places a copy of cities

  places.push("Amsterdam");
  places;
  // ['London', 'Paris', 'Budapest', 'Amsterdam']

  cities;
  // ["London", "Paris", "Budapest"]      // → cities unchanged
  ```

  *combine arrays*
  ```
  const cities = ["London", "Paris", "Budapest"];
  const countries = ["India", "China"];

  places = [...cities, ...countries];  
  // ['London', 'Paris', 'Budapest', 'India', 'China']
  ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to Spread Syntax](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#spread-syntax-)

<br>


  #### __[Spread in Object Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_object_literals)__
  Copies properties from one object into another object literal.   

  - like in arrays, we can spread properties from an object into a new object.

  - A lot of the time it is useful to spread into objects, so creating copies of an object. For instance when we are working with with libraries and tools (like React).

  - eg.:   
   *We have 2 objects: cat and dog. We can make a copy of the cat for example*
    ```
    const cat = { color : 'black', name : 'Milo'};
    const dog = { isBig : true, name: 'Charlie'};

    {...cat};
    // {color: 'black', name: 'Milo'}
    ```
    *we can add something to that copy*
    ```
    {...cat, type : 'Biman'};
    // {color: 'black', name: 'Milo', type: 'Biman'}
    ```
    *we can combine cat and dog into a new variable (pets).    
    It copies over properties from both, but there is a conflict: both have a `name` property.    
    __The order matters__: `dog` is the last one, so it overrites the `cat` property (see the `name`, it's from the `dog` property).*
    ```
    const pets = {...cat, ...dog};

    pets;
    // {color: 'black', name: 'Charlie', isBig: true}
    ```

  - eg.:   
    *Try to spread an array into an object. The __indices__ are used as the key.*
    ```
    {...[2, 6, 7, 4]};
    // {0: 2, 1: 6, 2: 7, 3: 4}     // 0 index : 2, 1 index : 6, etc...

    {...'Bonjour'};
    // {0: 'B', 1: 'o', 2: 'n', 3: 'j', 4: 'o', 5: 'u', 6: 'r'}
    ```
 - also useful to copy objects, when we have a form (a data), and we want to add something extra data to it.
    - eg.:   
      *We have a form, called `user`, and we cope and add our extra data to it, called `newUser`*
      ```
      const user = { email : "somethong@email.com", password : "123456789" };

      const newUser = {...user, id : "94576", isAdmin: false};                      // the copy of the user + our extra data

      newUser;
      // {email: 'somethong@email.com', password: '123456789', id: '94576', isAdmin: false}
      ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS Other Features](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#other-js-features)

<br>

#### __[Rest parameters](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters)__
The rest parameter syntax allows a function to accept an indefinite number of arguments as an array...

So __it collects all remaining arguments into an acutal array.__


- __`...`__
- collects the __rest__ of the parameters, arguments

- eg.:  
    *Using `rest` + only one parameter (`num`).   
    `Rest` will collect the rest of the parameters*
    ```
    function sum(...num){
      console.log(num);
    }

    sum(10,42,77);            // give an REAL ARRAY
    // [10, 42, 77]

    ```
    *without `rest`, only takes the first number*
    ```
    function sum(num){
      console.log(num);
    }

    sum(10,42,77);
    // 10
    ```
    *With rest, the `reduce` function will work, because `rest` creates an array*
    ```
      function sum(...num) {
      return num.reduce((total, num) => total + num)
    }

    sum(1, 2, 3);
    // 6
    ```

<br>

__bonus: about the `arguments` object__

  - it automatically holds all of the arguments passed into a function.  
  - it's an array __like__ object:   
    - it has a length property
    - doesn't have array methods (like push or pop, reduce, etc.)
  - it's available inside every function
  - __contains all the arguments passed to the function__
  - __not available inside of arrow functions__!

    - eg.:   
      *We have a function, with no arguments. Inside the function we print out the `arguments` object. When we give arguments to the function, the `arguemtns` object will contain those values, in an order, like an array. So it looks like an array but it's not an array → we can't use array methods.*   
      ```
      function sum() {
        console.log(arguments);
      }

      sum();                    // 'arguments' is empty
      // Arguments [callee: ƒ, Symbol(Symbol.iterator): ƒ]
      // length: 0


      sum(10,42,77);            // arguments contains all the values we gave
      // Arguments(3) [10, 42, 77, callee: ƒ, Symbol(Symbol.iterator): ƒ]
      // 0: 10
      // 1: 42
      // 2: 77
      ```
      *We want to have the sum of the numbers we give to `arguments`. But we can't use the `reduce` method, because `arguments` is not an array.*
      ```
      function sum() {
        return arguments.reduce((total, num) => total + num)
      }

      sum(10,42,77); 
      // Uncaught TypeError: arguments.reduce is not a function
    
      ```
     - when using `arguments`, we can't chose that name. Using rest, we can use any name for a parameter.


---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS Other Features](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#other-js-features)

<br>

#### __[Destructuring assignment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)__       
[from Arrays](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#from-arrays)      
[from Objects](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#from-objects)      
[Function Parameter](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#function-parameter-destructuring)

<br>

##### __*[from ARRAYS](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#array_destructuring)*__   
The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables.   

So, it's a way of unpacking, singling out values from arrays.  
Unpacking mean put values into ditinct variables.

A short syntax to unpack:    
__values from arrays__ and __properties from objects__ into distinct variables.

- __`[]`__ using brackets

- it's basically copying a value into a variable (not extracting from the array or object)

- based upon position

- eg.:
  *arrays of number. We can single out into 2 varbales (firstnum and secondnum) for example the first and the second number.*
  ```
  const  numbers = [10,20,30,40,50,60];

  const [firstnum, secondnum] = numbers;

  firstnum;
  // 10

  secondnum;
  // 20

  numbers;
  // [10, 20, 30, 40, 50, 60]
  ```
  *to single out the rest of the numbers into a variable*
  ```
  const  numbers = [10,20,30,40,50,60];

  const [firstnum, secondnum, ...restOfTheNumbers] = numbers;

  firstnum;
  // 10

  secondnum;
  // 20

  restOfTheNumbers;
  // [30, 40, 50, 60]
  ``` 

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS Other Features](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#other-js-features)

<br>

##### __*[from OBJECTS](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#object_destructuring)*__ 
extract values from __objects__.

- it is more commonly used (than extracting from arrays).

- __`{}`__ using curlybraces

- the name matters (how we access the value inside of the object)

- it doesn't change the object

- eg.:
  *We want to accass data more frequently, so here is a shorter syntax using a destrucring assignment*
  ```
  const user = {
    firstName : 'John',
    lastName : 'Doe',
    email : 'johndoe@email.com',
    address : '1600 Amphitheatre Parkway'
    state : 'California'
  };

  const { email, lastName, address} = user;

  email;                    // created an email varibale
  // 'johndoe@email.com'

  lastName;                 // created a lastName varibale
  // 'Doe'

  address;
  // '1600 Amphitheatre Parkway'
  ```

  - if we want to change the name of the variable where we singled out the object's value
  
   - eg.:   
    *rename the address to sameAddress*
    ```
    const user = {
      firstName : 'John',
      lastName : 'Doe',
      email : 'johndoe@email.com',
      address : '1600 Amphitheatre Parkway',
      state : 'California'
    };

    const {address : sameAddress } = user;

    newAddress;
    '1600 Amphitheatre Parkway'
    ```

  - adding default values
   - eg.:   
      *we have a user2, but user2 does not have an email and address*
      ```
      const user2 = {
        firstName : 'Jane',
        lastName : 'Doe',
        state : 'California'
      };

      const { firstName : janey, email, address } = user2;

      janey;
      // 'Jane'

      email;
      // undefined

      adress;
      // undefined

      const { email = 'jane@email.com', address = '10 Pl. de la Joliette, 13002 Marseille'} = user2;

      email;
      // 'jane@email.com'

      address;
      // '10 Pl. de la Joliette, 13002 Marseille'
      ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS Other Features](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#other-js-features)

<br>

##### __*[Function Parameter Destructuring](https://dmitripavlutin.com/javascript-object-destructuring/#92-function-parameter-destructuring)*__
 we can destructure on the way into the function!

 - eg.:   
  *We want to destructure the first and last name. We can do it on the fly.*     
  *Because we are expecting an object and from that object we want to destructure firstName and lastName, then return the fullName*
  ```
  const user = {
      firstName : 'John',
      lastName : 'Doe',
      state : 'California'
  };

  function fullName ({firstName, lastName}) {
      return `${firstName} ${lastName}`
  }

  fullName(user);
  // 'John Doe'


  // it's the same BUT WAY LONGER
  function fullName(user) {
    const {firstName, lastName} = user;
    return `${firstName} ${lastName}`
  }

  fullName(user);
  // 'John Doe'
  ```
  
<br>

- eg.:   
  *filter the movies based upon their score*
  ```
  const movies = [
    {
        title: 'Amadeus',
        score: 99,
        year: 1984
    },
    {
        title: 'Sharknado',
        score: 35,
        year: 2013
    },
    {
        title: '13 Going On 30',
        score: 70,
        year: 2004
    }
  ];

  // destructuring on the way in

  movies.filter(({score}) => score > 90);
  // {title: 'Amadeus', score: 99, year: 1984}


  // without destructuring

  movies.filter((film) => film.score > 90);
  // {title: 'Amadeus', score: 99, year: 1984}  

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS Other Features](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#other-js-features)

<br>

# __[The DOM](https://javascript.info/browser-environment#dom-document-object-model)__  
*Document Object Model*  
A bunch of __JavaScript objects that represents the webpage__. So the [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) represents all page content as objects that can be modified. The __document object__ is the main “entry point” to the page. We can change or create anything on the page using it.   

It's our window, our access portal into the contents of a Web page from JavaScript.  

So the DOM is a JS representation of a webpage, an interface to access the actual (i.e. already rendered) elements of an HTML document.    
It is the 'window' to the contents of a webpage.   
And many objects that we can interact with via JS.

- [How does it work?](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#how-does-it-work)   
  [What is the `document`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-document)   
  [`getElementById()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#getelementbyid)   
  [`getElementsByTagName()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#getelementsbytagname)   
  [`getElementsByClassName()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#getelementsbyclassname)    
  [`querySelector()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#queryselector) and [`querySelectorAll()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#queryselectorall)
  

## [How does it work?](https://www.w3.org/TR/DOM-Level-2-Core/introduction.html)

When a browser loads the Web page, the HTML and CSS loads, and then creating a bunch of JS objects based on the __style__ elements (which were loaded with the HTML + CSS).

- every single element (also the `body`) gets its own JS object!

- __[The DOM tree](https://javascript.info/dom-nodes)__:    
It is a __[tree structure](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/How_to_create_a_DOM_tree)__:   
  - the HTML elements are connected, there is a relationship, parent-children.   
  - The backbone of an HTML document are tags.   
  - According to DOM, every __HTML tag is an object__! Nested tags are *children* of the enclosing one. __The text inside a tag is an object as well. All these objects are accessible using JavaScript, and we can use them to modify the page.__ 
For instance: a *`document.body` is the object representing the `<body>` tag.*
 - eg.:   
  *the DOM tree*
  ```
  <html>
  <head>
    <title>About elk</title>
  </head>
  <body>
    The truth about elk.
  </body>
  </html>
  ```
  
  *[the structre](https://javascript.info/dom-nodes#an-example-of-the-dom):*
  
  ```
  HTML
    ▾
    HEAD
      ▾
      TITLE:
        #text About elk
    ▾
    BODY
      ▾
      #text ↵␣␣The truth about elk.↵

  // ↵   - sign of a newline
  // ␣   - sign of a space 
  ``` 
  
  *Tags are __element nodes__ and form the tree structure: __`<html>` is at the root, then `<head>` and `<body>` are its children__, etc.*   
 
 <br>
 
💡 [Node](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) (in the DOM):    
__all parts of the *DOM tree* is a "node"__, but also the text content from those elements and attributes can be "nodes" as well. These individual parts of the document are known as "nodes". So a "node" can be simply an HTML element. The __DOM is a tree structure that represents the HTML of the website, and every HTML element is a "node"__.     
💡 The *topmost node* is the root node (Document Node) of the DOM tree, which has one child, the `<html>`.   
💡 Elements are one type of *node*, so to be accurate, we call the Element Nodes. Only element nodes can be parents.  
Most common __node types__:  
  - Element Node
  - Text Node
  - Comment Node(s)
  - Document Node : the content of the entire HTML, in short it's the page.
  - Document Type Node it is the `<!DOCTYPE html>`

*a [good video about this topic](https://www.youtube.com/watch?v=y3itGTCseAk)*

<br>

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>

## [The document](https://developer.mozilla.org/en-US/docs/Web/API/Document)    
__The *document object* is the entry point into the DOM.    
It contains *representations of all the content on a page*, and lots of *methods and properties*.__    
If we want to reach an element, we can do it through the `document` (eg.: `document.getElementById()`, etc.).   

It is an __element on the top of the element tree structure__:   
*it is the top of a folder for everything*      
*it's the root of the tree*
 - write `document` on the console and it gives us:  
   - eg.:   
      *the representation of the HTML*   
      ```
      #document
        <!DOCTYPE html>
        <html dir="ltr" ... lang="en" class="md">
        <head>...</head>
        </body>...</body>
        </html>
      ```
- typing __`console.dir(document)`__ can __show the JavaScript object__ with a bunch of properties.   
  - eg.:   
    ```
    #document
      location: URL...
      activeElement: body
      adoptedStyleSheets: []
      alinkColor: ""
      all: [html, head, meta, meta, title, body, h1, img#banner, p, b, b, a, ...    // it contains every element of the page - tags. Each of them is a JS object❗️
      .
      .
      .
    ```

- so the *document object* is where everything is contained and starts. Inside we have methods and properties, we can change them to manipulate the document.   
(It contains objects that represent the content of a Web page.)


---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>

## [getElementById](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById)  
The Document method `getElementById` returns an Element object representing the element whose id property matches the specified string.   

Simply: __when we call this method, we pass in a *string* and this string has to correspond to an `ID` on an element.__   

 - a method to select one single element (because every ID is one and unique)

 - `document.getElementById('idname')`

 - it is a method that exists on the document
 - it only occurs once per page!
 - if there is an element found with that ID, it will be returned 
 - if the ID can't be found it returns `null` (it only gives us 1 thing, there's no collection of elements)
 - when we select something __JS fetchs us the object that represents some elements on the page__ based on the matching ID.
 - __it gives us the object representation of that element, which we can then manipulate__
 - we are not *asking* the HTML, __we are asking the DOM__ object (__the element object that JavaScript created__).


 - eg.:   
    *here's the html*
    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Dogs</title>
    </head>
    <body>
        <h1 id="mainheading">Woof woof woof</h1>
        <img src="https://images.unsplash.com/dogs" id="dogg" alt="cute dog">
    </body>
    </html>
    ```
    *to select an image*   
    ```
    document.getElementById('dogg')

    //returns:
    // <img id="banner" src="https://images.unsplash.com/dogs
    ```
    *we can save it to a variable*
    ```
    const image = document.getElementById('dogg'); 

    console.dir('image');      // call the variable

    // returns the object which contains a lots of properties
    // img#banner
    //  alt: ""
    //  currentSrc: "https://images.unsplash.com/dogs"
    // height: 879
    // tagName: "IMG"
    //  ...
    ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>

##  [getElementsByTagName](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByTagName) 


   The `getElementsByTagName` method of Document interface returns an HTMLCollection of elements with the given tag name.

   Simply: call `getElementsByTagName`, pass in a tag name, and it returns to an __HTML collection__.

  - a method to select elements

  - `document.getElementsByTagName('tagname')`

  - when *tag name* is not found, we have an empty collection (and not `null`)


  - an __[HTML collection](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCollection)__:   
    it represents a generic collection (array-like object similar to arguments) of __elements__ (in document order) and __offers methods and properties for selecting from the list__.
      - it is not an array (but array like)
      - has length
      - iterable `(for..of)`

  - an __[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)__:    
  in JavaScript is that *object that we're getting back that has all the properties that represent a single HTML element.*  
  Element is the most __general base class__ from which all element objects *(i.e. objects that represent elements)* in a __Document__ inherit. It only has methods and properties common to all kinds of elements. More specific classes inherit from Element.

<br>

  - eg.:   
      *to get the image, we pass the `img` tag*   
      The HTML   
      ```
      <html>
      <head>
        <title>getElementBy example</title>
      </head>
      <body>
        <img class="myimage" src="https://images.com/photo01.jpg" alt="">
        <img class="myimage" src="https://images.com/photo02.jpg" alt="">
        <img class="myimage" src="https://images.com/photo03.jpg" alt="">
        <p>Some outer text</p>
        <p>Some outer text</p>      
      </body>
      </html>
      ```
      JS
      ```
      const images = document.getElementsByTagName('img');

      images;

      // returns: 
      // HTMLCollection(3) [img.myimage, img.myimage, img.myimage]
      //  0: img.myimage
      //  1: img.myimage
      //  2: img.myimage
      ```
      *select the 2nd image*
      ```
      console.dir(images[1]);

      // returns an object:
      // img.myimage
      //   accessKey: ""
      //   align: ""
      //   ariaAtomic: null
      //   ariaAutoComplete: null
      //   src: "https://images.com/photo02.jpg"
      //   ...
      ```
      *we can iterate it*
      ```
      for (let img of images) {
        console.log(img.src)
      }

      // returns: 
      //   https://images.com/photo01.jpg
      //   https://images.com/photo02.jpg
      //   https://images.com/photo03.jpg      
      ```
      *we can change all the images' source*
      ```
      for (let img of images) {
        img.src = "https://upload.photos.org/images_example.jpg"
        console.log(img.src)
      }

      // all the 3 image became the same: https://upload.photos.org/images_example.jpg image
      ```

 ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>

##  [getElementsByClassName](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByClassName)

 we are selecting elements by a class.

- a method to select elements

- `document.getElementsByClassName('classname')`

- when *class name* is not found, we have an empty collection (and not `null`)

- eg.:   
*select an image by its class name*   
The HTML   
  ```
  <html>
  <head>
    <title>getElementBy example</title>
  </head>
  <body>
    <img class="myimage" src="https://images.com/photo01.jpg" alt="">
    <img class="myimage" src="https://images.com/photo02.jpg" alt="">
    <img class="myimage" src="https://images.com/photo03.jpg" alt="">
    <p>Some outer text</p>
    <p>Some outer text</p>      
  </body>
  </html>
  ```
  JS
  ```
  const images = document.getElementsByClassName('myimage');

  images;

  // returns: 
  // HTMLCollection(3) [img.myimage, img.myimage, img.myimage]  👈 this is not an array!
  //  0: img.myimage
  //  1: img.myimage
  //  2: img.myimage
  ```
  *we can change all the images' source*
  ```
  for (let img of images) {
    img.src = "https://upload.photos.org/images_example.jpg"
    console.log(img.src)
  }

  // all the 3 image became the same: https://upload.photos.org/images_example.jpg image
  ```


 ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>

## [querySelector](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector) 
an *all-in-one* method to select a single element.

- `document.querySelector('h1');`       ← tagname

- `document.querySelector('#id');`        ← id name

- `document.querySelector('.classname');` ← class name

- it works with any css style

- we have to use the __`.`__ or __`#`__ before the name `('#name')`

- `querySelector` just gives us the first match❗️ 

- we can chaine on other CSS style selectors   
  `document.querySelector('.image:nth-of-type(2)');`

- eg.:      
    *select an image with the querySelector - using the class*
    The HTML 
    
    ```
    <html>
    <head>
      <title>getElementBy example</title>
    </head>
    <body>
      <img class="myimage" src="https://images.com/photo01.jpg" alt="">
      <img class="myimage" src="https://images.com/photo02.jpg" alt="">
      <img class="myimage" src="https://images.com/photo03.jpg" alt="">
      <p>Some outer text</p>
      <p>Some outer text</p>   
      <a href="#" title="hello">Hello, click me!</a>
      <a href="#" title="bye">Good bye!</a>
    </body>
    </html>
    ```
    
    JS
    
    ```
    const images = document.querySelector('.myimage');

    images;

    // returns: 
    // <img class="myimage" src="https://images.com/photo01.jpg" alt="">    👈  shows me the first one
    ```
     
    *get the second image by chaining a CSS style*
     
    ```
    const images = document.querySelector(.myimage:nth-of-type(2));

    images;

    // returns: 
    // <img class="myimage" src="https://images.com/photo02.jpg" alt="">    👈  shows me the second
    ```
      
   __*select an `a` tag with the CSS (title="hello") attribute (in CSS we use `[]` to select an attribute)*__

    ```
    document.querySelector('a[title="hello"]');

    // returns:
    // <a href="#" title="hello">Hello, click me!</a>
    ```

---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>


## [querySelectorAll](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll) 
same idea as `querySelector` but returns a __collection__ of mathcing __elements__,  instead of just the first match.

- `document.querySelectorAll('h1');`       ← tagname

- `document.querySelectorAll('.classname');` ← class name

- we can use all th CSS selectors and the way we select is the same as in CSS

- eg.:   
  *we sleect ALL the `<p>`*   
  The HTML   
  ```
  <html>
  <head>
    <title>getElementBy example</title>
  </head>
    <body>
        <img class="myimage" src="https://images.com/photo01.jpg" alt="">
        <img class="myimage" src="https://images.com/photo02.jpg" alt="">
        <img class="myimage" src="https://images.com/photo03.jpg" alt="">
        <p>Some outer text</p>
        <p>Some outer text</p>  
        <h1><a href="wikipedia.com" title="text01">This is an h1</a></h1> 
        <h2><a href="wikipedia.com" title="text02">This is an h2</a></h2> 
        <p><a href="wikipedia.com" title="hello">Hello, click me!</a></p>
        <p><a href="wikipedia.com" title="bye">Good bye!</a></p>
      </body>
    </html>
    ````
  
  JS

    ```
    document.querySelectorAll('p');

    // returns: 
    // NodeList(2) [p, p]
    //  0: p
    //  1: p
    //  length: 2
    ```

    *with just simple querySelector*
    ```
    document.querySelector('p');

    // returns: 
    // <p>Some outer text</p>   👈  shows me the first one
    ```

  *__select all the `<a>` nested inside of a `<p>`__. The way we select is the same as we do it in CSS*
  
    ```
    document.querySelectorAll('p a');

    // returns:
    // NodeList(2) [a, a]
    //  0: a
    //  1: a
    ```
      
  *iterate over and print out every `href` source*
      
    ```
    const links = document.querySelectorAll('p a');


    for (link of links) {
        console.log(link.href)
    }

    // returns:
    // https://wikipedia.com/
    // https://wikipedia.com/
    ```


---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>

# [DOM manipulation](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents#active_learning_basic_dom_manipulation)   

DOM manipulation refers to using JavaScript in the middle of HTML to access to move, rename, show and hide things, update styles. So to impact the HTML.   

We use DOM manipulation when we want to modify parts of the page when the user interacts with it. Otherwise, if we feel like the initial page style should be modified, then changing the original code is the better approach. So, in general, we use CSS as much as possible, because it is lighter and faster and it is the indicated technology to style a webpage. However, when we want to modify a page after the initial code was rendered to make it dynamic, that is only possible with DOM manipulation.


- __[innerText](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#innertext)__   
- __[textContent](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#textcontent)__  
- __[innerHTML](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#innerhtml)__    
- __[difference between `innerText` vs `innerHTML` vs `textContent`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-difference-between-innertext-vs-innerhtml-vs-textcontent)__   
- __[attributes & properties](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties)__   
  - __[`getAttribute` & `setAttribute`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#accessing-attributes)__   
  - __[`style`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#style)__   
  - __[`classList`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#classlist)__  
  - __[`.parentElement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#parentelemment-access-a-parent-element)__   
  - __[`.children`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#children-it-gives-the-parent-elements-children)__   
  - __[`next/previousSibling`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#nextsibling-and-previoussibling)__
  - __[`next/previousElementSibling`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#nextelementsibling-and-previouselementsibling)__   
  - __[`Document.createElement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#documentcreateelement)__   
  - __[`appendChild`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#appendchild)__   
  - __[`append`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#append)__   
  - __[`prepend`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#prepend)__   
  - __[`insertAdjacentElement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#insertadjacentelement)__   
  - __[`after`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#after)__ and __[`before`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#before)__
  - __[`removeChild`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#removechild)__
  - __[`remove`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#remove)__ 


<br>

## [innerText](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText)   
The `innerText` __property__ of the HTMLElement interface represents the *rendered* text content of a node and its descendants.   
__The innerText property returns just the text, without spacing and inner element tags.__

Simply, the text that we see as a user showing up between the opening and closing tags.

- we can modify the inner text of an HTML

- syntax: `document. + selector + ('element') + .innerText`

- eg.:   
  *retrieve the `<p>` text*   
  HTML 
  ```
  <h3>Inner Text</h3>

  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.</p>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.</p>
  ```
  JS
  ```
  document.querySelector('p').innerText;
  
  // output:
  // "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod."      
  ```
  *__This paragraph element is just a JavaScript object, so we can change that into text value.__*   
  *So let's change the value of all the `<p>` to another text by iterating over*
  ```
  const paragraphs = document.querySelector('p');

  for (let par of paragraphs) {
      par.innerText = "Text has been overwritten!";
  }

  // output - all the <p> tags of the document (see the HTML below):
  //'Text has been overwritten!'
  ```
  *now see the HTML*

  ```
  <h3>Inner Text</h3>

  <p>Text has been overwritten!</p>
  <p>Text has been overwritten!</p>
  ```

<br>

- 💡 document.querySelectorAll('p') is similar to an array, so to get all the (`<p>`) elements, we can use either indexing or using iteration:

  - indexing:    
  `document.querySelectorAll('p')[0].innerText;`

  - iteration:   
    ```
    const paragraphs = document.querySelector('p');

    for (let par of paragraphs) {
      par.innerText = "Text has been overwritten!";
    }
    ```
    
---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>


## [textContent](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent#differences_from_innertext)
The `textContent` property is very similar to the `innerText` property. But it's not the same.

__The `textContent` property __returns__ every element, every piece of content inside the selected HTML element (shows everything which is in the markup).__   
But `innerText` property doesn't show everything what is in the markup (eg. if we had something by setting something to `display: none`, `innerText` doesn't show it).

- So `textContent` is give us everything, whereas `innerText` is actually sensitive to what is showing at the moment.


- `textContent` returns every element in the `node`. In contrast, `innerText` is aware of styling and won't return the text of "hidden" elements.   

- syntax: `document.querySelector('p').textContent`

- eg.:   
  *let's take the  `<b>` tag which is inside of the `<p>` tag. Let's set it to `display:none`. So the word (`<b>consectetur</b>`) is hidden now*   
  *But with `textContent` we can still see it*   
  HTML
  ```
  <styles>
    b { 
      display: none;
    }
  </stlyes>

  ...

  <h3>Text Content</h3>

  <p>Lorem ipsum dolor sit amet, <b>consectetur</b> adipiscing elit, sed do eiusmod.</p>
  ``` 
  JS
  ```
  document.querySelector('p').textContent;

  // 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.'   // 👈 consectetur word is there
  ```
  *but, `innerText` doesn't show the hidden `<b>` element's content (consectetur)*
  ```
  document.querySelector('p').innerText;

  // Lorem ipsum dolor sit amet, adipiscing elit, sed do eiusmod.   // 👈 consectetur word is missing
  ```
  
---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>  
  

## [innerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)   
The Element __property__ innerHTML gets or sets the HTML markup contained within the element.   
  
 `innerHTML` gives us the entirety of the markup contained within some element.

 - so __`innerHTML` retrieves the full content, including the tag names, of basically everything inside of an element between the opening and closing tag.__

 - __`innerHTML` is the only one we can use to add elements inside of some other element__ compared to `innerText` and `textContent`.

- eg.:   
  *When we do innerHTML, we get all of the tags included*   
  HTML
  ```
  <h1>My Inner HTML</h1>

  <p>LLorem ipsum dolor sit amet, consectetur adipiscing
  elit, labore et dolore magna aliqua.
  <br>Ut enim ad minim</b> veniam.
  <span>Excepteur sint occaecat</span> cupidatat non
  proident, sunt in culpa.
  </p>
  ```
  JS
  ```
  document.querySelector('p').innerHTML;

  // output: we get all the HTML tags as well❗️

  // <p>LLorem ipsum dolor sit amet, consectetur adipiscing
  // elit, labore et dolore magna aliqua.
  // <br>Ut enim ad minim</b> veniam.
  // <span>Excepteur sint occaecat</span> cupidatat non
  // proident, sunt in culpa.
  // </p>
  ```

<br>

- eg.:   
  *innerHTML can give us (just) text*   
  HTML   
  ```
  <h1>My Inner HTML</h1>

  <p>Lorem ipsum dolor sit amet, <b>consectetur</b> adipiscing elit, sed do eiusmod.</p>
  ```
  JS
  ```
  document.querySelector('h1').innerHTML;
  // output:
  // 'My Inner HTML'
  ```

<br>

 - 💡 why is it useful to see all the HTML tags?   
 Because __`innerHTML` is more useful when we are updating the content and we want to change the HTML.__   
    - eg.:  
      *we want to put the `<h1>` title into italic `<i>`.*   
      HTML
      ```
      <h1>My Inner HTML</h1>
      ```
      JS
      ```
      document.querySelector('h1').innerHTML = '<i>My Inner HTML</i>`

      // output: the title is in italic
      // see the HTML:
      // <h1>
      //   <i>My Inner HTML</i>
      // </h1>
      ```

- we can add elements to the element, using __`+=`__ 
    - eg.:  
      *adding a superscript to the title*   
      HTML
      ```
      <h1>
        <i>My Inner HTML</i>
      </h1>
      ```
      JS
      ```
      document.querySelector('h1').innerHTML += '<sup>Superscript</sup>`

      // output: in HTML
      // <h1>
      //   <i>My Inner HTML</i><sup>Superscript</sup>
      // </h1>
      ```
  
  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>
  
## The difference between `innerText` vs `innerHTML` vs `textContent`   

The `innerText` property __returns just the text, without spacing and inner element tags__.

The `innerHTML` property __returns the text, including all spacing and inner element tags__.

The `textContent` property __returns the text with spacing, but without inner element tags__.

- eg.:   
  HTML
  ```
  <p id="example">   This element has extra spacing     and contains <span>a span element</span>.</p>
  ```
  
  JS
  ```
  // innerText
  document.getElementById("example").innerText;
  
  // innerHTML
  document.getElementById("example").innerHTML;
  
  // textContent
  document.getElementById("example").textContent;
  
  // output:

  // innerText returns: "This element has extra spacing and contains a span element."
  // innerHTML returns: "   This element has extra spacing     and contains <span>a span element</span>."
  // textContent returns: "   This element has extra spacing    and contains a span element."
  ```
  
   ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br> 
  
# [Attributes & properties](https://javascript.info/dom-attributes-and-properties#html-attributes)  

  - __[`getAttribute` & `setAttribute`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#accessing-attributes)__   
  - __[`style`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#style)__   
  - __[`classList`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#classlist)__  
  - __[`.parentElement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#parentelemment-access-a-parent-element)__   
  - __[`.children`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#children-it-gives-the-parent-elements-children)__   
  - __[`next/previousSibling`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#nextsibling-and-previoussibling)__
  - __[`next/previousElementSibling`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#nextelementsibling-and-previouselementsibling)__   
  - __[`Document.createElement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#documentcreateelement)__   
  - __[`appendChild`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#appendchild)__   
  - __[`append`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#append)__   
  - __[`prepend`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#prepend)__   
  - __[`insertAdjacentElement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#insertadjacentelement)__   
  - __[`after`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#after)__ and __[`before`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#before)__  
  - __[`removeChild`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#removechild)__
  - __[`remove`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#remove)__ 
  


__[Attribute](https://www.geeksforgeeks.org/what-is-the-difference-between-properties-and-attributes-in-html/)__:   
When the browser requests a page, it receives the HTML source code. It then reads (*parses*) this code and builds the DOM from it. __During this process, the HTML attributes of the elements are translated into the corresponding DOM properties__.   
So the __[attributes](https://codoschool.ru/hu/uslugi/javascript-znachenie-atributa-manipulirovanie-atributami-elementov-v-jquery.html) are HTML entities and thay can be used to add specific data to elements of HTML code.__   
- Attributes are defined by HTML and are used to customize a tag.   
- When writing HTML source code, we can __define attributes on your HTML elements__. Then, once the browser parses our code, a __corresponding DOM node will be created. This node is an object, and therefore it has properties__.   
- __An attribute extends an HTML element, changing its behavior__ or providing metadata.    
For instance, this HTML element: `<input type="text" value="Name:">` has 2 attributes (`type` and `value`). 
  
- The HTML tags may have attributes. When the browser reads the HTML to create DOM objects for tags, it recognizes *standard attributes* and creates *DOM properties* from them.

- We consider the `#ID` and `.class` as attributes, an anchor tag `<a>` an `href="#"` an `input` is also .

- When a standard attribute changes, the corresponding property is auto-updated, and vice versa.

<br>

__[Properties](https://developer.mozilla.org/en-US/docs/Glossary/property/JavaScript)__:   
The DOM is built from the HTML code parsed by the browser. During this process, the __HTML attributes of the elements__ are __translated into the corresponding DOM properties__ and __these properties are referred to by JavaScript as properties of an object__ ❗️.      
- Properties are the values associated with a JavaScript object.  
- *(The object here is the DOM node (element).*   
- So, in contrast to the __attributes, which are defined in HTML__, __properties belong to the DOM__.   
- Since DOM is an object in JavaScript, we can get and set properties.   
- Once the browser parses the HTML code (this eg.: `<input type="text" value="Name:">`), an [HTMLInputElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement) object will be created, and this object will contain dozens of properties.   
For a given DOM node object, *properties are the properties of that object*, and *attributes* are the *elements of the attributes property* of that object.

<br>

__[Attribute vs Property](https://stackoverflow.com/questions/258469/what-is-the-difference-between-attribute-and-property)__:  
 the HTML representation of a DOM element has attributes, but when represented as a JavaScript object those attributes appear as object properties.   
So, for instance we have a text-box: `<input id="the-input" type="text" value="Name:">`. If we want to know what is inside __currently__ in this text-box, we have to read the __property__. If we want to know what the __initial value__ of that text-box was, we should read the __attribute__. 
  - eg.:   
    *A property shows what is currently inside of the text-box (what the user typed in, here it's "John").*   
    *The attribue shows what was the initial value (value="Name:")*   
    HTML
    ```
    <input id="the-input" type="text" value="Name:">
    ```
    JS    
    ```
    theInput.value                 
    // returns "John"   ← property

    theInput.getAttribute('value') 
    // returns "Name:"  ← attribute
    ``` 

<br>

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[Accessing attributes](https://www.tutorialrepublic.com/javascript-tutorial/javascript-dom-get-set-attributes.php)__:
  - eg.:   
    *selecting an image from a page, it has 2 attributes here, an `id` and a `src`*   
    HTML
    ```
    <img id="myimage" src="https://images.com/">
    ```
    JS   
    *selecting for example by `id`. The 1st attribute is the `id`, 2nd is the `src`*
    ```
    document.querySelector('#myimage');

    // <img id="myimage" src="https://images.com/">
    ```
    *__we can change the `id` with  a property. And thanks to that we can impact the `id` attribute__. (we cahnge `myimage` to `myId`)*

    ```
    document.querySelector('#myimage').id;

    // 'myimage'

    document.querySelector('#myimage').id = 'myId';

    // 'myId'
    ```

<br>

## [`getAttribute`](https://developer.mozilla.org/en-US/docs/Web/API/Element/getAttribute)   
this method returns the value of a specified attribute on the element.   
So when we use `getAttribute`, the __method is getting the content directly from the HTML itself__.
  - eg.:   
    *get the `href` with the `getAttribute` method*  
    HTML
    ```
    <a href="/wiki/Asia">This is a link</a>
    ``` 
    JS
    ```
    const link = document.querySelector('a');
    
    link.href
    // 'file://wiki/Asia'    ← value by going to the JS object

    link.getAttribute('href');
    // '/wiki/Asia'          ← value directly from the HTML
    ```
    There is a difference: `getAttribute` takes the value (/wiki/Asia) directly from the HTML. Whereas when we access a property directly on an element like `link.href` that is going to the JS object.  
    So, we get different value

  <br>

## [`setAttribute`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute)   
  Sets the value of an attribute on the specified element. If the attribute already exists, the value is updated; otherwise a new attribute is added with the specified name and value.

  - we have to give 2 arguments: `Element.setAttribute(name, value);`

  - eg.:   
    *__change the value__ of the `href` with `setAttribute`.*   
    HTML
    ```
    <a href="/wiki/Asiea">Example</a>
    ```
    JS
    ```
    const link = document.querySelector('a');

    // <a href="/wiki/Asiea">Example</a>


    link.setAttribute('href', 'www.mdn.org');

    // <a href="www.mdn.org">Example</a>
    ```

## [changing element with attributes](https://www.javascripttutorial.net/javascript-dom/javascript-setattribute/): 

  - eg.:   
    *[change the `<input type="checkbox>`](https://stackoverflow.com/questions/9093992/change-html-input-type-by-js/9094047) with the __type attribute__ to colorpicker*   
    HTML
    ```
    <input type="checkbox" class="toctogglecheckbox">
    ```
    JS
    ```
    const input = document.querySelector('input[type = "text"]')       // css attribute selector
    // <input type="text">

    input.type = 'color'

    // it creates a color picker on the selected input element.
    ```
  

    *set the `<input type="">` back to text*
    ```
    input.setAttribute('type', 'text')

    // <input type="text">
    ```

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`style`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style)__:   
the [`style`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style#getting_style_information) property.  

- sets the `style` properties throught the DOM

- If we select an element and we add __`.style`__, we can see that this object contains a bunch of properties corresponding to all the individual CSS properties (like *`color`* or *`font-size`*, etc). 

- __But__ in JS everything is camelcased: so eg.: `fontSize` (and not `font-size` as in CSS)❗️


- eg.:   
  *select the `<h1>` element, and with the `.style` we see it's has a bunch of properties*   
  HTML
  ```
  <h1>I'm a title</h1>
  ```
  JS
  ```
  const h1 = document.querySelector('h1');

  h1.style;

  // output: properties that are corresponding to all the individual CSS properties.
  // ‣CSSStyleDeclaration {accentColor: '', additiveSymbols: '', alignContent: '', alignItems: '', alignSelf: '', …}
  ```

<br>

__The style object does not contain styles from our stylesheets__ ❗️ It's empty. It contains any inline styles we have assigned.

  - eg.:
    *give a color to the `<h1>` with CSS*   
    CSS
    ```
    h1 {
      color: red;
    }
    ```
    *select the `<h1>` and use stlye.color, and we see it's empty*
    JS
    ```
    h1.style.color;
    // ""
    ```
    *It contains only __inline__ styles*
    *add inline stlyes (normally not recommended!)*
    HTML
    ```
    <h1 style="color: red;">I'm a title</h1>
    ```
    JS
    ```
    h1.style.color;
    // "red"      ← now it is set to 'red'
    ```

❗️We can use the __`style` property to change the value with JS__ ❗️     
  - eg.:   
    JS   
    *change the color of the `<h1>`, without using the inline styling*
    ```
    h1.style.color = 'green';

    // "green"
    ```
    *make the fontSize larger*
    ```
    h1.style.fontSize = '3em';
    // "3em"
    ```
- Try to avoid writing styles in line❗️ so there is a better way to make changes to apply new styles to elements, which is to use a class.

- We __can't__ get the information about the HTML elments' style with the `.style` property.   
But to the current styles of any element we can use the __`window.getComputedStyle(element)`__ object. It gives the *computed style* (so once the page is loaded and the browser computed all the styles).   
It is not a selector!

  - eg.:  
    *using the `window.getComputedStyle` method to get style informations*   
    HTML
    ```
    <h1>I'm a title</h1>
    ```
    JS
    ```
    const h1 = document.querySelector('h1');

    window.getComputedStyle(h1);        // add the h1 element without paranthesis

    // output: an CSS style declaration (not an object)
    // CSSStyleDeclaration {0: 'accent-color', 1: 'align-content', 2: 'align-items', 3: 'align-self'...
    ```
    *we can access the color by specifing it*
    ```
    window.getComputedStyle(h1).color;
    // 'rgb(0, 0, 0)'    ← black

    window.getComputedStyle(h1).fontSize;
    // '32px'            
    // it gives us a string ❗️ So to change it, we have to convert it to number, then change it (eg.: adding a number, etc). 
    // and then convert it back to string.
    ```

So the `getComputedStyle` method can access the final properties that are being applied to an element without having to manually access the CSS files and/or JavaScript DOM manipulation files.       
It is useful, when it is difficult to check what class/selector was applied when multiple selectors are added to the same element. So with `window.getComputedStyle(element)` we can know what *'won'* the specificity conflicts.
    
  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

#### [`classList`](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)
it is an easy way to get the current classes on an element, but also to manipulate them, to toggle classes, to remove classes, to add classes.
      
- `classList` is an object that we can interact with to control the CSS classes on an element and also to retrieve them and to manipulate them.

- as opposed to `.getAttribute('class')` wich just just tells us exactly what the class string currently looks like, `classList` has nice methods, does more and easier.

- After __`classList`__ object we hit __`.`__ (dot) we can add methods (eg.: `h2.classList.add('border')`)

- eg.:   
  *we have an `<h2>` element, it has no classes. We have 2 CSS classes (`.purple` and `.border`)*   
  HTML   
  ```
  <h2>Contents</h2>
  ```
  CSS
  ```
  .purple {
    color: #7b07ff;
  }

  .border {
    border: 1px solid red;
  }
  ```
  JS   
  *we select the `<h2>` and we check whether it has a class or not*
  ```
  const h2 = docuemnt.querySelector('h2');

  h2.getAttribute('class')        // check if 'h2' has a class
  // null                         // it has no class
  ```
  *By __using `classList`__ we can add as many classes to our HTML element as we want*   
  *So lets make `<h2>` purple AND add a border to it.*
  ```
  h2.classList.add('purple')
  h2.classList.add('border')
  ```
  HTML   
  *Let's see the HTML which looks like this*
  ```
  <h2 class="purple border">Contents</h2>
  ```
  JS   
  *Also, we can remove classes*   
  ```
  h2.classList.remove('border')
  // border removed
  ```
  *With __`classList.contains('border') we can test if border class exist on the element (true/false)__*
  ```
  h2.classList.contains('border')
  // false

  h2.classList.contains('purple')
  // true
  ```
  *We can __toggle classes__, with __`classList.toggle()`__ It is useful when we don't know if a certain class is activated or not (so if yes, it removes)*
  ```
  h2.classList.toggle('purple')
  // false      ← it exist, so it removes the class

  // call it again

  h2.classList.toggle('purple')
  // true      ← it doesn't exist, so it ADDS the class

  h2.classList.toggle('purple')
  // false      ← it exist, so it removes the class

  h2.classList.toggle('purple')
  // true      ← it doesn't exist, so it ADDS the class
  ```
  *Many times it is used for 'accordian buttons'*

  <br>

  *A heavy and problematic way to do without `classList` is the examples below:*
  *add a class with `setAttribute` and set that class to `purple`*
  ```
  h2.setAttribute('class', 'purple')     // creates a class = "purple" in the HTML 
                                         //and <h2>'s content becomes red  
  ```
  HTML
  ```
  <h2 class="purple">Contents</h2>
  ```
  *if we want to apply another class as well to have a `border` it is difficult*   
  JS
  ```
  h2.setAttribute('class', 'purple')

  h2.setAttribute('class', 'border')    // this overrites the class="purple" to class="border", we lose "purple". 
  // output: "border"                   // but we want to keep it purple plus add border

  // we can use string template literals to have more classes 👇

  let currentClasses = h2.getAttribute('class')
  // output: "border"

  h2.setAttribute('class', `${currentClasss} purple`)              //in CSS the classes are separated by space, that's why we use 'string template literal'.
  // now we have class="purple border"
  ```

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`.parentElemment`](https://www.geeksforgeeks.org/html-dom-parentelement-property/)__: access a parent element   
  Every element has only __1 parent__ (can not have 2) (but we can have multiple children)

  - `element.parentElemment`
    - eg.:   
      *access the parent element of the `<b>` bold text*   
      HTML
      ```
      <p>
        This is a <b>Bold text</b> in the regular <br>text</b>
        and some <a>anchor</a> <a>tags</a>.
      </p>
      ```
      JS
      ```
      const boldText = document.querySelector('b');

      boldText.parentElemment;
      // ▸ <p></p>
      ```
      *if we call the `boldText.parentElemment` again, and again, it goes higher, to the grandparent, and then great grandparent parent, etc.*
      ```
      boldText.parentElemment;
      // ▸ <p></p>

      boldText.parentElemment.parentElemment;
      // ▸ <body></body>

      boldText.parentElemment.parentElemment.parentElemment ;
      //  <html lang="en">
      //   <head></head>
      //   <body></body>
      //  </html>
      ```
      *Can be useful, when a user click on a button and it changes something on the parent element*

<br>

## __[`.children`](https://developer.mozilla.org/en-US/docs/Web/API/Element/children)__: it gives the parent elements children
gives an HTML collection (looks liek an array but it's not an array! It is iterable!!!)    
  We can have multiple children!

  - `parentelement.children`
    - eg.:  
      *lets see the `const boldText`'s children*   
      JS
      ```
      const boldText = document.querySelector('b');
      
      const paragraph = boldText.parentElemment;

      paragraph.children

      // HTMLCollection(4) [b, b, a, a ]    // ← the order as these children are found in the DOM
      ```
      *lets select the 1st child*
      ```
      paragraph.children[0];
      // <b>Bold text</b>       // it's an object, eventhough it shows us in this form
      ```
      *get the parent of that first child, just for the sake of the example*
      ```
      paragraph.children[0].parentElemet;
      // <p></p>
      ```

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

 ## __[`.nextSibling`](https://developer.mozilla.org/en-US/docs/Web/API/Node/nextSibling)__ and __[`.previousSibling`](https://developer.mozilla.org/en-US/docs/Web/API/Node/previousSibling)__:    
they allow us to navigate from one element to an adjacent sibling.   
__They give us the corresponding DOM Node__! Not HTML elements. 

   - eg.:  
      *We have 3 images, lets select the 1st `<img class="firstImg">`*   
      HTML
      ```
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      <img class="firstImg" src="https://upload.wikimedia.org/firstImage.png" alt="">
      <img class="secondtImg" src="https://upload.wikimedia.org/secondImage.png" alt="">
      ``` 
  
      JS   
      *the `first.nextSibling` gives is a DOM node*
      ```
      const first = document.querySelector('.firstImg')

      first.parentElement;
      // its parent is the: <body></body> 

      first.nextSibling;
      // #text      // ← it gives us a text Node, it is not an HTML element.
      ```
   
  
 ##  __[`.nextElementSibling`](https://developer.mozilla.org/en-US/docs/Web/API/Element/nextElementSibling)__ and __[`.previousElementSibling`](https://developer.mozilla.org/en-US/docs/Web/API/Element/previousElementSibling)__:   
  they allow us to navigate from one element to an adjacent sibling.   
  gives us the actual element sibling!
  
  - eg.:  
      *We have 3 images, lets select the 1st `<img class="firstImg">`*   
      HTML
      ```
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      <img class="firstImg" src="https://upload.wikimedia.org/firstImage.png" alt="">
      <img class="secondtImg" src="https://upload.wikimedia.org/secondImage.png" alt="">
      ``` 
  
      JS   
      *the `first.nextElementSibling` gives the actual element, an image in this case*
      ```
      first.nextElementSibling;
      // <img class="firstImg" src="https://upload.wikimedia.org/firstImage.png" alt="">
      ```
      *`first.previousElementSibling` gives the `<p>` because that is before the `<img>` tag.*
      ```
      first.previousElementSibling;
      // <p></p>
      ```
   ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`Document.createElement`](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement)__:
this method can create a new DOM element.  
It creates an empty element.
So, when we create an element after we fill it (update it) with content (it can be a text or image, etc).

- we pass in the type of element we want to create

  - eg.:   
    *We create an image*   
    ```
    document.createElement('img');
    // <img>                // it only makes an empty <img> tag
    ```
    *We have an empty <img> tag, so we can give source to not show an image*
    ```
    const newImg = document.createElement('img');

    newImg                  // it is an object

    console.dir(newImg);    // it is missing it's source (src)
    // img
        accessKey: ""
        align: ""
        alt: ""
        ariaAtomic: null
        ariaAutoComplete: null
        ariaBusy: null
        ... etc.
    ```
    💡 *remember: the `console.dir()` is the way to see all the properties of a specified JavaScript object in console by which the developer can easily get the properties of the object.*   

    *Give a source*
    ```
    newImg.src = 'https://en.wikipedia.org/dog.jpg'     // but it's still not on the page → 1 way is to appendChild
    ```
    *We have an image, but it's still not on the page*  
   *1 way is to append it with __`appendChild()`__* [go to `appendChild` 👇]()

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`.appendChild`](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)__    
This method appends a node as the __last child of a node__.

  - eg.:    
    *(continue from the previous example at [`Document.createElement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#documentcreateelement))*   
    *We have to select something (`<body>`) to append to my new image (we gave to `newImg`).*   
    JS
    ```
    document.body.appendChild(newImg);

    // it appends 'newImg' (the src) as the last child of the 'body'.
    ```
    *To adjust the size to the other images of the page, we can create the same class as the other images have (here its `class="firstImage"`* 

    HTML
    ```
    <body>
      <img class="firstImage" src="https://wikipedia.org/dogs.png">
      <img class="firstImage" src="https://wikipedia.org/cats.png">

    <!-- this is our appended image -->
      <img src="https://en.wikipedia.org/American_Eskimo_Dog.jpg">              
    </body>
    ```
    *using `classList.add`*     
    JS   
    ```
    newImg.classList.add('firstImage');

    // The HTML 👇 
    // <img src="https://en.wikipedia.org/American_Eskimo_Dog.jpg">  
    ```

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`.append`](https://developer.mozilla.org/en-US/docs/Web/API/Element/append)__   
this method is used to insert Node objects after the last child of the ParentNode.   
It allows us to __insert more than one thing at a time__ so we can have two different nodes to insert or multiple different elements we have created.

  - eg.:   
    *We call `.append` and pass a text "Hello there!" in the `<p>`, it just puts it to the end of the <p>* 
    HTML  
    ```
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    ```
    JS
    ```
    // select <p>
    const p = document.querySelector('p');

    p.append('Hello there!');
    ```
    HTML  
    ```
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Hello there!</p>
    ```
  - add __more than 1 thing with `Element.append()`__
    - eg.:   
      *add 2 pieces of texts*  
      JS
      ```
      // select <p>
      const p = document.querySelector('p');

      p.append('Hello there!', 'Goodbye people!');
      // both element is appended → see the html
      ```
      HTML
      ```
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Hello there!Goodbye people!</p>
      ```

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`.prepend`](https://developer.mozilla.org/en-US/docs/Web/API/Element/prepend)__   
This method allows us to insert something as __the first child__ of some elements (like at the beginning).

  - eg.:   
    *we create a bold `<b>` element with `createElement`, and inside that we add some text `append`...*       
    *... then, we want the 'Hello!!!' text in the __beginning__ of the `<p>` paragraph*  
    HTML  
    ```
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    ``` 
    JS
    ```
    // select <p>
    const p = document.querySelector('p');

    // create <b>
    const newBold = document.createElement('b');

    // add text
    newBold.append('Hello!!!')

    // prepend the <b> to the beginning of the <p> ❗️
    p.prepend(newBold)
    ```
    HTML
    ```
    <p><b>Hello!!!</b>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    ```
    With `.prepend` the element became the first __child__ now, instead of the last.

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`.insertAdjacentElement`](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentElement)__   
this method inserts a given element node at a given position relative to the element it is invoked upon.

- we have to specify the [position](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentElement#parameters):   
    __'beforebegin'__: Before the targetElement itself.   
    __'afterbegin'__: Just __inside__ the targetElement, __before its first child__.   
    __'beforeend'__: Just __inside__ the targetElement, __after its last child__.   
    __'afterend'__: After the targetElement itself.

- syntax: `targetElement.insertAdjacentElement(position, element);`

- eg.:   
  *I want to insert something between an `<h1>` and an `<img>` image. So after the `<h1>` befor the `<img>`.*   
  HTML
  ```
  <h1>Title</h1>
  <img class="firstImage" src="https://wikipedia.org/dog.png">
  ```
  JS
  ```
  const h2 = document.createElement('h2');
  // <h2></h2>

  //put some text there
  h2.append("Hello nice people!");
  // <h2>Hello nice people!</h2>

  // lets put that <h2> after the <h1>
  // select <h1>
  const h1 = document.querySelector('h1');

  // lets place <h2> after the target element( <h1> )
  h1.insertAdjacentElement('afterend', h2);
  ```
  HTML
  ```
  <h1>Title</h1>
  <h2>Hello nice people!</h2>
  <img class="firstImage" src="https://wikipedia.org/dog.png">
  ```

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`.after`](https://developer.mozilla.org/en-US/docs/Web/API/Element/after)__   
  this method inserts an element after some other element.

  - eg.:  
    *we create an `<h3>` and add some text*   
    HTML
    ```
    <h1>Title</h1>
    <img class="firstImage" src="https://wikipedia.org/dog.png">
    ```
    JS
    ```
    const h3 = document.createElement('h3');
    
    //add text
    h3.innerText = 'I am h3!!!';

    //select h1
    const h1 = document.querySelector('h1');

    //insert <h3> after <h1>
    h1.after(h3);
    ```
    HTML
    ```
    <h1>Title</h1>
    <h3>I am h3!!!</h3>
    <img class="firstImage" src="https://wikipedia.org/dog.png">
    ```

## __[`.before`](https://developer.mozilla.org/en-US/docs/Web/API/Element/before)__   
  this method inserts an element before some other element. Basically works the same as `.after` method.

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

## __[`removeChild`](https://developer.mozilla.org/en-US/docs/Web/API/Node/removeChild)__
this method removes a child node from the DOM and returns the removed node.   
So the way that it works is that we don't actually remove the particular element we have selected. __We remove a child from an element❗️__

- call the method on the parents of what we want to remove (hence the name remove child).

- syntax: `parent.removeChild(child);`

- has full browser support (Internet Explorer too)

- [eg.:](https://developer.mozilla.org/en-US/docs/Web/API/Node/removeChild#examples)  
  *If we want to remove an `<li>`, we can't just select the the `<li>` and `removeChild`. Instead, we have to select the parent, the `<ul>`, and then call remove child and pass in the `<li>`.*   
  HTML
  ```
  <ul>
    <li>List 1</li>
    <li>List 2</li>
    <li>List 3</li>
  </ul>
  ```
  JS
  ```
  const ul = document.querySelector('ul');
  const li = document.querySelector('li');

  ul.removeChild(li)      // ← removes the FIRST <li>
  ```
  *a __'one-go-way'__, commonly used: call the parent of the child __[`parentElement`](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentElement)__, and then remove the child, all in one line.*
  ```
  const li = document.querySelector('li');

  li.parentElement.removeChild(li)
  ```

  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)


## __[`remove`](https://developer.mozilla.org/en-US/docs/Web/API/Element/remove)__   
This method removes the element from the tree it belongs to.   
So, we call on the actual thing we want to remove, and we don't have to worry about the parent or the child.

- syntax: `node.remove()`  

-  has no full browser support (Internet Explorer does not support it)

- [eg.:](https://developer.mozilla.org/en-US/docs/Web/API/Element/remove#examples)   
  *remove the image*    
  HTML
  ```
  <body>
    <img class="image" src="wikipedia.org/dog.png">
  </body>
  ```
  JS
  ```
  const img =document.querySelector('img');

  img.remove();
  // images has been removed
  ```
  
  ---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `Attributes & properties`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#attributes--properties) OR [👆go up to JS DOM manipulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-manipulation)

<br>

# [DOM events](https://developer.mozilla.org/en-US/docs/web/api/event)    
creating interactive websites: responding to user events (inputs  and actions), so running a code when a user does something.

- __[inline events](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#inline-events)__   
- __[`addEventListener`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#addeventlistener)__   
- __[`this` as event handler](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#this-as-an-event-handler)__.  
- __[Event Objects](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#event-objects)__   
- __[`keyboardEvent`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#keyboardevent)__
- __[`Event.preventDefault`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#eventpreventdefault-using-a-form)__   
- __[`input.value`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#inputvalue)__
- __[`Change Event`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#change-event)__ & __[`Input Event`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#input-event)__ 
- __[Event Bubbling & `stopPropagation`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#event-bubbling)__
- __[Event Delegation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#event-delegation)__

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>


## __[inline events](https://www.htmlgoodies.com/javascript/working-with-inline-event-handlers/)__        
Inline events are bound to an element by their attribute name, which starts with the “on” prefix. Not all event types may be bound to all elements.
  

<br>

- __[Event references](https://developer.mozilla.org/en-US/docs/Web/Events#event_listing)__    
includes lots of properties we can use.   
*💡 especially useful for the [`addEventListener`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#addeventlistener)'s*
  
  - *[`onlcick`](https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onclick)*

  - *[`onmouseover`](https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onmouseover)*

  - *[`onmouseenter`](https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers/onmouseenter)*

  - *etc.*

<br> 

When a user clicks on a button something will happen. How to do it? There are 3 approaches: 
   1. write a code into the `<tag>`
   2. write a code in a JS file using a selector and function
   3. using the `addEventListener` method. 

<br>

  __1. way (BAD PRACTICE)__:    
  write the code in the tag:     
  (makes our markup longer, makes it difficult to write and so on, in short: it sucks.) 

  - eg.:   
  *The user clicks on the button. We add an attribute to the `<button>` tag which is named `onclick`.*      
  *Between the quotes in `onclick=""` we can write the code that we want to run when the user clicks.*   
    HTML + JS
    ```
    <button onclick="alert('You clicked!')">Click me!</button>

    <!-- Alert pops up with the 'You clicked!' message -->
    ```

<br>

__2. way__ :  
  we write the code in our JS file.   
  We need to have elements that we can select (with `querySelector` or other __selectors__).

  - eg.:   
    *When a user clicks on the button, something will happen. In our JS file we select a button using its `id`.*     
    HTML
    ```
    <button id="myBtn">Click me!</button>
    ```
    JS   
    *Using `onclick` property, often people use an inline function expression*   
    *__We are setting a property to be a function❗️__*   
    *The function is never executed, it is __called by the__ `onclick` __property__ when the user clicks.*   
    ```
    const btn = document.querySelector('#myBtn');

    //set the property
    btn.onclick = function() {
      console.log("You clicked!")
    }

    // when we click on the button, it runs the function
    // 'You clicked!'

    // to see if it is set to a function, we write:
    btn.onclick; 
    // f ()  { console.log("You clicked!") }
    ```
    *we can add an `onmouseenter` property, when a mouse enters the zone, it calls the function.*   
    *Also, we can write a function separately (here the `shout()` function), and then pass it into the`onmouseenter` property.*
    ```
    btn.onclick = function(){
      console.log("You clicked!")
    }

    function shout(){
      console.log("HELLLLOOOO!!!")
    }

    btn.onmouseenter = shout;
    ```

  - 💡When we use these properties, what we supposed to do is __set that specific property__ (eg. the `onclick` property) __to a function.__    
  So the value should be a function, it should reference a function.     
    - eg.:  
      *we can click on the `<h1>Events</h1>` title*   
      JS
      ```
      document.querySelector('h1').onclick = function () {
        alert('You have clicked on the title');
      }
      ``` 
      *if we DON'T set the property `onlcick` into a function, the code will execute right away.   
      That is why we have to set the property `onclick` to a function (as we have done above).*
      ```
      // this DOES NOT WORK!!!!!!
      document.querySelector('h1').onclick = alert('You have clicked on the title');
      ```

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>

__3. way__ :

## __[`addEventListener`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)__  
this method sets up a function that will be called whenever the specified event is delivered to the target.     
So: we can pass in any sort of event.   
If we want to listen for a click, a doubleclick, etc. __we can just pass in that string__ (like 'click', 'doubleclick', etc.) and add the second argument which is our __callback function__ (the code that we want to run when that event actually occurs).

- syntax: `something.addEventListener(' what to listen for ', function() 
{ call back - the code what we want to run } )`   
so in a short way (from [MDN](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener#syntax)):    
`addEventListener(type, listener);`   
`addEventListener(type, listener, options);`

- *💡 useful source for __[event listings](https://developer.mozilla.org/en-US/docs/Web/Events#event_listing)__*

- eg.:   
  *using `addEventListener` on a `<button id="button2">Click</button>`*   
  JS
  ```
  // select the button
  const btn = document.querySelector('#button2');

  // set addEventListener

  btn.addEventListener('click', function() {
    alert("Clicked!")
  })
  ```
- a great advantage of `addEventListener` is that we can combine lines, and it executes them withouth overwriting them (eg. overwrite the first line when it gets to the second):
  - eg.:   
    *we have two functions, when we click on a `<button>` one prints out 'Hello!' the other 'Goodbye!', and we want them to appear one after the other.*   
    *Using the `addEventListener` the 'Hello!' will not be overwritten by 'Goodbye!'. It means that __we can have as many callbacks as we want!__*   
    JS
    ```
    // select button
    const btn = document.querySelector('button');

    // create 2 functions
    function hello() {
      console.log('Hello!')
    }

    function bye() {
      console.log('Goodbye!')
    }

    // pass the function to the addEventListener
    btn.addEventListener('click', hello)
    btn.addEventListener('click', bye)

    // Hello!
    // Goodbye!
    ```
    *But with another way, by approaching property on the object directly (as it is below) we can see that it CAN NOT HAVE MORE THAN ONE. on the same `btn` object. Because the second function will overwrite the first function.*
    ```
    btn.onclick = hello;
    btn.onclick = bye;
    // Goodbye!         // ← we only getting 'Goodbye!'
    ```

- __[the option parameter](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener#parameters)__   
An object that specifies characteristics about the event listener. 
__`addEventListener(type, listener, options)`__

  option objects:
  - once:   
    A boolean value indicating that the listener should be invoked at most once after being added. If true, the listener would be automatically removed when invoked.
  - passive
  - signal

- eg.:   
  *the first function will run the callback only once, then it removes the `eventListener`, but the second one stays as we didn't include the __`once` option object__*  
  JS
  ```
  const btn = document.querySelector('button');
  
  function hello() {
      console.log('Hello!')
    }

  function bye() {
      console.log('Goodbye!')
    } 

  btn.addEventListener('click', hello, { once : true })
  btn.addEventListener('click', bye)  

  // click the button 3 times
  // 1. 'Hello!'
  // 1. 'Goodbye!'
  // 2. 'Goodbye!'
  // 3. 'Goodbye!'
  ```
 
 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>

## __[`this.` as an event handler](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this#as_a_dom_event_handler)__
when a function is used as an *event handler*, its `this` is set to the element on which the listener is placed.

  - eg.:   
    *We have 3 buttons and 3 `<h1>` titles, and we change their background when we click on them*   
    HTML
    ```
    <button>Click</button>
    <button>Click</button>
    <button>Click</button>

    <h1>Click me!</h1>
    <h1>Click me!</h1>
    <h1>Click me!</h1>
    ```
    JS   
    ```
    // select all the <button>s
    const buttons = document.querySelectorAll('button');

    // select all the <h1>s
    const titles = document.querySelectorAll('h1');

    // loop over all the <button>s
    for (let btn of buttons){
      btn.addEventListener('click', function(){
        btn.style.backgroundColor = 'red';       // button's background turns to red
        btn.style.color = 'blue';                // button's text turns to blue
      })
    }

    // loop over all the <h1>s
    for (let h1 of titles){
      h1.addEventListener('click', function(){
        h1.style.backgroundColor = 'red';
        btn.style.color = 'blue';       
      })
    }
    ```
    *__Using `this`__ we can save lines, and put all the repetitive code lines into a separate function (here: `colors()`)`* 

    *We replace the function in the `...addEventListener('click', function() {...})` with the function we have created separetaly (`colors()`) → ...addEventListener('click', colors())`*  
    ```
    function colors() {
      this.style.backgroundColor = 'red';     // the 'this' becomes the 'btn' and the 'h1'
      this.style.color = 'blue';
    }

    for (let btn of buttons){
      btn.addEventListener('click', colors(){
    }
    for (h1 btn of titles){
      btn.addEventListener('click', colors(){
    }
    ```
    
 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>    

## __[Event Objects](https://www.codecademy.com/courses/build-interactive-websites/lessons/dom-events/exercises/event-object-property)__
Event Object Represents is an object that contains information about an event that has occurred.     

When an *event listener’s* event occurs and it calls its associated function, it also passes a single argument to the function (a reference to the event object). The event object contains a number of properties that describe the event that occurred.   

__The event object is automaitcally passed every single time in to our callback function.__    
So it is basically an object which contains information about the event.

*[read more about this topic](https://medium.com/launch-school/javascript-lets-talk-about-events-572ecce968d0)*

- eg.:   
  *We create a `<button>` click event. The event object is automaitcally passed into our callback function. We can capture it as putting a parameter (name it `event`, but it can be anything) into our callback function.*   
  JS
  ```
  document.querySelector('button').addEventListener('click', function (event){
    console.log(event);       //← event is an object, it contains information about the object ❗️
  })

  // PointerEvent {isTrusted: true, pointerId: 1, width: 1, height: 1, …}
    isTrusted: true
    altKey: false
    altitudeAngle: 1.5707963267948966
    azimuthAngle: 0
    bubbles: true
    button: 0
    buttons: 0
    cancelBubble: false
    cancelable: true
    clientX: 28         // ← realtive to the window (coordinates)
    clientY: 17         // ← realtive to the window (coordinates)
    type: "click"       // event type
    …etc
  ```

 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>    

## __[KeyboardEvent](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent)__   
__*KeyboardEvent objects* describe a user interaction with the keyboard.__    
Each event describes a single interaction between the user and a key on the keyboard.   
The __event type__ *(keydown, keypress, or keyup)* __identifies what kind of keyboard activity occurred__.

- keydown
- keypress
- keyup

<br> 

- eg.:    
  *The user PRESSes DOWN a button on the keyboard, so typing in the `<input type="text" >`, and that creates the 'keydown' event, and it prints "You pushed key down!"*  
  JS   
  ```
  // select input
  const input = document.querySelector('input');

  input.addEventListener('keydown', function() {
    console.log("You pushed key down!");
  })

  // typing randomly: asdf+enter // ← 'keydown' event occurs
  // ("You pushed key down!")
  // ("You pushed key down!")
  // ("You pushed key down!")
  // ("You pushed key down!")
  //  …etc
  ```
  *Now we use 'key up'. The user press a button on the keyboard and the release it → UP.*   
  ```
   input.addEventListener('keyup', function() {
    console.log("It is a key up!");
  })

  // 3 times we release the keys
  // "It is a key up!"
  // "It is a key up!"
  // "It is a key up!"
  ```

  <br>
__What key is pressed?__    
To find it out, we use the `event` object in the call back function. The `keyboardEvent` object has several objects, here we are looking for 2 specific: the *'key'* and the *'code'*. Using them we can knwo what buttons were used on the keyboard.

- eg.:  
 *If we want to know what key was pressed on the `<input>`, we look into the __keyboardEvent__ object*   
 JS
 ```
  // select 'input'
  const input = document.querySelector('input');

  input.addEventListener('keydown', function(event) {
        console.log(event);
      })

    // prints out he keydown event object. We pressed "a" button. 
    // KeyboardEvent {...}
    // "KeyA", ....
    // ...
    // code: "KeyA"           // ← the "location" on the keyboard
    // detail: 0
    // eventPhase: 0
    // isComposing: false
    // key: "a"               // ← the character that was generated 
    // keyCode: 65
  ```
  *If we want to listen for the global keyboardEvent, we ca nuse `window`.*   
  *__We want to jnow what key is pressed, what the `key` object__: we add the `code` after the `event`.*
  ```
  window.addEventListener('keydown', function (event) {
    console.log(event.code);        // ← it will show the 'code'
  }) 
  
  // we just type on the window somewhere (up, right, left arrows)
  // ArrowUp
  // ArrowRight
  // ArrowLeft
  ```
  *If we want to ignore all keyboard buttons, excepet the arrow button (lets say we make a game), we use the [`switch statement`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#switch-statement)*
  ```
  window.addEventListener('keydown', function (event) {
    switch(event.code){
      case 'ArrowUp':
        console.log("you pressed UP!");
        break;
      case 'ArrowLeft':
        console.log("you pressed LEFT!");
        break;
      default:
        console.log("Ignored");
    }       
  }) 

  // pressing keyboardbuttons calls the 'default. Pressing the 'up arrow' then 'left arrow':
  // "Ignored"
  // "Ignored"
  // "you pressed UP!"
  // "you pressed LEFT!"
  ```
  
  ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>  

## __[`Event.preventDefault` (using a `<form>`)](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault)__
__This method cancels the event if it is cancelable, meaning that the default action that belongs to the event will not occur.__    
*(Like clicking on a "Submit" button, prevent it from submitting a form)*

- eg.:   
  *When we click to "Submit" in the `<form>`, it leads us to another page: `.../local?`*    

  *Let's say we don't want to lead us to another page* 

  *So how does it work? In HTML, when the `action` attribute is set to something (here "local") that is where the data (what we put in the `<input>`) will be sent to. And our browser window end up at that location as default behaviour*
  HTML  
  ```
  <form action="/local" id="localID">
    <input type="text">
    <button>Submit</button>
  </form>

  <!-- we click on the "Submit" → it goes to another page ".../local?" -->
  ```
  *Let's have a form that a user can submit, but we basically prevent it from changing the page, using the `event.preventDefault` method.*   
  *So we stay on the same page and we do something with the form data.*   
  JS
  ```
  // selecting the <form> id
  const form = document.querySelector('#localID');

  // adding eventListener when the form is submitted
  form.addEventListener('submit', function(event){
      event.preventDefault()                          // ← prevents the default behavior triggered by a given event
      console.log("Form is submitted!");
  })
  
  // result: 
  // the event is fired, the page doesn't go to ".../local?", the page stays.
  // "Form is submitted!"
  ```
  
 <br>
 
 
- How can we __extract data from the `<form>`__? With the __`input.value`__ attribute❗️

  ---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br> 

## __[`input.value`](https://www.geeksforgeeks.org/html-input-value-attribute/)__
The value attribute for <input> element in HTML is used to specify the initial value of the input element.

- *([continued from the previous exmaples](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#eventpreventdefault-using-a-form
)* eg.:    
  *We want to make a list with the words we write in the `<input>`. So when we hit the 'submit' button we want to take that value extracted from the `<form>` and appear in a `<ul>` list on the page.*   
  *So we want to append different items to the `<ul>` list.*   
  *Our goal is that when we click the 'submit', we want to take that input value and then make a new `<li>`. Then clear, reset the `<input>`.*    
  HTML
  ```
  <!-- we add a <ul> under the <form> where the submitted value will appear -->

    <form action="/local" id="localID">
      <input type="text" id="itemInput" name="itemName">
      <button>Submit</button>
    </form>

    <h2>List of items</h2>
    <ul id="list"></ul>
   ```     
   *We select the `<input>`'s value. We use `input.value`, and the __`value`__ attribute shows the value of the `<input>`, shows what is currently in the `<input>`.*       
   *❗️ If we write in the console `input.value`, it shows what is currently in the `<input>`.*   
   *❗️ When input is empty → `input.value = ""`*    
   JS
  ```
  // selecting the <form> id
   const form = document.querySelector('#localID');
   
  // selecting the input
   const input = document.querySelector('#itemInput');
   
  form.addEventListener('submit', function(event){
    event.preventDefault()      
    console.log("Form is submitted!");
    console.log(input.value);     // ← it shows what is currently in the input in the console (not on the page!)
  })
  ```
  *Now, we have to make a new `<li>` with the value what's in the `<input>`.*    
  JS
  ```
  // selecting the <form> id
   const form = document.querySelector('#localID');
 
  // selecting the input 💡 there are 2 ways to select the input. 1.'#id', 2.'name' element
   const input = document.querySelector('#itemInput')    // ← 1. selecting by '#id'
  // const input = localID.elements.itemName;            // ← 2. selecting by 'name': (form's "#id") + (elements) + (input's "name")


  // selecting the <ul id="list">
  const list  = document.querySelector('#list');

  form.addEventListener('submit', function(event){
    event.preventDefault()      
    console.log("Form is submitted!");
    // console.log(input.value);    
    
    const itemType = input.value;     //←  what's in the <input> we want to save it to a variable
    
    const newLI = document.createElement("LI");   // ← creating a new empty `<li>`

    newLI.innerText = itemType; // ← add the itemType to the empty `<li>` (newLI)
    
    list.append(newLI);         // ← we have to show the 'item' on the page, we have to append it to the 'const list' (the <ul>) 
  })
  ```
  *Now, we have to __reset the input form__ so it goes back to empty: `input.value = ''`*   
  JS
  ```
  form.addEventListener('submit', function(event){   // 1.
    event.preventDefault() 
    
    console.log("Form is submitted!");     
    
    const itemType = input.value;                    // 2.
    
    const newLI = document.createElement("LI");      // 3.
    
    newLI.innerText = itemType;                      // 4.
    
    list.append(newLI);                              // 5. 
    
    input.value = ""                                 // 6.  reset the input form     
  })
  ```
  *The process we did:*   
  *1.* *We prevented the default behavior so that the form doesn't go to another page.*    
  *2.* *Then we take the value from the input.*   
  *3.* *Then we extracted the value and then we made an empty `<li>`.*   
  *4.* *Then we added the value into the empty `<li>`.*   
  *5.* *Then we append that to our `<ul>`.*    
  *6.* *Then we reset the `<input>` form to empty.*

<br>

  - another eg.:   
      *`<form>` element contains 2 `<input>` elements, 1 for quantity and 1 for product. We want to add the product and qulaity next to each other, into a new `<li>` after each time we submit.*   
    HTML
    ```
    <h1>Grocery List</h1>
    <form action="/nowhere">
        <label for="item">Enter A Product</label>
        <input type="text" id="product" name="product">
        <label for="item">Enter A Quantity</label>
        <input type="number" id="qty" name="qty">
        <button>Submit</button>
    </form>
    
    <ul id="list"></ul>
    ```
    JS
    ```
    const form = document.querySelector('form');            // selecting the <form>
    const product = document.querySelector('#product');     // selecting the product <input>
    const qty = document.querySelector('#qty');             // selecting the qunatity <input>
    const list = document.querySelector('#list');           // selecting the <ul> list

    form.addEventListener('submit', function(event){
       event.preventDefault();                              // prevent form
       const productName = product.value;                   // we take the value from the product input
       const qtyName = qty.value;                           // we take the value from the qunatity input
       const newList = document.createElement('li');        // we create a new empty <li>
       newList.innerText = `${productName}, ${qtyName}`;    // we using template literals to put product and qty next to eachother + we add them to the <li>
       list.append(newList);                                // we append the <li> (newList) to our <ul> (#list)
       product.value= "";                                   // we reset the product input   
       qty.value= "";                                       // we reset the quantity input
    });
    ```
  ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>  

## __[Change Event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event)__
The change event is fired for `<input>`, `<select>`, and `<textarea>` elements when an alteration to the element's value is committed by the user.   
Unlike the input event, the change event is not necessarily fired for each alteration to an element's value.

- eg.:   
  *An `<h1>` and an `<input>`. Let's say we want to do something every time this input is updated.*   
  *The __change input only fires__ when we actually "blur" the input, which means leaving it the input, not clicking in it, __when we click away from the input__.*   
  HTML
  ```
  <h1>Type something below: </h1>
  <input type="text">
  ```
  JS    
  *We type soemthing into the `<input>` __nothing happens__.   We run the code, and it only prints out the "Change event has occured" text when we click away from the input.*
  ```
  // selecting the <input>
  const input = document.querySelector('input');

  // listen for the change event❗️
  input.adEventListener('change', function(event){
      console.log("Change event has occured");
  })
  ```
  *Changing the `<input>` means changing the value (what we type in into the `<input>`). __Change event__ only runs when we blur out (not when we type in the `<input>`).*

  💡 So thinking of it whatever you leave in that `<input>`, and it is __different__ than it was when you entered the `<input>`. So not whatever you see changing in that `<input>`. 
  
  💡 The `change` event is very useful when we use a [`<select>`](https://github.com/Klosmi/html-basics/blob/master/HTML-forms.md#select-) (HTML Select element).
  

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>  

## __[Input Event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/input_event)__    
The input event fires when the value of an `<input>`, `<select>`, or `<textarea>` element has been changed.   
*(Clicking away and or in doesn't matter.)*

The `input event` fires as soon as we type something in the `<input>`.

- eg.:   
 *When we change the value in the `<input>`, that fires the `event`.*   
  HTML
  ```
  <h1>Type something below: </h1>
  <input type="text">
  ```
  JS    
  *We type soemthing into the `<input>` and it fires the event, it prints out the "Input event event has occured".*
  ```
  // selecting the <input>
  const input = document.querySelector('input');

  // listen for the input event❗️
  input.adEventListener('input', function(event){
      console.log("Input event has occured");
  })
  ```

-  another eg.:   
    *Updating `<h1>` with the value what we type into the `<input>`*   
    HTML
    ```
    <h1>Type something below: </h1>
    <input type="text">
    ```
    JS    
    *We have input in a variable and we update the `<h1>`, whatever the `value` is (`input.value`).*   
    *So whenever the value changes inside of the `<input>` (input event) we take that value (`input.value`) and update the `<h1>` to display it (`innerText`).*
    ```
    // selecting the `<input>`
    const input = document.querySelector('input');

    // selecting the <h1>
    const h1 = document.querySelector('h1');

    // listen for the input event❗️
    input.adEventListener('input', function(event){
        h1.innerText = input.value;
    })          
    ```
    *We type "HELLO" into the `<input>` and the `<h1>` textt becomes "HELLO" as well.*    
     HTML
      ```
      <h1>HELLO</h1>
      <!-- we type "Hello" -->
      <input type="text">
      ```
      
 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>  


## __[Event Bubbling](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#event_bubbling_and_capture)__
  When an event is triggered first on an element, and that element has a parent element, which also has a parent element, etc, and they all have events, all these event are triggered.    
  
  __We describe this by saying that the event bubbles up from the innermost element that was clicked.__ (So the bubbling start from the buttom towards the top.)


- eg.:    
  *We have a `<button>` inside of a `<p>` paragpraph, which is inside of a `<section>`. All the elements have an `onclick` event.*  
  HTML
  ```
  <section onclick="alert('Section clicked!')">
    <p onclick="alert('Paragpraph clicked!')">
      <button onclick="alert('Button clicked!')">Click!</button>
    </p>
  </section>  
  ```
  *When we click on the `<button>`, it creates __bubbling__, because `<button>` triggers the `<p>`, and then the `<section>`.* 
  
#### __[`event.stopPropagation`](https://developer.mozilla.org/en-US/docs/Web/API/Event/stopPropagation)__: 
  a method that stops the bubbling

  - syntax: __`event.stopPropagation();`__

  - eg.:   
    *We have a `<button>` inside a `<div>`. When we click on the `<button>` it should change the background color to blue.
    When we click on the `<div>` it hides the `<div>` (so hides also the background color and `<button>`)*    
    HTML
    ```
    <div id="container">
        Please Hide me!
        <button id="changeColor">Change Color</button>
    </div>
    ``` 
    *We include a CSS class `.hide` which has a `display: none;`. We use this with the `classList` property in the JS file.*   
    CSS
    ```
    .hide {
      display: none;
    }
    ```
    JS    
    *When we click on the `<div>` element (which has the text: "Please Hide me!") it hides the `<div>` and its child `<button>`.*
    *Since the `<button>` is inside of a `<div>`, when we click on the `<button>` it triggers the `<div>` instead of changing the background color, it hides all the elements → bubbling.*   
    *__To stop that bubbling, we include the `event.stopPropagation()`__*
    ```
    const button = document.querySelector('#changeColor');
    const container = document.querySelector('#container');

    button.addEventListener('click', function (event) {
        container.style.backgroundColor = "blue";         // blue background
        event.stopPropagation();                          // stop the bubbling
    })

    container.addEventListener('click', function () {     // we get the current class (.hide) on the <div> element
        container.classList.add('hide');
    }) 
    ```
    *So what happens is that when we click on the `<button>` the last line of its function is the `event.stopPropagation();` which stops the bubbling.*

 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>  

## __[Event delegation](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#event_delegation)__
  It adds the event listeners to the parent elements.

  So instead of attaching the event listeners directly to the child element(s) (eg. a `<button>`), you *delegate* the listening __to the parent element__ (eg. `<div>`).   
  When a `<button>` is clicked, the listener of the parent element catches the bubbling event.   

  The event delegation is a useful pattern because you can listen for events on multiple elements using one event handler.

- eg.:   
 *Let's say we can add comments by writing a text into an `<input>`. Every comment gets a new `<li>` elemtnt (that is how we'll see on the page)*   
 *By clicking them, we want to remove them (using the `element.remove()` method)*      
 HTML
```
<form action="/local" id="localID">
    <input type="text" id="itemInput" name="itemName">
    <button>Submit</button>
</form>

<h2>List of items</h2>
<ul id="list"></ul>
```
JS
```
// selecting the <form>
const form = document.querySelector('#localID');

// selecting the <input>
const input = document.querySelector('#itemInput');

// selecting the <input> with its ID
const input = document.querySelector('#itemInput')

// selecting the <ul id="list">
const list  = document.querySelector('#list');


form.addEventListener('submit', function(event){
  event.preventDefault()  
  const item = input.value;                     //←  what's in the <input> we want to save it to a variable
  const newLI = document.createElement("LI");   // ← creating a new empty `<li>`
  newLI.innerText = itemType;                   // ← add the itemType to the empty `<li>` (newLI)
  list.append(newLI);                           // ← we append <li> to the 'const list' (the <ul>) to show on the page
  input.value = ""                              // reset the input form     
})
```
*EVENT DELEGATION (we use the parent:`<ul>`, to select the `<li>`*   
*By clicking on the `<li>`, which is just created, we can delete that `<li>`. So to do this we select the `<li>`'s parent the `<ul>`.*   
*Since each `<li>` is under the `<ul>`, we can 'click' on the `<li>` and it will work. But we have to specify which `<li>` we are clicking on.*    
*To tell the borwser which `<li>` we 'click', we have to use the __'target' property__ (part of the __'event' object__).*   
*__The 'target' property shows which `<li>` we are clicking on__*
```
// select <ul>
const list  = document.querySelector('#list'); 

// listening for the 'click' on the <ul>. 

list.addEvenetListener('click', function(event){
  // we have to make sure that we click on is an <li> type
  // then we remove that <li> type
  if(event.target.nodeName === 'LI') {
  event.target.remove()         // the thing which we clicked on + remove it
  }
})
```
*💡 the `event.target.nodeName`: the way we can get this is by writing the `console.dir(event.target)`. Then we can see in the console, all the properties of the `<li>` object. Among these properties, we can see the [`nodeName`](https://developer.mozilla.org/en-US/docs/Web/API/Node/nodeName).* 

- [useful to read about event delegation](https://dmitripavlutin.com/javascript-event-delegation/)

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to top to `DOM events`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#dom-events)

<br>  


# [Asynchronous JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Introducing)    
Synchronous JS:   
JS is a single-threaded programming language which means __only one thing can happen at a time.__ That is, the JS engine can only process one statement at a time in a __single thread__.   
This is why we can’t perform long operations (such as network access) without blocking the main thread.

__[Asynchronous JS](https://blog.bitsrc.io/understanding-asynchronous-javascript-the-event-loop-74cd408419ff):__   
using asynchronous JavaScript (such as callbacks, promises, and async/await), we can perform long network requests __without blocking the main thread__.

- __[Call Stack](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#call-stack)__
- __[Single Threaded ](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#single-threaded)__
- __[Web API](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#web-api)__
- __[Callback hell](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-hell)__
- __[Promise](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise)__   
- __[The `aync` keyword](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#async-keyword)__
- __[The `await` keyword](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#await-keyword)__   
- __[`try..catch` statement and error handling](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-trycatch-statement-and-error-handling-in-async-functions)__

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
  
<br>

## __[Call Stack](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)__   
is a mechanism for JS interpreter (in a browser) to keep track of its place (to know where it is) in a script that calls multiple functions.

So, this is how JavaScript knows where it is (like a bookmarker): what function is currently being run and what functions are called from within that function, etc.   
In other words, JS keeps track of the history of things that are waiting to be returned, so __which functions have been invoked but are not done yet__. Call Stack is the structure which stores that *(data structure)*.

__Stack__:  
 is a basic data structure in computer science.

 __LIFO:__ last in, first out    
 *(the last thing we added to the top, and that's the first thing that we remove)*
 
 <br>

 __How the call stack works?__   
 1. When a script calls a function (invoke a function), the interpreter adds it to the call stack and then starts doing (carrying out) the function.

 2. Any functions that are called by that function are also added to the call stack further up, and run where their calls are reached.

 3. When the current function is returned, the interpreter takes it off the stack and it continues the execution where it left off in the last code listing.

So the most recently invoked function is on the top of the stack.   
The bottom of the stack is the first function invoked.   
The stack is processed from top to bottom.   
 - eg.:   
   *We are calling the `second()` (on line 9). It calls the `function second()` on line 5, on line 6 the return doesn't return right away, because it has to call `function first()` on line 1, which returns the string "First" on line 2. Then it popps off, goes to line 6, return the string, popps off, and at line 10 we have the function invocations's result.*    
   *The stack is the following:*    
   *Starts at line 9, then line 6 (the return) then line 2. Line 2 returns so it's popped of because the top value of the stack is removed. Then it goes back at line 6, we return the string and then it's popped of and then we are at line 10.*    
   *__the last thing which is added to the top__ (`function first()`) __is the first thing to come off__ → LIFO*
   ```
   1. function first() {
   2.   return "First"
   3.  }
   4.
   5.  function second() {
   6.   return first() + "Second!";
   7.  }
   8.
   9.  second();
   10. // "First Second!"
   ```

- eg.:   
  *We have a function that calls another function.*   
  *`function isRightTriangle(a,b,c)` can't give us an answer, it has to call `function square(x)`, and this has to call the `function multiply(x,y)`*  
  *Then `function multiply(x,y)` gives a value and this function get removed from the stack, the value goes to `function square(x)` then the function removed from the stack, and finally the velue 9 goes to `isRightTriangle(9,b,c)`.*   
  *And it starts over again.*
  ```
  function multiply(x,y) {            // ← 1. x=3 * y=3 | 2. x=4 * y=4 | 3. x=5 * y=5  
      return x * y;                   // (Note: x and y can be called anything else, like x and x, a & b, c & c, etc.)
  }

  function square(x) {                // first its x=3 | x=4 | x=5
      return multiply(x,x);           // ← then 1. returns the value from the multiply(x, y) x=9 | 2. x=16 | 3. x=25
  }

  function isRightTriangle(a,b,c) {     // 9 , 16 , 25   
      return square(a) + square(b) === square(c);
  }

  isRightTriangle(3,4,5)

  // true   // because 9 + 16 = 25  ← square(3) + square(4) === square(5)
  ```
  *So how does the stack work?*    
  1. `isRightTriangle(3,4,5)`    
     `square(a) + square(b) === square(c);`  
     *the __1st__ thing that has to be evaluated is __`square(a)`__, which is `sqaure(3)`. That's added onto the __call stack__.*
  2. *call stack:*    
   `sqaure(x)`   
   `return multiply(x,x);`, *where x = 3*.      
   *This then calls `multiply(x,y)` (where x = 3  and y = 3).*   
  3. `multiply(3,3)`   
     `3  * 3`   
    *__Returns: `9`__, and there is no new function call, __so `multiply(3,3)` is removed from the call stack.__*   
    *So now, it goes back with the `a`'s value `9`:*   
  1. `square(a)` has a value `9` (not `3` anymore)
      *so `square(a)` is able to return `9` as well.*   
      *`square(9)` is removed from the call stack.*         
  2. `isRightTriangle(9,b,c)`    
     `square(9) + square(b) === square(c);`      
  *Then it moves on, to `square(b)` and then `square(c)`.*   
  *Then finally it can do the math `square(9) + square(16) === square(25);`*


  __JavaScript adds the function calls to the call stack and then it removes them whenever a value is returned.__

  (check it out [here](http://latentflip.com/loupe/?code=ZnVuY3Rpb24gbXVsdGlwbHkoeCx5KSB7CiAgICBjb25zb2xlLmxvZyhgZmlyc3Q6ICR7eCAqIHl9YCk7CiAgICByZXR1cm4geCAqIHk7CiAgICAKfQoKZnVuY3Rpb24gc3F1YXJlKHgpIHsKICAgIGNvbnNvbGUubG9nKGBzZWNvbmQ6ICR7bXVsdGlwbHkoeCx4KX1gKTsKICAgIHJldHVybiBtdWx0aXBseSh4LHgpOwp9CgpmdW5jdGlvbiBpc1JpZ2h0VHJpYW5nbGUoYSxiLGMpewogICAgY29uc29sZS5sb2coYHRoaXJkOiAke3NxdWFyZShhKSArIHNxdWFyZShiKSA9PT0gc3F1YXJlKGMpfWApOwogICAgcmV0dXJuIHNxdWFyZShhKSArIHNxdWFyZShiKSA9PT0gc3F1YXJlKGMpOwp9Cgppc1JpZ2h0VHJpYW5nbGUoMyw0LDUp!!!))
    
 <br> 

   💡 How to __[debug](https://developer.chrome.com/docs/devtools/javascript/#sources-ui)__?    
   Use Chrome's Dev Tool to debug. Open the Dev tool and open the __Sources__ panel, and there on *Pages*, and select the page (here app.js) we want to debug.        
   Here we can click on the code's line number (on the left), which adds a Breakpoint. This breakpoint stops our code at that line where we clicked.   
   Now line by line we can go throught the code, and read the `code` and the `breakpoint` (on the right panel).


---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br>


## __[Single Threaded](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Concepts#javascript_is_single-threaded )__
A [thread](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Concepts#threads) is basically a single process that a program can use to complete tasks. Each thread can only do a single task at once❗️

Single thread means that there is one thing (one line of code) in JavaScript that can run on a process at any given point. It cannot do multitasking, doing things simultaneously.


Even though JavaScript can only run 1 line at a time, that could slow down things → bad user experiences.
But there are ways around this issue:   

- __[`setTimeout()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#settimeout)__ : running a code after a delay
  - eg.:   
    *How that code works if JS is singlethreaded?*   
    *The execution of the lines should run from the first line to the last. But here the (`setTimeout()`) prints out the last. Because JS hands over this task to the browser. __That is a web API function__* ❗️  
    ```
    console.log("I am the first line")

    setTimeout(function() {
      console.log("I am the second line")
    }, 3000)

    console.log("I am the third line")

    // I am the first line
    // I am the third line
    // I am the second line
    ```
    *The browser is doing the work. Browsers are not written in JS, so they can do certain tasks that JS can't. That is how eg. `setTimeout()` is printed on the last line.*

    <br>

- Browseres come with Web APIs that are able to handle certain tasks in the background (like making request or `setTimeout`)
- The JS call stack recognizes these Web API functions and passes off to the browser to take care of
- Once the browser finishes those tasks, they return and are pushed onto the stack as a callback.

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br>

## __[Web API](https://developer.mozilla.org/en-US/docs/Web/API)__
web APIs are generally methods that we can call from JS and they are handed off to the browser.   
*(eg.: `setTimeout()`, JS can't do it, the browser does it.)*

- eg.:   
  *JS pass `setTimeout()` off to the Web APIs, to the browser. Because it is a web API function*    
  *After the 3 seconds, the JS goes back and runs the next thing the 2nd line which is (`console.log("3rd")`).*   
  *After 3 seconds, `setTimeout()` is printed out.*
    ```
    console.log("1st")

    setTimeout(function() {
      console.log("2nd")
    }, 3000)

    console.log("3rd")

    // 1st
    // 3rd
    // 2nd
    ```
  The concept of the callback: passing a function in that is not executed right away, but executed later.

<br>

  💡 The `setTimeout()` adds to the call stack __immediately__, the callback passed to the `setTimeout()` will be added after the delay.     
  💡 More about the [__`setTimeout`__ in relation with the __Call Stack__](https://www.javascripttutorial.net/javascript-bom/javascript-settimeout/)

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br>


## __[Callback hell](https://www.geeksforgeeks.org/what-is-callback-hell-in-node-js/)__  
Because we have to call callbacks inside callbacks, we get a deeply nested functions, which is much harder to read and debug. This is sometimes called "callback hell" or the "pyramid of doom" (because the indentation looks like a pyramid on its side).
  - eg.:  
    *Background-color changing program*      
    *We have a `setTimeout`, which after 2 sec changes the background to red. In that `setTimeout` we have another `setTimeout` which after 2 sec changes the background to orange. In that `setTimeout` we have another which after 2 sec changes the background to yellow, and another `setTimeout` which after 2 sec changes the background to green, etc.*
    ```
    setTimeout( () => {
      document.body.style.backgroundColor = 'red';
        setTimeout( () => {
          document.body.style.backgroundColor = 'orange';
            setTimeout( () => {
              document.body.style.backgroundColor = 'yellow';
                setTimeout( () => {
                  document.body.style.backgroundColor = 'green';
                }, 2000)              
            }, 2000)          
        }, 2000)
    }, 2000)
    ```
    *We want to re-use this code, maybe we want to change the delays... To avoid writing again this long code, we set it to a function.*   

    *In that `colorSwitch` function, we have to pass in the __color we want ot change to__ and pass in the __delay__ (so we can change the time), and pass in a __call back__ wich tells the function __what to do next__ (lets name it `next`).* 

    *With this technique we can easily add nested callbacks inside of the setTimeout, and it permets us to easily set the callback, like set them to the same delay time. It's much clearer.*
    ```
    const colorSwitch = (setColor, delay, next) => {
      setTimeout(()=> {
        document.body.style.backgroundColor = setColor;
        next && next();
      }, delay)
    }


    // calling the function
    // "next" is after the delay time, as an anonymus function
    
    colorSwitch('blue', 3000, function() {
      colorSwitch('black', 2000, function() {
      })
    })
    ```
    *💡 the __`next && next`__:* 

    *It checks if the variable `next` does exist (has a value assigned to it). AND (&&) checks if invoking that variable (here that function) returns a truthy value. If both of those checks gives `true`, then proceed with the statement.*   

    *If we remove the `next && next()` part the code will work, but it will break when it will reach the end.*

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br>

## __[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)__
Promises are objects that represent the eventual completion, the eventual success or failure of some operation (some async operation).
__So a promise is a returned object to which you attach callbacks, instead of passing callbacks into a function.__

- *promises* keep the nested branching path, but they make it [nicer](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#return-%EF%B8%8F).

__👇 this topic's parts:__     
   - __[`promise`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise-1)__     
   - __[`.then()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#then)__ and __[`.catch()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#catch)__         
   - __[`return` - the clean code](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#return-%EF%B8%8F)__
   - __[`new Promise` - creating promises](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#new-promise---constructing-a-promise)__

Here's an example, when our code is NOT nice, deeply nested → complicated:   
- eg.:  
    *Here we have a `request` function with 3 properties. First is a `URL` request (hellowebsite.com/page1), the other 2 are callbacks, 1 for `succes` and 1 for `failure`.*      
    *This 2 callbacks: 1 for when the request works, 1 when it doesn't.*        
    *In case of `hellowebsite.com/page1`, we need to nest another function for `hellowebsite.com/page2`, if 'page2' works or not, and for `page3`, and so on.*   

    *This example is based on a random number (`Math.random`): it imitates a `delay` which is between 500 ms - 4000 ms (if it's more than 4000 ms it's a failure, but less than 4000ms is a success).*
    ```
    const request = (url, success, failure) => {
      const delay = Math.floor(Math.random() * 4500) + 500;
      setTimeout(() => {
          if (delay > 4000) {
              failure('Connection timeout')         // it is a function call
          } else {
              success(`Here is your URL: ${url}`)   // it is a function call
          }
      }, delay)
    }


    // calling the function. 3 arguments, the last 2 are callBack functions.   
    // The last 2 arguments refer to the failure and success functions
    // so it looks like this:  request('URL', function(response){…2nd request…}, function(error){…message…} )

    request('hellowebsite.com/page1', 
        function(response) {                        // response refers to request = (url,success,failure) => { }...
          console.log(response);                    
        },
          request('hellowebsite.com/page2',         // this is the second request
              function(response){     
                console.log(response); 
              },
              function(error){
                 console.log(error); 
              }),               
        function(error) {                           // error refers to request = (..,.., failure) => { }...
          console.log(error);                       // if at any point failes it stops                                              
    })

    // possible results:
    // Here is your URL: hellowebsite.com/page2
    // Here is your URL: hellowebsite.com/page1
    // or:
    // Here is your URL: hellowebsite.com/page1
    // Connection timeout
    // or:
    // Connection timeout
    ```
 
 That is when we use `promise`:  
 
### __[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)__   
 
- `promise` is just an object:    
  it is the __eventual__ guarantee of either a value or an error.      
  __Promises__ represent this __asynchronous value that eventually will be resolved or rejected__.
    
- `promise`s have 3 possible mutually exclusive __[states](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md#states)__:   
    - __pending__: initial state, neither fulfilled nor rejected. *(at the beginning)* __Waiting for something__.
    - __fulfilled__: meaning that the operation was completed successfully. *(= success)*   
    `promise.then(f)`
    - __rejected__: meaning that the operation failed. *(= failure)*    
    `promise.then(undefined, r)` 

  We say that a *`promise` is settled if it is not pending*, i.e. if it is either fulfilled or rejected. (Being settled is not a state, just a linguistic convenience.) 

- `promise`s have 2 possible mutually exclusive __[fates](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md#fates)__:   
    - __resolved__: if the `promise` is trying to resolve or reject has no effect:    
    i.e. the promise has been "locked in" to either follow another promise, or has been fulfilled or rejected.
    - __unresolved__: if the `promise` is not resolved:    
    i.e. if trying to resolve or reject it will have an impact on the promise.

<br>

- we can __run a code when a `promise` is *rejected* or when it is *fulfilled*__.

- the way `promise` works:   
  we are __attaching callbacks to the object__ (to the `promise` itself), rather than passing callbacks into a function.   
  We wait the function to return a promise object.
  (We get this object → `Promise` 
    `{<fulfilled>}`
    `[[Prototype]]: Promise)...`)

- eg.:   
  *Here we are imitating a request, which sometimes works, sometimes doesn't. Inside the `requestPromise` function we have 2 callbacks. 1 for when the request fulfilled, 1 when it's rejected.* 

  *Here the `requestPromise` function doesn't expect any callbacks to pass in (as properties), we only pass the `(url)` property.*
  ```
  const requestPromise = (url) => {
      return new Promise((resolve, reject) => {
          const delay = Math.floor(Math.random() * (4500)) + 500;
          setTimeout(() => {
              if (delay > 4000) {
                  reject('Connection Timeout :(')
              } else {
                  resolve(`Here is your URL: ${url}`)
              }
          }, delay)
      })
  }

  requestPromise('something');
 
  // Promise 
    {<pending>}
    [[Prototype]]: Promise
    [[PromiseState]]: "fulfilled"
    ...
    
    
  const hello = request('hello');
  hello;
  
  // Promise {<fulfilled>: 'Here is your URL: '}
  //  [[Prototype]]: Promise
  //  [[PromiseState]]: "fulfilled"
  //  [[PromiseResult]]: "Here is your URL: "  
  ```
  
---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to beginning of Promises](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br>  

### __[`.then()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/then)__    
The `then()` method returns a Promise.    
It takes up to two arguments: callback functions for the success and failure cases of the Promise.

- eg.:   
  *The requestPromise function*
  ```
   const requestPromise = (url) => {
      return new Promise((resolve, reject) => {
          const delay = Math.floor(Math.random() * (4500)) + 500;
          setTimeout(() => {
              if (delay > 4000) {
                  reject('Connection Timeout :(')
              } else {
                  resolve(`Here is your URL: ${url}`)
              }
          }, delay)
      })
  }
  ```
  *__If the `promise` is fulfilled, we attach `.then()` and we pass a callback in `.then(callback () => ...)`__*
  ```
  // calling 'requestPromise()' : we pass an actual URL site

  requestPromise('website.com/api/page1');   //← gives an object
  

  // save it to a variable

  const request = requestPromise('website.com/api/page1');


  // if the 'promise' is fulfilled, we pass a callback

  request.then( function(){
    console.log("👍 worked");
  })
  // 👍 worked


  // check that the promise is fulfilled
  
  request;
  // [[Prototype]]: Promise
  // [[PromiseState]]: "fulfilled"
  // [[PromiseResult]]: "Here is your URL: website.com/api/page1"
  ```
 ### __[`.catch()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/catch)__    
 The `catch()` method returns a Promise and deals with rejected cases only.
 
 - eg.:   
    *(following the previous example)*    
    *__We can run code__ also, __when the `promise` is rejected, using `catch()`__. We can pass a callback in to `catch()`.*

    __*If the promise is fulfilled it runs: `.then(()=>{})`*__ *❗️*  
    __*If the promise is rejected it runs: `.catch(()=>{})`*__ *❗️*
    ```
    // it tells us that the promise is rejected
    
    requestPromise;
    // 1 Uncaught (in promise) Connection Timeout :(
    // Promise.then (async)		
    // (anonymous)  

    requestPromise                         //← request here is an object
      .then( function(){                   //← .then() is a method on the object
        console.log("👍 worked");   
      })
      .catch( function() {                 //← .catch() is a method on the object
        console.log("👎 error");    
      })
    ```

- we can __chain__ the methods (so we don't have to save the function into a variable)   
  - eg.:  
    *following the previous example(s)* 
    *chaining `.then()` and `.catch()`*  
    ```
    requestPromise('website.com/api/page1')         //← returns a promise object
        .then( function(){          
          console.log("👍 worked");  
          requestPromise('website.com/api/page2')   //← nest a '/page2'
        })
            .then( function(){                      //← '/page2' works
                console.log("👍 worked 2");   
            })
            .catch( function(){                     //← '/page2' doesn't work
                onsole.log("👎 error 2");
            })
        .catch( function() {       
          console.log("👎 error");    
        })

    
    // if it is fulfilled '/page1' and '/page2'
    // 👍 worked
    // 👍 worked 2   
    ```
    *Here  we are not passing the `requestPromise(function(){})` function into the `requestPromise(function(){}) function`, instead we are calling it `.then()` and `.catch()` methods on the returned promise object.*
    
<br> 

- So what is the point of using __`promise`__ ?    
  __Instead of *nesting*, we can *chain* events on__ ❗️
 (So there is no need to nest → avoiding the [callback hell](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-hell))

### __return__ (❗️) 
 - eg.:     
  *We __[return](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#return) a promise__ from within the `.then(callback)`. __That allows us to chain things together.__*    
  *Note that, we are passing a `data` in the function, because in real, a promise can be rejected and resolved with a value passed to it.*  
    ```
    const requestPromise = (url) => {
    return new Promise((resolve, reject) => {
        const delay = Math.floor(Math.random() * (4500)) + 500;
        setTimeout(() => {
            if (delay > 4000) {
                reject('Connection Timeout :(')
            } else {
                resolve(`Here is your URL: ${url}`)
                }
            }, delay)
        })
    }
    
    
    requestPromise('website.com/api/page1')               //← returns a promise object
        .then( function(data){ 
          console.log(data)                               // ← data = `Here is your URL: ${url}`  
          console.log("👍 worked 1");  
          return requestPromise('website.com/api/page2')  //← we RETURN the promise
        })
        .then(function(data){
          console.log(data)
          console.log("👍 worked 2");                     
          return requestPromise('website.com/api/page3')   
        })
        .catch( function(error){                          // ← data = 'Connection Timeout :('
          console.log(error)
          console.log("👎 error 1"); 
        })


    // Here is your URL: website.com/api/page1
    // 👍 worked 1
    // Connection Timeout :(
    // 👎 error 1    
    ```
    *We have only one `.catch()`, so if at any point one of the promises is rejected, it hits the `.catch()` on the end of the code*.
    
---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to beginning of Promises](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br>

### __[`new Promise` - constructing a promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/Promise)__    

The Promise constructor is primarily used to wrap functions that do not already support promises.

- Syntax: `new Promise(executor)`

- eg.:    
  *The __`new Promise` expects us to pass in a function, which has 2 parameters__.*  

  *The 1st parameter is a function that resolves the promise, the 2nd rejects it.*  

  *If at any point we call `resolve` the promise object will be resolved, and the same logic with `reject`.*

  *fulfilled*
  ```
  new Promise(function(resolve, reject) {
    resolve();
  })

  // Promise {<fulfilled>: undefined}
  //  [[Prototype]]: Promise
  //  [[PromiseState]]: "fulfilled"
  ```
  *rejected*
  ```
  new Promise(function(resolve, reject) {
    reject();
  })

  // Promise {<rejected>: undefined}
  //  [[Prototype]]: Promise
  //  [[PromiseState]]: "rejected"
  ```
  *pending (until we call resolve or reject inside of the function)*
  ```
  new Promise(function(resolve, reject) {
    
  })

  // Promise {<pending>}
  //  [[Prototype]]: Promise
  //  [[PromiseState]]: "pending"
  ```
  *Let's make a request, which will be resolved after 1000 ms.*    
  *Process: we [`return`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#return-%EF%B8%8F) our `new Promise` function, inside we give a `setTimeout` and inside we call `resolve()`, which will resolve after 1000 ms, if the `const num` variable is true or false*

  ```
  function myRequest(url) {
    return new Promise((resolve, reject) => {
      const num = Math.floor(Math.random() * 10)
      setTimeout(function() {
        if (num < 7) {
          resolve(`Your site is: ${url}`);
        } 
          reject('Request error');
        
      }, 1000)
    })
  }


  //call myRequest with a URL and add a '.then()' and '.catch()'
  
  myRequest('mysite.com/page1')
    .then((data) => {
      console.log('Fulfilled the request!');
      console.log(data);
    })
    .catch((error) => {
      console.log('It is an error!');
      console.log(error);
    })

  
  // Promise {<pending>}
  // Fulfilled the request!
  // Your site is: mysite.com/page1
  ```

- eg.:    
  *Let's see that in real practice*    
  *The [background-color](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-hell) changing program*   
  HTML
  ```
  <body>
    <script src="app.js"></script>
  </body>
  ```
  JS   
  *Here we will not call `reject`, because we are only resolving the colours*
  ```
  // creatng a function with a new promise

  function delayedColorChange (color, delay) {
    return new Promise((resolve, reject) => {
      setTimeout(()=>{
         document.body.style.backgroundColor = color;
         resolve();
      }, delay)
    })
  }


  // calling the promise, chainging the '.then()'

  delayedColorChange('red', 1000)
  .then(()=>{
    return delayedColorChange('orange', 1000)
  })
  .then(()=> {
    return delayedColorChange('green', 1000)
  })
  .then(()=> {
    return delayedColorChange('blue', 1000)
  })
  ```
---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to beginning of Promises](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br>

## __[`async` Keyword](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)__

- async functions make our code cleaner *(syntactic sugar, means make code easier to read)*.

- async functions make promises prettier

- the `async` keyword:   
we use the __`async` key word__ to __declare a function, an async function__.   
(It stands for asynchronous.)

- when we declare the `async` function, it __automatically returns a `promise`__ ❗️

  - if the function returns a value → the `promise` will be fulfilled
  - if the function throws an exception → the `promise` will be rejected   

- syntax: `async function name() { … }`

- eg.:   
  *`async` returns a promise automatically. We don't have to write`return new Promise…`*
  ```
  // declaring function as an async function

  async function hi() {
  }

  //calling hi()
  hi();

  // returns a promise (automatically):
  // [[Prototype]]: Promise
  // [[PromiseState]]: "fulfilled"
  // [[PromiseResult]]: undefined       // undefined because there is no value
  ```
 
- eg.:   
  *Declaring `async` function and returning a value. When our function returns a value, then the promise will be fulfilled with that value.*
  ```
  const name = async() => {
    return 'John Doe';
  }

  name();

  // Promise {<fulfilled>: 'John Doe'}
  ```

__Promise fulfilled__
- eg.:    
  *We can chain the `async` function, because technically it is a promise.*
  ```
  const name = async() => {
    return 'John Doe';
  }

  name().then((data) => {
    console.log('async function resolved: ',data);
  });

  // async function resolved: John Doe
  // Promise {<fulfilled>: undefined}
  ```

__Promise rejected__   
  - __[`throw`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/throw)ing__ an error:   
    The `throw` keyword should be used when we want to handle an error, and nothing else should be run after that.     
  - So, the `throw` statement displays a user-defined exception (the technical term for errors that occur when the application is already running). It can be helpful to debug the issue and/or indicate to the user what s/he might be doing wrong that is causing that error.   
  The way it works: is that the execution of the current function stops (the statements after `throw` won't be executed), and control will be passed to the first `catch` block in the call stack. If there is no `catch.` the program will terminate.   
    - More about [`throw`](https://stackoverflow.com/questions/46295340/what-is-the-difference-between-throw-foo-throw-errorfoo-throw-new-e/46295341#46295341)

- eg.:   
  *Throwing an error is a way to reject a `promise`*   
  *The error can be: a syntax error, or our defined error.*
  ```
  // we can just throw a string as an error.

  const name = async() => {
    throw 'Sorry for this error!'
    return 'John Doe';
  }

  name();

  // it's still a promise, and we get an error
  // Uncaught (in promise) Error: Sorry for this error!
  // at name (<anonymous>:2:11)
  // at <anonymous>:6:3
  ```


- eg.:      
    *A login example (however there is nothing asynchronous in our code here).*        
    *__chaining__ using the `.catch` and the `.then`!*       
    ```
    // login function takes 2 parameters

    async function login(username, password) {
      if (!username || !password)           // if there is no username OR password throw message
        throw 'No username or no password'
      if (password === 'Password')
        return 'Hello!'
    }

    login('User01', 'Password')
      .then(message => {
        console.log('You logged in!!')
        console.log(message)
      })
      .catch(error =>{
        console.log('Error')
        console.log(error)
      })

    // You logged in!!
    // Hello!
    ```
    
  ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to beginning of Promises](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br> 

## __[`await` keyword](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)__
the `await` keyword pauses the execution of our `async` function, and wait for a `promise` to be fulfilled __before__ continuing on.

- we can only use the `await` keyword inside of a function declared with `async`. For `await` we need to get an `async function`, and inside that we have our `await`. So `await` does the same job as `.then()`, but cleaner.

- __async__ is an easy to use and understand approach of returning promises. It __is used to return the new promise in a simpler way__.

- `then` and `catch` methods belong to the Promise. When using `await` the value gets unwrapped from the `promise`. We can imagine that a promise is some sort of container/box data type. If we remove the `await`, it returns a `promise` which then can be "`then`able" or "`catch`able".

- eg.:   
  *The [background-color changing](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#callback-hell) program* 

  *But now, we use the `async` function declaration and `await`.* 

  *Whe we use the `await` keyword, it's going to wait for a promise to be fulfilled. That means it will just __pause until__ a promise is fulfilled after X second.*
  ```
  // creatng a function with a new promise

  const delayedColorChange = (color, delay) => {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            document.body.style.backgroundColor = color;
            resolve();
        }, delay)
    })
  }

  // calling it with async function declaration

  async function colorChange(){
    await delayedColorChange('red', 1000)     // ← returns a promise. await = pause
    await delayedColorChange('orange', 1000)  // ← returns a promise
    await delayedColorChange('green', 1000) 
    await delayedColorChange('blue', 1000) 
    return "Now, the promise is fulfilled"    // ← promise isn't fulfilled until it gets to this return 
  }                                           // it's fulfilled because it returned a value

  // call the function
  colorChange();
  ```
  *We can console.log a message after `colorChange()` is done.*   
  *The `colorChange()`'s await promises are only fulfilled until they reach the `return "Now, the promise is fulfilled"`.*
  ```
  async function printColorChange() {
    await colorChange();                // waits until the promise is fulfilled
    console.log("End of color changes");
  }

  // call the function 

  printColorChange();
  ```
 
- When promises are resolved with information we use mostly `await`. We `await` some request.  

  - eg.:   
    *We use this request modell, when a promise is fulfilled with some data (request). (You can see the previous version [here](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#then))*    
    *The data from `requestPromise` is `await`ed, stored in a variable `let data`.*
    ```
    const requestPromise = (url) => {
      return new Promise((resolve, reject) => {
            const delay = Math.floor(Math.random() * (4500)) 
            + 500;
            setTimeout(() => {
                if (delay > 4000) {
                    reject('Connection Timeout :(')
                } else {
                    resolve(`Here is your URL: ${url}`)
                }
              }, delay)
          })
      }

    // here we await for the request

    async function waitingRequest() {
      let data = await requestPromise('/page1');
      console.log(data);
    }

    waitingRequest();

    // Here is your URL: /page1
    ```
    
    💡 [good video about `await` vs `.then()`](https://www.youtube.com/watch?v=V_Kr9OSfDeU)
  ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to beginning of Promises](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br> 

## __[the `try..catch` statement and error handling in `async` functions](https://javascript.info/async-await#error-handling)__   
in the case of a rejection, `await` promise throws the error.   
→ we can catch them with `try...catch`.

<br> 

__The [`try..catch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch) statement__:
 
   The `try...catch` statement marks a try block and a catch block.   
   If the code in the try block throws an exception then the code in the catch block will be executed.   
     
 - eg.:   
   *How [`try..catch` works](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch#try_it).*  
   *In the `try` block we have an error in the console.log, so it goes to the `catch` block, and prints the `catch` block's error message.*.  
    ```
    try {
      console.log(hello);                      //← it should be "hello" with quotes.

    } catch {
       console.error("Catch the error!");     //← Note: the console.error() method outputs an error message to the Web console.
     }  

    //❌ ▸ Catch the error!
    ```

- eg.:   
  *We make the time longer, to have an error for sure : `const delay = 4500; `.*   
  *If the `try` block's code has an error (throws an error), we can catch it with the `catch`, so we can handle that error.*   
  *The `error` in the `catch(error)` refers to the error itself (here "Connection Timeout").*
  ```
  const requestPromise = (url) => {
    return new Promise((resolve, reject) => {
          const delay = 4500; 
          setTimeout(() => {
              if (delay > 4000) {
                  reject('Connection Timeout')        //← the value that our promise was rejected with.
              } else {
                  resolve(`Here is your URL: ${url}`)
              }
            }, delay)
        })
  }

  // here we await for the request

  async function waitingRequest() {
      try {                             // ← what we are trying to do
        let data = await requestPromise('/page1');
        console.log(data);              //← data = "Here is your URL: /page1"
        let data2 = await requestPromise('/page2');
        console.log(data2);

      } catch(error)  {
        console.log('We catch the error!')
        console.log('error is: ', error)             // ← error message itself: Connection Timeout
      }

  }

  waitingRequest();

  // We catch the error!
  // error is:  Connection Timeout
  ```

  ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to beginning of Promises](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#promise) or [👆 go up to Asynchronous JS](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#asynchronous-javascript)
  
<br> 

# [AJAX](https://developer.mozilla.org/en-US/docs/Web/Guide/AJAX)    
AJAX = __Asynchronous JavaScript And [XML](https://developer.mozilla.org/en-US/docs/Web/XML/XML_introduction)__   
*(XML = Extensible Markup Language)*

(Correctly would be AJAJ, since XML is depricated, we use JSON instead)

- AJAX refers to:   
 a) making requests to load information *(behind the scenes)*        
 b) to send information    
 c) to save something on a given website    
 d) interacting with a server

- So the idea of AJAX is: creating applications where by using JavaScript we can load data / we can fetch information / we can send data somewhere, to save something to a database. And all this happens behind the scenes.

- There's no need to refresh the page, because we can make a request to the API every X minutes.   
What the API sends back is pure information in a JSON format.

 - eg.:     
  *The infinite scroll on instagram, reddit, etc.*       
  *The live searching (google) it gives suggestions while typing*

 - dev.tool → __network__ tab:   
  shows requests that have been made on a given page, new information that has been loaded.

- [API](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#api)  
  [JSON](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#json)     
  [API management tools](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#api-management-tools--platforms---http-requests)    
  [HTTP Verbs](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#http-verbs)   
  [HTTP response status codes](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#http-response-status-codes)   
  [Query Strings](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#query-strings)    
  [HTTP Headers](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#http-headers)    
  [XHR - XMLHttpRequest](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#xhr--xmlhttprequest)     
  [Fetch API](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#fetch-api)      
  [Axios](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#axios)    
  [A search app using Axios](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#search-app-with-axios)   
  
  
  

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
  
<br> 

## __[API](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction#what_are_apis)__   
  __Application Programming Interfaces__   

  API is very broad term that refers to any interface for one computer to interact or communicate with another software.

 - An API allows to create complex functionality __more easily__.    
   An API abstracts more complex code away from you, providing some __easier syntax__ to use in its place.

__[Web API](https://www.geeksforgeeks.org/what-is-web-api-and-why-we-use-it/)__   
Web apps are interfaces that are Web based __(HTTP based)__.    With a Web API we are referring to an interface that occurs over HTTP.

So we can make requests to particular URLs, which we usually call __endpoints__.    

💡An __[endpoint](https://www.w3.org/TR/wsdl20/#Endpoint)__ is the URL where your service can be accessed by a client application (eg.: `https://catfact.ninja/fact`).



Web APIs are like a *portal into a different application or database*.

__Interface not for humans, but for applications!__

 -  When we make requests using JavaScript, AJAX requests, we are looking the data (not the HTML, CSS).


---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br> 

## __[JSON](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON)__
 __JavaScript Object Notation__

 JSON is just a format for sending data for, for sending information from an API to, our browser for instance.

 It is a data-interchange format.    
  
-  [JSON](https://www.json.org/json-en.html) possible values are *not exactly the same as in JS*:   
   - object, array, string, number, "true", "false", "null"
   - ❗️ undefined is not a valid JSON (it's valid in JavaScript)

- It's a way of formatting data that is consistent and predictable and it's very __similar to JavaScript__.  

- Syntax:
  - key-value pairs
  - curly braces `{}`
  - every key has to be a __"double quoted string"__

- eg.:   
  ```
  {
    "stringKey" : "string value",
    "intigerKey" : 2022,
    "booleanKey" : true,
    "arrayKey" : [
      "array01",
      "array02",
      "array03"
    ]
  }
  ```

- __[`JSON.parse()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse)__:   
The __`JSON.parse()` method__  to turn JSON into a valid JavaScript object.

  - eg.:   
    *turning a JSON into a JavaScript object with the `JSON.parse()` method*   
    ```
    const json = '{"result":true, "count":42}';
    
    JSON.parse(json);

    // result: true, count: 42
    ``` 
    *To extract the data*
    ```
    const json = '{"result":true, "count":42}';
    
    // save it to a variable
    const obj =  JSON.parse(json);

    obj.count;

    // 42
    ``` 


- __[`JSON.stringify()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify)__:   
The JSON.stringify() method converts a JavaScript object or value to a JSON string.    
  - It is useful when we want to send information to an API and API needs the data as JSON.

  - eg.:   
    *Turn a JavaScript object into a valid JSON*   
    ```
    const object = {phone : 'mobile', color : 'silver', isWorking : true, number : undefined}

    // calling the method
    JSON.stringify(object);

    // '{"phone":"mobile","color":"silver","isWorking":true}'
    ```
 
 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br> 

## __[API Management Tools & Platforms - HTTP requests](https://www.talend.com/resources/what-is-api-management/)__     
We can use tools to make requests, to save requests, helps us make API calls and to test out different API requests.    

__[postman](https://www.postman.com/)__   
it is an API platform for building and using APIs.
    
__[hoppscotch](https://hoppscotch.io/)__    
it is the same as Postman, but it is opensource and free.

- eg.:   
  *We send a URL with a base API (.../api) → `https://catfact.ninja/fact` via Postman (we place the URL into the GET and click send).*    
  *What we get, is a JSON, it is the __response__*   
  *It looks like this...*
  ```
  {
    "fact": "Fossil records from two million years ago show evidence of jaguars.",
    "length": 67
  }
  ```
 
 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br> 

## __[HTTP Verbs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)__   
  HTTP defines a set of request methods to indicate the desired action to be performed for a given resource. 
  
  - 💡 a [very useful article](https://www.freecodecamp.org/news/http-request-methods-explained/) about the topic of HTTP Requests.

  - Each verb is a different type of request.

    - __[GET](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET)__ request :    
    to get or retrieve information, it's just a way of getting stuff from an API.

    - __[HEAD](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/HEAD)__

    - __[POST](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST)__ request :   
    to send data somewhere, trying to *post* data. The data we are sending is going to be saved somewhere / stored in a database / have an impact on a server.

    - __[PUT](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PUT)__

    - __[DELETE](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/DELETE)__ request :    
      to delete something via an API.

    - __[CONNECT](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/CONNECT)__

    - __[OPTIONS](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS)__

    - __[TRACE](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/TRACE)__

    - __[PATCH](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/PATCH)__

 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>

## __[HTTP response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)__    
HTTP response status codes indicate whether a specific HTTP request has been successfully completed.    
So __it is a code that comes back in an HTTP response, and it has a meaning.__  

- they are grouped in 5 classes:
  - __Informational responses__ ([100–199](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#information_responses))
 
  - __Successful responses__ ([200–299](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#successful_responses))
      - [200](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/200) : the most common. It means that the request has succeeded. 
      - [201](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/201) : when we create something successfully with a POST request.
  
  - __Redirection messages__ ([300–399](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#redirection_messages)) :   
      __do soemthing with rederiction.__    
      Eg.: *google.co instead of google.com → redirect to google.com*  

  - __Client error__ responses ([400–499](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#client_error_responses)):    
  __These are all status codes that indicate something the user or the client side did wrong.__   
      - [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400) : Bad request. It means that the server cannot process the request due to something that is perceived to be a client error 
      - [401](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/401) : Unauthorized. It means that the client request has not been completed because it lacks valid authentication credentials for the requested resource.
      - [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404) : Not found. It means that the server cannot find the requested resource.

  - __Server error__ responses ([500–599](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status#server_error_responses)) :    
  __these are the server side errors.__ When somethig went wrong on the server side, rather than on the client side. (Something is wrong on the API side).


 - eg.:   
  *Client error responses __404__*      
  When we asking for an end point that doesn't exist (like a misspelled URL).  
 It means that the API doesn't know what we are asking → it sends an HTML 404.    
 By opening the DEV tool:we can see on the `devtool/netwrok` part that status is 404.

 - eg.:   
  *Client error responses __405__*      
  It means that endpoint exists, but it doesn't support whatever we tried to do a post instead of a get (method not allowed).
  
 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>

## __[Query Strings](https://en.wikipedia.org/wiki/Query_string)__
  A query string is __the portion of a URL where data is passed to a web application and/or back-end database__.  

  So we can include a lot of information in a URL, and each endpoint means something different.

  - eg.:    
   `https://example.com/over?field1=value1&field2=value2`
   The UR: `https://example.com/over`   
   The __query string__ : `?field1=value1&field2=value2`
  
  Some API endpoints have variables in the URL, something that can change in the URL.

  - parts of the [URL](https://medium.com/@joseph.pyram/9-parts-of-a-url-that-you-should-know-89fea8e11713)

  - __`id`__ (can be `:id` or `{{id}}` or `<id>`):    
    it is a common variable, it tells us to replace this with an actual ID.
    - eg.:  
      *`:id` indicting that we can replace it with something, here like a number.*     
      *Many times there is a documentation of the given [API](https://swapi.dev/documentation), where they explain what is what.*  
      ```
      https://swapi.dev/api/people/:id/
      ```
      we can replace the `:id` with a number
      ```
      https://swapi.dev/api/people/7
      ```
      and it gives us something (here a spceific resource, the 7th person eg).

  - __[`?`](https://en.wikipedia.org/wiki/Query_string#Structure)__   
    at the and of the URL there is `?` (question mark) starts the query string, where a lots of key-value pairs can be found:    
    __key `=` value__    
    These key-value pairs are sparated by `&` (ampersands).

    - eg.:   
      `https://example.com/over?color=blue&material=wood`

  
  - eg.:   
    `https://developer.mozilla.org/en-US/?q=react`
    The server of mozzilla, is looking for a *value* `q` and use what it finds under `q` as the __search term__ (query).   
    Here the API finds a lot of React search results.

 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>


## __[HTTP Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)__   
__[HTTP headers](https://www.ionos.com/digitalguide/hosting/technical-matters/http-header/) are a lot of key-pair information shared between the client and the server to set up a lot of stuff behind the scenes__, like [caching](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)-related data (which helps make data persistent in your browser even if you reload the page), authorization data (which proves you are who you're saying you are when accessing restricted-access webpages) and so on. 

So, __headers are an additional way of passing information with a given request and also with a response__. 

*Sort of metadata, little add on details of your request.*

- __HTTP headers are key-value pairs__

- eg.: the *Accept-* headers indicate the allowed and preferred formats of the response. Other headers can be used to supply authentication credentials (e.g. Authorization), to control caching, or to get information about the [user agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent) or referrer, etc.

- dev.tool → *network tab* : in the __headers__ tab → : 
  - __Request Headers__:     
    - here are the request headers that were sent
    - we can see key-value pairs, which are __pairs of information that goes along with the request__.   
      (eg.: *`cookie: user=E1011034406231; remember=true;`*)

  - __[Response Headers](https://developer.mozilla.org/en-US/docs/Glossary/Response_header)__:   
    - information comming back from the server
    - __so an HTTP response which doesn't relate to the content of the message__   
    (eg.: *Age*, *Location* or *Server* are used to give a more detailed context of the response).

    - the server that tells us more about the content, the language, the data type, the format (HTMLor JSON), etc.

- eg.:   
  *Using Postman and custom Headers*   
  *From [this](https://icanhazdadjoke.com/) API, we type API endpoints (URL) to the GET request.*    
  *To adjust the response formatting, so if we want JSON (or HTML, or plain text), we need to specify the Header called 'Accept'*   
  *→ we add the key and then the value information:*   
  *we set the `key: Accept` | `value: application/json`*

- some APIs can require from us to send a Header or multiple Headers along with our request. We can do this via code or using Postman.

 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>

## __[XHR = XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest)__
Is a way of sending request via JavaScript.

- There's no support for `promises`, so we have lots of callbacks, so it is messy.
- The capitalization makes it difficult (like here: XMLHttpRequest)
- clunky syntaxes
- eg.:  
  *The way that we make a request is by creating a new `XMLHttpRequest` __object__ and save it to a variable (`request`).*    
  *Then we add the `open` method with the `("GET", "URL")` GET request and the URL.*  
  *After that we opened it, we have to send it (`variable.send();`).*
  *But before we add 2 `EventListener` callbacks: `variable.onload` and `variable.onerror`.*
  ```
  const request = new XMLHttpRequest();                       //← creating a request object

  request.onload = function() {
    console.log("Loaded!");
    console.log(this);                                        //← 'this' is the request object
  }
  
  request.onerror = function() {
    console.log("ERROR!");
    console.log(this);                                        //← 'this' is the request object
  }

  request.open("GET", "https://swapi.dev/api/planets/1/");    //← open a request
  request.send();                                             //← send the request

  // we send it, and the result:
  // Loaded!
  // ▸ XMLHttpRequest                                         //← XMLHttpRequest object
       response:...
    🔹 responseText:...                                       //← it is a text (string), we have to convert it to JS object
       responseType: ""                                                                 
  ```
  *We `console.log` the `responseText` → we get a long string.*    
  *We have turn it into a JS object by __parsing__ because it is a __string__ (__we can not access the value such as__ eg.: `request[population]`, this doesn't work!!!)*
  ```
  const request = new XMLHttpRequest();                       //← creating a request object

  request.onload = function() {
    console.log("Loaded!");
    console.log(this.responseText);
    const variable = JSON.parse(this.responseText);           //← variable is a JS object here | JSON.parse() is a method object                                       
  }
  
  request.onerror = function() {
    console.log("ERROR!");
    console.log(this);                                        //← "this" is the request object
  }

  request.open("GET", "https://swapi.dev/api/planets/1/");    // ← open a request
  request.send();                                             //← send the request

  // we send it and the result is:
  // Loaded!
  // {"name":"Tatooine","rotation_period":"23",,"population":"200000",...}   //← it's an object: key-value pairs → now we can extract the values.
  ```
  *Note [JSON.parse()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse) method*.  
  *After the `const variable = JSON.parse(this.responseText);` we received a JS object, key-value pairs.*    
  ❗️*We can extract the value: `console.log(variable.name, variable.population)`*
  ```
  .
  .
  .
  request.onload = function() {
    console.log("Loaded!");
    const variable = JSON.parse(this.responseText)
    console.log(variable.name, variable.population) ;                            
  }     // extracting the values by using the key
  .
  .
  .

  // Loaded!
  // Tatooine 200000
  ```
  
 ---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>

## __[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)__   
  it allows us to make requests using a the `fetch()` function.  

  - it supports `promises` and async functions (compared to XMLHttpRequest, which doesn't really.)

  - syntax: `fetch("https://here we place the URL")`

  - eg.:   
    *We just call `fetch("our URL")`, and it turns back a pending promise.*
    ```
    fetch("https://swapi.dev/api/planets/1/");

    // ▸ Promise {<pending>}
    ```
    
    *We add `.then()` and `.catch()`*   
    
    ```
    fetch("https://swapi.dev/api/planets/1/")   //← we send a request with 'fetch', and we wait for a response from the server
      .then(response =>  {                      //← we handle the response with this .then() wich is chained to the 'fetch()'
        console.log("Fulfilled!!!", response);  //← if the response status is ok, it will show "Fulfilled!!!" and we display the "response" 
      })  
      .catch(error => {
        console.log("Error!!!", error);
      })

    // Fulfilled!!! ▸ Response                  //← Response is an object   
    //              💡 ▸ body: ReadableStream   //← normally it should contain the value (JSON)
    //                                          // here it is an incomplete body → we don't have the data, because the HTTP request was made before this is resolved. 
    //                   bodyUsed: false
    //                 ▸ headers: Headers {}    //← these are the response headers
    //                   ok: true
    //                   redirected: false
    //                   status: 200
    //                   statusText: ""
    //                   type: "cors"
    //                   url: "https://swapi.dev/api/planets/1/"
    //                 ▸ [[Prototype]]: Response
    ```
    *`fetch()` sends a request: we wait for a response from the server and then we handle it with the `.then()` which is chained to the `fetch()` call.*   
    *So, __inside of the `.then()` we can access the server's response__. We get the response back the moment the server sends back headers. (Here we don't have the data in the `body` because the `promise` is fulfilled as soon as `fetch("https://...)` receives any headers.)*  
   💡*Note: the `ReadableStream` means that we actually need to read it and pass it. There's a method on the Response called `response.json()`.*.     
    *So the `response.json()` method is added on to the `fetch()`'s response object, and it also returnes a `promise`.*   
    *Since the `response.json()` method returnes a `promise`, we can chain a `.then()` method.*   
    ```
    fetch("https://swapi.dev/api/planets/1/")         //← we send a request with 'fetch', and we wait for a response from the server
      .then(response =>  {                            //← we handle the response with this .then(). Inside the 'then()' we can access the server's response... 
        console.log("Fulfilled!!!", response);        //...we get back the response the moment the server sends back headers
        response.json().then(data => console.log("JSON is DONE!!!", data));      //← json() method |  we can use any name instead of the "data" 
      })  
      .catch(error => {
        console.log("Error!!!", error);
      })

    // Fulfilled!!! Response {type: 'cors', url: 'https://swapi.dev/api/planets/1/', redirected: false, status: 200, ok: true, …}
    // JSON is DONE!!! {name: 'Tatooine', rotation_period: '23', orbital_period:     //← we get back the data'304', diameter: '10465', climate: 'arid', …}
    ```
    *A NICER refactured way for the above code is to not to use the `response.json()` in a single line.*   
    *We put a `return` before the `response.json()`, and place the `.then(data =>...)` below, outside of the other `.then()`method.*
    ```
    fetch("https://swapi.dev/api/planets/1/")
      .then(response =>  {                      
        console.log("Fulfilled!!!", response);  
        return response.json()
      })
      .then(data => {
          console.log("We got back these data: ", data);
          })     
      .catch(error => {
        console.log("Error!!!", error);
      })

    // Fulfilled!!! Response {type: 'cors', url: 'https://swapi.dev/api/planets/1/', redirected: false, status: 200, ok: true, …}
    // We got back these data:  {name: 'Tatooine', rotation_period: '23', orbital_period: '304', diameter: '10465', climate: 'arid', …}  
    
    ```
    *__So what happens:__*   
    *1. as a start `fetch()` sends a request to this ("https://URL") URL first, then it returns a promise, which promise either fulfilled or rejected.*   
    *2. if it is fulfilled, we get into the 1st `.then()`, we __call it and return the `response.json()` method__.*    
    *3. `response.json()` method reads the response object (ReadableStream), and then this `response.json()`method __returns a promise__*   
    *4. after the return, we chain on the `.then()` and `.catch()`.*   

    <br>

Clear explanation:    
So when we __send a request with `fetch`__ we wait for a __response from the server__, and then __we handle that response from the server with the 1st `.then()`__ (its chained to the `fetch()` call).   
  Inside of the 1st `.then()` we can access the server's response. __We get response back the moment the server sends back headers.__ (Some servers might send back only headers, or headers and some data other than what we originally expected (like an error message)).     
If the __response status is ok__ (200 status code) then __we can expect to get back some data (in the body property) from the server__.   
`fetch()` gives us the body property as a `ReadableStream` (from the [Streams API](https://developer.mozilla.org/en-US/docs/Web/API/Streams_API)), which gives us a lot of options for how we can interpret that data:  

  - we can get the data back as a blob, text, json, etc.    
  *(For certain kinds of data this can give us the ability to process it as it comes in, such as a video. In the past we had to wait for the entire video file to be sent over, but now we can process the `ReadableStream` and that allows us to play the video as its data becomes available = the Streams API)*.      
    Most common use cases, we are just expecting back JSON data that we can parse and render to the page or do some sort of update to the page based on the data we get back. 

<br>

  *When we want a __2nd request__, we don't have to do complicated nesting.*       
  *The 1st request has to be fulfilled inorder to get to the 2nd request.*      
  *(We can make these requests independently, so they don't depend on each other, thus the 2nd request can be fulfilled without worrying about the 1st request.)*   
  *__We just add a `fetch(URL2nd Request)` below the `response.json()`'s `.then()` method.__*
  
  ```
  fetch("https://swapi.dev/api/planets/1/")                   //← 1st request
      .then( response =>  {                      
        console.log("1st request!");  
        return response.json()
      })
      .then( data => {
          console.log("1st response: ", data);  
          return fetch("https://swapi.dev/api/planets/2/");   //← 2nd request, only runs if the 1st request fulfilled
      })
        .then( response =>{
            console.log("2nd request!!!");
            return response.json()
        })
        .then( data => {
            console.log("2nd response: ", data);  
        })
      .catch( error => {
          console.log("Error!!!", error);
      })


  // 1st request
  // 1st response  {name: 'Tatooine', rotation_period: '23', orbital_period: '304', diameter: '10465', climate: 'arid', …}
  // 2nd request!!!
  // 2nd response  {name: 'Alderaan', rotation_period: '24', orbital_period: '364', diameter: '12500', climate: 'temperate', …}
  ```
 
*Let's refactor the code above using the [`async()`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#async-keyword) function and [`try..catch`](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-trycatch-statement-and-error-handling-in-async-functions).*   
  ```
  const loadStarWarsPlanets = async () => {
    try {
      const response = await fetch("https://swapi.dev/api/planets/1/");                 // ← 1st request
      const data = await response.json()
      console.log(data);

      const response2 = await fetch("https://swapi.dev/api/planets/2/");                 // ← 2nd request
      const data2 = await response2.json()
      console.log(data2);

    } catch (error) {
      console.log("Error!!!", error);
    }
  }

  // call the function
  loadStarWarsPlanets();


  // {name: 'Tatooine', rotation_period: '23', orbital_period: '304', diameter: '10465', climate: 'arid', …}
  // {name: 'Alderaan', rotation_period: '24', orbital_period: '364', diameter: '12500', climate: 'temperate', …}
  ```

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>

## [Axios](https://github.com/axios/axios#installing) 
it's a separate library, made for HTTP requests (creating requests and working with them), to make it easy and simple.

- behind the scenes, it uses `fetch()` in the browser

- we can install this library ([see on the gitHub](https://github.com/axios/axios#installing)), or we can just use this CDN script in our HTML:   
  `<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>`

- the big advantage, that it is already parses the JSON (`response.json()`). So in the promise object, we already have data (it's not empty).

- *Axios* has [methods](https://github.com/axios/axios#note-commonjs-usage)

- eg.:   
  *Make a `get` request we use `.get` + `URL`*   
  HTML
  ```
  <body>
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

    <script src="app.js"></script>
  </body>
  ```
  JS   
  *Instead of calling `fetch()`, we call `axios.get(URL)`, which makes a request AND parses the JSON.*       
  *We chain the `.then()` to see what is the response.*   
  *We add a `.catch()` if there is an error.*
  ```
  axios
    .get("https://swapi.dev/api/planets/1")
    .then((response) => {
      console.log("Our response: ", response);
    })
    .catch((e) => {
      console.log("ERROR! ", e);
    });
  
  // it gives us a promise! See the response object below, filled with data (because it parses the JSON behind the scence)
  // Our response:  ▼{data: {…}, status: 200, statusText: '', headers: {…}, config: {…}, …}
  // ▼ data:   
  //      climate: "arid"
  //      created: "2014-12-09T13:50:49.641000Z"
  ```
  *__Refactoring to `async` function format!__*
  ```
  const getStarWarsPlanets = async () => {
      const response = await axios.get(`https://swapi.dev/api/planets/1/`);
      console.log(response.data);
  };

  getStarWarsPlanets();

  // {name: 'Tatooine', rotation_period: '23', orbital_period: '304', diameter: '10465', climate: 'arid', …}
  //    climate: "arid"
  //    created: "2014-12-09T13:50:49.641000Z"
  ```
  *We make it with an `id`, so we can write our numbers there, when we call the function.*
  ```
  const getStarWarsPlanets = async (id) => {
      const response = await axios.get(`https://swapi.dev/api/planets/${id}/`);
      console.log(response.data);
  };

  getStarWarsPlanets(3);        //← we can add our number

  //► { name: 'Yavin IV', rotation_period: '24', orbital_period: '4818', diameter: '10200', climate: 'temperate, tropical', …}
  ```
  *__Best practice__: wrap it into a `try..catch`.*
  ```
  const getStarWarsPlanets = async (id) => {
    try{
      const response = await axios.get(`https://swapi.dev/api/planets/${id}/`);
      console.log(response.data);
    } catch(error){
      console.log("Error!", error);
    }
  };

  getStarWarsPlanets(4);        //← we can add our number

  //► { name: 'Hoth', rotation_period: '23', orbital_period: '549', diameter: '7200', climate: 'frozen', …}
  //      climate: "frozen"
  ```

__[Axios vs  Fetch API](https://blog.logrocket.com/axios-vs-fetch-best-http-requests/)__
```
// axios
axios.get('https://api.github.com/orgs/axios')
  .then(response => {
    console.log(response.data);
  }, error => {
    console.log(error);
  });

// fetch()
fetch('https://api.github.com/orgs/axios')
  .then(response => response.json())    // one extra step
  .then(data => {
    console.log(data) 
  })
  .catch(error => console.error(error));
```

 [A video about Axios](https://www.youtube.com/watch?v=qM4G1Ai2ZpE).  
 [Another Axios video "crash course"](https://www.youtube.com/watch?v=6LyagkoRWYA)
 
---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>

## __Search app with Axios__


- eg.:    
  *We are making a search form, where we use an [API of TV shows](https://www.tvmaze.com/api#show-search), so we can search for TV shows. The image of the searched show will be displayed on our page.*       
  HTML
  ```
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TV Show Search</title>
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
  </head>

  <body>
    <h1>TV Show Search</h1>
    <form id="searchFrom">
      <input type="text" placeholder="TV Show Title" name="query">
      <button>Search</button>
    </form>

    <script src="app.js"></script>
  </body>
  ```
  JS   
  *Listening for the `submit` event object.* 
  *The [`event.preventDefault()`](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault) prevents the default behavior of the page being reloaded when we submit the form. So if we don't use `event.preventDefault()` on a form `submit` event listener, then when we click the submit button (to submit the form) it would reload the page.*
  ```
  const form = document.querySelector('#searchForm');
  form.addEventListener('submit', function (event){
    event.preventDefault()
    console.dir(form)
  })

  // ► form#searchForm
  //    0: input
  //    1: button
  //       ...   
  //      ►  elements: HTMLFormControlsCollection(2)      //← elements property
  //            0: input
  //            1: button
  //            query: input                              //← we gave the name "query" in the <form> (name ="query")
  //            length: 2
  //            [[Prototype]]: HTMLFormControlsCollection
  ```
   *We want to get the `input` value, so we use the elements property (what we can see in the above example). We get the input value with that line `form.elements.query.value`.*
   ```
    const form = document.querySelector('#searchForm');

    form.addEventListener('submit', function (event){
      event.preventDefault()
      const searchTerm = form.elements.query.value;
    })

   // searchTerm gives back what we type in the searchbar, eg. we type "hello"
   // output is:
   // hello 
   ```
   *We are doing the API call* 
   *We add `axios.get('URL')`*     
   *So the API eg.: `https://api.tvmaze.com/search/shows?q=girls`, where the `q` is the query string.*    
   *Our plan is that what the user types in the searchbar, it will be the `q`'s value (eg. `q = ${what the user types here}`).*  
   *We make it an `async` function so we can use the `await`.*
    ```
    const form = document.querySelector('#searchForm');

    form.addEventListener('submit', async function (event){
      event.preventDefault()
      const searchTerm = form.elements.query.value;
      const response = await axios.get(`https://api.tvmaze.com/search/shows?q=${searchTerm}`)
      console.log(response.data);
    })

    // we type 'chicken' in the search bar, the output is:
    //► (10) [{…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}, {…}]   //← an array with 10 different shows
    // open the first one [0]:
    //  ► 0:
    //      score: 0.70269716
    //      ► show:                             //← 'show' is a property
    //          averageRuntime: 15
    //          dvdCountry: null
    //          ended: null
    //          externals: {tvrage: 5027, thetvdb: 75734, imdb: 'tt0437745'}
    //          genres: (2) ['Comedy', 'Science-Fiction']
    //          id: 686
    //          image: {medium: 'https://static.tvmaze.com/uploads/images/medium_portrait/5/14886.jpg', original: 'https://static.tvmaze.com/uploads/images/original_untouched/5/14886.jpg'}
    //      ► [[Prototype]]: Object
    ```
    *We acces the the 'show' property's image.*
    ```
    const form = document.querySelector('#searchForm');

    form.addEventListener('submit', async function (event){
      event.preventDefault()
      const searchTerm = form.elements.query.value;
      const response = await axios.get(`https://api.tvmaze.com/search/shows?q=${searchTerm}`) 
      const img = document.createElement('img');
      img.src = response.data[0].show.image.medium      //← this gives back the image's url
      document.body.append(img)                         //← append the img to the body
    })

    // it adds the searched show's image on the page
    ```
    *To get all the images for the search show, we need to use a loop.*    
    *We create a separate function (we cal it `makeImages`) for the loop.*   
    *So for each show we make a new image and then we set its source. Instead of the `response.data` we set `result.shows`, where the `show` is comming from the API itself.*
    ```
    const form = document.querySelector('#searchForm');

    form.addEventListener('submit', async function (event){
      event.preventDefault()
      const searchTerm = form.elements.query.value;
      const response = await axios.get(`https://api.tvmaze.com/search/shows?q=${searchTerm}`) 
      makeImages(response.data)

    })

    // a loop function

    const makeImages = (shows) => {       //← shows: each element in the array
      for (let result of shows){
        const img = document.createElement('img');
        img.src = result.show.image.medium      //← show is from the API
        document.body.append(img)                        
      }
    }
    ```
    *There are cases when there is no image (image is Null). We add some logic for these cases, using `if`.*   
    *Also, we empty the `input`!*
    ```
    const form = document.querySelector('#searchForm');

    form.addEventListener('submit', async function (event){
      event.preventDefault()
      const searchTerm = form.elements.query.value;
      const response = await axios.get(`https://api.tvmaze.com/search/shows?q=${searchTerm}`) 
      makeImages(response.data)
      form.elements.query.value = '';         // empty the input

    })

    // a loop function

    const makeImages = (shows) => {       
      for (let result of shows){
        if(result.show.image){          // if there is image, the block runs, otherwise ignore.
          const img = document.createElement('img');
          img.src = result.show.image.medium      
          document.body.append(img)                        
        }
      }
    }
    ```

<br>

__Making API calls with multiple query strings__

eg.:    
*multiple query strings*
`https://api.tvmaze.com/schedule?country=US&date=2014-12-01`

- With Axios we can set a so called *config object*:    
  `{ params: { q: searchTerm } }`

- `{ params : { own object with key-value pairs}, headers: { own object with key-value pairs} }` is set it to its own object → `{ q: searchTerm }`. We can add several things, like headers, etc.

- Every key value pair in the `{ q: something }` will be added to the query string

- let see in practice:   
  *We create a `const config` where we store the config params.*
  ```
  const form = document.querySelector('#searchForm');

  form.addEventListener('submit', async function (event){
    event.preventDefault()
    const searchTerm = form.elements.query.value;
    const config = { params: { q: searchTerm } };             //← we have the params
    const response = await axios.get(`http://api.tvmaze.com/search/shows`, config);                  //← we added the params
    makeImages(response.data)
    form.elements.query.value = '';         // empty the input

  })

  // a loop function

  const makeImages = (shows) => {
    for (let result of shows) {
      if (result.show.image) {          // if there is image, the block runs, otherwise ignore.
          const img = document.createElement('IMG');
          img.src = result.show.image.medium;
          document.body.append(img)
        }
    }
  }
  ```
  A little explanation about this example:      
  - The name `config` is a variable name that we arbitrarily chose. 
  - `config` it holds an object with the `params` key which the axios request will understand when we pass it as an argument. 
  - The key `q` is something that the particular API that we are using expects. 
  - To know what `params` we can pass to an API, we need to study the API documentation for the __route/address__ that we are sending a request to - that way we can know of all the options/params supported by the API endpoint in question.

💡 about the __[`params`](https://github.com/axios/axios#request-config)__, how to use, etc. we can read the details in the __Axios doc__.

---

  [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to AJAX](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#ajax)
  
<br>

# [Object Prototype - introduction to OOP](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes)   
__Prototypes__ are the mechanism by which JavaScript objects inherit features from one another. 

   - Prototypes are template objects (a bunch of methods).

   - We can create multiple objects that share the same prototype (so they all have acces to the same methods).

   - Objects can have a prototype object which acts as a template object. So it means is that certain objects eg.:  an array, have a a lot of methods.

   - [`__proto__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto#description) :   __it is a property that *references* the array prototype.__     
 So a prototype is the *template object* for in this case, arrays. It contains a bunch of methods typically.   
   Every array have access to all of these methods❗️ 
   - So rather than having a separate method on every single array called push, filter, concat, find, etc. , there is one prototype. Each array has a reference to that prototype, with a special property called `__proto__`❗️
   - __`__proto__` is a reference to the blueprint objet: the prototype__.

   - eg.:       
    *lets examine an other type of JS object the `document.body`*. 
      ```
      const body = document.body;
      
      console.dir(body);
      
      // ► body                           //←  we can see properties that are specific to this body
      //    ...
      //    background: ""
      //    baseURI: "chrome://newtab/"
      //    bgColor: ""
      //    ...
      //    ► __proto__: HTMLBodyElement   //← at the bottom there is __proto__
      //        aLink: (...)               //← __proto__ is an HTML body element, it has different methods and properties
      //        background: (...)
      //        bgColor: (...)
      //        link: (...)
      //        ...
      ```

- eg.:   
  *__`Array.prototype`__*    
  *With capital 'A', it is an individual instance of an array. We can see everything on that array prototype.*
  ```
  Array.prototype;

  // ► [constructor: ƒ, concat: ƒ, copyWithin: ƒ, fill: ƒ, find: ƒ, …]
  //    ► at: ƒ at()
  //    ► concat: ƒ concat()
  //    ► constructor: ƒ Array()
  //    ► copyWithin: ƒ copyWithin()
  //      ...
  ```

- eg.:    
  *__`String.prototype`__*   
  *We cen see a bunch of string methods.*
  
  ```
  String.prototype;

  // ► String {'', constructor: ƒ, anchor: ƒ, big: ƒ, blink: ƒ, …}    // bunch of string methods 
  //   ►  anchor: ƒ anchor()
  //   ►  at: ƒ at()
  //   ►  big: ƒ big()
  //      ...
  ```

  __We can add our own methods__
  - eg.:   
    *Adding our own methods, `foobar` to `String.prototype`.*
    ```
    String.prototype.foobar = () => { console.log("Hello!") }

    //nothing happened. 
    //But if we look the String.prototype, it has a property 'foobar'

    String.prototype;

    // ► String {'', constructor: ƒ, anchor: ƒ, big: ƒ, blink: ƒ, …}   
    //   ►  🔹foobar  
    //   ►  anchor: ƒ anchor()
    //   ►  at: ƒ at()
    //      ...
    ```
    *Lets make a new string and add our new string method 'foobar()'.*
    ```
    const dog = "Black";

    dog.foobar();

    // "Hello!"
    ```

    __Adding and defining our own method on the `String.prototype`__

   - eg.:      
      *Creating a method `hello` on the String.prototype object, so it will be in the String.prototype.*
      ```
      String.prototype.hello = function() {
        console.log(`Good day ${this}!!!`);
      };

      // just typing a string and adding our method
      "John Doe".hello();

      // "Good day John Doe!!!"
      ```

    __Overwriting our method to an Array.prototype__*(same process is valed for other prototypes, like String.prototype)*
    - eg.:    
      *Overwriteiny an existing `pop` method on the Array.prototype*
      ```
      Array.prototype.pop = function() {
        return "Say hi to this array";
      };

      // calling an array

      [3, 4, 5].pop;

      // instead of popping
      // "Say hi to this array"
      ```

💡 The difference between `String.prototype` or `Array.prototype` vs. `__proto__`:    
`String.prototype` is the actual prototype object, where `__proto__` inside a string or array or etc. is a reference to the `String. prototype` (or `Array.prototype`, or other stuff).

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👇 jump to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>


# [OOP- Object-oriented Programming](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_programming)    
An Object is a unique entity that contains property and methods.   
- the characteristics of an Object are called as Property, in Object-Oriented Programming and the actions are called methods.
- an Object is an instance of a class. Objects are everywhere in JavaScript almost every element is an Object whether it is a function, array, and string.  

<br>

__What is an object__:   
- In OOP we combine a groupd related functions and variables into a unit, and this unit is called an __object__.    
- We refer the object's variables as __properties__. 
- We refer the object's functions as __methods__.    
`function() variable` → function() is method and variable is property.   

- eg.:    
  A car:    
  it has properties: color, model.   
  it has methods: start(), stop(), move()

<br>

[encapsulation](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#1-encapsulation)   
[abstraction](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#2-abstraction)   
[inheritance](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#3-inheritance)   
[polymorphism](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#4-polymorphism)   
[Creating Objects](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#creating-objects)   
[Factory Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#factory-functions)    
[Constructor Functions](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#constructor-function)    
[Constructor Property](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#constructor-property)   
[Functions are Objects](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#functions--objects-1)   
[Value vs Reference Type](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#value-vs-reference-type-1)    
[Adding/Removing Properties](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#addingremoving-properties) →  *[(adding)](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#adding-properties)* | *[(removing)](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#deleting-properties)*   
[Enumerating Properties](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#enumerating-properties)    
[Private Properties and Methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#private-properties-and-methods)    
[Getters and Setters](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#getters-and-setters)     
[Classes](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#classes)     


<br>

## __[the 4 core concepts of OOP](https://medium.com/@khmel87/javascript-four-principles-of-object-oriented-programming-cd81a04262cb#:~:text=There%20are%20four%20main%20principles,abstraction%2C%20inheritance%2C%20and%20polymorphism.)__

### 1. __[encapsulation](https://www.javatpoint.com/javascript-oops-encapsulation)__   
encapsulation is: we group related variables and functions that operate on the variables into objects.    
So, in other words binding the data (variables) with the functions acting on that data. 

- reduce complexity
- increase reusbaility

- eg.:  
  *Calculate the wage of an employee.*   
  *This is a procedural implementation: variables on one side, function(s) on the other side.*  
  ```
  let baseSalary = 30000;
  let overTime =  10;
  let rate = 20;

  function getWage(baseSalary, overTime, rate) {
    return baseSalary + (overTime * rate);
  }
  ```
  *Let's turn this to an OOP way, so we create an `employee` object.*   
  ```
  let employee = {
    let baseSalary = 30000,   // ← property of the object
    let overTime =  10,
    let rate = 20,
    getWage: function () {
      return this.baseSalary + (this.overTime * this.rate);
    }
  };

  employee.getWage();
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

### 2. __[abstraction](https://www.javatpoint.com/javascript-oops-abstraction)__
 is a way of hiding the implementation details and showing only the functionality to the users. In other words, it ignores the irrelevant details and shows only the required one.

 - simpler interface of the objects:   
 using only a few properties and methods
 - reduces the impact of change:   
 the change on an object doesn't impact the rest of the application.   

 <br>

 - reduce complexity
 - isolate the impact of changes in the code

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

 ### 3. __[inheritance](https://www.tutorialsteacher.com/javascript/inheritance-in-javascript)__
inheritance allows us to eliminate redundant code.      
So, using less code: we define an object, and other objects can inherit those properties and methods.   

- eg.: we have several HTML elements like button, checkbox, select. We define an htmlElement object, and help other objects inherit those methods and properties which are deifned in the htmlElement object.

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>


### 4. __[polymorphism](https://www.javatpoint.com/javascript-oops-polymorphism#:~:text=The%20polymorphism%20is%20a%20core,data%20members%20with%20the%20methods.)__   
(poly = many, morph = form)   
it is a technique that allows us to get rid of long `if and else` or `switch and case` statements.   

- defining a specific method on several objects, and that specific method behaves differently depending on the object we are referencing.

- refactor ugly if/else and switch/case statements

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Creating Objects](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_programming#classes_and_instances)__

__creating an object using the [`object literal syntax`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer), referred as `{}`__ ❗️

(An object in JS is a collection of key:value pairs.)

- eg.:   
  *Creating object with the: [object literal syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer).*   
  *Creating a circle object.*    
  *This object has 3 members: `radius`, `location` and `draw`.*   
  *`draw` is a function, so we refer to it as a method.*
  *`radius` and `location` are properties.*
  ```
  const circle = {
    radius : 1,                           //← property
    location : {                          //← property
      x : 1,
      y : 1
    },
    draw : function() {                   //← method
      console.log("Drawing a circle");
    }
  };
  ```
  *We can access the `circle`'s members with the `.` dot notation.*   
  *Here we are calling the `draw()` method.*
  ```
  circle.draw();

  // Drawing a circle
  ```
  
---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## [Factory Functions](https://www.geeksforgeeks.org/what-are-factory-functions-in-javascript/) 
In object-oriented programming (OOP), a factory is an object for creating other objects – formally a factory is a function that returns objects of a varying prototype or class from some method call.

- if an Object has 1 or more method, we call it as object has behaviour (like a person).

- when a function creates and returns a new object, it is called a factory function. By using the factory function, we can create any number of the eg.: `circle` objects without duplicating code, and it could be several different circle objects depending on some parameter.

- eg.:    
*The circle object (which has no behaviour).*
```
 const circle = {
    radius : 1,
  };
```
*We use factory function to create the circle object.*   
*We add the `draw()` method.*
  ```
  //Factory Function

  function createCircle(radius){
    return {
      radius,                         //← normally it is "radius : radius", if key and value are the same name, we can just use one name.
      draw: function(){
        console.log("Drawing a circle");
      }
    };
  }

  const circle = createCircle(1);    // (1) is the radius

  circle.draw;

  // ƒ (){
  //    console.log("Drawing a circle");
  //  }
  ```

Other, more in-depth example:   
eg.:    

*This code converts RGB color to HEX colors*

  ```
  function hex(r, g, b) {
    return '#' + ((1 << 24) + (r << 16) + (g << 8) + b).toString(16).slice(1);
  }

  // takes rgb values in the r, g, and b
  hex(255, 100, 25);

  //gives back:
  // "#ff6419" 

  //another function for rgb
  function rgb(r, g, b){
    return `rgb(${r}, ${g}, ${b})`
  }

  rgb(255,100,25)

  //gives:
  //"rgb(255, 100, 25)" 
  ```

*Instead of having 2 functions and each time we have to type the R, G, B numbers, we can createa a __factory function__. We can pass in R, G and B.*

  ```
  // factory function
  function makeColor(r, g, b){
    // color is an empty object, so we can add stuff to it
    const color = {};

    // the values of the makeColor(r, g, b) we can pass in
    color.r = r;
    color.g = g;
    color.b = b;

    return color 
  }

  makeColor(40, 50, 60);

  //▶︎ Object { r: 40, g: 50, b: 60 }
  ```

*We add a method in our factory function*   
*__The factory name comes from__ this: we pass in some values, the factory makes an object and returns it at the end, so we can use it.*

  ```
  // factory function
  function makeColor(r, g, b){
    const color = {};
    color.r = r;
    color.g = g;
    color.b = b;

    // adding a method
    color.rgb = function() { 
      // instead of hard-coding, we add the `this ` keyword
      //`this` refers to the object `const color = {};`
      return `rgb(${this.r}, ${this.g}, ${this.b})`;
      // or simply just destructure `const {r, g, b} = this;`
    }

    return color 
  }

  const firstColor = makeColor(100,200,250);
  firstColor.rgb();

  //"rgb(100, 200, 250)" 
  ```

💡 Check out [Destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment):   
 this expression makes it possible to unpack values from arrays, or properties from objects, into distinct variables.

*Lets give the `hex` function to our factory function*   

  ```
  // factory function
  function makeColor(r, g, b){
    const color = {};
    color.r = r;
    color.g = g;
    color.b = b;

    // rgb
    color.rgb = function() { 
      // using the destructuring assignment
      const {r, g, b} = this;
      return `rgb(${r}, ${g}, ${b})`;
    };

    //hex
    color.hex = function() {
      const {r, g, b} = this;
      return '#' + ((1 << 24) + (r << 16) + (g << 8) + b).toString(16).slice(1);
    }

    return color 
  }

  const firstColor = makeColor(100,200,250);
  firstColor.hex();

  // "#64c8fa" 
  ```

*It is also possible to chage the value, like the R's value*
  
  ```
  const firstColor = makeColor(100,200,250);
  firstColor.r = 10

  // let's check the firstColor.rgb();
  firstColor.rgb();

  //"rgb(10, 200, 250)"
  ```

So the __factory function__ is a way of making objects based off of a pattern or a recipe.   
 
So the fatory function makes us __an object__ `const color = {}`.     
`const color = {}` object starts empty, but the we add some __properties__ `color.r = r; color.g = g; color.b = b;`.    
Then we add some __methods__ `color.rgb = function() { ... }` and `color.hex = function() { ... }`.     
Then we __return__ the `color` object.

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Constructor Function](https://www.programiz.com/javascript/constructor-function)__

The [__`new`__](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new) operator❗️:       
  to create an instance of a user-defined object type or of one of the built-in object types that has a constructor function.   
  
  - function name starts with capital letter `function Color()` → just indicating that it is a constructor function (function to create objects)
  - inside the function no return value
  - referencing directly in the function when using `this`

  
  
  
- eg.:   
    ```
    function Color(r, g, b) {
      this.r = r;
      this.g = g;
      this.b = b;
    }
    
    Color(255, 0, 0)
    // undefined
    ```
    __But, when we call the `Color` function with `new` before the function call, it behaves differently.__
    ```
    function Color(r, g, b) {
      this.r = r;
      this.g = g;
      this.b = b;
    }

    // it sets the constructor of `this` object to another object
    // it creates a new object, set `this`
    // so we give R B G to that new object
    // return `this` at the end
    new Color(255, 0, 0)

    // we get an object, it has properties:​ b: 0 g: 0 r: 255
    //► { r: 255, g: 0, b: 0 }
    //  ►<prototype>: 
    //     ►constructor: function Color(r, g, b)
    ```
    *If we don't use the `new` keyword, `this` referes to the window object (check it by writing `console.log(this)` in the `function Color(r,g,b){...}`).*    
    
    When we call a function with `new` before the function call, that function will be used as a constructor.    
    
    The `new` do the following things:

1. Creates a blank, plain JavaScript object. For convenience, let's call it `myinstance`.    

2. Points `myinstance`'s `[[Prototype]]` to the constructor function's `prototype` property, if the `prototype` is an Object. Otherwise, `myinstance` stays as a plain object with `Object.prototype` as its `[[Prototype]]`.    

3. Executes the constructor function with the given arguments, binding `myinstance` as the `this` context (i.e. all references to `this` in the constructor function now refer to `myinstance`).
4. If the constructor function returns a *non-primitive*, this return value becomes the result of the whole `new` expression. Otherwise, if the constructor function doesn't return anything or returns a *primitive*, `myinstance` is returned instead.    (Normally constructors don't return a value, but they can choose to do so to override the normal object creation process.)



*So if we call `new Color(255, 0, 0)` and save that to a variable `const color1`, we have an object that has RGB, but not only that. It does not have that method RGB defined on the actual object, it's defined on the `prototype`.*
```
function Color(r, g, b) {
      this.r = r;
      this.g = g;
      this.b = b;
  }

const color1 = new Color(255, 0, 0)

color1
//►Object { r: 255, g: 0, b: 0 }
//  ​b: 0
//  ​g: 0
//  ​r: 255
​//  ►<prototype>: Object { … }
​​//      constructor: function Color(r, g, b)   //← the RGB method is defined on the prototype
```
*We can __add methods to the__ `Color` __prototype__: we define that method __outside of the constructor function__ (outside of the `function Color(r,g,b){...}`).*      
*So so that the methods are only defined once (rather than on each individial color as in the factory function ).*

*Also, we can have several color obejcts*
```
function Color(r, g, b) {
      this.r = r;
      this.g = g;
      this.b = b;
  }

//we define the method outside of the the constructor function❗️
Color.prototype.rgb = function() {
  const {r, g, b} = this;
  return `rgb(${r}, ${g}, ${b})`;
};

const color1 = new Color(255, 0, 0);
const color2 = new Color(10, 10, 10);
const color3 = new Color(0, 0, 0);
```

In short, __constructor__ method is more efficient than the __factory__ approach where we return a new object every time it is called.


---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Functions = Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)__
functions are first-class objects in JS, because they can have properties and methods just like any other object.     
What distinguishes functions from other objects is that functions can be called.

- eg.:   
  *We can add properties and/or methods to our function, just as we do it with other objects.*
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  Circle.name;        //← adding a property
  Circle.length;      //← adding a property
  
  //'Circle'
  // 1
  ```
  *We add the `.call()` method to the `Circle` function.*   
  *With `call()` we can call a function.*  

  *Circle.call({}, argument) → we have to pass an empty objects. The `this.something` in the `function Circle(radius)` references that `{}` empty object in the `Circle.call({}, argument)`.*
  ```
   function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  Circle.call({}, 1);           //this expression is exactly this `const circle = new Circle(1);`❗️    

  const circle = new Circle(1);     //(1) is the argument
  ```
  *So the `Circle.call({}, 1);` expression is exactly `const circle = new Circle(1);`.*   
  *Because, when we use the `new` operator, it internally creates an empty object `{}`, and pass it as the first argument to the `call()` method.*
  ```
  //with apply method we can pass an array to the function as an argument

  Circle.apply({}, [1, 2, 3, 4]);  
  Circle.call({}, 1);  

  ```
  
 ---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br> 

## __[Value vs Reference Type](https://dmitripavlutin.com/value-vs-reference-javascript/#:~:text=In%20JavaScript%2C%20you%20can%20pass,by%20reference%20when%20assigning%20objects.)__
We can pass by __value__ and by __reference__ in JS.    
The main difference between the two is that passing by value happens when assigning primitives while passing by reference when assigning objects.

- we have 2 categories of types:   
  1. Value Type (also called primitives)  
      - number, string, boolean, symbol, undefined, null
  2. Reference Types
      - object
      - function
      - array

💡 Primitives are copied by their value.         
💡 Objects are copied by their reference.

*So technically in JS we have primitives and objects.*

- eg.:   
  *We define 2 primitives, `x` and `y`, they are __2 independent variables__ ❗️*  

  *The value (`10`) is stored in `x`. When we copy the `x`, we copy the value what `x` stores, it is copied ont the `y` variable.*    
  *So they are completely independent from eachother.*
  ```
  let x = 10;
  let y = x;

  x = 20;

  x;
  // 20

  y;
  // 10
  ```
  *Now, we are using a reference type (an object).*    
  *When we use the `{value: 10}` object, the object is not stored in the `x` variable.*   
  *`{value: 10}` object is stored somewhere else in the memory.*   
  *The address of the memory location is stored in the `x` variable (not the value).*    
  *When we copy `x` into the `y`, it is the address (reference) what is copied. → `x` & `y` are pointing to the same object in the memory.*
  ```
  let x = {value: 10};        //← an object, key-value pairs
  let y = x;

  x.value = 20;

  x; 
  // {value: 20};

  y;
  // {value: 20};
  ```

- eg.:   
  *Primitives are copied by their value.*  
  *When we call `increase(number)`, its value is copied on to the function's parameter `  function increase(number)`. The `number++`'s scope is local in the function.*   
  *The `number++` insode the function is independent from the `let number = 10`.*  
  *The `console.log(number);` is basically dealing woth the `let number = 10;` and not the function's `number++`. Because they are independent.*
  ```
  let number = 10;

  function increase(number) {
    number++;
  }

  increase(number);       //← call increase() and pass the number as an argument
  console.log(number);
  // 10;
  ```
  *Now lets use an object `let obj = {value: 10};`*   
  *`function increase(obj)` is pointing to the same object (reference to the same object) as `let obj = {value: 10};`.*    
  *So these are not independent copies.*
  ```
  let obj = {value: 10};

  function increase(obj) {
    obj.value++;
  }

  increase(obj);
  console.log(obj);

  // {value: 11}
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Constructor Property](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/constructor)__   
  every object in JS has a property called `constructor`.  
  `constructor` references a function which was used to construct (create) an object.

- `Object()` function is a built-in constructor function 

- when we create an object using the object literal syntax `{}`, the JS engine uses the `Object()` constructor function (internally).

- eg.:    
  *x's object literal `{}` references the `Object()` constructor*   
  *`new String;` instead we use the string literal  `''` or `""`.*    
  *`new Boolean;`instead we use boolean literals, `true` or `false`.*      
  *`new Number;` instead we use number literal `1, 2, 3` etc.*    
  ```
  let x = {}

  //JS engine translates it: let x = new Object()
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Functions = Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)__
functions are first-class objects in JS, because they can have properties and methods just like any other object.     
What distinguishes functions from other objects is that functions can be called.

- eg.:   
  *We can add properties and/or methods to our function, just as we do it with other objects.*
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  Circle.name;        //← adding a property
  Circle.length;      //← adding a property
  
  //'Circle'
  // 1
  ```
  *We add the `.call()` method to the `Circle` function.*   
  *With `call()` we can call a function.*  

  * Circle.call({}, argument) → we have to pass an empty objects. The `this.something` in the `function Circle(radius)` references that `{}` empty object in the `Circle.call({}, argument)`.
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  Circle.call({}, 1);           //this expression is exactly this `const circle = new Circle(1);`❗️    

  const circle = new Circle(1);     //(1) is the argument
  ```
  *So the `Circle.call({}, 1);` expression is exactly `const circle = new Circle(1);`.*   
  *Because, when we use the `new` operator, it interannyl creates an empty object `{}`, and pass it as the first argument to the `call()` method.*
  ```
  //with apply method we can pass an array to the function as an argument

  Circle.apply({}, [1, 2, 3, 4]);  
  Circle.call({}, 1);  

  ```
---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Value vs Reference Type](https://dmitripavlutin.com/value-vs-reference-javascript/#:~:text=In%20JavaScript%2C%20you%20can%20pass,by%20reference%20when%20assigning%20objects.)__
We can pass by __value__ and by __reference__ in JS.    
The main difference between the two is that passing by value happens when assigning primitives while passing by reference when assigning objects.

- we have 2 categories of types:   
  1. Value Type (aslo called primitives)  
      - number, string, boolean, symbol, undefined, null
  2. Reference Types
      - object
      - function
      - array

💡 Primitives are copied by their value.       
💡 Objects are copied by their reference.

*So technically in JS we have primitives and objects.*

- eg.:   
  *We define 2 primitives, `x` and `y`, they are __2 independent variables__ ❗️*        

  *The value (`10`) is stored in `x`. When we copy the `x`, we copy the value what `x` stores, it is copied ont the `y` variable.*          
  *So they are completely independent from eachother.*
  ```
  let x = 10;
  let y = x;

  x = 20;

  x;
  // 20

  y;
  // 10
  ```
  *Now, we are using a reference type (an object).*    
  *When we use the {value: 10} object, the object is not stored in the `x` variable.*   
  *`{value: 10}` object is stored somewhere else in the memory.*   
  *The address of the memory location is stored in the `x` variable (not the value).*    
  *When we copy `x` into the `y`, it is the address (reference) what is copied. → `x` & `y` are pointing to the same object in the memory.*
  ```
  let x = {value: 10};        //← an object, key-value pairs
  let y = x;

  x.value = 20;

  x; 
  // {value: 20};

  y;
  // {value: 20};
  ```

- eg.:   
  *Primitives are copied by their value.*  
  *When we call `increase(number)`, its value is copied on to the function's parameter `  function increase(number)`. The `number++`'s scope is local in the function.*   
  *The `number++` inside the function is independent from the `let number = 10`.*  
  *The `console.log(number);` is basically dealing with the `let number = 10;` and not the function's `number++`. Because they are independent.*
  ```
  let number = 10;

  function increase(number) {
    number++;
  }

  increase(number);       //← call increase() and pass the number as an argument
  console.log(number);
  // 10;
  ```
  *Now lets use an object `let obj = {value: 10};`*   
  *`function increase(obj)` is pointing to the same object (reference to the same object) as `let obj = {value: 10};`.*    
  *So these are not independent copies.*
  ```
  let obj = {value: 10};

  function increase(obj) {
    obj.value++;
  }

  increase(obj);
  console.log(obj);

  // {value: 11}
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Adding/Removing Properties](https://www.geeksforgeeks.org/how-to-add-and-remove-properties-from-objects-in-javascript/)__
objects are dynamic: after we created an object we can add extra properties in them or delete some properties.

### __Adding properties__
- eg.:   
  *We have the `circle` object, and we want to add something, a new property which holds a text.*    
  *We can add this property whenever we need it, we don't have to define it before.*   
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  const circle = new Circle(10);

  // add a new property to the circle object

  circle.location = { x: 1};      //← we set it to { x: 1};

  circle;
  //► Circle {radius: 10, location: {…}, draw: ƒ}
  // ► draw: ƒ ()
  // ► location: {x: 1}
  // ►  radius: 10
  ```
*Accessing properties with `[]` bracket notatition.*   
*Using `[]` and a string `['reference_a_property']` to reference the property.*
```
circle.['location'] = {x: 1};  //← same as circle.location = { x: 1};

circle;
//► Circle {radius: 10, location: {…}, draw: ƒ}
// ► draw: ƒ ()
// ► location: {x: 1}
// ►  radius: 10
```
*Bracket notation is useful when we want to access dynamically the name of the property (so when we don't know the name of that property).*   
```
const propertyName = 'location';
circle.[propertyName] = { x: 1};
```

<br>

#### __Deleting properties__
using the `delete` operator and reference the property name.

- eg.:   
  *Removing the 'location' property.*
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }
  const circle = new Circle(10);

  circle.location = { x: 1};      //← we set it to { x: 1};

  // DELETE the property

  delete circle.location;

  // we can also use the bracket `[]` notation instead of the `.` dot notation

  delete circle.['location'];
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Enumerating Properties](https://www.oreilly.com/library/view/javascript-the-definitive/9781449393854/ch06s05.html)__   
Instead of testing for the existence of individual properties, we sometimes want to iterate through (or enumerate) a list of all the properties of an object. This is usually done with the for/in loop.   

- eg.:  
  *[Enumerating](https://www.merriam-webster.com/dictionary/enumeration) the circle object.*
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }
  const circle = new Circle(10);

  for (key in circle){
    console.log(key);
  }

  // radius
  // draw
  ```
  *To get the __value__ of the properties with iteration, we can use the bracket `[]` notation.*   
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  const circle = new Circle(10);
  for (key in circle){
    console.log(key, circle[key]);
  }

  // radius 10
  // draw ƒ () {
  //    console.log("Drawing a circle");
  //  }
  ```
  *If we want ot get __only__ the properties and not the methods. This case, we can use the `typeof` operator, to check the type of the value.*
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  const circle = new Circle(10);

  for (key in circle){
    if (typeof circle[key] !== 'function')
      console.log(key, circle[key]);
  }

  // radius 10
  ```
  The [`Object.keys`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys) method:   
  *Another approach to get all the keys of an object, by using the Object which has a method `keys` and we pass the `circle` object. This returns all the keys of the `circle` object as an array.*
  ```
  function Circle(radius){
    this.radius = radius;     
    this.draw = function() {
      console.log("Drawing a circle");
    }
  }

  const circle = new Circle(10);

  Object.keys(circle);

  //► (2) ['radius', 'draw']
  ```
  *Check for the existence of propert or a methodin an object we is the `in` operator.*   
  ```
  if ('radius' in circle) {
    console.log('Circle has a radius.');
  }

  // Circle has a radius.
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Private Properties and Methods](https://javascript.info/private-protected-properties-methods)__    
One of the most important principles of object oriented programming – delimiting internal interface from the external one.   

### [Abstraction](https://developer.mozilla.org/en-US/docs/Glossary/Abstraction)
Abstraction means that hide the details and complexity and show only the essentials.   

It is useful, because by hiding complexity, eg.: we do not expose our methods, it won't be modifiably from the outside. Thus we avoid that making changes from the outside can create errors in our complex program. We can tell where exactly we allow to modify that method.

- eg.:   
  *In the `Circle` object we want to hide the `defaultLocation` and the `optimumLocation` because they are the complexity of this object.*     *Instead we expose only the essentials: `radius` and `draw`.*  
  ```
  function Circle(radius){
    this.radius = radius; 

    this.defaultLocation = {x: 0, y: 0};
    this.optimumLocation = function (){
      console.log('Very complex function.');
    } 

    this.draw = function() {
      this.optimumLocation;
    }
  }
  ```
  *So, we set the `this.defaultLocation` as a local property of the `Circle` object by using the `let`. With this technique it is only accessible in the object (outside it dies).*     
  *We convert `optimumLocation` to a private method: `let optimumLocation`.* 
  ```
  function Circle(radius){
    this.radius = radius;  

    let defaultLocation = {x: 0, y: 0};
    let optimumLocation = function (){
      console.log('Very complex function.');
    }   

    this.draw = function() {
      console.log("Drawing a circle");
    }
  }  
  ```
  [Closure](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures): __closure is a function that references variables in the outer scope from its inner scope.__     
  *We have the `draw` function inside of the `Circle` function. `optimumLocation` is defined in the `Circle` so it is accessible in the `draw` function.*   
  ```
  function Circle(radius){
    this.radius = radius;  

    let defaultLocation = {x: 0, y: 0};
    let optimumLocation = function (factor){
      console.log('Very complex function.');
    }   

    this.draw = function() {
      optimumLocation(0.1);           //← closure
      console.log("Drawing a circle");

      this.radius;                    //← we want to use members of the Circle, we have to use `this`
    }
  }   

  // we can not access outside the 'defaultLocation' and 'optimumLocation'. We can only access 'radius' and 'draw'.
  const circle = new Circle(10);
  circle.draw();


  // Very complex function.
  // Drawing a circle
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>


## __[Getters and Setters](https://javascript.info/property-accessors)__
they are object properties, precisely *accessor properties*.   
They are essentially functions that execute on *getting* and *setting* a value, but look like regular properties to an external code.

### [Getter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/get)   
The get syntax __binds an object property to a function that will be called when that property is looked up.__        

A `get`ter is a function to read a property.

- eg.:    
  *We have a private property (in OOP point of view) `let defaultLocation`. We can not access it outside of the `Circle` object.*    
  *But we want to be able to read this `defaultLocation` (we don't want to modify it).*   
  
  __[Object.defineProperty](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty):  defines a new property directly on an object.__   
  
  *The 1st argument of this method is the object that we want to add a new property to: here is the `this`, the new Circle object.*    
  *The 2nd argument is the name of our property: `'defaultLocation'`*    
  *The 3rd argument is an object which has a key:value pair → the key is `get`, the value is a `function`. In this function we return the `defaultLocation`.*
  ```
  function Circle(radius){
    this.radius = radius;  

    let defaultLocation = {x: 0, y: 0};


    this.draw = function() {
      console.log("Drawing a circle");             
    }

    Object.defineProperty(this, 'defaultLocation', {
      get : function() {
        return defaultLocation;   //← defaultLocation is a closure of the inner function
      }
    })
  }   

  const circle = new Circle(10);
  circle;

  //▼ Circle {radius: 10, draw: ƒ}
  //  draw: ƒ ()
  //  radius: 10
  //  defaultLocation: Object     //← get function is executed, the result is x: 0. y:0
  //    x: 0
  //    y: 0
  //    ► [[Prototype]]: Object
  //  ► get defaultLocation: ƒ () //← defaultLocation also stored here: a getter function (used to read a property)
  //  ► [[Prototype]]: Object
  ```

### [Setter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/set)   
The set syntax __binds an object property to a function to be called when there is an attempt to set that property.__   


We want to change the value of the `defaultLocation` function from the outside.   

- eg.:     
  *We have to define a `setter` in the `Object.defineProperty`, to be able to modify the `defaultLocation` from the outside of the object.*      
  ```
  function Circle(radius){
    this.radius = radius;  

    let defaultLocation = {x: 0, y: 0};


    this.draw = function() {
      console.log("Drawing a circle");             
    }

    Object.defineProperty(this, 'defaultLocation', {
      get : function() {
        return defaultLocation;   //← defaultLocation is a closure of the inner function
      },
      set : function(value) {
       // put here some validation 
        if (!value.x || !value.y)   //← if value.x is falsy or value.y is falsy
          throw new Error('Invalid location');;         //← Error is a built in constructor
        defaultLocation = value;
      } 
    })
  } 

  const circle = new Circle(10);
  circle.defaultLocation = 1;

  // Error: Invalid location
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>

## __[Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)__    
Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.

We use class when we need many objects of the same type.

So class is a template for an object in the code. It makes it easier, quicker and more reliable to build several objects of the same type (called *instances of the same class*).

- eg.:   
  *Defining a Class*. 
  ```
  class Book {
  }
  ```
  *For this class, we want each Book to have a title, an author and a number of pages. To do this, we use what is called a constructor.*
  ```
  class Book {
    constructor(title, author, pages) {
    }
  }
  ```
  💡 *The constructor of a class is the function that is called when a new instance of that class is created with the keyword `new`.*    
  *We use the `this` keyword and the dot notation to assign the title, author and number of pages received to this instance.*
  ```
  class Book {
    constructor(title, author, pages) {
        this.title = title;
        this.author = author;
        this.pages = pages;
     }
  }
  ```
  *Here, the keyword `this` refers to the new instance. So it uses the dot notation to assign the received values to the corresponding keys.*
  *Now that the class is complete, we can create instances with the keyword `new`.*
  ```  
  let myBook = new Book("The Lord of the Rings", "J. R. R. Tolkien", 1250);    
   //creating the following object ↓
  {
      title: "The Lord of the Rings",
      author: "J. R. R. Tolkien",
      pages: 1250
  }
  ```
  *With a Book class, we can easily and quickly create new Book objects.*
  
---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>  

## [Object prototypes](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes)   
__Prototypes__ are the mechanism by which JavaScript objects inherit features from one another. 

   - Prototypes are template objects (a bunch of methods).

   - We can create multiple objects that share the same prototype (so they all have acces to the same methods).

   - Objects can have a prototype object which acts as a template object. So it means is that certain objects eg.:  an array, have a a lot of methods.

   - [`__proto__`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/proto#description) :   __it is a property that *references* the array prototype.__     
 So a prototype is the *template object* for in this case, arrays. It contains a bunch of methods typically.   
   Every array have access to all of these methods❗️ 
   - So rather than having a separate method on every single array called push, filter, concat, find, etc. , there is one prototype. Each array has a reference to that prototype, with a special property called `__proto__`❗️
   - __`__proto__` is a reference to the blueprint objet: the prototype__.

   - eg.:       
    *lets examine an other type of JS object the `document.body`*. 
      ```
      const body = document.body;
      
      console.dir(body);
      
      // ► body                           //←  we can see properties that are specific to this body
      //    ...
      //    background: ""
      //    baseURI: "chrome://newtab/"
      //    bgColor: ""
      //    ...
      //    ► __proto__: HTMLBodyElement   //← at the bottom there is __proto__
      //        aLink: (...)               //← __proto__ is an HTML body element, it has different methods and properties
      //        background: (...)
      //        bgColor: (...)
      //        link: (...)
      //        ...
      ```

- eg.:   
  *__`Array.prototype`__*    
  *With capital 'A', it is an individual instance of an array. We can see everything on that array prototype.*
  ```
  Array.prototype;

  // ► [constructor: ƒ, concat: ƒ, copyWithin: ƒ, fill: ƒ, find: ƒ, …]
  //    ► at: ƒ at()
  //    ► concat: ƒ concat()
  //    ► constructor: ƒ Array()
  //    ► copyWithin: ƒ copyWithin()
  //      ...
  ```

- eg.:    
  *__`String.prototype`__*   
  *We cen see a bunch of string methods.*
  
  ```
  String.prototype;

  // ► String {'', constructor: ƒ, anchor: ƒ, big: ƒ, blink: ƒ, …}    // bunch of string methods 
  //   ►  anchor: ƒ anchor()
  //   ►  at: ƒ at()
  //   ►  big: ƒ big()
  //      ...
  ```

  __We can add our own methods__
  - eg.:   
    *Adding our own methods, `foobar` to `String.prototype`.*
    ```
    String.prototype.foobar = () => { console.log("Hello!") }

    //nothing happened. 
    //But if we look the String.prototype, it has a property 'foobar'

    String.prototype;

    // ► String {'', constructor: ƒ, anchor: ƒ, big: ƒ, blink: ƒ, …}   
    //   ►  🔹foobar  
    //   ►  anchor: ƒ anchor()
    //   ►  at: ƒ at()
    //      ...
    ```
    *Lets make a new string and add our new string method 'foobar()'.*
    ```
    const dog = "Black";

    dog.foobar();

    // "Hello!"
    ```

    __Adding and defining our own method on the `String.prototype`__

   - eg.:      
      *Creating a method `hello` on the String.prototype object, so it will be in the String.prototype.*
      ```
      String.prototype.hello = function() {
        console.log(`Good day ${this}!!!`);
      };

      // just typing a string and adding our method
      "John Doe".hello();

      // "Good day John Doe!!!"
      ```

    __Overwriting our method to an Array.prototype__*(same process is valed for other prototypes, like String.prototype)*
    - eg.:    
      *Overwriteiny an existing `pop` method on the Array.prototype*
      ```
      Array.prototype.pop = function() {
        return "Say hi to this array";
      };

      // calling an array

      [3, 4, 5].pop;

      // instead of popping
      // "Say hi to this array"
      ```

💡 The difference between `String.prototype` or `Array.prototype` vs. `__proto__`:    
`String.prototype` is the actual prototype object, where `__proto__` inside a string or array or etc. is a reference to the `String. prototype` (or `Array.prototype`, or other stuff).

---

[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆 go to OOP](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#oop--object-oriented-programming)

<br>
