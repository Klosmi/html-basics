# [CSS Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model) :
it is the idea that everything in CSS is a box, and these boxes have a bunch of different properties.  
So, when laying out a document, the browser's rendering engine represents each element as a rectangular box according to the standard CSS basic box model.   

CSS determines the size, position, and properties (color, background, border size, etc.) of these boxes.   

Everything in the browser treated as a box, and each box has different properties: different pieces:
  - inner __contet box__ : the actual content in an element. Eg.: the text in a paragraph. (In Devtool is the *🔵blue area*)
  - __padding__
  - __border__
  - __margin__

<br>

- [width & height](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) : they control the inner content box's with and height (**the inner content area**).
  -  [width](https://developer.mozilla.org/en-US/docs/Web/CSS/width): set the width of an element.    
  
      By default, it sets the width of the content area, **but if box-sizing is set to border-box, it sets the width of the border area**.

      eg.:
      ###### *the content takes up the 200px space, that's the __width of the content area__*
      ```
      div {
        width: 200px;
      }
      ```

  -  [height](https://developer.mozilla.org/en-US/docs/Web/CSS/height): set the height of an element   
  
      By default, the property defines the height of the content area. **If box-sizing is set to border-box, however, it determines the height of the border area**.

      eg.:
      ###### *the content takes up the 200px by 200px space, that's the __height and width of the content area__*
      ```
      div {
        width: 200px;
        height: 200px;
      }


- [border](https://developer.mozilla.org/en-US/docs/Web/CSS/border) : __it is a border around an element__. So, it is a CSS property which sets an element's border. 

  It sets the values of **border-width**, **border-style**, and **border-color**.  

  There are dozens of border properties (thickness, style, color, etc.).

  The main <u>**border properties**</u>:   
    - [border-width](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width) : controls the thickness of the border.
      - eg.:
        ###### *setting only the __border-width__ doesn't show anything, you need to add the color and style, to see it❗️*
        ```
        #element {
          border-width: 5px;
        }
        ```
      - a 5px border-width gives 5px to each side of the box, so it makes our box 10px wider and taller. 
      
         👉 you can controll this by adding [__box-sizing: border-box__](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing#syntax) : if we have 200px width box + 10px border, it subtracts the width of our box, it becomes 190px + 5px border on each side the box, together. it is 200px.

    - [border-color](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color) :  controls the color of an element's border.
      - eg.:
        ###### *setting only the __border-width__ and __border-color__ doesn't show anything, you need to add the style, to see it❗️*
        ```
        #element {
          border-width: 5px;
          border-color: black;
        }
        ```
  
    - [border-style](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style) :  controls the line style (dashed, solid, etc.) for all four sides of an element's border.
  
      - [__different styles__](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#syntax):   
      [values *(explanation for each style on this link)*](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style#values):   
        -  none *(In the case of table cell and border collapsing, the none value has the lowest priority: if any other conflicting border is set, it will be displayed.)*    
        -  hidden *(In the case of table cell and border collapsing, the hidden value has the highest priority: if any other conflicting border is set, it won't be displayed.)*   
        -  solid,    
        -  double,    
        -  dotted,    
        -  dashed,        
        -  groove,    
        -  ridge,    
        -  inset,    
        -  outset,    
        -  dotted inset,    
        -  dashed solid : *top-bottom: dashed, left-right: solid.* 
        -  dashed double none : *top: dashed, right: double, bottom: none, left: double.*    
        -  dashed grrove none dotted : *top: dashed, right: groove, bottom: none, left: dotted.*
  
      - eg.:
        ###### *setting only the __border-width__ and __border-color__ and __border-style__, and now we can see the border.*
        ```
        #element {
          border-width: 5px;
          border-color: black;
          border-style: solid;
        }
        ```
  - [border-left](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left) & [border-right](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right) & [border-top](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top) & [border-bottom](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom) : property sets an element's left, right, top and bottom border. *(You can also set the values combined like: border-left-width, border-right-style and border-top-color.)*
    -  eg.:
        ```
        .class{
          border-top: dashed red;
        }
        ```

  - [box-sizing: border-box](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing#syntax) : **the width and height properties include the content, padding, and border**, but do not include the margin. 

      - eg.:
        ######  *you can set the width of the entire element, including the border.*
        ```
        #element {
          border-width: 5px;
          border-color: black;
          border-style: solid;
          box-sizing: border-box:
        }
        ```
  - **[border](https://developer.mozilla.org/en-US/docs/Web/CSS/border) + [shorthand](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties)** :  
    *Shorthand properties:* are CSS properties that let you set the values of multiple other CSS properties simultaneously. (In case of the border properties usually in one single line.)

    Using a shorthand property, you can write more concise (and often more readable) style sheets, saving time and energy.

    - eg.:
      ###### *width ・ style ・ color*
      ```
      #element {
        border: 4px dashed rgba(170, 50, 220, .7);
      }
      ```
  - [border-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius) : this property rounds the corners of an element's outer border edge. You can set a single radius to make circular corners, or two radius to make elliptical corners.
     - eg.:
        ###### *using [percentage](https://developer.mozilla.org/en-US/docs/Web/CSS/percentage) is a best-practice in case of border-radius*
        ```
        #element {
          border-radius: 10% 30% 50% 70%;;
        }
        ```
      - [separate properties are on this link or below](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius#constituent_properties) : 
        - [border-top-left-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-left-radius)
        - [border-top-right-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-right-radius)
        - [border-bottom-right-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-right-radius)
        - [border-bottom-left-radius](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-left-radius)
---
<br>

## [Box Model: padding](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) :    
padding property sets the padding area on all four sides of an element at once.

**Padding is the space between the actual content box and the border of an element.**

In the Chrome Devtool this is the *🟢green color* (when inspecting an element).

Use it when you want to spacing things out.

- [individual (constituent) properties](https://developer.mozilla.org/en-US/docs/Web/CSS/padding#constituent_properties):
    - [padding-left](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-left)
    - [padding-right](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-right)
    - [padding-bottom](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-bottom)
    - [padding-top](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-top)
  
- [shorthand property](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties#margin_and_padding_properties):
    - best-practice 
    - apply to __all four__ sides (at once) `padding: 10px;`
    - apply to __vertically__ & __horizontally__: `padding: 5px 10px;`
    - apply to the __top__, __horizontal__ and __bottom__ side(s): `padding: 1px 2px 3px;`
    - padding: __top right bottom left__
    - eg.:
      ###### *all four sides have separate values clockwise(top→right→bottom→left)*
      ```
      .class{
        padding: 10px 50px 30px 7px;
      }
      ```
      ###### *top-bottom 10px | left-right: 50px*
      ```
      .class{
        padding: 10px 50px;
      }
      ```
      ###### *when we don't want padding give 0 eg.: top-bottom 0 | left-right: 20px*
      ```
      .class{
        padding: 0 20px;
      }
      ```
      ###### *quite rarely used  like this, but you can give top(10px) | horizontal(20px) | bottom(30px)*
      ```
      .class{
        padding: 10px 20px 30px;
      }
      ```
---
<br>

## [Box Model: margin](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) :    
The margin CSS property sets the margin area on all four sides of an element.

Margin is the space outside of an element's border between an element and an other element(s).

So __padding is the spacing on the inside of the border__, while <u>__margin is the spacing on the outside__</u>.

In the Chrome Devtool this is the *🟠orange color* (when inspecting an element).

- **Individual properties**:
    - [margin-left](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)
    - [margin-right](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
    - [margin-bottom](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom)
    - [margin-top](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top)

<br>

- **[Shorthand properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties#margin_and_padding_properties) of [margin](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties#margin_and_padding_properties)** :
  - set all four sides at once
  - best-practice 
  - apply to __all four__ sides (at once) `margin: 10px;`
  - apply to __vertically__ & __horizontally__: `margin: 5px 10px;`
  - apply to the __top__, __horizontal__ and __bottom__ side(s): `margin: 1px 2px 3px;`
  - margin: __top right bottom left__
  - eg.:
    ###### *all four sides have separate values clockwise(top→right→bottom→left)*
    ```
    .class{
      margin: 10px 50px 30px 7px;
    }
    ```
    ###### *top-bottom 10px | left-right: 50px*
    ```
    .class{
      margin: 10px 50px;
    }
    ```
    ###### *when we don't want margin give 0 eg.: top-bottom 0 | left-right: 20px*
    ```
    .class{
      margin: 0 20px;
    }
    ```
    ###### *quite rarely used  like this, but you can give top(10px) | horizontal(20px) | bottom(30px)*
    ```
    .class{
      margin: 10px 20px 30px;
    }
    ```
<br>

- By default, your `<body>` element has some spacing, it has some margin associated with it (8px) 👉 When we start a new web page we can **set margin to be zero so that we don't get that extra space in our content**.
      
  (*Sometimes you want some margin on your site all the way across, than you can set the `<body>`'s margin to something else*)
    ```
    body  {
      margin: 0;
    }
    ```

<br>

- border-box **do NOT include margin** ❗️
 
- **the top and bottom margins have no effect on** non-replaced inline elements, such as **`<span>`** or **`<code>`**.

---
   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
