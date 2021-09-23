# [SASS: Syntactically Awesome StyleSheets](https://sass-lang.com/guide)    

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

  - **one-to-one mode**:
    - typing the following command in the terminal:
      ```
      sass main.scss main.css
      ```
    - result is 2 new files:   
        main.css   
        main.css.map

<br>    

 - **many-to-many mode**:   
    - if you have a components directory  `/scss/components/` with a `button.scss`, `input.scss`, and `modal.scss`.    
    We want them to go to the `/assets/` directory:
      ```
      sass --watch --no-source-map scss/components:assets/css/components
      ```
      
      <br>

      this comiles everything: directory with sass to a directory ti css

      ```
      sass --watch sass:css
      ````
      <br>

- **let's get into the code**   
  I show you the __SCSS__ way, basic key concepts

  -  __variables:__
      ``` 
      $primary-color:#503d4d;
      $accent-color:#ff652f;
      $text-color:#fff;
      ```

<br>

  - __variables with key-value pairs:__
    ```
    $font-weights: ("regular": 400, "medium": 500, "bold": 700);
    ```

  <br>

  - __the key-value `map-get`:__
    ```
    p {
      font-weight: map-get($font-weights, "bold");
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
    
  - __nesting:__
    ```
    .main {
      width: 80%;
      margin: 0 auto;

      p {
        font-weight: map-get($font-weights, "bold");
      }

    }
    ```
    - in plain css:
      ```
      .main p {
        font-weight: 700;
      }
      ```
 
 <br>
 
  - __nesting using the `&` shortcut and class names:__
    **`&`** let us not to repeat the parent's name
      ```
      .main {
        width: 80%;
        margin: 0 auto;

        & .main_text {
          font-weight: map-get($font-weights, "bold");
        }

      }
      ```

<br>

  - __nesting with classes demands using interpolation:__    
      using: **`#{ }_`**
      ```
      .main {
        width: 80%;
        margin: 0 auto;

        #{&}_text {
          font-weight: map-get($font-weights, "bold");
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

  - __nesting classes without interpolation:__
      ```
        .main {
        width: 80%;
        margin: 0 auto;

        &_text {
          font-weight: map-get($font-weights, "bold");
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

  - smsm