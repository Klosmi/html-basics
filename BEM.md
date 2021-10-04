__[BEM - naming methodology](http://getbem.com/naming/)__

- The BEM approach ensures that using proper naming will prepare you for the changes in design of the website.   

-  BEM is an abbreviation of the key elements of the methodology — Block, Element and Modifier:   

    - `.blockname`

    - `.blockname__element`

    - `.blockname__element--modifier`
   
 - eg.: a Card:
    - Block →   `class="card"`
    - Element → `class="card__picture"`
    - Element → `class="card__title"`
    - Element → `class="card__description"`
    - Element → `class="card__button"`
    - Modifier → `class="card__button  card__button--active"` 
  
  - eg.:
    the card in HTML
    ```
    <div class="card">
      <span class="card__img"></span>
        <div class="card__content">
          <ul class="card__list">
            <li class="card__item card__item--active">Adobe XD</li>
            <li class="card__item">Figma</li class="card__item">
            <li class="card__item">Sketch</li class="card__item">
          </ul>
            <p class="card__desc">Lorem ipsum, dolor sit amet consectetur adipisicing elit</p>
            <a class="card__link" href="#">Visit the link</a>
       </div>
    </div>
    ```
    The SCSS [in short]   
    💡 note that using the SASS **`&`**
    ```
    .card {
        padding: 0 5em;

        &__img {
          display: block;
          height: 100px;
          width: 100%;
          background: #e0466b;
        }

        &__content {
            padding: 1.5em;
            background: white;
        }

        &__list {
            list-style-type: none;
            margin: 0;
            padding: 0;
        }

        &__item {
            padding: .3em .5em;
            margin-right: .5em;
            background: rgb(230, 230, 230);
            border-radius: .3em;
            font-size: .85em;

            &--active {
                background: #d4d4d4;
                font-weight: bold;
            }
        }

        &__link {
            background: #2c8973;
            color: white;
            text-decoration: none;
            padding: .5em 1em;
            border-radius: .5em;
            display: inline-block;
            margin-top: .5em;

            &:hover {
                background: #267764;
            }
        }
    }    
    ```
    [source](https://codepen.io/designcourse/pen/KKwjKNE)
    
  #[OOCSS - Object Oriented CSS](https://github.com/stubbornella/oocss/wiki)
  
  ## Useful Links
  __[Methodology Documentation](https://en.bem.info/methodology/)__
---
   [👈 go back](https://github.com/Klosmi/html-basics#html-and-css--basics)
