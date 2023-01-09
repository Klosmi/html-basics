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
