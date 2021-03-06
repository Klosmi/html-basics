**[How to center an element on a page (with flex)?](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#how-to-center-an-element-on-a-page-)   
[Basic navbar](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#basic-navbar-)   
[Advanced navbar](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#advanced-navbar)      
[Basic button](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#basic-button-)   
[What does mobile frist mean?](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#what-does-mobile-frist-mean-)    
[What is *max-width min-width max-length min-length / fit-content*](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#what-is-max-width-and-min-width--max-height-and-min-height-)   
[Min-content / max-content / fit-content](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#min-content--max-content--fit-content)      
[BEM Methodology (naming)](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#bem-methodology)     
[Links collection](https://github.com/Klosmi/html-basics/blob/master/CSS-center_an_element.md#links-collection-)**   

<br>

# How to center an element on a page? 🤓

###### In HTML we have a `<button>`
  ```
  <body>
    <button>Hello</button>
  </body>
  ```
###### In CSS the centering
  ```
body {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
}
  ```
<br>

# Basic navbar 🤓

###### In HTML the navbar `<nav>` constructed from 3 items: `<a>` + `<ul>` + `<a>`
  ```
<nav>
    <a href="#home">Home</a>
      <ul>

        <li>
            <a href="#Home">Career</a>
        </li>
        <li>
            <a href="#Home">About us</a>
        </li>
        <li>
            <a href="#Home">Contact</a>
        </li>

      </ul>
    <a href="#signup">Sign Up</a>
 </nav>
  ```
###### In CSS: we use flexbox and @media queries to arrange the navbar depending on screen sizes
 1. *note: a good move to give the `<ul>` and `<li>` a  `display: inline;`*.  
 2. *note: `<nav>` use flexbox's `justify-content: space-between;` → the 2 `<a>`s move both sides of the page and the 3 `<li>`s in the center.*
 3. *note: to give more space to the `<li>` elements, I can give a `flex-grow: 1` (shorthand `flex: 1`) and define its width, eg. `max-width: 50%` so it doesn't grow all the away  and take up all the space. Then give a `justify-content: space-evenly;`.*
 4. *note: below 768px screen size, the `nav` item has a `flex-direction: column`, so the items will be vertical.*
 5. *note: 💡 we used **nested flexbox**. `<nav>` parent element is a flex-container, inside the `<ul>` is the nested flex-container.*


  ```
h1 {
    font-size: 6em;
    text-align: center;
}

nav {
    font-size: 1.5em;
    display: flex;
    justify-content: space-between;
}

ul,li {
    display: inline;
    margin: 0;
    padding: 0;
}

ul {
    flex: 1;
    max-width: 50%;
    display: flex;        	   /* this is here because it is a nseted flex box! */
    justify-content: space-evenly;
}

@media (max-width: 768px) {
    h1 {
      font-size: 4em;
    }
    nav, nav ul {
        flex-direction: column;     /* items go vertical */
        align-items: center;  	  /* cross-axis because the column */
    }
  } 

  @media (max-width: 576px) {
    h1 {
      font-size: 3em;
    }
  } 
  ```
  *With some extra background-colors for the better representation...*   
  
  ![](basic-navbar-big01.png) 👉
   ![](basic-navbar-small01.png)

<br>

# Advanced navbar  
  the [code is in codepen](https://codepen.io/kevinpowell/pen/jxppmr)      
  the walk through [video is here](https://www.youtube.com/watch?v=8QKOaTYvYUA)   

<br>

# Basic button 🤓
###### In HTML we have a `<a href="#">`
  ```
<a href="#/" class="download-button">Download</a>
  ```
###### In CSS we give the style. Note: *__`display: inline-block`__*
  ```
.download-button {
	border: 1px solid blue;
	border-radius: 10px;
	color: #yellow;
	display: inline-block;  /* 💡💡💡 */
	padding: 15px 35px;
	text-decoration: none;
	margin: 25px 0;
	transition: background-color 200ms ease-in-out;
}

.download-button:hover, .download-button:focus {
 background-color: #lightblue;
}
  ```
It looks like this:  
![](basicbutton.png)

<br>

# What does [mobile frist](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Responsive/Mobile_first) mean? 📱
It means to create the mobile layout as the default first and then the larger screen sizes, which usually change to be row based instead of column based.   

[Here are some basic break-points](https://github.com/Klosmi/html-basics/blob/master/CSS-extra-properties.md#breakpoints---mobile-1sr)

<br>

# What is [max-width](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width) and [min-width](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width) / [max-height](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height) and [min-height](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height)? 📐

- **When you set the height property on an element, the element will occupy the mentioned space irrespective of the content.**    
In this case, if the content is more than the mentioned height, than it [overflows](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow).    

	With `min-height` property we can __set a minimum height for the element to occupy the space if the content in the element is less__ than the that (so if the content is less than the space). The __height__ of the element will __increase when the content increases__.

	When setting the value of `max-height`, its benefit lies in preventing the used value for height property from becoming more than the specified value for max-height. (So, it can not be bigger than what we set for max-height.) Note that the default value for max-height is none.

- **[max-width](https://ishadeed.com/article/min-max-css/#max-width)** sets the maximum width of an element. The element can not be larger than the value specified by `max-width`.    
	**[max-height](https://ishadeed.com/article/min-max-css/#max-height)** sets the maximum height of an element. The element can not be larger than the value specified by `max-height`.
 
 
	**[min-width](https://ishadeed.com/article/min-max-css/#min-width)**
	 sets the minimum width of an element. The element can not be smaller than the value specified by `min-width`.    
	**[min-height](https://ishadeed.com/article/min-max-css/#min-height)**
	 sets the minimum height of an element. The element can not be smaller than the value specified by `min-height`.   

 
 - **[Use Cases For Min And Max Properties](https://ishadeed.com/article/min-max-css/#use-cases-for-min-and-max-properties)**.  
	- example for **'min-width'** with tags-list   
		- eg. `min-width: 100px;` *even if the tag is empty it should not be smaller than 100px.*
	![](https://ishadeed.com/assets/min-max/use-case-1.png).  
	- example for **`max-width`** with tags-list 
		- eg. `max-width: 250px;` *if the text is longer than the tag, it will be truncated.*
	![](max-width.png)

<br>

# **[min-content](https://developer.mozilla.org/en-US/docs/Web/CSS/min-content) / [max-content](https://developer.mozilla.org/en-US/docs/Web/CSS/max-content) / [fit-content](https://developer.mozilla.org/en-US/docs/Web/CSS/fit-content)**

- **[`min-content`](https://devstory.net/12557/les-mots-cles-min-content-max-content-fit-content-stretch-en-css#a54855642)** : represents the intrinsic minimum width of the content.     
	- In other words: the [min-content](https://css-tricks.com/almanac/properties/w/width/#min-content) value is the smallest measure that would fit around its content if all soft wrap opportunities within the box were taken.
	- In case of text content, the content will take all soft-wrapping opportunities, becoming as small as the longest word.     

	- You can use it for background sizes for cards when you don't know how muach content will the card contain.   
	
	- In [horizontal orientation](https://devstory.net/12557/les-mots-cles-min-content-max-content-fit-content-stretch-en-css#a54855642), the min-content keyword represents the __minimum value of the width__ without reversing the content of the element horizontally.   
	[<img src="https://s1.o7planning.com/fr/12557/images/55028199.png">]()   
	
	- In vertical orientation, the min-content keyword represents the minimum value of the height without reversing the content of the element vertically.   
	
	  [<img src="https://s1.o7planning.com/fr/12557/images/55028280.png">]() 

<br>

- **[`max-content`](https://devstory.net/12557/les-mots-cles-min-content-max-content-fit-content-stretch-en-css#a54855640)** : represents the intrinsic maximum width or height of the content.    
	- The content will not wrap at all even if it causes overflows in case of text content.   
	- In other words: the [max-content](https://css-tricks.com/almanac/properties/w/width/#max-content) property refers to the narrowest measure a box could take while fitting around its content – if no soft wrap opportunities within the element were taken.
	- Suppose you make the parent element infinite in width (or very large) and the current element the minimum height. Then the __max-content value is the minimum width__.
	- eg.:    
	  ```
	  width: max-content;
	  min-width: max-content;
	  max-width: max-content;
	  ```
	 
	 
	 [<img src="https://s1.o7planning.com/fr/12557/images/54870779.gif">]()  
	
	- Suppose you make the parent element infinite in height (or very large) and the current element minimum in width. The max-content value is then the minimum height. 
	- eg.:   
	```
	height: max-content;
	min-height: max-content;
	max-height: max-content;
	```   
	
	
       [<img src="https://s1.o7planning.com/fr/12557/images/55010821.gif">]()  
       
<br>

- **[`fit-content`](https://devstory.net/12557/les-mots-cles-min-content-max-content-fit-content-stretch-en-css#a54855707)** : the box will use the available space, but never more than max-content. 
	- It is like stretching, behvaes as fit-content(stretch).
	- When used as laid out box size for `width`, `height`, `min-width`, `min-height`, `max-width` and `max-height` the __maximum and minimum sizes__ apply to the content size.    
	- If the writing mode is (writing mode) horizontally. An element with a CSS width {width: fit-content} means:
		1. If the parent element can provide the current element with a width value greater than max-content, then `fit-content = max-content`.   
		2. If the parent element cannot provide the current element with a width value greater than min-content, then `fit-content = min-content`.   
		3. If the parent element can only provide the current element with a width value in the range (min-content, max-content) , then the current element will have a width "fitted" to the parent element.   
		[source](https://devstory.net/12557/les-mots-cles-min-content-max-content-fit-content-stretch-en-css#a54855707)
	- eg.:   
 	  ```
	  .element  {
  	     width: fit-content;
	  }
	  ```
	  
	  [<img src="https://s1.o7planning.com/fr/12557/images/55053249.gif">]()  
	  
	
	- for vertically is the same as horizontally.
	eg.:
	Vertical writing mode.
	```
	.element {
    	   writing-mode: vertical-rl | vertical-lr;
    	   width: fit-content;
	}
	```
	
	[<img src="https://s1.o7planning.com/fr/12557/images/55060805.gif">]()
	  	 

	- an example from [css-tricks]():   
		The HTML
		```
		<ul>
		  <li>Home</li>
		  <li>News</li>
		  <li>About</li>
		  <li>Contact</li>
		</ul>
		```   
		The CSS
		```
		ul {
		  background: deepskyblue;
		  padding: 1em;
		  width: fit-content;
		  margin: 1em auto;
		}

		li {
		  display: inline-block;
		  background: red;
		  padding: .5em;
		}
		```
	result   
	 ![](fit-content.png)
	 

<br>

<br>

# [BEM Methodology](http://getbem.com/naming/)


# Links collection 🔗

**[reset CSS](https://meyerweb.com/eric/tools/css/reset/) 👉 it is to normalize how browser styles work across different browsers.**.  
**[pricing table html css code](https://codepen.io/travisw/pen/EvbKwd)** 👉 a nice example of responsivity.  
**[min-max hegith-width css](https://ishadeed.com/article/min-max-css/)** 👉 detailed article about the min and max css properties

---

   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
