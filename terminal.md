__[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)__

---


# The [Terminal](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Command_line)
 is a text based interface, is a device that gives us access to the console of our computer.   

 ## __[Shell](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/Shell#:~:text=A%20shell%20is%20a%20program,block%2C%20similar%20to%20code%20examples.)__
The shell is the name of the program that runs in the terminal.    

(Way back, the terminal was a hardware and the program that was running on the terminal was the Shell.)


There are different Shells that run on the terminal.

## __[Bash](https://opensource.com/resources/what-bash)__  
it is the most popular Shell.

The other is __[Z-Shell](https://zsh.sourceforge.io/)__:   
it is a newer shell, it has newer freatures compared to __bash__.

---

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>

# [Basic commands: `LS`, `PWD`, etc.](https://www.earthdatascience.org/workshops/setup-earth-analytics-python/introduction-to-bash-shell/#:~:text=cd%20~%20(the%20tilde).,in%20which%20the%20Terminal%20opens)      
__Home Directory__ ► __`~`__ :     
the default directory (the default location) in which the Terminal opens.    
 (Usually our user account directory. If we have 5 accounts, each account has its own home directory.)    

- tilde __`~`__ is a shortcut way of referencig our home directory (if we want to "go home").   

<br>

__List__ ► __`ls`__ :    
a list of the current contents of the directory that we are in at the moment.      
command: __`ls`__  ► brings back to your home directory
 
 <br>

__Print Working Directory__ ► __`pwd`__ :     
 a quick way of orientating, shows which directory we are, so that's how we now where we are.

 <br>

__Change Directory__ ▶︎ __`cd`__ :   
to move forward or backwards.   
tpye: `cd` and then some directory that we want to change directories into.    
 - eg.:   `cd DirectoryName` 

To __back up a directory__ : __`cd ..`__ (cd followed by __`..`__) 

 - eg.:   
  *We are in the /Code/Mydirectory/Foldername/*   
  *We want to go back to Mydirectory*  
  *We type:* `cd ..` *and we are in /Code/Mydirectory/* .    
  *If we write it again* `cd ..` *we go back to /Code/ directory.*


---

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>

# [Absolute vs. Relative path](https://www.mygreatlearning.com/bash/tutorials/bash-relative-and-absolute-path) 

__Relative__: to access a directory is relative where we are.   
- eg.:    
  *We want to access `hello` directory from `/Users/mydirectory/hello`.*     
  *We are at `mydirectory`*    
  *The relative path to access `hello` directory is the following:*     
   Terminal        
  ```
  Users/mydirectory/

  cd hello
  ```
  *so when we write `cd hello`, it will find that directory. It __only works if that specific directory is in the directory where we are__*    
  *So the directory is __relative to where we are__.

<br>

__Absolute__: we can __access a specific directory from anywhere__ in our machine.    

- abolute path always start with a slash __`/`__.
- eg.:      
  *We want to access `mydirectory` directory from `/Users/mydirectory/hello`.*    
  *We are at `hello` directory.* .  
  *The _ansolute way to acces `mydirectory` is the followoing:*      
   Terminal    
  ```
  cd Users/mydirectory
  ```
  *It doesn!t matter where we are, it is not relaitve to our current location.*

 <br> 

Go to __Root directory__:  
is the first __`/`__.   
- `cd /` bring us to our root directory.    

- eg.:    
  *The slash `/` before the `Users`.*    
   Terminal    
  ```
  /Users/mydirectory/hello

  cd /

  ls

  Applications Users        home         Library      Volumes      System       private      usr
  ```

<br> 

Go to __Home directory__:   
Write __`cd ~`__ and it brngs us to our home directory.   
- The tilde __`~`__ always signifies our home directory.


- eg.:    
  *We are at the root directory. We want to go to our home directory.*    
   Terminal
  ```
  / cd ~

  ~

  ls

  Applications         Movies               
  Desktop              Pictures             
  Documents            Downloads        Public               Library            
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>

# [Make new Directories](https://openclassrooms.com/en/courses/4614926-learn-the-command-line-in-terminal/4634361-create-your-first-directory)

 __`mkdir`__ : (make directory) it creates a new empty folder.

 - eg.:   
  *Make a new folder named `Cats`*     
  Terminal
  ```
  mkdir Cats
  ```

- __multiple sub direcotries__ in one go:

  *Make 2 folders, __subdirectories__ in the `Cats` folder.*    
  *To make all at once, we can separate the folder names we create by space.*    
  Terminal
  ```
  //go to Cats folder
  cd Cats
  ls
  mkdir Dogs Birds
  ```

- directory in different path:    
  *To make a folder in a different path, in an other location, like a folder up.*   
  ```
  mkdir ../Mice
  ```

- quick way of making directory and it's subdirectory:
  *In the `Cats` folder we create 2 folders, Rats folder and Beavers folder*    
  Terminal
  ```
  Cats/Rats Beavers

  // list the Cats` folder content
  ls

  Rats                 Beavers                
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>


# [man command](https://www.freecodecamp.org/news/command-line-for-beginners/#:~:text=In%20a%20similar%20way%2C%20the%20man%20command%20will%20return%20info%20about%20any%20particular%20command.) = Manual command   

__`man`__ : short for manual, it is a help command.  
after the `man` we can type the name of a command we want to get information about.

- eg.:    
  *We want to get information about the `ls` command*   
  Terminal
  ```
  man ls


  // that's what we get

  NAME
     ls – list directory contents


  SYNOPSIS
      ls [-@ABCFGHILOPRSTUWabcdefghiklmnopqrstuvwxy1%,] [--color=when] [-D format] [file ...]


  DESCRIPTION
      For each operand that names a file of a type other than directory, ls displays its name as well as any requested, associated information.  For each operand that names a
      file of type directory, ls displays the names of files contained within that directory, as well as any requested, associated information.
      ... etc.


  The following options are available:

     -@      Display extended attribute keys and sizes in long (-l) output.

     -A      Include directory entries whose names begin with a dot (‘.’) except for . and ...  Automatically set for the super-user unless -I is specified.

     -B      Force printing of non-printable characters (as defined by ctype(3) and current locale settings) in file names as \xxx, where xxx is the numeric value of the
             character in octal.  This option is not defined in IEEE Std 1003.1-2008 (“POSIX.1”).

     -C      Force multi-column output; this is the default when output is to a terminal.
    
     ... etc.

  ```

  __[flags](https://www.ibm.com/docs/en/aix/7.2?topic=names-command-flags)__ ❗️     
  Flags are almost like arguments in a function, __options__ or sort of different parameters for how we want to work with the specific command.  So *flags* modify the behavior of the command.
  

  On the example above, we can see `-a`, `-B`, `-d`, etc. These are called flags of the specific command (in this case these are the flags of the `ls` command).   
   
   - eg.:    
     *the `-S` flag of `ls`*    
     ```
     -S   Sort by size (largest file first) before sorting the operands in lexicographical order.   
     ```

 💡 *to quit from the manual type `q`*

 💡 using `ls -a` lists the hidden files


 - we can __combine the flags__ (❗️) of a specific command   
   - eg.:   
     *We combine the `ls` command's flag `-l` + `-a`. Where`-l` gives long list and `-a` shows hidden files.*    
     Terminal
     ```
     ls -la
     ```
     
---

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>

# [touch command - create files](https://www.techrepublic.com/article/16-terminal-commands-every-user-should-know/#:~:text=a%20text%20file-,Command%3A%20touch,-What%20it%20does)

__`touch`__ : create file(s)   
However, the `man touch` manual says:    
  *The touch utility __sets the modification and access times of files__.*     
  *__If any file does not exist, it is created with default permissions.__*    

- how to use `touch`:  

  `touch + space + `filename` (with extension, like  `filename.txt`)

  - eg.:    
    *Create an HTML file*    
    Terminal
    ```
    touch Redcat.html

    // check if it's created
    ls

    Redcat.html 
    ```

- Make __multiple files__ at once
  - eg.:   
    *Create a folder named `Projects`, and go into it with `cd Projects`*    
    *Create html, css, js files*   
    Terminal
    ```
    mkdir Projects

    cd Projects

    touch index.html styles.css app.js

    ls
    index.html    styles.css    app.js
    ```

---

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>

# [`rm` & `rmdir` command - delete files / folders](https://www.webservertalk.com/rm-and-rmdir-commands)    
__`rm`__ : remove a file or folder     

Once you `rm` a file, it is permanently deleted.

- how to use:   
  `rm` + space + `filename`   

  - eg.:   
    *Delete the previously created html file*   
    Terminal
    ```
    cd Projects

    ls
    index.html    styles.css    app.js

    // remove❗️
    rm index.html

    ls
    styles.css    app.js
    ```

- remove multiple files    
  - eg.:   
    *Remove the css and js files*   
    Terminal
    ```
    cd Projects

    ls
    styles.css    app.js

    // remove❗️
    rm styles.css app.js

    ls
    // empty directory
    ```

- deleting __directory__ (folder(s))   

  - __`rmdir` + `directory name`__   
    It only works if the directory is empty.

    (With `rm` + `directory` would give a sort of error)

   - eg.:   
     *Remove the previously created `Projects` folder*    
     Terminal
     ```
     rmdir Projects
     ```

  - __`rm -rf` + `directory name`__     
    this command deletes a directory which contains file(s)   

    Note, using `rm` with flags `rf` 

    `r`  = recursive (it means that removes everything, nested folders as well, different levels)    
    `f`  = force` (it means removing without asking)

   - eg.:    
     *Removing a folder which contains files*   
     Terminal
     ```
     // Assume Projects exists and contains 3 files 
     ls
     Projects

     rm -rf Projects
     ```
      
---

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

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

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>

# [`process` . `argv`]()

  ### __[Process](https://nodejs.org/dist/latest-v18.x/docs/api/process.html)__ 
  is an object which provides information about, and control over, the current Node.js process.   
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

[👈 go back](https://github.com/Klosmi/html-basics#terminal-command-line--basics)

<br>
