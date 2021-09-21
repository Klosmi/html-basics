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
  
---
   [👈 go back](https://github.com/Klosmi/html-basics#javascript--basics)
