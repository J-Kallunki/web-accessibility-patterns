# Checkbox

- Supports touch screen readers
  - by placing transparent input-element with the SVG-icon

``` html
<label for="checkbox-id" class="checkbox">
  <input type="checkbox" id="checkbox-id" class="checkbox__input" />
  <svg
    viewBox="0 0 100 100"
    width=".75em"
    height=".75em"
    xmlns="http://www.w3.org/2000/svg"
    class="checkbox__icon"
  >
    <circle cx="50%" cy="50%" r="49" fill="#000" class="checked" />
    <circle
      cx="50%"
      cy="50%"
      r="42"
      stroke="#000"
      fill="transparent"
      stroke-width="12"
      class="unchecked"
    />
    />
  </svg>
  <span>Checkbox label</span>
</label>
```

```css
.checkbox {
  position: relative;
}
/* Same placement as SVG and set to transparent */
.checkbox .checkbox__input {
  position: absolute;
  /* SVG-icon size */
  width: 0.75em;
  height: 0.75em;
  opacity: 0;
}
.checkbox .checkbox__input:focus + .checkbox__icon {
  outline: orangered auto 5px;
}
.checkbox .checkbox__input + .checkbox__icon .unchecked {
  opacity: 1;
}
.checkbox .checkbox__input + .checkbox__icon .checked {
  opacity: 0;
}
.checkbox .checkbox__input:checked + .checkbox__icon .unchecked {
  opacity: 0;
}
.checkbox .checkbox__input:checked + .checkbox__icon .checked {
  opacity: 1;
}
```

<label for="checkbox-id" class="checkbox">
  <input type="checkbox" id="checkbox-id" class="checkbox__input" />
  <svg
    viewBox="0 0 100 100"
    width=".75em"
    height=".75em"
    xmlns="http://www.w3.org/2000/svg"
    class="checkbox__icon"
  >
    <circle cx="50%" cy="50%" r="49" fill="#000" class="checked" />
    <circle
      cx="50%"
      cy="50%"
      r="42"
      stroke="#000"
      fill="transparent"
      stroke-width="12"
      class="unchecked"
    />
    />
  </svg>
  <span>Checkbox label</span>
</label>