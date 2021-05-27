# [TABLES](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)
> `<table>` represents **tabular data** *(¡¡ Only use it for tabular data ‼️)*.   
<u>Tabular data</u>: information presented in a two-dimensional table comprised of **rows and columns of cells containing data**.

&nbsp;
## Elements:
- [`<table>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table) : it is the table element 

- [`<td>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td) : stand for <u>t</u>able <u>d</u>ata (cell). **It represents a single <u>*cell*</u> of a table that contains data.**

- [`<tr>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tr) : stand for <u>t</u>able <u>r</u>ow.  
**It defines a row of cells in a table.**

- [`<th>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/th) : stand for <u>t</u>able <u>h</u>eader.  
**It defines a cell as header.**  
*The exact nature of this group is defined by the scope and headers attributes.*

- [`<thead>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/thead) : stand for <u>t</u>able <u>head</u>.  
**It defines a set of rows defining the *head* of the <u>*columns*</u> of the table**  

- [`<tbody>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/tbody) : stand for <u>t</u>able <u>body</u>.  
**it encapsulates a set of table rows (`<tr>` elements), indicating that they comprise the body of the table (`<table>`).**  
*The `<tbody>` element, along with its cousins `<thead>` and `<tfoot>`, <u>provide useful semantic information</u> that can be used when rendering for either screen or printer as well as for accessibility purposes.*
&nbsp;
---
&nbsp;
## Attributes:
- [`rowspan`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attr-rowspan) : this attribute contains value that indicates for how many <u>**rows**</u> the cell extends.  
*Its default value is 1; if its value is set to 0, it extends until the end of the table section that the cell belongs to.*

- [`colspan`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/td#attr-colspan) : this attribute contains value that indicates for indicates for how many <u>**columns**</u> the cell extends..  
*Its default value is 1. Values higher than 1000 will be considered as incorrect and will be set to the default value (1).*


---

