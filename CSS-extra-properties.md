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

-  **`transition` is a shorthand property** for :   
  &nbsp; &nbsp;[`transition-property`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-property) *(none, all, etc.),*    
  &nbsp; &nbsp;[`transition-duration`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-duration) *(3s, etc.),*    
  &nbsp; &nbsp;[`transition-timing-function`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function) *(eas-in, eas-out, etc.),*    
  &nbsp; &nbsp;[`transition-delay`](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-delay) *(1s, 250ms, etc.)*.


<br>

- **Syntax of `transition` property** consists the following:   
  1. [property name](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-property) → specify a specific property name, so **which `transition` effect** to use.  

  2. [duration](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-duration) → sets the **length of time a transition animation** should take to complete. So how long it takes.

  3. [timing function](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function) → sets how **intermediate values are calculated** for CSS properties being affected by a transition effect.

  4. [delay](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-delay) → specifies the duration to **wait before starting** a property's transition effect **when its value changes**.  
    
    <br>
    
- **duration:**
  - eg.:
    ###### *HTML*
    ```
    <div class="circle"></div>
    ```
    ###### *CSS: a hover transition __`duration`__*
    ```
    .circle {
      width: 300px;
      height: 300px;
      background-color: green;
      transition: 3s;     /* → duration is 3 seconds */
    }

    .circle:hover {
        background-color: blue;
        border-radius: 50%;
    }
    ```
    When you hover, the background color and shape changes in 3s as they would all be animated.

    <br>

- **singling out property names**:
  -  eg.:  singling the `background-color` transition
    ###### *HTML*
    ```
    <div class="circle"></div>
    ```
    ###### *CSS: only the background-color changes with a hover transition __`duration`__*
    ```
    .circle {
      width: 300px;
      height: 300px;
      background-color: green;
      transition: background-color 3s;  /* → single-out background-color */
    }

    .circle:hover {
        background-color: blue;
        border-radius: 50%;
    }
    ```
    By singling-out the `background-color`, it will changes with a 3s animation **ONLY** the `background-color`, the rest doesn't use the 3s animation.

    <br>

- **all properties**: 
  - eg.:  
    ###### *CSS: all properties change with a hover transition __`duration`__*
    ```
    .circle {
      width: 300px;
      height: 300px;
      background-color: green;
      transition: all 3s;  /* → all properties */
    }

    .circle:hover {
        background-color: blue;
        border-radius: 50%;
    }
    ```
    All the properties changes with `3s` animation.
    
    <br>

- **delay** : 
  - eg.: 
    ###### *CSS: specify `1s` `delay`*
    ```
    .circle {
      width: 300px;
      height: 300px;
      background-color: green;
      transition: all 3s 1s;  /* → 1s delay */
    }

    .circle:hover {
        background-color: blue;
        border-radius: 50%;
    }
    ```
    All the properties change with `3s` `duration` and `1s` `delay` animation. So when we hover over, it's going to take `1s` **before that transition even begins**. It goes both direction.
    
    <br>

- **specify different transitions at once:**
  - eg.: 
    ###### *CSS: specify `1s` `delay` `for background-color`, and `2s` for `border-radius`*
    ```
    .circle {
      width: 300px;
      height: 300px;
      background-color: green;
      transition: background-color 1s, border-radius 2s;  /* → 1s background-color, 2s border-radius delay */
    }

    .circle:hover {
        background-color: blue;
        border-radius: 50%;
    }
    ```
    specify `1s` `delay` `for background-color`, and `2s` for `border-radius`. We can see the background-color finishes before the border radius finishes.
    
    <br>
    
- **timing-function**: on the link are all the [syntax of timing-functions](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function#syntax) !
  - `linear;` → *never speeds up or slow down*
  - `eas-in;` → *start slow, speeds up* ・ ease-out; ・ ease-in-out;
  - `steps` `(6, end);` → *6 steps*
  - `cubic-bezier``(.29, 1.01 1, -0.68);` → *goes forward and backwards*
    
    <br>
    
  - **the way it works:**   
    there are four things what we can specify:  
      - `property` that we want to animate,     
      - `duration` that can be in seconds, milliseconds (500ms),
      - `timing-function`, like ease-in.
      - `delay` (the default is no delay)
      eg.: 
        ```
        transition: background-color 1s ease-in, border-radius 500ms;
        ```

   - eg.: 
      ###### *CSS: we have four `<div>` squares, each of them has a **separate**, different `timing-function` transition.*
      ```
      section div {
          height: 100px;
          width: 100px;
          background-color: blue;
          margin: 30px 0;
          transition: margin-left 2s;
        } 

      section:hover div {                       /*  → on hover all the "<div> squares" activated */
          margin-left:500px;                    /* → on hover the "<div> squares" go till 500px*/
        }

      div:nth-of-type(1){
          transition-timing-function: ease-in;
        }                                       /* → starts up a bit slow */

      div:nth-of-type(2){
          transition-timing-function: ease-out;
        }                                      /* → starts up quickly then slows down */

      div:nth-of-type(3){
          transition-timing-function: cubic-bezier(0.7, 0, 0.84, 0);
        }                                      /* → starts very slow */

      div:nth-of-type(4){
          transition-timing-function:  cubic-bezier(0.85, 0, 0.15, 1);
        } 
      ```
      All the four `<div>` squares get a `transition: margin-left 2s;`, **but** each one has a **separate** `timing-function` transition, and they get to the same spot at the end at the **exact same time**.

    💡 for different [timing-function or easings](https://easings.net/)❗️


    💡 Advice: it is better to **single out those properties which you want to make the transition**❗️ *(So, don't just do `transition all` because when you will make some changes in your code later, it will make your work harder.)*
    
---

   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
