# [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- we use CSS **rules**
-  is a stylesheet language used to describe the presentation of a document written in HTML or XML. CSS describes how elements should be rendered on screen...
-  the CSS basic pattern/template looks like this: 
    ```
    selector { 
      property: value; 
    }
     ```
     here's a much more complex, but the same pattern, same logic:  
      *(selector – property – value)*  
     ```
     input[type="text"]:nth-of-type(2n) {
       border: 5px solid green;
     }
     ```
    ##### *This means the following: all inputs where type is set to text, and every second one is selected, and give them a border which is 5px solid and green color.*

- ### [MDN's CSS reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) is a great documentation & resource
---
## How to include the styles?
  - <u>inline styles</u>: when writing the style directly inline on each element.  

 - <u>`<style>`</u> element: when you write your styles inside of a `<style>` element.  You write it in the `<head>` section.
   ##### *Makes it impossible to share styles between documents.*  

 - <u>External stylesheet</u>: when you write your styles in a separate `.css` file. include them using the `<link>` element in the `<head>` of the html doc.
    ```
    <head>
      <title>CSS demo page</title>
      <link rel="stylesheet" href="assets/style/styles.css">
    </head>
    ```
---
## [CSS color properties](https://developer.mozilla.org/en-US/docs/Web/CSS/color)
  - [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color) and [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) technically are different. The `background` property does more than just changing the *background* *color*, we can set also a background image, a gradient, etc.
  - `named colours` are supported with every browser
  - [`rgb(255, 255, 255)`](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/rgb) *red, green, blue*
  - **Hex** = hexadecimal (also red-green-blue, 0-255) = base 16.   
    Every spot has 16 choices: **0-9**, **A**=10, **B**=11, **C**=12, **D**=13, **E**=14, **F**=15  
    `#ff|ff|ff = r|g|b`    
    eg.: yellow is `#ffff00` or `#55ff00` = `#5f0`

- [hsl](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/hsl) : functional notation expresses a given color according to its hue, saturation, and lightness components. An optional alpha component represents the color's transparency.  
  eg.: `hsl(100, 100%, 50%)` =  `#55ff00`

- #### [*color picker*](https://htmlcolorcodes.com/)
  ---
## [CSS text properties](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)
- [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align): this property sets the horizontal alignment of the content **inside a block element*** or table-cell box. This means it works like vertical-align but in the horizontal direction. 
  ##### *\*(It does not mean how an element is aligned on the page itself, a.k.a. not spatially where it goes, but within an element.)*

- [font-weight](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight) :  CSS property sets the weight (or boldness) of the font. 
  -  [values](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight#common_weight_name_mapping): you can use numeric values, like 400 (which is normal), etc.
  -  [realitve font-wieght](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight#meaning_of_relative_weights): when **lighter** or **bolder** is specified.

- [text-decoration](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) :  
- CSS property sets the appearance of decorative lines on text. It is a [shorthand](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties) for text-decoration-line, text-decoration-color, text-decoration-style, and the newer text-decoration-thickness property.
    - we can specify the **color** of the eg. underline, and the **thickness**:
      ``` 
      text-decoration: blue underline 4px;
      ```
   - remove a default underline (usually anchor `<a>` tags):
      ```
      text-decoration: none;
      ```
- [line-height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)  :  controls the hieght of a line in a text.

  - it is possible to just use numbers (eg. 2), which will multiply by the value(2 times) of the number of the font-size:   
    ###### if my font-size is 10px, than 20px is the line-height
      ```
      line-height: 2;
      ```
- [letter-spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing) : sets the horizontal spacing behavior between text characters.

- <u>**[font-size](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)**</u> :  CSS property sets the size of the font. **Changing the font size also updates the sizes of the font size-relative <length> units**, such as em, ex, and so forth.
- ([units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)) :
    | realtive size | absolute size |
    |---------------|---------------|
    | EM            | PX            |
    | REM           | PT            |
    | VH and. VW    | IN            |
    | %             | MM            |
    | etc.          | etc.          |

  - PX: 💡 *not recommended to use for responsive websites!*
  - 
    ```
    font-size: 18px;
    ````
- [text-transform](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform) : CSS property specifies how to capitalize an element's text.
    -  eg. `text-transform: uppercase;` sets the text in uppercase letters.
- [font-family](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) :  CSS property specifies a prioritized list of one or more font family names and/or generic family names for the selected element. 
  - [most commonly used fonts and their support in os systems, etc.](https://www.cssfontstack.com/)
  - font-stack : a list of fonts that are used in order.  
    eg: `font-family: Helvetica, Arial, sans-serif;` 
    The fallback font here is the `sans-serif` *(a backup font)*, it's not a specific font, it is a family of sans-serifs.
---
 [👈 go back](https://github.com/Klosmi/html-basics)

