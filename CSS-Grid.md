# [Grid](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids) :
CSS Grid Layout is a 2-dimensional layout system. It lets you lay content out in __rows__ and __columns__.

So a grid is a collection of horizontal(**row**) and vertical(**column**) lines creating a pattern against which we can line up our design elements.

- similar to Flex, but while Flex-box is 1 dimensional, Grid is 2 dimensional.

In other words: grid items (*contents*) are distributed along the *main axis* and *cross axis*.([source](https://www.freecodecamp.org/news/css-grid-tutorial-with-cheatsheet/)).

- __the model__:
  - __explicit grid__:    
    a grid layout you explicitly call.   
    So the explicit grid is the one that you create using grid-template-columns or grid-template-rows.

  - __implicit grid__:    
    a grid layout that is automatically created (rows and columns) for extra elements that don't fit into the explicit grid.     
    So, the implicit grid is created when content is placed outside of the explicit grid.

    By default, tracks created in the implicit grid are __auto__

 <br>

- __grid-container__ (the parent) properties:

  - __[defining a grid](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids#defining_a_grid)__:   
    __`display: grid;`__   
    Call it on the parent element (just like in Flex-box).
    All direct children of grid containers become grid items.   
    By declaring `display: grid;`, it gives a one column grid, so your items will continue to display one below the other as they do in normal flow. 

  <br>

  - __[grid-template-rows](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows)__ :   
  defines the line names and track sizing functions of the grid rows.

    - a row track is created for each value specified for grid-template-rows. Track size values can be any non-negative, length value (px, %, em, etc.)  

   - eg.:
    *`<div>` 1 and 2 have fixed heights of 50px and 100px. Because only 2 row tracks (`<div>`)s were defined: 80px 150px, heights of `<div>` 3 & 4 & 5 are defined by the contents of each.*   
    HTML
    ```
    <div id="parent">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
    </div>
    ```
    CSS
    ```
    #parent {
    display: grid;
    grid-template-rows: 80px 150px;
    }
    ```
    ![](starting-grid-01.jpg)


  - __[grid-template-columns](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns)__ :   
  defines the line names and track sizing functions of the grid columns.   
  So when you call this, you declare (explicitly) how many columns you want. (And implicitly it gives you rows)

  - units:
    - px, pt, em, rem, %, fr (fraction unit), auto

    - a __fr__ (fraction unit) diveds the free space in the grid into equally distribute the space.   
    Margins and paddings are automatically built in.  
    __fr__ units are flexible

  - 💡 __fr__ distributes available space, not all space. So, if one of your tracks has something large inside it, there will be less free space to share.

    - eg.:   
    *I have a `<div id="parent">` and 5 children `<div>`s.*   
      HTML
    ```
    <div id="parent">
      <div>1</div>
      <div>2</div>
      <div>3</div>
      <div>4</div>
      <div>5</div>
    </div>
    ```
    CSS
    ```
    #parent {
      display: grid;
      grid-template-columns: 2fr 1fr;   //first col. takes twices as much space as the second col.
    }
    ```
   ![](grid-template-columns-FR.jpg)


- __grid items__ (children element) properties:

- __[the minmax() function](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids#the_minmax_function)__ :    
   it lets us set a minimum and maximum size for a track.
    `minmax(minimum-value, maximum-value)`

  eg.:
  * first row track: `<div>` 1 is set to have a minimum height of 100px, but its maximum size of auto will allow the row track to grow the content taller than 100px.*   
  CSS
    ```
    #parent {
      display: grid;
      grid-template-rows: minmax(100px, auto);
      grid-template-columns: 1fr 1fr;
    }
    ```
  ![](minmax-rows01.jpg)
 
  * first column track `<div>`1 & `<div>`4 has a minimum size of auto, but its maximum size of 20% will prevent it from getting no wider than 20% of the grid container width.*   
  CSS
    ```
    #parent {
      display: grid;
      grid-template-columns: minmax(auto, 20%) 1fr 1fr;
    }
    ```
  ![](minmax-columns01.jpg)

<br>

- [Repeating Grid Tracks](https://developer.mozilla.org/en-US/docs/Web/CSS/repeat()) :   
define __repeating grid tracks__ using the `repeat()` notation. This is useful for grids with items with equal sizes or many items.   
This function can be used in the CSS Grid properties __grid-template-columns__ and __grid-template-rows__.

  - `repeat()` accepts 2 arguments:   
  The first represents the __number of times the defined tracks should repeat__.   
  The second is the __track definition__.  
  - eg.:

    ```
    grid-template-rows: repeat(3, 100px);
    ```
  ![]](grid-template-rows_ repeat.jpg)  
    ```
    grid-template-columns: repeat(3, 1fr);
  ![](grid-template-columns_repeat)  ```

- __vocabulary__:
  - __grid lines__:
    - __row grid line__ : horizontal row line
    - __column grid line__ : vertical column line
  - __grid tracks__:
    - the area between two lines (can be between rows and can be between columns)
  - __grid cells__ (or grid items):
    - individual cells in the grid (has 4 sides made by 2 rows and 2 columns)

<br>

