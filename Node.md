__[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)__

---

# [What is Node JS?](https://www.codecademy.com/article/what-is-node)
Node JS is a JS runtime that executes outside of the browser.   
In other words, Node JS is an implementation of JS that runs outside of the browser.

It doesn't rely on other languages, it uses JavaScript. *(Before JS was only running on web browsers.)*

Some examples of what is built or uses with Node JS: 
- Web Servers
- Command Line Tools (application that run in command line, eg. npm)
- Native Apps (eg. VSCode, Slack is a Node application)
- Games
- Netflix uses it
- etc.

---

[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)

<br>

# [REPL](https://nodejs.dev/en/learn/how-to-use-the-nodejs-repl/#:~:text=BASH%20copy-,node,quickly%20test%20simple%20JavaScript%20code.)

__REPL__ : stands for **R**ead **E**valuate **P**rint **L**oop.   
It is a __programming language environment__ (basically a console window) that takes single expression as user input and returns the result back to the console after execution.  
(Also, the JS console in our browser is a REPL too.)   
The REPL session provides a convenient way to quickly test simple JS code.

- To enter into the Node REPL in our Terminal, we type `node`   
*💡 `.help` is a useful command in Node JS*

- the __global__ scope here is called `global` (not like in the DOM environemnt, where it is thw __window__)
  - eg.:   
    *We type `global` in the Terminal*
    ```
    > global

    // output, shows all the functions that live in the 'global'

    Object [global] {
    global: [Circular *1],
    clearInterval: [Function: clearInterval],
    clearTimeout: [Function: clearTimeout],
    setInterval: [Function: setInterval],
    setTimeout: [Function: setTimeout] {
      [Symbol(nodejs.util.promisify.custom)]: [Function (anonymous)]
    },
    queueMicrotask: [Function: queueMicrotask],
    clearImmediate: [Function: clearImmediate],
    setImmediate: [Function: setImmediate] {
      [Symbol(nodejs.util.promisify.custom)]: [Function (anonymous)]
    }
    ```

  - we don't have to write `global.setTimeout()`, we just type `setTimeout()`
    - eg.:   
      *Let's write a function, which says 'Bonjour !' after 2 seconds (we don't need to write `global`, of course we can if we want)*    
      ```
      > setTimeout(() => console.log("Bonjour !), 2000 )
      Timeout {
        _idleTimeout: 2000,
        _idlePrev: [TimersList],
        _idleNext: [TimersList],
        _idleStart: 440713,
        _onTimeout: [Function (anonymous)],
        _timerArgs: undefined,
        _repeat: null,
        _destroyed: false,
        [Symbol(refed)]: true,
        [Symbol(kHasPrimitive)]: false,
        [Symbol(asyncId)]: 285,
        [Symbol(triggerId)]: 5
      }
      > Bonjour !

      // let's quit

      > .exit
      ```
---

[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)

<br>

# [How to run files in Node?](https://www.brainstormcreative.co.uk/node-js/how-to-run-a-node-js-file/#:~:text=Run%20a%20Node%20js%20file%20in%20terminal%20%2F,to%20your%20node%20project%203%20Type%20node%20filename.js)   
Write code in a JS file, instead of in the Terminal.

- eg.:   
  *creating a JS file in the Terminal (bash or zsh mode)*   
    ```
    touch myScript.js
    ```
  *in the JS file we write a simple test code*    
    ```
    for (let i = 0; i < 5; i++){
      console.log("Hello!");
    }
    ```
  *and to run it in Node, we write `node` + `the name of our file`, in this case `node myscript.js`*
    ```
    node myscript.js

    Hello!
    Hello!
    Hello!
    Hello!
    Hello!
    ```

---

[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)

<br>
