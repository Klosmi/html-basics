[👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

---

# **[JS: Primitive Types](https://developer.mozilla.org/en-US/docs/Glossary/Primitive)**

- basic building blocks, basic types of information that we can store.

<br>

- [**number**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#number)
- [**boolean**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#boolean-)
- [**string**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#string-)
- [**null**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#null-)
- [**undefined**](https://github.com/Klosmi/html-basics/blob/master/JS-primitiveTypes.md#undefined)
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
      let numberOfEggs = 12;
Then if we ever want to change the value of a variable, we simply reference the variable name WITHOUT let/const/var like: 
<br>  
 numberOfEggs = 10;
Now, it seems like you might be asking about defining a variable without let/const/var at all.  This is an option in JavaScript, but you should never do it.  JS will treat your variable as a global variable, which is something you want to avoid.  It's just a bad idea and you won't see anyone do this in the real world.*

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
  eg.: the *"hello" string* can do the same as the *"goodbye" string*    
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
    eg.: trim a space beginning of a string
      ``` 
      const input = "    Hi, my name is...";
      input.trim()    // "Hi, my name is ..."
      ```
    - [thing.indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf) :     
    __first occurrence__ of the specified value
    - [thing.slice()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice) :    
    it extracts a portion of a string and returns it as a new string, __without modifying the original string__   
    eg.: pass in a begin index and an optional end index
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
  eg.: pass the argument into the `indexOf()` method
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

---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
