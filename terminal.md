__[👈 go back](https://github.com/Klosmi/html-basics#terminal--basics)__

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

[👈 go back](https://github.com/Klosmi/html-basics#terminal--basics)

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

[👈 go back](https://github.com/Klosmi/html-basics#terminal--basics)

<br>

# [Absolute vs. Relative path](https://www.mygreatlearning.com/bash/tutorials/bash-relative-and-absolute-path) 

__Relative__: to access a directory is relative where we are.   
- eg.:    
  *We want to access `hello` directory from `/Users/mydirectory/hello`.*     
  *We are at `mydirectory`*    
  *The relative path to access `hello` directory is the following:*     
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
  ```
  / cd ~

  ~

  ls

  Applications         Movies               
  Desktop              Pictures             
  Documents            Downloads        Public               Library            
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#terminal--basics)

<br>

# [Make new Directories](https://openclassrooms.com/en/courses/4614926-learn-the-command-line-in-terminal/4634361-create-your-first-directory)

 __`mkdir`__ : (make directory) it creates a new empty folder.

 - eg.:   
 *Make a new folder named `Cats`*     
```
mkdir Cats
```

- __multiple sub direcotries__ in one go:

  *Make 2 folders, __subdirectories__ in the `Cats` folder.*    
  *To make all at once, we can separate the folder names we create by space.*    
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
  ```
  Cats/Rats Beavers

  // list the Cats` folder content
  ls

  Rats                 Beavers                
  ```

---

[👈 go back](https://github.com/Klosmi/html-basics#terminal--basics)

<br>


# [man command](https://www.freecodecamp.org/news/command-line-for-beginners/#:~:text=In%20a%20similar%20way%2C%20the%20man%20command%20will%20return%20info%20about%20any%20particular%20command.) = Manual command   

__`man`__ : short for manual, it is a help command.  
after the `man` we can type tha name of a command we want to get information about

- eg.:    
  *We want to get information about the `ls` command*    
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


 - we can __combine the flags__ (❗️) of a specigic command   
   - eg.:   
     *We combine the `ls` command's flag `-l` + `-a`. Where`-l` gives long list and `-a` shows hidden files.*    
     ```
     ls -la
     ```
     
---

[👈 go back](https://github.com/Klosmi/html-basics#terminal--basics)

<br>
