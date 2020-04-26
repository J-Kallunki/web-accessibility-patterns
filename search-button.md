# Search Button

🖥️[Example](search-button-example.html)

## JavaScript

On the click of the button you need to change
- label<sup>1</sup> and input<sup>2</sup> remove or add hidden-attribute
- Set focus to input<sup>2</sup> after screenreader has the new rendered layout (example 400ms)

### VanillaJS queryselectors
- <sup>1</sup>'[for="search-input-id"]'
- <sup>2</sup>'[id="search-input-id"]'

``` html
<form action="." role="search" class="search" data-search-form="search-input-id">
  <label for="search-input-id" class="visually-hidden" hidden>Search</label>
  <input type="search" id="search-input-id" class="search__input" hidden>
  <button type="button" aria-label="Search" aria-expanded="false" class="search__button">
    <svg
      viewBox="0 0 20 20"
      width=".75em"
      height=".75em"
      xmlns="http://www.w3.org/2000/svg"
      class="search__icon"
      aria-hidden="true"
      focusable="false"
    >
      <path d="M19 17l-5.15-5.15a7 7 0 1 0-2 2L17 19zM3.5 8A4.5 4.5 0 1 1 8 12.5 4.5 4.5 0 0 1 3.5 8z"/>
    </svg>
    <span>Search</span>
  </button>
</form>
```

```css
.search {
  /* Container styles */
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  width: 100%;
  max-width: 400px;
}
.search__input {
  -moz-appearance: none;
  -webkit-appearance: none;
  appearance: none;
  /* Input styles */
  flex: 1;
  align-self: stretch;
  margin-right: 12px;
}
.search__button {
  /* Button styles */
  margin-left: auto;
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  border: none;
  font: inherit;
  color: inherit;
  background-color: transparent;
  cursor: pointer;
}
.visually-hidden { 
  position: absolute !important;
  height: 1px; 
  width: 1px;
  overflow: hidden;
  clip: rect(1px 1px 1px 1px); /* IE6, IE7 */
  clip: rect(1px, 1px, 1px, 1px);
  white-space: nowrap; /* added line */
}
```
