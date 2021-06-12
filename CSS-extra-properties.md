# [(Other) Useful CSS properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) :    
these are a few CSS properties which are nice to know, but not crucial for the basic knowledge.

## [Alpha Channel](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity) + [Opacity](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity)
  
  <br>

 [RGB**A**](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/rgba()) - **Alpha Channel**:  : 

  The `rgba()` [functional notation](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions) expresses a color according to its red, green, and blue components. An optional alpha component represents the color's transparency.    

  **The 'a' from the 'rgba' is the alpha, which governs the transparency of the color**.  

  - it is a value from 0 to 1.
    - eg.:
      ###### *The HTML*
      ```
        <section>
          <div id="rgba">
              Lorem ipsum dolor sit amet.
              <button>Button</button>
          </div>
      ``` 
      ###### *The CSS:  we give background-color to the `<div>`*
      ```
      #rgba {
        background-color: rgba(255,255,255,0.7) /* → 0.7 is the alpha channel, here it's partially transparent. */
      }
      ```
      Only the background color will be partially transparent. The text and `<button>` are not. Only the element which have the `RGBA` value will be impacted.


    - you can add `Alpha Channel` to hexadecimal colors : add two digits at the and of the hexadecimal color from 00 to FF.
      - `00` full transparency is.
      - `FF` is no transparency at all.
        - eg.:
          ###### *CSS, hexadecimal color eg.: `#60f7ab` + `4f` alpha channel.*
          ```
            #hex {
              background-color: #60f7ab4f     /* → #60f7ab  + 4f */
            }
          ```

      <br>

  **[Opacity](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity#values)** :   
  The opacity CSS property **sets the opacity of an element**. Opacity is **the degree to which content behind an element is hidden**, and is the **opposite of transparency**.

  Opacity is not a part of a color or a channel like rgb**a**.   
  Opacity is a property we set on an element which governs the entire element's "transparency" (although it is not transparency), **including its contents and any descendants**.   
  - eg.: 
    ###### *The HTML*
    ```
      <section>
        <div id="opacity">
            Lorem ipsum dolor sit amet.
            <button>Button</button>
        </div>
    ```
    ###### *The CSS*
    ```
      #opacity {
        background-color: yellow;
        opacity: 0.5;     /* → the background-color has 0.5 opacity */
      }
    ```
    Thet text in the `#opacity` `<div>` and the `<button>` will be "transparent" too not just the background color. **The entire element within that `<div>` will be impacted by the `opacity`.**

<br>
<br>

## [Position](https://developer.mozilla.org/en-US/docs/Web/CSS/position) 
  The position CSS property sets how an element is positioned in a document. The `top`, `right`, `bottom`, and `left` properties determine the final location of positioned elements.

  Postion [Values](https://developer.mozilla.org/en-US/docs/Web/CSS/position#values):   

  - `static` : **this is the default value**.   
    The element is positioned according to the normal flow of the document.   
     The `top`, `right`, `bottom`, `left`, and `z-index` properties **have no effect**. *(If you try using eg. the `top`, nothing will happen.)*
      -   eg.: 
          ###### *The CSS, `<section>` `id="#static"`*
          ```
          #static {
            position: static;
          }
          ```

  - `relative` : it is going to keep the element in the normal flow of the document, but we can offset it relative to itslef by using the `top`, `right`, `bottom`, `left`.   
  *The element is positioned relatively to where it would be, if I didn't offset it.*
      -   eg.: 
          ###### *The CSS, `<section>` `id="#relative"`*
          ```
          #relative {
            position: relative;
            top: 50px;      /* → offset my element from its current position - pushing it down */
            left: 70px;     /* → offset, it pushes to the right.
          }
          ```

  - `absolute` : the element is **removed from the normal document flow**, and **no space is created for the element**. And **it is positioned relative to its closest positioned ancestor if any**; otherwise, it is placed relative to the initial containing block (basically to the `body`).
  

      -   eg.: 
          ###### *The HTML, `<section>` `id="#absolute"`, `<div> `id="#second"`*
          ```
          <section id="absolute">
            <h2>Absolute</h2>
            <div></div>
            <div id="second"></div>
            <div></div>
          </section>
          ```
          ###### *The CSS, `<div> `id="#second"`*
          ```
          #second {   
            position: absolute;
          }
          ```
          From the three elements, which are next to each other (horizontally), I can see only two, because the third element got behind the `#second`. It is like the space collapsed and they're stacked.     
          Why? Because the `#second` element **doesn't take up any space in the document, it is removed from the normal flow**.
          <br>   
          But: 
          ###### *The CSS, `<section>` `id="#absolute"` (the parent element), `<div> `id="#second"`(the child element)*
          ```
          #absolut {  
            position: relative;
          }

          #second {  
            position: absolute;
            left: 70px;
          }
          ```
          Now `#second` does not take up any space. And it is now positioned relative to its parent(`#absolute`), which also is positioned (*to realtive btw*).
  
  <br>

  - `fixed` : the element is removed from the normal document flow, and no space is created for the element in the page layout.
  **It is positioned relative to the initial containing block.**

    When an element is positioned fixed, it's going to stay "there". Its position is relative to the containing block always. 
    *(It is like absolute, **except** it has nothing to do with any parent elements.)*

      -   eg.: 
          ###### *The HTML, `<section>` `id="#fixed"`, `<div> `id="#second"`*
          ```
          <section id="fixed">
            <h2>fixed</h2>
            <div></div>
            <div id="second"></div>
            <div></div>
          </section>
          ```
          ###### *The CSS, `<div> `id="#second"`*
          ```
          #second {   
            position: fixed;
          }
          ```
          From the three elements, which are next to each other (horizontally), I can see only two, because the third element got behind the `#second`.   
          Why? Because the `#second` element **doesn't take up any space in the document, it is removed from the normal flow**.
          <br>   
          But: 
          ###### *__Here there is no parent element.__ The `<div> `id="#second"*
          ```
          #second {  
            position: fixed;
            top: 0;      /*→ it moves up to the containing block */
            left: 400px;
          }
          ```
          When something is positioned `fixed` it is gonna **stay** there. It is positioned **relative to its containing block**, always.
  <br>

- `sticky` : it sticks. 
  The element is positioned according to the normal flow of the document, and **then offset relative to its nearest scrolling ancestor and containing block** (nearest block-level ancestor). The offset does not affect the position of any other elements. 

  In other words: it starts not fixed and then later it get fixed. So the element begins not fixed to the top. It will scroll along with content until it hits the top and then it stays there.

  It's kinda mixture of position `relative` and `fixed`.

  - eg.: 
    ###### *The HTML `<div> `class="second"`*
      ```
      <section id="sticky">
        <h2>Sticky</h2>
        <div></div>
        <div class="second"></div>
        <div></div>
      </section>
      ```
      ###### *The CSS, `<div> `class="second"`*
      ```
      #sticky {
        height: 600px;  /*→ .second's nearest block-level ancestor */
      }

      #sticky .second{   
        position: sticky;
        top: 0;
      }
     ```
    The sticky item’s container (here is `<section id="sticky">`) is the only area in which the sticky item can stick.  
    In other words, the container is the scope of the sticky item, and the item can’t get out of its sticky container. So **it only sticks within its container**(here the  `<section class="sticky">`).   

    The above example (the sticky portperty) only works if we use classes!   
    
    (This [video](https://www.youtube.com/watch?v=9xygOHSuzQ8) explaines it quite well.)

💡 Note, that normally the 'second' id's should actually be **classes**. **You should only have one unique id per page.** If it needs to replicate, then a class is the correct choice!


<br>
<br>

## [Transition](https://developer.mozilla.org/en-US/docs/Web/CSS/transition) 
  Transitions enable you to define the transition between two states of an element. 

   `transition` is a shorthand property for `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`.

     

---

   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
