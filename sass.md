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
