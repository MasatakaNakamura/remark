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