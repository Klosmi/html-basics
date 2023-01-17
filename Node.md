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

# [Running Node files](https://www.brainstormcreative.co.uk/node-js/how-to-run-a-node-js-file/#:~:text=Run%20a%20Node%20js%20file%20in%20terminal%20%2F,to%20your%20node%20project%203%20Type%20node%20filename.js)   
Write code in a JS file, instead of in the Terminal.

- eg.:   
  *creating a JS file in the Terminal (bash or zsh mode)*   
   Terminal
    ```
    touch myScript.js
    ```
  *in the JS file we write a simple test code*    
   JS
    ```
    for (let i = 0; i < 5; i++){
      console.log("Hello!");
    }
    ```
  *and to run it in Node, we write `node` + `the name of our file`, in this case `node myscript.js`*    
   Terminal
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

# [`process` . `argv`]()

  ### __[Process](https://nodejs.org/dist/latest-v18.x/docs/api/process.html)__ 
  is an object which provides information about, and control over the current Node.js process.   
  This includes: 
  
  - the version of Node,  
  - it has methods to get input and write to the standard output (output in the console)
  - memory usage 
  - information about the current working directory where the user is running the script in.
  - etc.

  We type `process` in the terminal, it is always available (it is a big object with lots of methods and properties).
 - eg.:   
   *Let's type `process` when we are in Node*   
   Terminal
   ```
   > process

     process {
       version: 'v18.13.0',
       versions: {
         node: '18.13.0',
         v8: '10.2.154.23-node.21',
         uv: '1.44.2',
         zlib: '1.2.13',
         brotli: '1.0.9',
         ares: '1.18.1',
         modules: '108',
         nghttp2: '1.51.0',
         napi: '8',
         llhttp: '6.0.10',
         uvwasi: '0.0.13',
         openssl: '3.0.7+quic',
         cldr: '42.0',
         icu: '72.1',
         tz: '2022f',
         unicode: '15.0',
         ngtcp2: '0.8.1',
         nghttp3: '0.7.0'
       },
       arch: 'x64',
       platform: 'darwin',
       release: {
         name: 'node',
         lts: 'Hydrogen',
         sourceUrl: 'https://nodejs.org/download/release/v18.13.0/node-v18.13.0.tar.gz',
         headersUrl: 'https://nodejs.org/download/release/v18.13.0/node-v18.13.0-headers.tar.gz'
       },
       ...
       ...
       ...
       etc
   ```

  - eg.:   
    *Let's use a process __property__ like `release`, `version`*     
    Terminal
    ```
    > process.release
    {
      name: 'node',
      lts: 'Hydrogen',
      sourceUrl: 'https://nodejs.org/download/release/v18.13.0/node-v18.13.0.tar.gz',
      headersUrl: 'https://nodejs.org/download/release/v18.13.0/node-v18.13.0-headers.tar.gz'
    }

    > process.version
    'v18.13.0'
    ```
  
  - eg.:   
    *Let's use a process __method__ like `cwd` (path we are currently working)*    
    Terminal
    ```
     process.cwd()
    '/Users/Documents/Node/MyLibrary'
    ```

__[args]()__ represents the list of arguments that were passed in when invoking the function.

- eg.:   
  *We create a new JS file (args.js) and we write the following code into it and call it from the Terminal*      
  JS
  ```
  console.log("Hello there!")
  console.log(process.argv)
  ```
  *It looks like this in the Termnial*    
  Terminal
  ```
  node args.js

  Hello there!
  [
  '/Users/Documents/bin/v14.15.0/bin/node',   //← executable path 
  '/Users/Documents/Node/MyLibrary/args.js'   //← the path to the file
  ]
  ```

  ### So, what is __[`process.argv`](https://nodejs.org/dist/latest-v18.x/docs/api/process.html#processargv)__ ?     
  In short:     
  it is a way to get arguments in the comand line.   
  In detail:   
  it is a property that returns an __array__ containing the command-line arguments passed when the Node.js process was launched. So, it means __we can pass elements as an argument__, and it will add it to the `argv`.   
  - 1st element is the [process.execPath](https://nodejs.org/dist/latest-v18.x/docs/api/process.html#processexecpath) (that's where the node executable is)   
  - 2nd element is the JavaScript file that we are executing. 
  - any remaining elements are the additional command-line arguments     

  So basically it means that we can pass in arguments to a script (not to a function, but it is a similar idea). 
   - eg.:    
    *We have our node scripts `args.js` and then we can __pass arguments__ separated by space `argument01` `argument02` `argument03`*   
    *The arguments we just gave are all __added to the `argv` array__*     
    Terminal
     ```
     node args.js argument01 argument02 argument03

      '/Users/Documents/bin/v14.15.0/bin/node',   //← executable path 
      '/Users/Documents/Node/MyLibrary/args.js',  //← the path to the file
      'argument01',    //← arguments added to the argv array
      'argument02',
      'argument03'
     ```
    *With another example, let's see how can we use these arguments.*   
    *Create another JS file, named `sayHi.js`, and it will say hello to the arguments we pass in to the `argv`.*    
    Terminal 
    ```
    // create JS file
    touch sayHi.js

    // give any number of arguemnts
    node sayHi.js John Paul Ringo
    ``` 
    *Note the `slice(2)`. We use it because we need the 3rd argument (John, Paul, etc.). 1st one is the executable path. The 2nd one is the path to the file. The 3rd one at index of two in `argv` (the John, Paul, etc.).*

The second one is the path to the file.

And then the third one at index of two in ARG. 
    JS file   
    ```
    const args = process.argv.slice(2)  //← slice from index of 2
    
    //loop over args, and say hi! to each argument
    for(let arg of args){
      console.log(`Hi ${arg} !`)
    }
    ```
    Terminal    
    *give any number of arguemnts, hit enter*
    ```
    node sayHi.js John Paul Ringo

    // result

    Hi John !
    Hi Paul !
    Hi Ringo !
    ```
    
---

[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)

<br>

# [`node:fs` - File System Module](https://nodejs.org/dist/latest-v18.x/docs/api/fs.html)

it is a built-in Node.js module that allows us to __interact with the [file system](https://www.w3schools.com/nodejs/nodejs_filesystem.asp)__ on our computer.  

This means __we can use `fs` to read and write files, create and delete directories, and more__.   
So it has lots of methods. 

<br>

There are 2 different ways of reading files or making folders, deleting files and folders, etc.    

So it means that `fs` has a [synchronous](https://nodejs.org/dist/latest-v18.x/docs/api/fs.html#synchronous-example) and an [asynchronous](https://nodejs.org/dist/latest-v18.x/docs/api/fs.html#callback-example) version:      
  - __asynchronous__ form:   
   it always takes a completion callback as its last arguments. 

    - eg.:    
      *The ASYNCHRONOUS way:*   
      *Lets [try it out](https://nodejs.org/dist/latest-v18.x/docs/api/fs.html#fsmkdirpath-options-callback), how does `fs.mkdir` work*   
      *Note: we use the `require` function (explanation [see below](  https://github.com/Klosmi/html-basics/blob/master/Node.md#require))*  
      Terminal
      *creating the JS file*
      ```
      touch web.js
      ``` 
      JS
      ```
      // we have to require the module
      const fs = require('fs');

      fs.mkdir('directoryAsyncWay', { recursive: true }, (err) => {
        console.log('We are in the callback')
        if (err) throw err;       //← it throws an error if there is an error
        });
        console.log('We are after mkdir in the file');
      ```
      Terminal
      *call the JS file*   
      *Because it is asynchronous, the "After mkdir in the file - 2nd" printed out 1st.*    
      *When the directory is created (mkdir), then the callback ran: "In the callback - 1st" printed out.* 
      ```
      node web.js

      // After mkdir in the file - 2nd     //←printed out 1st
      // In the callback - 1st             //←printed out last
      ```
      *Verify that directory is created*   
      Terminal
      ```
      ls

      directoryAsyncWay   //← directory created, it's an empty folder
      ```

  - __synchronous__ form:   
   it will block the entire process - stops any other code - until they complete halting all connections.      
  (So, exceptions that occur using synchronous operations are thrown immediately and must be handled with *try and catch*.)  
  This is eg. the [`fs.mkdirSync(path[, options])`](https://nodejs.org/dist/latest-v18.x/docs/api/fs.html#fsmkdirsyncpath-options)

    - eg.:   
      *The SYNCHRONOUS way:*   
      *Lets try it ou, how does [`fs.mkdirSync`](https://nodejs.org/dist/latest-v18.x/docs/api/fs.html#fsmkdirsyncpath-options)work*   
      *Note: we use the `require` function (explanation [see below](https://github.com/Klosmi/html-basics/blob/master/Node.md#require))*   
      JS
      ```
      // we have to require the module
      const fs = require('fs');

      fs.mkdirSync('directorySyncWay')     //← the directory name
      console.log('After mkdir in the file');
      ```
      *It executes in a row: creates the directory 1st, print out the message 2nd*
      Terminal
      ```
      node web.js

      // After mkdir in the file
      ```
      *Verify that directory is created*    
      Terminal
      ```
      ls
      directorySyncWay   //← directory created
      ```


### [Require](https://www.w3schools.com/nodejs/nodejs_filesystem.asp)   
`require` is a function that is used to import the functionality of a Node.js module. So it allows us to include and use code from another JavaScript file in our current file. It is a way to reuse code. 

We use `require` to include a module in our code by __passing the name or path of the module as a string argument__.    
  eg.:     
  *to include the built-in `fs` module*   
  JS
  ```
  const fs = require('fs');
  ```

In other words: since __`fs` is a module__, practically that means we have to __require__, by default it is not defined (unlike `process` which is always on the scope). 

<br> 

Practice by using the synchronous way of creating files and directory:
  
  - *We make a Node script that creates our standard HTML, CSS and JavaScript file(s) in a new folder.*    
  *(What our script does: make a folder, make files, put the files in the folder)*    

    *create the JS file*
    Terminal
    ```
    touch web.js
    ```
    *Using argv with index 2 (check it at the [argv]() section).*
    *Creating the folder. If folder name undefined will be named as 'Project'*
    JS
    ```
    const fs = require('fs');
    // folder name, if it is undefined than it called 'Project'
    const folderName = process.argv[2] || 'Project'

    fs.mkdirSync(folderName);        //← the directory name
    ```
    *Creating the files, they will be placed in the folder.*   
    *We are using the [`fs.writeFile(file, data[, options], callback)`](https://nodejs.org/dist/latest-v18.x/docs/api/fs.html#fswritefilefile-data-options-callback) method, it writes data to a file (if already exists, it replaces the file).*      
    *Now we just create empty files.*
    JS
    ```
    const fs = require('fs');
    // folder name, if it is undefined than it called 'Project'
    const folderName = process.argv[2] || 'Project'

    // try and catch as best safety practice
    try {
        fs.mkdirSync(folderName);        //← the directory name
        //to go inside of that directory: use string templateliteral
        fs.writeFileSync(`${folderName}/index.html`, '')
        fs.writeFileSync(`${folderName}/app.js`, '')
        fs.writeFileSync(`${folderName}/styles.css`, '')
    } catch(e) {
        console.log("Sorry, it's an error");
        console.log(e);
    }
    ```
    *We name the directory `myProject`, and it will create the 3 files in that directory.*
    Terminal
    ```
    node web.js myproject
    ls
    myproject

    cd myproject
    ls
    app.js     index.html     styles.css
    ```
    
---

[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)

<br>

# [`module.exports`](https://www.tutorialsteacher.com/nodejs/nodejs-module-exports)     
 `exports` is an object. So it exposes whatever we assigned to it as a `module`.   
 For example, if we assign a string literal then it will expose that string literal as a module.

 <br>

## The way [`module.exports`](https://nodejs.org/dist/latest-v18.x/docs/api/modules.html#moduleexports) works with [`require`](https://github.com/Klosmi/html-basics/blob/master/Node.md#require)   
When we require a file, we are not going to get anything from that specific JS file *unless* in that specific file we explicitly say what we want to export out of the file.   
- eg.:    
  *Let's creat 2 JS files. One called math.js the other called app.js.*   
  *math.js has some basic functions*    
  JS (math.js)
  ```
  const add = (x, y) => x + y;
  const PI = 3.14159;
  const square = x => x * x;
  ```
  *In app.js we `require` the math.js file.*   
  *So we can `require` an exisiting file, not only built in modules.*    
  *We have to use `./` before the file name in the require line. `.` dot is the specific directory where our file which we requiring is placed.*    
  *Also, we don't have to us the `.js` after the file name.*   
  JS (app.js)
  ```
  const math = require('./math');
  console.log(math);
  ```
  *When we run app.js in the Terminal, we recieve an empty obejct `{}`. So require worked.*   
  Terminal   
  ```
  > node app.js

  {}
  ```
When we require a file, we not going to get anything from the specific JS file unless in that specific JS file we explicitly say what we want to export out of the file.     
By __default, it is the `module.exports`__, an empty object. 
 - eg.:   
    *So, in our math.js and app.js example, we have to say what we want to export.*   
    *So here, we set the functions to the `module.exports`, so th app.js file can require those functions*    
    JS math.js
    ```
    const add = (x, y) => x + y;
    const PI = 3.14159;
    const square = x => x * x;

    module.exports.add = add;
    module.exports.PI = PI;
    module.exports.square = square;
    ```   
    *Now, we have access to thses functions. Lets run the app.js in the Terminal.*   
    Terminal    
    ```
    > node app.js
    
    { add: [Function: add], PI: 3.14159, square: [Function: square] }
    ```
    *We can specify what we want to print out in the app.js console.log → here `(math.squre(5))`*   
    JS app.js
    ```
    const math = require('./math');
    console.log(math.squre(5));
    ```
    *We receive the sqaure of 5*
    Terminal   
    ```
    > node app.js

    25
    ```
    *Shorter ways of adding functions to the `module.exports`*    
    *1st way is create an object with all the functions*   
    JS math.js   
    ```
    const add = (x, y) => x + y;
    const PI = 3.14159;
    const square = x => x * x;  

    const math = {
      add: add,
      PI: PI,
      square: square
    }
    module.exports = math;
    ```
    *2nd way add functions directly onto the `module.exports`*   
    ```
    module.exports.add = (x, y) => x + y;
    module.exports.PI = 3.14159;
    module.exports.square = x => x * x;  
    ```

  ## [`exports` shortcut](https://nodejs.org/dist/latest-v18.x/docs/api/modules.html#moduleexports:~:text=x.a)%3B-,exports%20shortcut,-%23)   
  The module allows a shortcut, so that `module.exports.f = ...` can be written more succinctly as `exports.f = ....`    
  However, be aware that like any variable, if a new value is assigned to exports, it is no longer bound to module.exports.   

  So it's just a quick reference to `module.exports`.   
  - eg.:   
    *the shortcut `exports`*  
    JS math.js
    ```
    const add = (x, y) => x + y;
    const PI = 3.14159;
    const square = x => x * x; 

    exports.PI = PI;
    exports.square = square;
    ```
    JS app.js  
    ```
    const math = require('./math');
    console.log(math.PI);
    console.log(math.square(5));
    ```
    Terminal
    ```
    3.14159
    25
    ```
    *But, if we assign a string literal, it will think `exports` just a variable, and give ans error.*   
    JS math.js 
    ```
    const add = (x, y) => x + y;
    const PI = 3.14159;
    const square = x => x * x; 

    exports = "Hello!";
    exports.PI = PI;
    exports.square = square;  
    ```
    Terminal   
    ```
    > app.js

    TypeError: math.square is not a function...
    ```
     
---

[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)

<br>  

# [Require an enitre Directory](https://lavalite.org/blog/require-all-files-in-the-folder-in-nodejs)
  to require all the content from a directory.   
  __In Node the main file for a specific directory is called the `index.js`__    
 
  When we require an enitry directory, Node is looking for the `index.js` file. What the index.js exports, that specific directory is exporting❗️

- eg.:    
  *We have a directory (colors), inside we have 3 files (blue.js, yellow.js, red.js)*   
  *Each file is just an `exports`, very simple objects.*   
 
  JS blue.js
  ```
  module.exports = {
    name: "navy blue",
    tone: "saturated"
  } 
  ```
  JS yellow.js
  ```
  module.exports = {
    name: "lemon",
    tone: "light"
  }
  ``` 
  JS red.js
  ```
  module.exports = {
    name: "velvet",
    tone: "dark"
  }
  ```
  *We combine all the 3 files, put them in an array in another file (index.js).*    
  JS index.js
  ```
  //require the files
  const blue = require('./blue');
  const yellow = require('./yellow');
  const red = require('./red');

  // combine into an array
  const mainColors = [blue, yellow, red];
  console.log(mainColors);
  ```   
  *Check in the Terminal. It prints out an object.*    
  Terminal
  ```
  > index.js

  [
    { name: 'navy blue', tone: 'saturated' },
    { name: 'lemon', tone: 'light' },
    { name: 'velvet', tone: 'dark' }
  ]
  ```
  *`module.exports` the `mainColors` object in the `index.js` files* 
  JS index.js
  ```
  //require the files
  const blue = require('./blue');
  const yellow = require('./yellow');
  const red = require('./red');

  //combine into an array
  const mainColors = [blue, yellow, red];

  //exports
  module.exports = mainColors;
  ```
  *outside of the `colors` directory in another file (app.js), we `require` the index.js file's `mainColors` object*    

  JS app.js
  ```
  //require
  const allColors = require('./colors');
  console.log(allColors);
  ```  
  *We verify it by console.log(). It prints out what the index.js file exports*    

  Terminal
  ```
  > cd colors
  > node app.js

  [
    { name: 'navy blue', tone: 'saturated' },
    { name: 'lemon', tone: 'light' },
    { name: 'velvet', tone: 'dark' }
  ]
  ```

  Requiring an entiry directory is useful when we working with packeges.
  
  
  ---

[👈 go back](https://github.com/Klosmi/html-basics#node-js--basics)

<br>  
