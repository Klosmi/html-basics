# How to center an element on a page 🤓

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
    height: 100vh;
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


  ```
body {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
}
  ```
<br>
---
   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
