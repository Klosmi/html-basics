# [CSS Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade) :  
it is about the order our styles are declared in actually matters. The order that things are encountered in is going to be reflected in what you
see in the browser.
- eg.: if you have two `h3` styles, the last one will matter *(here font-soze will be 40px)*.
  ``` 
  h3 {
    font-size: 30px;
  }
  h3 {
    font-size: 40px;
  }
  ```
---

# [CSS Specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) :

is how the browser decides which rules to apply when multiple rules could apply to the same element. 
It is a measure of how __specific__ a given selector is. The __more specific__ selector will be applied.   
*(So the browser decides which rule(s) to apply when there is a conflict.)*

- a simple example: I have  a paragpraph(`p`) 🔵blue. But I have a more **specific** `section p` with 🟡yellow color. So the 🔵blue will not apply on `section p`, which stays 🟡yellow.
  ```
  .post button:hover{
    background-color: yellow;
  }
  button:hover{
    background-color: blue;
  }
  ```

- [specificity calculator](https://specificity.keegan.st/)

- **element selector** vs. <u>**element selector + element selector**</u> (<u>this</u> is the strongest, because it is **more specific**)

- the general formula of specificity:
    - #### **ID** > **Class** > **Element**

- the specificity [calculation's math read it here](https://www.w3.org/TR/selectors-3/#specificity)
   - count *the number of ID selectors* in the selector *(A)*
   - count *the number of class selectors*, *attributes selectors*, and *pseudo-classes* in the selector *(B)*
   - count *the number of type selectors* and *pseudo-elements* in the selector *(C)*
   - *ignore the universal selector*

## <u>[Inline Styles](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity#selecNtor_types)</u>
*(Here they mention the inline style in one sentence)*:   
__Inline style(s)__ added to an element (e.g., style="font-weight: bold;") __always overwrite any styles in external stylesheets__, and thus can be thought of as having the __highest specificity__.
  - **bad practice!** ot recommended to use inline styling (however it is a valid way of styling elements).

## <u>[The **!important** exception](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity#the_!important_exception)</u> : 
When an `!important` rule is used on a style declaration, this declaration overrides any other declarations.   
*Although technically `!important` has nothing to do with specificity, it interacts directly with it.*     
Actually it **ignores specificity**, it just *wins*.

  - `!important` signals to the browser that this should be the most specific possible thing and it should override any other declarations.
  
  - **bad practice!** Not recommended to use it, however there are situations where it makes sence to use it. *Eg.: exteranlusing libraries and you want to override a style...*
  
  - you put `!important` after the declaration, like this:
      ```
      button {
        background-color: green !important;
      }
      ```

--