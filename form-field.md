# Form field

🖥️[Example](form-field-example.html)

- Add more divs for styling

``` html
<fieldset class="fieldset">
  <legend class="legend">Fieldset legend</legend>
  <label>
    <input type="checkbox">
    Checkbox
  </label>
</fieldset>
```

```css
.fieldset {
  min-width: 0;
  margin: 0 0 1rem;
  padding: 0;
  border: 0 solid transparent;
}
.legend {
  box-sizing: border-box;
  display: table;
  width: 100%;
  max-width: 100%;
  margin: 0 0 .5rem;
  padding: 0;
  font-weight: 600;
  line-height: inherit;
  white-space: normal;
  color: inherit;
}
```
