# [Semantic Markup](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantics_in_html) 🚀 *(meaningful markup)*
- *semantic: **relating to meaning***. So it answers to *what purpose or role that HTML element have?*  
- *relates to the content that the html contains*
- useful: 
  - [web crawlers](https://en.wikipedia.org/wiki/Web_crawler) can immediately read it
  - [accessibelity](https://www.w3.org/WAI/fundamentals/accessibility-intro/), eg. people who're useing screenreaders
- [stripe.com](https://stripe.com/) a good example (*use the devtool to inspect*) 

## <u>elements</u>:

- [`<main>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main) : 
  - **The main content of the page!** *The dominant content of the document.*  
  - It should **exclude any content of the page which will be repeated on the page**. So sidebars, navigation links, copyright information, site logos, and search forms shouldn't be included.
  - `<main>` doesn't affect the DOM's concept *(unlike `<body>` or `<h1>` and such)* of the structure of the page. It's strictly informative.

- [`<nav>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav) : 
  - **represent anything on the page that provides navigation links**. 
  - fill the `<nav>` with links (breadcrumbs, navbars).  
   💡 *you can have several navs in a page.*
  - can be links to other part on the same page
  - can be links to completely different resources

- [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section) :  
  -  very generic
  -  it represents a *generic* **standalone** section of a document, which **doesn't have a more specific semantic element to represent it**.  
  `<section>` is still far better than a `<div>`, where a `<div>` is just a generic container *(you can  use a `<div>` for anything)*. 
  - a `<section>` supposed to be a section of content, a standalone *section* of your website.
  - it's one option dividing up your markup
  - if you would give a border or other CSS, maybe use a `<div>` rather than `<section>`.
- [`<article>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article) :
  - `<article>` element represents a self-contained composition in a document.
  - you can have multiple articles and sub-articles on a page
  - `<article>` **supposed to be any self-contained composition**
  - **anything that should be independently distributable or reusable**
  - just an other element to group content together:
    - there should be a heading *(`<h1>` `<h2>`)* that explaines what the `<article>` is about. (eg. a film review, which can have inside a bunch of sections and sub-articles)

- [`<aside>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/aside) :
  - it is something that is indirectly related to the document, not essential. *(like: sidebars, call-out boxes)*
  - represents a portion of a document whose content is only indirectly related to the document's main content.

- [`<header>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header) : 
  - any sort of  introductory content, often include a group of **introductory** and/or navigational content  
  *It can include more than just a navbar.* It can inlcude several `<section>`
  - **the header of the page**
- [`<footer>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer) :
  -  represents a footer for its nearest sectioning content or sectioning root element.
  - often include several `<div>` and `<nav>` that are **nested** just like the `<header>` does.

> 💡 You can have an `<article>` element with a header and a footer inside of it. So you can have more than one footer on a  page.
- [`<time>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time) : 
  - it is an **inline element**, you wrap it around
  - represents a specific period in time.
  - it may include the datetime attribute to translate dates into **machine-readable format**, allowing for **better search engine results** or custom features such as reminders.

- [`<figure>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figure)
  - represents a self-contained piece of content, with and with an optional caption. 
  - the caption is specified using the [`<figcaption>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/figcaption) element. 
  - it calls out a special meaning, usually an illustration, a diagram. Something you want to call attention to and may often have a caption alongside it.

- [`<abbr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr)
  - represents an abbreviation or acronym
  - the optional title attribute can provide an expansion or description for the abbreviation. If present, title must contain this full description and nothing else.
  - The **title attribute has a specific semantic meaning when used with the `<abbr>`** element: **it must contain a full human-readable description** or expansion of the abbreviation. *This text is often presented by browsers as a **tooltip** when the mouse cursor is hovered over the element.*

- [`<data>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/data)
  - links a given piece of content with a machine-readable translation.
  - if the content is **time- or date-related**, the [`<time>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time) element must be used.

### There is a lot of flexibility, not super rigid. The point is the general intent of the semantics of each of these elements. 

---

[👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
