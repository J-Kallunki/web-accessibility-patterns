# Radiogroup with CSS

🖥️[Example](radiogroup-css-example.html)

- Support for older browsers not guaranteed. For wider support customize [SVG checkbox version](checkbox-svg.html)

``` html
<fieldset class="radiogroup">
  <legend class="radiogroup__legend">Radiogroup legend</legend>
  <label class="radiogroup__item">
    <input name="group-name" type="radio">
    Default
  </label>
  <label class="radiogroup__item">
    <input name="group-name" type="radio" checked>
    Checked
  </label>
  <label class="radiogroup__item">
    <input name="group-name" type="radio" disabled>
    Disabled
  </label>
</fieldset>
```

```css
.radiogroup {
  min-width: 0;
  margin: 0 0 1rem;
  padding: 0;
  border: 0 solid transparent;
}
.radiogroup__legend {
  box-sizing: border-box;
  color: inherit;
  display: table;
  max-width: 100%;
  white-space: normal;
  /* Legend styles */
  width: 100%;
  margin: 0 0 .5rem;
  font-weight: 600;
  line-height: inherit;
}
.radiogroup__item {
  /* Radiogroup item styles */
  display: flex;
  justify-content: flex-start;
  align-items: center;
  margin: 0 0 .5em 0;
  padding: 0;
}
.radiogroup [type="radio"] {
  position: relative;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  vertical-align: middle;
  box-sizing: inherit;
  /* Item selector styles */
  width: 1.25em;
  height: 1.25em;
  margin: 0 0.5em 0 0;
  color: orange;
  background-color: lightgoldenrodyellow;
  border-radius: 50%;
  border: 2px solid orange;
  cursor: pointer;
}
.radiogroup [type="radio"]:before {
  content: '';
  position: absolute;
  left: 50%;
  top: 50%;
  box-sizing: inherit;
  /* Item selector styles */
  height: 5px;
  width: 5px;
  border-radius: 50%;
  opacity: 0;
  pointer-events: none;
  background-color: white;
  transform: translate(-50%, -50%);
}
.radiogroup [type="radio"]:checked {
  /* Item checked styles */
  background-color: orange;
  color: lightgoldenrodyellow;
  border-color: orange;
}
.radiogroup [type="radio"]:checked:before {
  opacity: 1;
}
.radiogroup [type="radio"]:disabled {
  opacity: .25;
  border-color: darkgoldenrod;
  cursor: not-allowed;
  pointer-events: none;
}
.radiogroup [type="radio"]:focus {
  /* Focus styles */
  outline: orangered auto 2px;
}
```
