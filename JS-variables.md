# **[JS: Variables](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#declarations)**
  - varables are like __labels for values__:
    - we can store a value and give it a name so that we can:
      - refer back to it later
      - use that value to do things
      - change it laters


<br>

 To define a variable, we should use `let`, `const`, or `var` (though var isn't recommended these days anymore).      
 **We only use those keywords when first declaring the variable (the first time we tell javaScript it exists).**  After we declared the variable and then if we want to change it the value of a that variable, we just reference the variable name **without** `let` or `const` or `var`.    
<br>
💡defining a variable without `let`/`const`/`var` is an option in JavaScript, but you should never do it!!!  
  *JavaScript will treat your variable as a global variable, which is better to avoid. It is a bad idea and you do not see anyone do this in the real world.*

- **basic syntax**:   
  #### [**let**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)  :    
  let statement declares a block-scoped local variable, optionally initializing it to a value.

  <br>

  -   eg.:   
      ```
      let numChickens = 4;
      let numRoosters = 1;

      let totalChickens = numChickens + numRoosters   //5;
      ```


     
