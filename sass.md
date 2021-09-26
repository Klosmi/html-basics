# [The basics of  SASS: Syntactically Awesome StyleSheets](https://sass-lang.com/guide)    

is an extension language for CSS. 
Sass lets you write clean, sustainable CSS code and solve the repetition and maintenance problems which are in traditional CSS.

- Sass must first be converted, or __compiled__, to CSS before the browser can directly understand it
- compiling means: to converting code to lower level code so that it can be executed. 

- by __compiling SCSS to CSS__, it can be __interpreted by your browser__ and the results will appear on a webpage.

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

 ### **[Let's dive into the code(s)](https://sass-lang.com/documentation)**   
  I show you the __SCSS__ way, basic key concepts


  ####  __[variables:](https://sass-lang.com/documentation/variables)__
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
 - eg.:
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

        &_text {
          font-weight: map-get($font-weight, "bold");
        }

      }
      ```
      - in plain css:
        ```
        .main_text {
          font-weight: 700;
        }
        ```

<br>

#### __nesting with classes, [using interpolation:](https://sass-lang.com/documentation/interpolation)__          
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

##### __[Maps:](https://sass-lang.com/documentation/values/maps#using-maps)__   


**<sup>*[back to variables](https://github.com/Klosmi/html-basics/blob/master/sass.md#variables)*</sup>**



<br>

#### __partials:__   
- baiscally snippets, parts of SCSS what we can keep in a separate file and include in to our main SCSS

-  file name start with **`_`** underscore, eg.: **`_reset.scss`**

- to include it into our main SCSS, we use   
       **`@import './reset';`**    
       💡 note that the no need to include now the `.scss` part
 - eg.:
        ```
        import './reset';

        .main {
          width: 80%;
          margin: 0 auto;

          &_text {
            font-weight: map-get($font-weight, "bold");
          }
        }
        ```
 
 <br> 

#### __functions:__   
- to compute and return **values**  

- we can put the `font-weight: map-get($font-weights, "bold");` into a function, so we can call it later.

- we can use arguments: **`$argument`** 

- declare with **`@function`** + **function_name** + **`($argument)`**
- eg.:
    ```
    @function weight_func($weight-name) {
      @return map-get($font-weight, $weight-name);
    }

    // ($font-weight, $weight-name) is a key-value paire
    ``` 
    so this can be used like:
    ```
    .main {
          width: 80%;
          margin: 0 auto;

          &_text {
            font-weight: weight_func("bold");
        }
      }
    ```
<br>

#### __mixins:__
- you can put into mixins all the content you don't want to repetedly type.

- the define **styles**

- **`@mixin`** + space + **`name`**

- to include **`@include`** + **`name`**

- eg.:
      ```
      @mixin flexCenter {
        display: flex;
        justify-content: center;
        align-items: center;
      }
      ```
      and use this mixin
      ```
      .main {
        @include flexCenter;
        width: 80%;
        margin: 0 auto;
      }
      ```

<br>

#### __mixins with $arguments:__
- like function mixins can also have arguemnts

- using the `$` sign

- `@mixin flexCenter($direction)` and later we call it `@include flexCenter(column);`

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

#### __mixin__ is good for **@media** and using the **@content block**:
- To taking arguments, a mixin can take an __entire block of styles, known as a content block__. A mixin can declare that it takes a content block __by including the @content__ at-rule in its body. The content block is passed in using curly braces like any other block in Sass, and it’s injected in place of the @content rule.

- eg.:
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
        .
        .
        .
        @include mobile{
          flex-direction: column;
        }
      }
     ```

<br>

#### __[extend:](https://sass-lang.com/documentation/at-rules/extend)__
- we can extend elements, so the element that we extended it to ihnerits the all tstyle from the selected element.
- `@exted`

 - eg.:   
    We have to identical parapgraph classes: `.text1` and `.text2`    
    We want to change only the `:hover` color on `.text2`
    ```
    .main {
      width: 80%;
      margin: 0 auto;
      .
      .
      .
      & .text2 {
        @extend .text1;

        &:hover {
          color: red;
        }
      }
    }
    ```

<br>

#### __[operations:](https://sass-lang.com/documentation/operators#order-of-operations)__
- addition, substraction, multiplication, division, etc.

- ❗️SASS you can not mix type: `80% - 40px` will not work.   
The operation has to be the same type❗️

- plain css it is the **[`calc()`](https://developer.mozilla.org/en-US/docs/Web/CSS/calc())**
- eg.:   
  in SASS no need to `calc(800px - 400px)`, it just simple:
    ```
    .main {
      width: 800px - 400px;   // intsead of calc(800px- 400px);
      margin: 0 auto;
      .
      .
      .
    }
    ```

<br>

  ###  Useful links
  - [Learn more by reading the SASS Documentation](https://sass-lang.com/documentation)
  - [Most useful features](https://levelup.gitconnected.com/a-beginners-guide-to-sass-cb53596777dd)
