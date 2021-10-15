# [The basics of  SASS: Syntactically Awesome StyleSheets](https://sass-lang.com/guide)    

is an extension language for CSS. 
Sass lets you write clean, sustainable CSS code and solve the repetition and maintenance problems which are in traditional CSS.

- Sass must first be converted, or __compiled__, to CSS before the browser can directly understand it
- compiling means: to converting code to lower level code so that it can be executed. 

- by __compiling SCSS to CSS__, it can be __interpreted by your browser__ and the results will appear on a webpage.

<br>

**[Installation](https://github.com/Klosmi/html-basics/blob/master/sass.md#how-to-install-sass)   
[Compiling](https://github.com/Klosmi/html-basics/blob/master/sass.md#how-to-compile-sass-to-css)   
[Basic Sass documentation](https://github.com/Klosmi/html-basics/blob/master/sass.md#lets-dive-into-the-codes)   
[Variables](https://github.com/Klosmi/html-basics/blob/master/sass.md#variables)   
[Nesting](https://github.com/Klosmi/html-basics/blob/master/sass.md#nesting)   
[Partials](https://github.com/Klosmi/html-basics/blob/master/sass.md#partials)   
[Mixins](https://github.com/Klosmi/html-basics/blob/master/sass.md#mixins)   
[Extend](https://github.com/Klosmi/html-basics/blob/master/sass.md#extend)   
[Operations](https://github.com/Klosmi/html-basics/blob/master/sass.md#operations)   
[Maps](https://github.com/Klosmi/html-basics/blob/master/sass.md#maps)    
[Interpolation](https://github.com/Klosmi/html-basics/blob/master/sass.md#interpolation)   
[Functions](https://github.com/Klosmi/html-basics/blob/master/sass.md#functions)   
[@use](https://github.com/Klosmi/html-basics/blob/master/sass.md#use)   
[@forward](https://github.com/Klosmi/html-basics/blob/master/sass.md#forward)   
[Useful links](https://github.com/Klosmi/html-basics/blob/master/sass.md#useful-links)**  

<br>

### [How to install Sass?](https://sass-lang.com/install)
 - my expereince: the easiest way for me was just using NPM and terminal:   
 *(If you use Node.js, you can also install Sass using npm by running)*
    ```
    npm install -g sass
    ```

### [How to compile Sass to CSS?](https://sass-lang.com/guide)

  - **[one-to-one mode](https://sass-lang.com/documentation/cli/dart-sass#one-to-one-mode)**:
    - typing the following command in the terminal:
      ```
      sass main.scss main.css
      ```
    - result is 2 new files:   
        main.css   
        main.css.map

<br>    

 - **[many-to-many mode](https://sass-lang.com/documentation/cli/dart-sass#many-to-many-mode)**:   
    - if you have a components directory  `/scss/components/` with a `button.scss`, `input.scss`, and `modal.scss`.    
    We want them to go to the `/assets/` directory:
      ```
      sass --watch --no-source-map scss/components:assets/css/components
      ```
      
      <br>

      this compiles everything: directory with sass to a directory ti css

      ```
      sass --watch sass:css
      ````
      <br>

      💡 note that you can also `--watch` individual files or directories with the `--watch` flag.    
      The watch flag tells Sass to watch your source files for changes, and re-compile CSS each time you save your Sass.    
      So, when you use it and you save, it 'automatically' compile your Sass or SCSS to CSS.


  <br>    

 ### **[Let's dive into the code(s)](https://sass-lang.com/documentation)**   
  I show you the __SCSS__ way, basic key concepts


  ####  __[variables:](https://sass-lang.com/documentation/variables)__   
  - eg:
    ``` 
    $primary-color:#503d4d;
    $accent-color:#ff652f;
    $text-color:#fff;
    ```

<br>

  #### __variables with [key-value pairs:](https://sass-lang.com/documentation/values/maps)__**<sup>*[see key-value under maps](https://github.com/Klosmi/html-basics/blob/master/sass.md#maps)*</sup>**
 - eg.:
    ```
    $font-weight: ("regular": 400, "medium": 500, "bold": 700);
    ```
<br>

 #### __the key-value `map-get`: **<sup>*[more about maps](https://github.com/Klosmi/html-basics/blob/master/sass.md#maps)*</sup>**__   
 - eg.:
    with @use → map.get  
    ```
    @use 'sass:map';

    p {
      font-weight: map.get($font-weight, "bold");
    }
    ```
    without @use → map-get
    ```
    p {
      font-weight: map-get($font-weight, "bold");
    }
    ```
    - in plain css:
      ```
      p {
        font-wieght: 700;
        /* since we defined the "bold" as 700 */
      }
      ```

  <br>
    
#### __[nesting:](https://sass-lang.com/documentation/style-rules/declarations#nesting)__
  try not nesting too many levels, because in a larger project it can be hard to read it. (It is preferred to create unique classes for read and searchability.)
 - eg.:
    without @use → map-get
    ```
    .main {
      width: 80%;
      margin: 0 auto;

      p {
        font-weight: map-get($font-weight, "bold");
      }

    }
    ```
    - in plain css:
      ```
      .main{
        width: 80%;
        margin: 0 auto;
      }

      .main_text {
        font-weight: 700;
      }
      /* .main_text it's alone, not .main .main_text */
      ```
 
 <br>
 
#### __[nesting using the `&` parent selector:](https://sass-lang.com/documentation/style-rules/parent-selector)__ 
when ever you nest an **&** it is taking the parent selector again.   
**`&`** let us not to repeat the parent's name
  - eg.:   
      ```
      .main {
        width: 80%;
        margin: 0 auto;

        & p {
          font-weight: map-get($font-weight, "bold");
        }

      }
      ```

<br>
 
#### __[nesting with classes adding suffixes:](https://sass-lang.com/documentation/style-rules/parent-selector#adding-suffixes)__   
**`&`** let us not to repeat the parent's name
 - eg.:
      ```
      .main {
        width: 80%;
        margin: 0 auto;

        &-text {
          font-weight: map-get($font-weight, "bold");
        }

      }
      ```
      - in plain css:
        ```
        .main-text {
          font-weight: 700;
        }
        ```

<br>

#### __nesting @media with &___
very useful, saves a lot of time.
  - eg.:
    ```
    .card {
      padding: 1em;

      &-title {
        font-size: 1.5rem;
      } 

      @media (min-width: 45em) {
        padding: 2em;
      }
    }
    ```
    - in plain css: 
      ```
      .card {
        padding: 1em;
      }

      .card-title {
        font-size: 1.5rem;
      }
      
      @media (min-width: 45em) {
        .card {
          padding: 2em;
        }
      }
      ```

<br>

#### __[nesting: interpolation:](https://sass-lang.com/documentation/interpolation)__          
using: **`#{ }_`** = it includes everything before (before the `.main_text` class)

- eg.:
     ```
     .main {
       width: 80%;
       margin: 0 auto;

       #{&}_text {
         font-weight: map-get($font-weight, "bold");
       }

     }
     ```
     - in plain css:
       ```
       .main {
         width: 80%;
         margin: 0 auto;
       }

       .main .main_text {
         font-weight: 700;
       }
       ```
<br>

#### [__partials:__](https://sass-lang.com/guide#topic-4)   
- baiscally snippets, parts of SCSS what we can keep in a separate file and include in to our main SCSS.   
So partials are *little snippets of CSS* that you can include in other Sass files.    
It's a way to modularize your CSS and help keep things easier to maintain.   
(eg.: `_partial.scss`)

- any file start with underscore `_` will not be compiled to CSS!

-  file name start with **`_`** underscore, eg.: **`_reset.scss`**

- to include it into our main SCSS, we use   
       **`@use './reset' as *;`**    
       💡 note that the no need to include now the `.scss` part
 - eg.:
      ```
        @use './reset' as *;

        .main {
          width: 80%;
          margin: 0 auto;

          &_text {
            font-weight: map-get($font-weight, "bold");
          }
        }
      ```
 
 <br> 

#### __[mixins:](https://sass-lang.com/documentation/at-rules/mixin)__
- you can put into mixins all the content you don't want to repetedly type.  

- so, mixins allow you to define styles that can be re-used throughout your stylesheet.

- mixins define by: **`@mixin <name> { ... }`**    
  or **`@mixin name(<arguments...>) { ... }`**

- mixins are __included into the current context__ using the __@include__ at-rule:    
**`@include <name>`**   
 or **`@include <name>(<arguments...>)`**,with the name of the mixin being included.

- to include **`@include`** + **`name`**

- eg.:
    ```
      .main {
        @include flexCenter;
        width: 80%;
        margin: 0 auto;
      }
    ```
    - in plain css:
        ```
        .main {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 80%;
          margin: 0 auto;
        }
        ```

<br>

#### __[mixins: $arguments + @include:](https://sass-lang.com/documentation/at-rules/mixin#arguments)__
- like function mixins can also have arguemnts
- arguments allows their behavior to be customized each time they’re called.

- list of **`($variable)`** names surrounded by parentheses

- then, the mixin must be included with the same number of arguments

- eg: `@mixin flexCenter($direction)` and later we call it `@include flexCenter(column);`


- eg.:
    ```
    @mixin flexCenter($direction) {
      display: flex;
      justify-content: center;
      align-items: center;
      
      flex-direction: $direction;
    }
    
    .main {
      @include flexCenter(column);
      width: 80%;
      margin: 0 auto;
    }
    ```
    
  - in plain css:

       ```
         .main {
           display: flex;
           justify-content: center;
           align-items: center;
           flex-direction: column;
           width: 80%;
           margin: 0 auto;
         }
       ```


<br>

#### __[mixins: @media + @content](https://sass-lang.com/documentation/at-rules/mixin#content-blocks)__:   

  - in addition to taking arguments, a mixin can take an __entire block of styles, known as a content block__.   

  - A mixin can declare that it takes a content block __by including__ the __@content__ in its body.    
  The content block is passed in using `{ }` like any other block in Sass, and it’s injected in place of the `@content`.

  - so, __whatever style we put after the `@include`, that goes to the `@content` section__.

  - eg.:   
     - the `maxi-width: $mobile`, we can give a size to the `$mobile` later or define it before.
     - see the __`@content`__: we can define it when we `@include` it.
    ```
     $mobile: 800px;

     @mixin mobile {
       @media (max-width: $mobile) {
         @content;
       }
     }
    ```
    and include it
    ```
    .main {
      width: 80%;
      margin: 0 auto;
      @include mobile{
        flex-direction: column;
      }
    }
    ```
    - in plain css:
      ```
      .main {
          width: 80%;
          margin: 0 auto;
        }

        @media (max-width: 800px) {
          .main {
            flex-direction: column;
          }
        }
      ```
<br>

#### __[extend:](https://sass-lang.com/guide#topic-7)__
- it is similar to mixins.
- it lets you share a set of CSS properties from one selector to another.   
So the element that we extended to, ihnerits all the styles from the selected element.

- it helps to keep your Sass very DRY

- basically, if you want to copy one class to another class without repeating the same code (DRY), use the `@extend` keyword.

- `@extend`

 - eg.:   
    adding the class name (`.container`) after the `@extend`, what it does that it applies the exact same style to the `ul` as we use in the `.contaner`.
    ```
    .container {
      width: 85vw;
      margin: 0 auto;
      dispaly: flex;
      justify-content: space-between;
      align-items: center;

      ul {
        width: 200px;
        @extend .container;

        li {
          text-decoration: underline;
        }
      }
    }
    ```
      - in plain css:   
        *note the line: `.container, .container ul`
        . The SCSS @extand compiled to CSS the styles of the `.container` and 'extended' to the `ul`.*
        ```
        .container, .container ul {
          width: 85vw;
          margin: 0 auto;
          dispaly: flex;
          justify-content: space-between;
          align-items: center;
        }
        .container ul {
          width: 200px;
        }
        .container ul li {
          text-decoration: underline;
        }
        ``` 


<br>

#### __[operations:](https://sass-lang.com/guide#topic-8)__
- addition, substraction, multiplication, division, etc.

- ❗️SASS you can not mix type: `80% - 40px` will not work.   
The operation has to be the same type❗️

- plain css it is the **[`calc()`](https://developer.mozilla.org/en-US/docs/Web/CSS/calc())**
- eg.:   
  in SASS no need touse the  CSS `calc(80% - 20%)`, it just simple:
    ```
    .container {
      width: 100% - 20%;
      margin: 0 auto;

      ul {
        width: 200px;
        li {
          text-decoration: underline;
        }
      }
    }
    ```
    - in plain css:
      ```
      .container {
        width: 80%;
        margin: 0 auto;
      }
      .container ul {
        width: 200px;
      }
      .container ul li {
        text-decoration: underline;
      }
      ```

<br>

##### __[Maps:](https://sass-lang.com/documentation/values/maps#using-maps)__   
Maps hold **pairs of keys and values**, and make it easy to look up a value by its corresponding key.   

- use brackets `( )`

- eg.:
  ```
  $variable: (<expression>: <expression>, <key>: <value>)
  ```
The expression before the `:` is the key, and the expression after is the value associated with that key. The keys must be unique, but the values may be duplicated.

In the [SASS documentation](https://sass-lang.com/documentation/values/maps#using-maps) it shows to use maps with the **`.`** **(where I have to use the [`@use`](https://sass-lang.com/documentation/at-rules/use))**, rather than with **`-`** which I found in [other sources](https://github.com/sass/sass/blob/main/accepted/module-system.md#built-in-modules-1) and it works witout the `@use`.      
[It is a useful discussion](https://stackoverflow.com/questions/64210390/sass-map-get-doesnt-work-map-get-does-what-gives) to see the difference between the above mentioned 2 ways

**Some main `map` functions (with `.`):**   
for better compatibility reasons to get access to map.get you must explicitly import the map module using the __@use keyword.__
- __map.get($map, $key)__:   
  - this functions gets the value associated with a key. 
  - This function returns the **value** in the map **associated with the given key**.    
  *It returns null if the map doesn’t contain the key.*
    - eg.:   
      [@use 'sass:map'](https://sass-lang.com/documentation/modules/map)
      ```
      //first get the @use
      @use 'sass:map';


      // create a key-value pair variable
      $font-thickness: ("regular": 400, "medium": 500, "bold": 700);

      // use it on your class (here is `.text`)   
      .text {
        font-weight: map.get($font-thickness , bold)
      }
      ```
      -  in plain css:
          ```
          .text {
            font-weight: 700;
          }
          ```

<br>

**Some main `map` functions (with `-`):**
-  __map-keys()__ :    
    - this function produces a list of all the keys available in a map.
    - it requires one argument to be passed in.
      - eg.:
        ```
        // defining a variable:
        $map1 : ( 'keyName' : 'value', 'keyName2' : 800px );

        // using the map-keys function
        .main {
          content: map-keys($map1);
        }
        ```
        in plain css:
        ```
        .main {
          content: 'keyName1','keyName2'
        };
        ```

-  __map-values()__ :    
    - this function prints out a list of values within a map.
    - it requires one argument to be passed in.     
    *(If the argument contains nested map, it creates en error)*
       - eg.:
        ```
        .main {
          content: map-values($map1);
        }
        ```
        in plain css:
        ```
        .main {
          content: 'value', 800px;
        }
        ```

-  __map-has-key()__ :    
    - this function determins if a map has a key stored within it.
    - it requires two argument to be passed in:    
    first: the map (variable eg: `$map1`), second: the key we're looking for   
    this return a boolean: true (if the key is found) or false (key is not found).
      - eg.:
        ```
        .main {
          content: map-has-keys($map1, 'keyName');
        }
        ```
        in plain css:
        ```
        .main {
          content: true;
        }
        ```
-  __map-get()__ : 
    - this function obtains the value of a key.
    - it requires two argument to be passed in:    
    the first: the map  (variable eg: `$map1`), the second: the key we want to target.
      - eg.:
        ```
        .main {
          content: map-get($map1, 'keyName');
        }
        ```    
        in plain css:    
        *as a result, we can see the key's value being produced*
        ```
        .main {
          content: 'value';
        }    
        ```
-  __map-merge()__ : 
    - this function merge some maps together.
    - it requires two argument to be passed in:    
    the map (the variables eg: `$map1, $var2`) we want to merge together.
      - eg.:
        ```
        // defining 2 variables:
        $map1 : ( 'keyName' : 'value', 'keyName2' : 800px );

        $var2 : ( 'key1' : 'value1', 'key2' : 'value2', 'key3' : 'value3');

        // using the map-merge function
        // using the inspect function, otherwise it produces error in the css❗️
        .main {
          content:inspect(map-merge($map1, $var2));
        }
        ```
        in plain css:
        ```
        // the result is a string
        .main {
          content: ('keyName1' : 'value', 'keyName2' : 800px, 'key1' : 'value1', 'key2' : 'value2', 'key3' : 'value3');
        };
        ```    
-  __map-remove()__ :  
  - this function removes a single or multiple keys from the map, then output the map itself.
  - it requires several arguemnts:
    first: the map (variable eg: `map1`), second: key we want to remove (eg: `value`).
      - eg.:
        ```
    
        $map1 : ( 'keyName' : 'value', 'keyName2' : 800px );

        // using the map-remove function
        // using the inspect function, otherwise it produces error in the css❗️
        .main {
          content:inspect(map-remove($map1, 'value'));
        }
        ``` 
        in plain css:
        
        ```
        // the result is a string, because we used the 'inspect'
        .main {
          content: ('keyName2: 800px);
        }
        ```   

**<sup>*[back to variables](https://github.com/Klosmi/html-basics/blob/master/sass.md#variables)*</sup>**

<br>

#### [__interpolation__](https://sass-lang.com/documentation/interpolation)

<br>

#### [__functions:__](https://sass-lang.com/documentation/at-rules/function)  
- to compute and return **values**  

- functions allow you to define complex operations on SassScript values that **you can re-use throughout your stylesheet**. 

- we can use arguments: **`$argument`** 

- declare with **`@function`** + **function_name** + **`($argument)`**.   
So `@function name($variable) { @return... }`

- the [@return](https://sass-lang.com/documentation/at-rules/function#return) indicates the value to use as the result of calling a function. 

- eg.:   
    function name is `thickness`   
    the argument is `$variable`   
    the action is `@return` which returns the `$font-thickness` with the argument
    we call the function with the its name `thickness`, and specify the argument (`$variable`) with the value eg:(`bold`).
    ```
    // create the variable key-value pairs
    $font-thickness: ('regular' : 400, 'medium' : 500, 'bold' : 700);

    // deifne the function
    @function thickness($variable) {
      @return map.get($font-thickness, $variable);
    }

    //call the function
    .container {
      width: 85vw;
      font-weight: thickness(bold);
      margin: 0 auto;

      ul {
        width: 200px;
        li {
          text-decoration: underline;
        }
      }
    }
    ```
    - in plain css:
      ```
      .container {
        width: 85vw;
        font-weight: 700;
        margin: 0 auto;
      }
      .container ul {
        width: 200px;
      }
      .container ul li {
        text-decoration: underline;
      }
      ```

<br>

#### **[@use](https://sass-lang.com/documentation/at-rules/use)**:   
  ❗️💡 SASS descourage us to us `@import`! Use **`@use`** instead.    
  [Using `@use` demands **name spacing**](https://sass-lang.com/documentation/at-rules/use#loading-members):   
   *You can access variables, functions, and mixins from another module by writing **<namespace>.<variable>, <namespace>.<function>()**, or **@include <namespace>.<mixin>()**. By default, the namespace is just the last component of the module’s URL.*

   (`@use` is **only accessible in that individual file**. **Solution:**    
   I have to include `@us`e for all the components where I use the given component.)

   💡 A solution to avoid namespacing (it can be tiring to write it every time): use **`as *`** ❗️
   - eg.:
      Let say I have a colors.scss component.
      The namespacing way:
      ```
      @use '../folder/colors';

      .car {
        color: colors.$primariy-color;
      }
      ```
      **Avoiding the namespace:**
      ```
      @use '../folder/colors' as *;

      .car {
        color: colors.$primariy-color;
      }
      ```


  

####  **[@forward](https://sass-lang.com/documentation/at-rules/forward)**:   
   *If you want to **load members from many files at once**, you can use the @forward rule to forward them all from one shared file.*

   The best way to use it:   
   When you have several components with a long path, and you don't want write them all in your style.scss, it can be very long.      
   👉 create and **index.scss** file.    
   👉 list all your components here, using the **@forward**   
   👉 go back to your style.scss and now you can just include only the component's folder name using `@use` + `as *;`. It will automatically know where the component is, becasue it is in an index.scss file.   
   - eg.:   
      I have 2 components, both are in the abstract folder. I am in my style.scss
      ```
      @use '../abstract/colors' as *;
      @use '../abstract/fonts' as *;

      .car {
        color: colors.$primariy-color;
        font-size: $font-size;
      }
      ```  

      **using the forward, index.scss method**:     
      I am in the abstract folder, and I "import" the components with @forward
      ```
      @forward '../abstract/colors';
      @forward '../abstract/fonts';
      ```
      Now back to the style.scss. I have to only "import" 1 single line, and it includes all my components.
      ```
      @use '../abstract' as *;

      .car {
        color: colors.$primariy-color;
        font-size: $font-size;
      }
      ```


<br>

  ###  Useful links
  - [Learn more by reading the SASS Documentation](https://sass-lang.com/documentation)
  - [Most useful features](https://levelup.gitconnected.com/a-beginners-guide-to-sass-cb53596777dd)
  - [@use, @forward and namespace](https://www.youtube.com/watch?v=CR-a8upNjJ0)

---
   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)

