# Accordion

🖥️[Example](accordion-example.html)

## JavaScript

On the click of the button you need to change
- button<sup>1</sup> aria-expanded -boolean attribute
- div<sup>2</sup> remove or add hidden-attribute

### VanillaJS queryselectors
- <sup>1</sup>'[data-accordion="accordion-content-id"] [aria-expanded]'
- <sup>2</sup>'[id="accordion-content-id"]'

``` html
<div class="accordion" data-accordion="accordion-content-id">
  <h2> 
    <button aria-controls="accordion-content-id" aria-expanded="false">Title</button>
  </h2>
  <div class="accordion__content" id="accordion-content-id" hidden>
    <p>Hideable content.</p>
  </div>
</div>
```

```css
.accordion [aria-controls] {
  display: inline-block;
  text-decoration: none;
  background: transparent;
  color: #000;
  font: inherit;
  text-align: left;
  cursor: pointer;
  -webkit-appearance: none;
  -moz-appearance: none;
  border: 1px solid #000;
}
.accordion [aria-controls]:focus {
  /* Focus styles */
}
```
