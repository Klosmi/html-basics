# [CSS Box Model - Display Property](https://developer.mozilla.org/en-US/docs/Web/CSS/display) :
it sets whether an element is treated as a **block element** or an **inline element** and the layout used for its children, such as **flow layout**, **grid** or **flex**.

> Reminding: an [__inline element__](https://github.com/Klosmi/html-basics/blob/master/inlene-vs-block.md) is going to fit alongside other elements in the same line (is not pushing everyone else onto a separate line). It takes out the minimum amount of space.
> 
> However a [__block level element__](https://github.com/Klosmi/html-basics/blob/master/inlene-vs-block.md) is pushing everyone else onto a separate line, it is something that it wants to exist on its own line, its own "block".

1. **Block** - [changing element levels](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#changing_element_levels): *(`display: inline;`)*:   
    Block elements break the flow of a document.   
    Width, Height, Margin, & Padding  are respected.
    - all heading elements, like `h1` are inline

    - paragraph elements (`p`)

    - We can **change the block level element's like `h1` or `p` behaviour**: when we use **`display: inline;`**
      - eg.:
        the `<h1>` block level element is behaving now as an inline element (like a `<span>`)
        ```
        h1 {
            background-color: palegoldenrod;
            border: 1px solid black;
            display: inline;
        }
        ```
    - block level elements do <u>respect</u>: **width-height, padding, margin** properties 
    <br>

2. **Inline** - [changing element levels](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements#changing_element_levels): *(`display: block;`)*:   
    Width & Height are ignored.   
    Margin & padding push elements away horizontally but not vertically.  
    - `<span>`

    - We can **change the inline level element's like `span` behaviour**: when we use **`display: block;`**
        - eg.: 
            the `<span>` block level element is behaving now as a block level element (like an `<h1>`)
            ```
            span {
                background-color: palegoldenrod;
                border: 1px solid black;
                display: block;
            }
            ```  
     - inline elements don't <u>respect</u>: **width-height, padding, margin** properties  

<br>

3. **Inline-Block** - *(`display: inline-block;`)*:   
    It is going to __behave like an inline element__, but __with height, margin and padding are going to be respected__, when we use. **`display: inline-block;`**.
     - eg.:   
     I  create 3 `<div>`s, and I want them to be horizontally next to each other, I can give a **`display: inline-block;`**.   
     *(Note, if I give `display: inline;` it's not going to work, because `inline` doesn't respect width, padding, margin)*  
     
       The `<div>`s are sharing the space, the row by sitting in line together. They're not forcing each other onto a separate line, __but all the other properties with respect to the box model are going to work__ (width and height and margin will work).
        ```      
        div {
            background-color: green;
            border: 5px solid black;
            display: inline-block;
        }
        ```

4. `display: none;` :
    - to hide an element, just set the `display` property to `none`.
    - the element itself is not going to be deleted (it's there in the document)❗️ But they take up no space, and we don't see them.

    <br>
    
- **[Block and Inline Layout in Normal Flow](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flow_Layout/Block_and_Inline_Layout_in_Normal_Flow#elements_participating_in_a_block_formatting_context)**
- **[Further reading 💡](https://css-tricks.com/when-do-you-use-inline-block/)**

---
   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
