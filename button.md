# Button without styles

🖥️[Example](button-example.html)

- Do not use onClick on divs
- Use button for clickable actions
- `<a>` can be used to navigate

``` html
<button class="button--without-styles">I am a button</button>
```

```css
.button--without-styles {
  padding: 0;
  border: none;
  font: inherit;
  color: inherit;
  background-color: transparent;
  cursor: pointer;
  /* Button withouts styles styles*/
  position: relative;
  padding: 0 .25em;
}
.button--without-styles:active {
  /* Down clicked styles */
  transform: translateY(1px);
}
.button--without-styles:after {
  /* Custom styles */
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
.button--without-styles::-moz-focus-inner {
  border: none;
}
.button--without-styles:focus {
  /* Focus styles */
  outline: none;
  box-shadow: -2px 2px orange;
}
.button--without-styles:focus:after {
  /* Custom styles */
  box-shadow: 2px -2px orange;
}
.button--without-styles:hover {
  /* Hover styles */
  box-shadow: -2px 2px currentColor;
}
```
