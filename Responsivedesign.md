# [CSS - Responsive Design](https://developer.mozilla.org/en-US/docs/Glossary/Responsive_web_design)
Responsive Web Design (RWD) is a Web development concept focusing on making sites look and behave optimally on all personal computing devices, from desktop to mobile.  

So the point is to make a website that is responsive to something around the device that it's being displayed on.

<br>

## [Media Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)
media queries allow us to modify our styles depending on  praticular parameters like screen width or device type.

<br>

**@media ( [media features](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries#media_features) )**
  Media features describe specific characteristics of the user agent, output device, or environment.    

  Media feautres, are like [width](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/width) and [height](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/height), [orientation](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/orientation), etc.

<br>

💡 **[breakpoints](https://devfacts.com/media-queries-breakpoints-2021/)**    
   breakpoints are points where the website content responds according to the device width, allowing you to show the best possible layout to the user.

<br>

- **[width](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/orientation)**   
  The width CSS media feature can be used to test **the width of the viewport** (or the page box, for paged media).   

    The **[viewport](https://developer.mozilla.org/en-US/docs/Glossary/Viewport)** is not the size of the entire page or the width of the page, it's what is **currently visible**s.


  - NOT very common to use one exact size   
    eg.: for **exact width** 
    ```
      @media (width: 360px) {
        div {
          color: red;
        }
      }
    ```

  <br>

  - Commonly used: min- and max-width:  
    eg.: **Minimum width** *(basically means minimum and above the given size)*
    ```
      @media (min-width: 35rem) {
        div {
          background: yellow;
        }
      }
    ```

  <br>

  - Quite commonly used: combining min and max:   
  eg.: **`@media (min-width: 400px) and (max-width: 700px)`** *(above min size to below max size)*
    ```
      @media (min-width: 600px) and (max-width: 800px) {
      h1 {
        color: red;
      }
    }
    ```
  
  <br>

  - Very commonly used: start from 0 to max:   
  eg.: **`@media (max-width: 400px)
  `** *(above zero to below max size)*
    ```
      @media (max-width: 400px) {
      h1 {
        color: blue;
      }
    }
    ```
    *The `h1`'s color will be blue **up to** 400 pixels.*

  <br>

  - the order matters: using multiple __max__ @media queries, start with the highest number.   
      eg.: **`@media (max-width: 400px)`** *(above zero to below max size)*

    ```
        @media (max-width: 1200px) {
        h1 {
          color: blue;
        }

          @media (max-width: 400px) {
        h1 {
          color: green;
        }
      }
    ```
    *The `h1`'s color will be blue **up to** 1200 pixels and green up to 400px. If it starts withd `max-width: 400px` and ends with `max-width: 1200px` than it would be always blue, the 400px width won't work.*

  <br>

  - Other very commonly used: start without @media, and then use the `min-width` for each break point.   
        eg.: **`@media (min-width: 500px)
    `** *(starts without @media query and then changes)*
      ```
        h1 {
          color: red
        }

        @media (min-width: 500px) {
        h1 {
          color: blue;
        }
        }

        @media (min-width: 800px) {
        h1 {
          color: green;
        }
        }

        @media (min-width: 1200px) {
        h1 {
          color: yellow;
        }
      }
      ```

  <br>

 - [oriantation](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/orientation#css)     
   when landscape or portrait: @media (orientation: landscape)     
    eg.:

    ```
    @media (orientation: landscape) {
      body {
        background-color: orange;
      }
    }
    ```
    
<br>

## Breakpoints - mobile 1sr:   

- **[Mobile-first CSS Media Queries Breakpoints](https://gist.github.com/janily/8453473#file-breakpoints)**   
  
@media (min-width:320px)   →   *smartphones, portrait iPhone, portrait 480x320 phones (Android)*   
  
@media (min-width:480px)   →   *smartphones, Android phones, landscape iPhone*   
  
@media (min-width:600px)   →   *portrait tablets, portrait iPad, e-readers (Nook/Kindle), landscape 800x480 phones (Android)*   
  
@media (min-width:801px)   →   *tablet, landscape iPad, lo-res laptops ands desktops*   
  
@media (min-width:1025px)  →   *big landscape tablets, laptops, and desktops*   
  
@media (min-width:1281px)  →   *hi-res laptops and desktops*   
  
<br>
  
- **[Bootstrap breakpoints](https://getbootstrap.com/docs/5.0/layout/breakpoints/#available-breakpoints)**  
  - **max-width**
        
      @media (max-width: 575.98px) { ... }   →   *X-Small devices (portrait phones, less than 576px)*

      @media (max-width: 767.98px) { ... }   →   *Small devices (landscape phones, less than 768px)*

      @media (max-width: 991.98px) { ... }   →   *Medium devices (tablets, less than 992px)*

      @media (max-width: 1199.98px) { ... }  →   *Large devices (desktops, less than 1200px)*

      @media (max-width: 1399.98px) { ... }  →   *X-Large devices (large desktops, less than 1400px)*
  
  - **min-width**
  
      @media (min-width: 576px) { ... }   →   *X-Small devices (portrait phones, less than 576px)*

      @media (min-width: 768px) { ... }   →   *Small devices (landscape phones, less than 768px)*

      @media (min-width: 992px) { ... }   →   *Medium devices (tablets, less than 992px)*

      @media (min-width: 1200px) { ... }  →  *Large devices (desktops, less than 1200px)*

      @media (min-width: 1400px) { ... }  →   *X-Large devices (large desktops, less than 1400px)*
      
<br>      

**[Further reading❗️](https://css-tricks.com/a-complete-guide-to-css-media-queries/)**   
**[From W3C](https://www.w3.org/TR/CSS2/media.html/)**   
**[About the 'only' keyword](https://stackoverflow.com/questions/8549529/what-is-the-difference-between-screen-and-only-screen-in-media-queries/14168210#14168210)**
  
---
   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
