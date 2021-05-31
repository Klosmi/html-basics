# [CSS basics](https://developer.mozilla.org/en-US/docs/Web/CSS)
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

 [👈 go back](https://github.com/Klosmi/html-basics)
