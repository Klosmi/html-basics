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
  - __[for ... of]()__
  - __[for ... in]()__
  - __[Object methods[()__: [Object.keys()]() • [Object.values()]() • [Object.entries()]()

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

   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)

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

### __using `Object.something()`methods with `for...of`__

- eg.:
  *to get the avaregae of the values*
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
---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
