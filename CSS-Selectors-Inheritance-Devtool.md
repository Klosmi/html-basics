# [CSS Inheritance](https://developer.mozilla.org/en-US/docs/Web/CSS/inheritance) :
it controls what happens when no value is specified for a property on an element.    

Some CSS properties inhereted by child elements, if they're not set on that element specifically.

 - eg.: you give a color to the `body` (we can give also to `section` etc.), and all the rest, `h1`, `p` which are not set to any color, will inheretet the `body`'s color.
      ```
      body {
        color: red;
      }
      ```
- in the Devtool we can see, at the Styles, scrolling down: `inhereted from` : *(in this case)* `body`
  
- inheritance goes to a closer element if I have several elements and they inherit from eachother. Eg.:
    ```
      body {
        color: red;
      }
      section {
        color: blue
      }
    ```
- **certain elements don't inherit** things by default, like the `<form>` element.  **But** using the `inherit`, and the `<form>` will inherit the color.   
  
  ###### *we set the `form` to 🟡yellow, but the `button` and other parts of the `form` don't inherirt the 🟡yellow color.*
  ```
  form {
    color: yellow;
  }
  ```
  ###### *setting the 'button's color property to  **`inherit`**, makes the `button` to inherit the `form`'s color.
    ```
  form {
    color: yellow;
  }

  button {
    color: inherit;
  }
  ```

- inheritance is always from the parent element in the document tree, even when the parent element is not the containing block.
---
 
# [CSS Devtools *in chrome*](https://developer.chrome.com/docs/devtools/css/) :
  - right click 👉 __inspect elements__
  - see the `Styles` when you inspect an element
  -  you can tweak the styles
  -  you  can search on `Filter`
  -  when a style is ~~crossed off~~ it means, it is lost in specificity battle. Maybe it is order, maybe it is less specific.
  
  ---
   [👈 go back](https://github.com/Klosmi/html-basics)
