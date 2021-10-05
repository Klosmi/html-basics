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
