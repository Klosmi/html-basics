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
    display: flex;      // this is here because it is a nseted flex box!
    justify-content: space-evenly;
}

@media (max-width: 768px) {
    h1 {
      font-size: 4em;
    }
    nav, nav ul {
        flex-direction: column;     // items go vertical
        align-items: center;  //cross-axis because the column
    }
  } 

  @media (max-width: 576px) {
    h1 {
      font-size: 3em;
    }
  } 
  ```
  
<br>

# What is [mobile frist](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Responsive/Mobile_first)? 📱
It means to create the mobile layout as the default first and then the larger screen sizes usually they change to be eow based instead of column based.

<br>

# Links collection 🔗

[reset CSS](https://meyerweb.com/eric/tools/css/reset/) 👉 it is to normalize how browser styles work across different browsers.


---

   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
