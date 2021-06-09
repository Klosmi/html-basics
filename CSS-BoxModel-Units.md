# [CSS Box Model - Units in depth](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units) [*(focus on relative units)*](https://www.w3.org/TR/css-values-3/#relative-lengths) :
__Relative length units__ specify a length __relative to another length__.  
*Style sheets that use **relative units can more easily scale** from one output environment to another.*

- EM・REM・VH・VW・%・*etc.*

- [percentage: `%`](https://developer.mozilla.org/en-US/docs/Web/CSS/percentage)  : percentages are always relative to some other value (*it is a percentage of something; it depends on what that something, propert is that we're setting*).  

  - it's a value from the parent and other times it's a value from the element itself.
    - value from the parent:
        - eg.: `width: 50%;` 👉 50% on qn element which means that we are setting that element to be **half the width of the parent element**.  
            ###### *HTML example: section (parent) contain the div (child)*
            ```
            <section>
                <div></div>
            </section>   
            ```
            ###### *CSS of the HTML above: section (parent) contain the div (child)*
            ```
            section {
                background-color: grey;
                width: 800px;
                height: 800px;
            } 

            div {
                background-color: red;
                width: 50%;       /* →  going to be 400px */
                height: 50%;      /* →  going to be 400px */
            }
            ```
            *The `div` is exactly half the size of its parent `section`.*
  -  value from the element itself:
        - elements are relative not to the parent but to themselves.  
          - eg.: our font size on an element is 100px, we give `line-height: 50%`, it means it is 50% of the elements itself, its own font size (not the parent).
            ###### *HTML example: `h1`*
              ```
              <h1>CSS Units</h1>
              ```
              ###### *CSS of the HTML above.*
              ```
              h1 {
                font-size 40px;
                line-height: 200%   /* →  200% of 40px = 80px */
              }
              ```

- [em](https://www.w3.org/TR/css-values-3/#em) :   
  *"my parent element's font-size, so each successive level of nesting gets progressively larger, eg.: if font size set to 1.3em, each nesting gives a 1.3 times bigger text.*   

  **With font size**: `1em` equals the font-size of the parent. `2em`s is twice the font-size of the parent, etc.
    - eg.:   
      ###### *HTML example: in an `<article>` see `h2` and `p`*
      ```
      <article>
        <h2>I am an h2</h2>
        <h3>I am an h3</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing.</p>
      </article> 
      ```
      ###### *`h2` is twice the font size of its parent element: `<article>` `h3` 1.5 times of its parent element`<article>`, `p` 0.8 times of its parent element `<article>`*
      ```
      article {
        font-size: 20px;
      }

      h2 {
        font-size: 2em;    /* →  2 times 20px = 40px | parent is <article> */
      }
      
      h3 {      
        font-size: 1.5em;    /* →  1.5 times 20px = 30px | parent is <article> */
      }

      p {
        font-size: 0.8em;  /* →  0.8 times 20px = 16px | parent is <article> */
      }
      ```

  **With other properties**, `1em` is equal to the computed font-size of the element itself.   
    Other properties like: `padding` and `margin`, and it's quite common to use `em`s with these properties. 👉 **`1em` is equal to the element itself*** *(and  not with the parent element❗️)*

    - eg.:  
      ###### *HTML example: in an `<article>` see `h2` and `p`*
      ```
      <article>
        <h2>I am an h2</h2>
        <button>Click</button>
      </article> 
      ```
      ###### **`margin-left: 1em`: the `1em` refers to itself, the `h2` element, where the fontsize is `2em`, so `1em` refers to the `2em`.
      ```
      article {
        font-size: 20px;
      }

      h2 {
        font-size: 2em;
        margin-left: 1em;    /* the current font size: 2em, and 1em refers to that → = 20px
      }

      button  {
        font-size: 1em;        /* = 20px */
        padding: 0 1em;        /* = 0 20px */
        border-radius: 0.5em;  /* = 0 10px */
      }
      ```
      Useful: when I want to proportionally scale the button to its content, em is handy: `padding` and `border-radius` all depends on the font-size. So if the `button`'s text is bigger the `border-radius` & `padding` will be proprtional, maintaince it's general shape.
      
      <br>

      💡 Shortcomings of the `em`: a multiple nested element can stack quickly (grow or shrink extremly), because the child's property value changes depending on the parent's parent's parent element.  
       - eg.:
            ###### *HTML example*
          ```
          <article>
            <ul>
              <li>
                Pasta
                <ul>
                  <li>Spaghetti
                    <ul>
                      <li>Spaghetti bolognese</li>
                    </ul>
                  </li>
                </ul>
              </li>
            </ul>
          </article>
          ```
          ###### *since the `<ul>` is `1.5em` (30px), the nested `<ul>`'s stack up, meaning that the *Spaghetti bolognese* (the child `<ul>`) will be 1.5 time 1.5 time 1.5em (67.5px)*
          ```
          article {
            font-size: 20px;
          }
          ul {
            font-size: 1.5em;  /* = 30px */
          }
          ```

- [rem](https://www.w3.org/TR/css-values-3/#rem) (= root em) :   
  relative to the **root html element**'s font-size. Oftern easier to wrok with.    
  The root element, is the **`<html lang="eng">`** right under the `<!DOCTYPE html>` (we can change of course the root `<html>` element's default font-size) 

  **If the root `font-size: 16px`, `1rem` is always `16px`, `2rem` is always `32px`, etc.**

  It is constant.

  So, rather than deriving the font size from the parent element like `em`,  
  💡  **`rem` derives the font size from the root HTML element's font size**.   
  (*👉 `rem` is relative to this (root) font size for **the entire document**.*)

  If your root `<html>` element has (the default) font-size= 16px; it is 16px anywhere in the document.
    - eg.:
      ```
        <article>
        <h2>I am an h2 rem</h2>
          <ul>
            <li>
              Pasta
              <ul>
                <li>Spaghetti
                  <ul>
                    <li>Spaghetti bolognese</li>
                  </ul>
                </li>
              </ul>
            </li>
          </ul>
        </article>
      ```
      *the root element `<html>` has the default 16px font size , the `<ul>` is `1rem` (16px), the nested `<ul>` is also `1rem` (16px) (rem doesn't stack up) so the "Spaghetti bolognese" (the child `<ul>`) will be as well `1rem` (here 16px).*
      ```
        html {
          font-size: 16px;  /* normally I can change this from default 16px to anything */
        }

        h2{
          font-size: 2rem; /* = 32px */
        }
        article {
          font-size: 1.5rem; /* 1.5 * 16 = 24px */
        }
        ul {
          font-size: 1em;  /* = 16px */
        }
      ```

  - you can mix `em` and `rem`:
    - eg.: when you have a `<button>`, and the `font-size` is based upon `rem`, but the `padding` the `border-radius` should change depending on what this actual `font-size` is: so using `em` for `padding` and `border-radius`.
