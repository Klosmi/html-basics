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


        
    