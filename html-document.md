# HTML document and landmarks

🖥️[Example](html-document-example.html)

- [https://www.w3.org/TR/wai-aria-practices/examples/landmarks/resources.html](https://www.w3.org/TR/wai-aria-practices/examples/landmarks/resources.html)

``` html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <!-- Enable zoom. -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <!-- First page desciption then website name -->
    <title>Page title — Website name</title>
  </head>
  <body>
    <!-- Skip link -->
    <a href="#main" id="skip-link">Skip to main content</a>
    <!-- Roles for banner, navigation and main are well supported via HTML5 semantics (header, nav, main) -->
    <nav class="navigation">
      <!-- Navigation should use list and items should be link not buttons -->
      <ul class="navigation__list">
        <!-- If visual only items: <li class="navigation__item" aria-hidden="true">img etc.</li> -->
        <li class="navigation__item">
          <a href="/" aria-current="page" class="navigation__link"
            >Current page</a
          >
        </li>
        <li class="navigation__item">
          <a href="/" class="navigation__link">Put</a>
        </li>
        <li class="navigation__item">
          <a href="/" class="navigation__link">navigation</a>
        </li>
        <li class="navigation__item to-right">
          <a href="/" class="navigation__link">links</a>
        </li>
        <li class="navigation__item">
          <a href="/" class="navigation__link">here</a>
        </li>
        <!-- You may implement search here etc. (remember focus trapping) -->
      </ul>
    </nav>
    <header>
      <p>Put company logo, etc. here.</p>
    </header>
    <main tabindex="-1" id="main">
      <p>Put main content here.</p>
    </main>
    <footer role="contentinfo">
      <p>Put copyright, etc. here.</p>
    </footer>
  </body>
</html>
```

```css
header,
nav,
main,
footer,
article,
section,
aside {
  display: block;
}
#skip-link {
  position: absolute;
  top: -999vw;
  left: 0;
}
#skip-link:focus {
  top: 0;
}
.navigation {
  /* Nav styles */
  background-color: hotpink;
}
.navigation__list {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  margin: 0;
  padding: 0;
  list-style: none;
}
.navigation__item {
  display: block;
  position: relative;
  /* Nav item styles */
}
.navigation__item.to-right {
  margin-left: auto;
}
.navigation__link {
  display: block;
  /* Nav link styles */
  padding: 1em;
}
.navigation__link[aria-current='page'] {
  /* Nav link current page styles */
  background-color: #0f0;
}
.navigation__link:hover {
  /* Nav link hover styles */
  background-color: #fff;
}
```
