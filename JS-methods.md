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