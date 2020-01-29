# Windows High Contrast-mode

```css
@media screen and (-ms-high-contrast: white-on-black) {
  /* Style tweaks for the High Contrast Black theme */
}
@media screen and (-ms-high-contrast: black-on-white) {
  /* Style tweaks for the High Contrast White theme */
}
@media screen and (-ms-high-contrast: active) {
  /* Style tweaks High Contrast Mode, Any Theme */
  .svg-styles {
    stroke: windowText;
  }
  .card {
    background-color: window;
  }
  .navigation__link {
    color: highlight;
  }
}
```

## Windows High Contrast properties to CSS Color names
- Text: `windowText`
- Hyperlinks: <a>
- Selected Text: `highlightText` & `highlight`
- Button Text: `buttonFace`
- Background: `window`