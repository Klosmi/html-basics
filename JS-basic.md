[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

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
  - __methods__ are built-in __ACTIONS__ we can perform with individual __strings__.   

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

- (an obejct is a collection of properties and methods.)

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
  since everything is truythy excpe twhen falsy, when you write something to the input, is going to be true.
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
  if (0) {  // null, NaN, undefined aslo Falsy
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
      * we expect that it will sort ascending, but becuase it uses teh 1st digit, the result is different*
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
  - __[Object methods](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#special-obejct-methods)__:    
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

- when writing a loop always make sure that how your loop will end, to avoid infinte loops.

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
  one syntax: __`while`__ and then insode of the parentheses, a __(single condition)__.
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

## __special Obejct methods__:
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
  
  - in this case we have to tell the function, how many arguemnts we'll use.
  
  - separate the paramteres & arguements by a __comma__.

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

- A __[factory function](https://www.codecademy.com/courses/introduction-to-javascript/lessons/advanced-objects/exercises/factory-functions)__: is a function that __returns an object and can be reused to make multiple object instances__.   
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
 - If a function is part of an obejct, it is called a method → If the function is a method in an object, `this` references that object itself.   
   Otherwise, if that function is a regular function, so it's not part of an obejct, `this` references the global object, the `window`. 

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
__It to runs a function__, (so run some code) __once per item in some array__.   
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
Basically when we don't use a paramter, we can give it a default value.

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
- we add an __`=`__ sign to the paramters in the function. 
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
    *we can use multiple default paramters*
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

  // NaN          // because we passed a single array full of numbers, not multiple sperate arguemnts
  ```
  *so we are going to use the __spread syntax__, and by that, we're separating the `nums` into separate arguments, so the functions can use it.*
  ```
  const nums = [3, 5, 9, 1];

  Math.max(...nums);           // num array spreaded out into separate arguemnts: 3, 5, 9, 1
  // 9
  ```
  *the __`...`__ syntax doesn't change `nums`*   
 
- eg.:   
  *using `console.log`, and printing out `nums`. Then using the separate syntax, see the differnce: __each element from `nums` array passed in as a separate argument__ to the `console.log`.*
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
- collects the __rest__ of the paramters, arguemnts

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
    *With rest, the `reduce` function will work, because `rest` creates an array`
    ```
      function sum(...num) {
      return num.reduce((total, num) => total + num)
    }

    sum(1, 2, 3);
    // 6
    ```

<br>

_bonus: about the `arguments` object__

  - it automatically holds all of the arguments passed into a function.  
  - it's an array __like__ object:   
    - it has a length property
    - doesn't have array methods (like push or pop, reduce, etc.)
  - it's available inside every function
  - __contains all the arguemnts passed to the function__
  - __not available inside of arrow functions__!

    - eg.:   
      *We have a function, with no arguments. Inside the function we print out the `arguments` object. When we give arguments to the function, the `arguemtns` object will contain those values, in an order, like an array. So it looks like an array but it's not an array → we can't use array methods.*   
      ```
      function sum() {
        console.log(arguments);
      }

      sum();                    // arguemnts is empty
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

- the name matters (how we access the value insode of the object)

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

# __[The DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)__  
*Document Object Model*  
A bunch of __JavaScript objects that represents the webpage__.

It's our window, our access portal into the contents of a Web page from JavaScript.  

So the DOM is a JS representation of a webpage.   
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

- [tree structure](https://developer.mozilla.org/en-US/docs/Web/API/Document_object_model/How_to_create_a_DOM_tree)   
the HTML elements are connected, there is a relationship, parent-children   
  eg.: `<body>` holds the `<h1>`, the `<ul>` holds the `<li>`

## [The document](https://developer.mozilla.org/en-US/docs/Web/API/Document)    
__The *document object* is the entry point into the DOM.    
It contains *representations of all the content on a page*, and lots of *methods and properties*.__   

it is en element on the top of the element tree structure:   
*it is the top of a folder for everything*      
*it's the root of the tree*
 - typeing `document` on the console gives us:  
   - eg.:   
      *the representation of the HTML*   
      ```
      <!DOCTYPE html>
      <html dir="ltr" ... lang="en" class="md">
      <head>...</head>
      </body>...</body>
      </html>>
      ```
- typing __`console.dir(document)`__ we can __shows the JavaScript object__ with a bunch of properties.   
  - eg.:   
    ```
    #document
      location: URL...
      activeElement: body
      adoptedStyleSheets: []
      alinkColor: ""
      all: [html, head, meta, meta, title, body, h1, img#banner, p, b, b, a, ...    // it contains every element the page - tags. Each of them is a JS object❗️
      .
      .
      .
    ```

- so the *document object* is where everything is contained and starts. Inside we have methods and properties, we can change them to manipulate the document.   
(It contains objects that represent the content of a Web page.)


---

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics) or [👆go up to JS DOM](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#the-dom)

<br>

## [getElementById](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById).  
The Document method `getElementById` returns an Element object representing the element whose id property matches the specified string.   

Simply: __when we call this method, we pass in a *string* and this string has to correspond to an `ID` on an element.__   

 - a method to select (an) element(s)

 - `document.getElementById('idname')`

 - it is a method that exists on the document
 - it only occurs once per page!
 - if there is an element found with that ID, it will be returned 
 - if the ID can't be found it return `null` (it only gives us 1 thing, there's no collection of elements)
 - when we select something __JS fetchs us the object that represents some elements on the page__ based on the matching ID.
 - __it gives us the object representation of that element, which we can then manipulate__
 - we are not'asking' the HTML, __we are asking the DOM__ object (__the element object that JavaScript created__).


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
      *to get the image, we pas the `img` tag*   
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
an all-im-one method to select a single element.

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
same idea as `querySelector` but returns a __collection__ of mathaing __elements__,  instead of just the first match.

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

    // with just simple querySelector


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

We use DOM manipulation when we want to modify parts of the page when the user interacts with it. Otherwise, if we feel like the initial page style should be modified, then changing the original code is the better approach. So, in general, we use CSS as much as possible, because it iss lighter and faster and it is the indicated technology to style a webpage. However, when we want to modify a page after the initial code was rendered to make it dynamic, that is only possible with DOM manipulation.


- [innerText](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#innertext)   
  [textContent](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#textcontent)   
  [innerHTML](https://github.com/Klosmi/html-basics/blob/master/JS-basic.md#innerhtml)   


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

- So `textContent` is give us everything, whereas `innerText is actually sensitive to what is showing at the moment.


- `textContent` returns every element in the `node`. In contrast, `innerText` is aware of styling and won't return the text of "hidden" elements.   

- syntax: `document.querySelector('p').textContent`

- eg.:   
  *let's take the  `<b>` tag which is inside of the `<p>` tag. Let's set it to `display:none`. So the word (consectetur) is hidden now*   
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
  
## the difference between `innerText` vs `innerHTML` vs `textContent`   

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
  document.getElementById("demo").innerText;
  
  // innerHTML
  document.getElementById("demo").innerHTML;
  
  //textContent
  document.getElementById("demo").textContent;
  
  // output:

  // innerText returns: "This element has extra spacing and contains a span element."
  // innerHTML returns: "   This element has extra spacing     and contains <span>a span element</span>."
  //textContent returns: "   This element has extra spacing    and contains a span element."
  ```
