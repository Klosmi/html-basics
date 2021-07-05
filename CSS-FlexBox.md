# [CSS - Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)
- Flexbix is a one-dimensional layout method for laying out items in rows or columns.

- it is a **series of properties** that we use to layout items on our page in a box of content: a way of **distributing space** inside a container.

- Flexbox allows us to distribute space dynamically across elements of an unknown size, hence the term *flex*.

<br>


[Axes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox#the_two_axes_of_flexbox) :     
 there are 2 axes:  the **main axis** and the **cross axis**.   
 
   - **main axis:**  defined by the **flex-direction property**     
      By default it goes from left to right. 
      
   - **cross axis:** runs perpendicular to the main axis. 
    
   - Everything we do with flexbox refers back to the *main and cross axes*.

<br>

**Flexbox properties:**   
1. **`display: flex;`** :    
it defines a flex container.   
The container can be inline or block depending on the given value. It enables a flex context for all its direct children.  
All other *flexbox* properties rely on the `display: flex` property.

<br>

2. **[flex-direction](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)** :   
  *(the main axis is defined by this property)*   
  this CSS property sets how flex items are placed in the flex container defining the main axis and the direction (normal or reversed).    
  - 4 directions: **row ・ row-reverse ・ column ・ column-reverse**

  -  `flex-direction: row;` **left-to-right** horizontally! (this is by default)

  - `flex-direction: row-reverse;` **right-to-left** horizontally!

  - `flex-direction: column;` **top-to-bottom** vertically!

  - `flex-direction: column-reverse;` **bottom-to-top** vertically!

    - eg.: We have some `div`s, with flexbox we arrange these `div`s horizontally from top to bottom.
      ```
      #container {
        display: flex;
        flex-direction: column;
      } 

      #container div{
        width: 50px;
        height: 50px;
      }
      ```
  
  <br>
  
 3. **[justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)** :  
    this poperty determines how the actual elements (the content) is **distributed across the main axis**.

    (So, it defines how the browser distributes space between and around content items along the main-axis of a flex container, and the inline axis of a grid container.) 

    Main [values](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content#values) : 

    - `justify-content: flex-start;` the default.   
      If the **main axis goes from left to right**, the **start is on the left**. 

    - `justify-content: flex-end;`   
       It takes the content and move it to the **end of the main axis**.    

       The items are packed flush to each other toward the edge of the alignment container depending on the flex container's main-end side.

    - `justify-content: center;`   
       It centers our content along the main axis. 
         
    - `justify-content: space-between;`   
        Space between takes all of the extra space and distribute it between the elements, but not on the outside edges.   
        So it gives space between elements, but not between the element and the container.


    - `justify-content: space-around;` 
       It gives each element the same amount of space around it.  

       **So the items are evenly distributed within the alignment container along the main axis.** The spacing between each pair of adjacent items is the same. The empty space before the first and after the last item equals half of the space between each pair of adjacent items.

       It looks a bit **uneven** between the container and the item, and item between item.


    - `justify-content: space-evenly;`   
      it spaces evenly and space evenly just ensures that the **space is even between every element and between the elements and the container**.
         
      So the **items are evenly distributed within the alignment container along the main axis.** The spacing between each pair of adjacent items, the main-start edge and the first item, and the main-end edge and the last item, are all exactly the same. 


      - eg.: We have some `div`s, with flexbox, lets say we arrange these `div`s vertically from top to bottom with even space between the `div` items and the container.
        ```
          #container {
            display: flex;
            flex-direction: column;
            justify-content: space-evenly;
          } 

          #container div{
            width: 50px;
            height: 50px;
          }
        ```
        <br>

4. **[flex-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap)** :   
  this property sets whether flex items are forced onto one line or can wrap onto multiple lines. If wrapping is allowed, it sets the direction that lines are stacked.

   So it determines whether the elements are going to wrap along the main axis onto a new line if it's horizontal or a new column if it's a vertical main axis.

  - **`flex-wrap: nowrap;`** : 
    doesn't wrap (the default)

  - **`flex-wrap: wrap;`** : 
    The flex items break into multiple lines.    
    The cross-start is either equivalent to start or before depending flex-direction value and the cross-end is the opposite of the specified cross-start.
    
  - **`flex-wrap: wrap-reverse;`** :
    Behaves the same as wrap but cross-start and cross-end are permuted, rearranged (if `wrap` goes top-to-bottom, `wrap-reverse` goes bottom-to-top).

    - eg.:
      We have let say 6 `div`s, with flexbox *(1, 2, 3, 4, 5, 6)*. The `div`s are top-to-bottom, but because the `container`'s height is only 500px, the 6 `div`s' heights are all squished down to fit in the `container`.
      But, using `felx-wrap: wrap;` the `div`s go to top-to-bottom in a new column, as many columns are necessary and they are not squished.
      ![](flex-wrap.png)

        ```
        #container {
          hegiht: 500px;
          display: flex;
          flex-direction: column;
          justify-content: space-evenly;
          flex-wrap: wrap;
        } 

        #container div{
          width: 300px;
          height: 300px;
        }
        ``` 
