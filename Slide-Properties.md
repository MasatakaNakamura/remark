Several slide properties have been implemented:

### Name

The `name` property accepts a name used to identify the current slide:

```markdown
name: agenda

# Agenda
```

A Slide name may be used to:

 - Link a slide directly using URL fragment, i.e. `slideshow.html#agenda`

 - Identify slide DOM element, either for scripting or styling purposes:

    ```html
    <div id="slideshow">
      <div class="slide">
        <div id="slide-agenda" class="content">
          <h1>Agenda</h1>
    ```

 - Reference slide when used as `template` for some other slide

### Class

The `class` property accepts a comma-separated list of class names, which are applied to the current slide:

```markdown
class: center, middle

# Slide with content centered in both dimensions
```

Resulting HTML extract:

```html
<div id="slideshow">
  <div class="slide">
    <div class="content center middle">
      <h1>Slide with content centered in both dimensions</h1>
```

Built-in slide classes include `left`, `center`, `right`, `top`, `middle` and `bottom`.