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

### Template

The `template` property names another slide to be used as a template for the current slide:

```markdown
name: other-slide

Some content.

---
template: other-slide

Content appended to other-slide's content.
```

The final content of the current slide will then be this:

```markdown
Some content.

Content appended to other-slide's content.
```

Both template slide content and properties are prepended to the current slide, with the following exceptions:

- `name` and `layout` properties are not inherited
- `class` properties are merged, preserving class order

The `template` property may be used to (apparantly) add content to a slide incrementally, like bullet lists appearing a bullet at a time.

Using only two dashes (--) to separate slides implicitly uses the preceding slide as a template:

```markdown
# Agenda

--
1. Introduction

--
2. Markdown formatting
```

Template slides may also contain a special `{{content}}` expression to explicitly position the content of derived slides, instead of having it implicitly appended.

### Layout

The `layout` property either makes the current slide a layout slide, which is omitted from the slideshow and serves as the default template used for all subsequent slides:

```markdown
layout: true

# Section

---

## Sub section 1

---

## Sub section 2
```

Or, when set to false, reverts to using no default template.

Multiple layout slides may be defined throughout the slideshow to define a common template for a series of slides.