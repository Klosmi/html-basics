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
  - eg.: another example:   
    *concatenation*
    ```
    let product = "pizza";
    let amount = 3;
    let price = 10;

    "I ordered " + amount + " " + product + "s" + for + price*amount + "€"."   // I ordered 3 pizzas for 30€.
    ```
    *temaplate literals*
    ```
    let product = "pizza";
    let amount = 3;
    let price = 10;

    `I ordered ${amount} ${pizza}s for ${price*amount}€. // I ordered 3 pizzas for 30€.`
    ```
