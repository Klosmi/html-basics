# [CSS Selector](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors) 
##### and some [further reading about selectors](https://css-tricks.com/how-css-selectors-work/)

<br>

- asterisk <u>[**\***](https://developer.mozilla.org/en-US/docs/Web/CSS/Universal_selectors)</u>  = universal selector : it selects everything in the document

- **element selector**: select everything in a given type.
   - eg.:
      ###### *selects all the images*
      ```
      img {
        width: 100px;
        height: 200px;
      }
      ```
- **selector list**: use a comma `,` to combine selectors in list.
  -  eg.:
      ###### *selects all the h1 and h2*
      ```
      h1, h2 {
        text-decoration: underline plum;
      }
      ```
- [ID selector](https://developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors) : single out a single element. It provides a hook to our CSS element. By adding an ID to your markup and you can reference it using the name of the ID and the hash sign.
    - it styles one **thing**, only used once.
  
    - unique identifier

    - keep them to the minumum (don't spam them everywhere)
  
    - the ID selectos sign is: #, so `#idselector`
    eg.: 
      ``` 
      <button id="login">Login button</button> 
      ```
      so in you CSS it looks like this:   
      ###### only that login element which has the ID is singled out. 
      ```  
        #login {
          color: white;
          background-color: black;
        }
      ```

- [Class selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors) : a class selector matches elements based on the contents of their class attribute.  It is a similar idea to the ID, except that a class can be applied to multiple elements.
  - you can have deifferent groups to style them.
  
  - by defining a class, you can group together content, also they don't have to be the same type of element.

  - use classes more often than IDs.
  
  - class selectors sign is **.** so use `.classselector`   

  - eg.:
    ``` 
    <span class="tag">fish</span>
    ```
    so in your CSS it looks like this:
    ###### only those span elements which have the class are singled out.
    ```
    .tag {
      color: blue;
    }
    ```
- [Descendant combinator (selectors)](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_combinator) : are represented by a single space ( ) character, it **combines** two selectors *(not with comma, but with white space)*. Selectors that utilize a descendant combinator are called descendant selectors. 
    -  also called as *generic descendent* selector
  
    -  so you can select elements which are nested inside of an other elements.
  
    - eg.:
      ###### *selecat all of those `<a>` **that are nested inside** an `<li>`*
      ```
      li a {
            color: red;
          }
      ```   

- [Adjacent combinator (selectors)](https://developer.mozilla.org/en-US/docs/Web/CSS/Adjacent_sibling_combinator) : `+ `separates two selectors and matches the second element only if it immediately follows the first element, and both are children of the same parent element.
  
   - not parent or children, they are adjacent, **one after the other**.
      ```
      <h2>Lorem ipsum dolor sit amet...</h2>
      <button>Click</button>
      ```
      ###### *select a `button` that comes right after every `h2` on the same level (so this applies all the `buttons` which  are strictly after `h2`).*
      ```
      h2 + button {
        background-color: yellow;
      }
      ```
- [Direct child combinator (selector)](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_combinator) : `>` is placed between two CSS selectors. It selects  the children which are nested somewhere in an other element. Children which are the <u>**direct descendants**</u>. In other words, "one level down".
  - it only selects **direct** descendence of the parent element. It **doesn't select general descendents**.
  
  - eg.: an `<a href="#link">` nested directly in the `<footer>`, the other `<a>`s are nested in `<ul>`. So the direct child of the footer is  only the `<a href="#link">`.
    ```
    <footer>
     <nav>
        <ul>
          <li> <a href="#home">Home</a></li>
          <li> <a href="#contact">Contact</a></li>
        </ul>
      </nav>
      <a href="#link">Select me</a>
    </footer>
    ```
    so in your CSS it looks like this:
    ##### *you can select the `<a href="link">...` because it is a direct child of the footer, it is directly 1 level below the parent `footer`, compared to the other `<a>`s which are nested in a `<ul>`*.
    ```
    footer > a {
      color: blue;
    }
    ```

- [Attribute selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) : matches elements based on the presence or value of a given attribute. So, it allows us to select elements based upon some particular attribute.
  - attribute selector: `[ attribute_name = something ]`
  - eg.: if you want to select all input elements where the type attribute is set to "password"
    ###### *if I have several inputs, but I want to style **only** the `password` input differently, than I can do it with attribute selector:*
      ```
      input[type="password"] {
        width: 300px;
        color: green;
      }
    ```
--- 

## [Pseudo-Classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) :  
`pseudo-class` is a keyword added to a selector that specifies a **special state of the selected element(s)**.   
For example, :hover can be used to change a button's color when the user's pointer hovers over it.   
*(They all start with a colon **`:`**)*

- [:hover](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover) : it modifies our selection when the element is hovered over. 
    - usually used to show you can interact with the element.

   - eg.: change the background color of a `<button>` when we hover over:
      ```
      button:hover {
        background-color: pink;
      }
      ```

- [:active](https://developer.mozilla.org/en-US/docs/Web/CSS/:active) : represents an element (such as a button) that is being activated by the user.   
  - Eg.: a `button` when I **press** it changes the background-color to green (while I keep pressed down the mouse on it)
      ```
      button:active {
        background-color: green;
      }
      ```
- [:checked](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked) : selector represents any radio `<input type="radio">`, checkbox `<input type="checkbox">`, or option `<option>` in a `<select>` element that is checked or toggled to an on state.
   - eg.: any `<input>` with type of `checkbox` where it's actually checked
      ```
      input[type="checkbox"]:checked {
      box-shadow: 0 0 0 3px pink;
      }
      ```

- [:nth-of-type()](https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-of-type) : help us select based upon a position in a group of siblings.  
*(In other words it matches elements of a given type (tag name), based on their position among a group of siblings.)*
    - eg.: I have ten `<section class="post">`s in a document, and I want to select the *third* to change the `background-color` to red.
      ```
      .post:nth-of-type(3){
        background-color: red;
      }
      ```
    - to change **every third** `<section class="post">` the syntax is different: `nth-of-type(3n)`. *(number + n)* ❗️
      ```
      .post:nth-of-type(3n){
        background-color: red;
      }
      ```

- many other pseudo classes (check on [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)):
   - :first
   - :first0of-type
   - :not()
   - :nth-of-child()  
   ...etc.

---
## [Pseudo-**Elements**](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) : 
*(they are not pseudo-classes, they are a distinct concept)*  
 Pseudo-Elements is a **keyword added to a selector** that lets you style a **specific part of the selected element(s)**.   
 *(For example, `::first-line` can be used to change the font of the first line of a paragraph.)*  
   __We use two colons **`::`**__   
  

&nbsp;

- [**::first-letter**](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter) : we can select the first letter of some selection.   
Pseudo-Elements applies styles to the first letter of the first line of a block-level element, but only when not preceded by other content (such as images or inline tables).
  - you can select the first letter of every paragraph, every span, etc.

   - eg.: select the first letter of **every** `h2`  and change it to red.     
      ```
      h2::first-letter {
        color: red;
      }
      ```

-  [**::first-line**](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-line) : applies styles to the first line of a block-level element.   
*(Note that the length of the first line depends on many factors, including the width of the element, the width of the document, and the font size of the text.)*
    - eg.: the first line of a paragraph (`p`)
      ```
      p::first-line {
        color: blue;
      }
      ```
- [**::selection**](https://developer.mozilla.org/en-US/docs/Web/CSS/::selection) : applies styles to any part of a document, or some part of an element that has been highlighted/selected (such as clicking and dragging the mouse across text, and eg. the selection colour is purple), 
   - eg.: you select a paragraph (`p`)
      ```
      p::selection {
        background-color: orange;
      }
      ```
      To use it to the entire document:
      ```
      ::selection {
        background-color: yellow;
      }
      ```
 - some other pseudo elements (check on [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements#index)):
   - ::after
   - ::before
   ...etc.

---
 [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
