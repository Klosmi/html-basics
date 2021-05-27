# [FORMS](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)
- a `<form>` element represents a document section containing interactive controls for submitting information.   

- the `<form>` element itself is a shell or container that doesn't have any visual impact.

- we fill `<form>` with inputs, checkboxes, buttons, etc. and we groupd them together with the `<form>`.

- the `<from>` element represents a document section containing  interactive controls for submitting information.

- when you submit a `<from>` an HTTP request will be sent.  
We control where the request goes to with the *`action`* attribute, and we control which type of HTTP method should be used with the *`method`* attribute. 

 - <u>**`<form>` attributes**</u>:

    - [`action`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form#attr-action) attribute  :specifies **where** the form data should be sent.

    - [`method`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form#attr-method) attribute : specifies which HTTP method should be used. (GET and POST)

&nbsp;
## The (form) `input elements`:
- [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) :
  - is used to create a variety of different form controls.
  - there are 20+ possible types of inputs (like date pickers, color picker, password input, text input, checkboxes, etc.)
  - `<input>` attributes:
    - the [<u>***type***</u>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-type) attribute 🚀 is the most important attribute, it is where the magic happens:
    changing type dramatically alters the input's behaviour and appearance.  
    - [placeholder](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefplaceholder) attribute specifies the placeholder text for an `<input>`. It is the text you that shows up before you type anything (while it is empty).
 
 &nbsp;

- [`<label>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label) : represents a caption for an item in a user interface. 
  - really important in terms of **accessibility**!!! A  screen reader will read out the label when the user is focused on the form input.

  - To associate the `<label>` with an `<input>` element, you need to give the `<input>` an `id` attribute. The `<label>` needs a `for` attribute whose value is the same as the input's `id`.

  - Alternatively, you can nest the `<input>` directly inside the `<label>`, in which case the <u>**for**</u> and id attributes are not needed because the association is implicit.

     - <u>**`<label>` attributes**</u>:
        - [**`for`**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label#attr-for) : basically it answers the question of what the `<label>` is for?  
        - The first element in the document with an `id` matching the value of the `for` attribute, that is the labeled control for this label element.  
        - **If you nest the `<input>` inside of the label, you don't need to use the *for* attribute (and the *id)*!.** However it is a less common standard (styling is less easy).

        - **`id`** : <u>**is in the `<input>`!!!**</u> the value (what name we give to the *id*) should be the same of the **for** attribute's value. So we set the *id*'s value to the *for*'s value.💡  
 
 &nbsp;

- **`<button>`** 👉 [<button>Button</button>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button)  
A `<button>` represents a clickable button, used to submit forms or anywhere in a document for accessible, standard button functionality.   
Also, `<button>` not necesseraly has to be inside of a form (eg. a "sign up" button, links).

  - `<button>` has a closing tag `</button>`.
  - the text inside of the `<button></button>` is used to label the button.
  - a `<button>` **inside in a form** has a default behaviour: to submit.

  - <u>**`<button>` attributes**</u>:
    - [**type**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button#attr-type) :`<button type="button">`*Button*`</button>` 👉 <button type="button">Button</button>  
   **The `type` over write** the default `submit` attribute when the `<button>` is in a form!!! 
    - *default `<button type="submit">Submit</button>`*  
    (Well, you don't even have to write the `type="submit"` if you want to keep it default.)

    - an other way to make a sumbit button:
        **`<input type="submit">`** **BUT** you can only change the text if you use another `<input>` attribute `value`.
    - [**value**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#htmlattrdefvalue) : The input control's value.  
    When specified in the HTML, this is the initial value, and from than on it can be altered or retrieved at any time using JavaScript to access it.

    - [name](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button#attr-name) : The name of the button, submitted as a pair with the button’s `value` as part of the form data.  
    `name` is a way of referring to the `value` when the data is sent to the server. The server look for that 
    `name`. *(If the name is `name="user"`), than the server looks for the name "user"*.   
      - `name` is just a *"name"* (ususally very short, like `name="q"`)  
      -  The `<form>` will be labeled under the `name` attribute when it is sent to the server.

  - [**checkbox**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox) : `<input type="checkbox">` 👉 <input type="checkbox"> <input type="checkbox"> <input type="checkbox">   
  A check box allowing single values to be selected/deselected.	
    - you can specify if the checkbox is `checked` or  not.

  - [**radiobutton**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/radio) : `<input type="radio">` 👉 <input type="radio" name="radio"> <input type="radio" name="radio">   
  The `radiobutton` allowing only one single value to be selected out of multiple choices with the same `name` value.  
  In  a group of `radiobuttons` you can only select one (so they are connected).
    - They are associated by the **same `name`**, so they are pointing to the same thing.

    - `value` attribute selects what to send through when the form was submitted. So which `radiobutton` was selected and sent when clicking on the submit button.

- [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select) : 
<select name="pets" id="pet-select">
    <option value="">--Please choose an option--</option>
    <option value="dog">Dog</option>
    <option value="cat">Cat</option>
    <option value="hamster">Cute little hamster</option>
</select>  

The [`<select>`] element represents a control that provides a menu of options.  
It is essentially a dropdown menu.  
  - Two elements working together: `<select>` and the `<option>` elements. The `<select>` is the parent it groups together a bunch of `options`.  

  - `<option value="hamster">Cute little hamster</option>` the value attribute will be sent through when it is submitted *(here the `value="hamster"`)*.
    - it can be preselected with the attribute `selected`.
    
---
**<u>[many other `<input>` elements can be found here.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)
So here's a little selection, which might be useful: </u>**

- [**range**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range) : `<input type="range">` 👉 
<input type="range">  - we can control the "min" and "max" values (eg. `min="0" max="100"`)

- [**number**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number) : <input type="number" min="10" max="1000"  placeholder="num"> 👉   `<input type="number">` elements of type number are used to let the user enter a number.

- [**textarea**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea) : <textarea id="story" name="story" rows="1" cols="40"> This is a textarea...
</textarea> 👉 `<textarea>`  
  - It is a multiline text input. 
  - **❗️It is NOT an input element❗️**


