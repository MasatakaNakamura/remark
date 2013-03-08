Work in progress.

### DOM hierarchy

Below is a visualization of the DOM hierachy of a slideshow:

```markdown
html
 | - body
      | - div#slideshow                    # Slideshow container
               | - div.slide               # First slide
               |      | - div.content      # First slide content
               | - div.slide               # Second slide
               ...
```

Every slide is represented by a separate `div.slide` that is visible when it's the current slide and hidden when not. The `div.slide` has `display: table`, and contains a `div.content` with `display: table-cell` that holds the actual slide content.

The default styles are defined using [LESS](http://lesscss.org/) in [remark.less](https://github.com/gnab/remark/blob/master/src/remark.less).

### Applying styles

You can use regular CSS to style slides. It's primarily the `div.content` element that should be styled, as its ancestors are more or less the slideshow framework itself, visually speaking.

To target a specific slide's `div.content` element, you can use the `[[name|Slide-Properties#wiki-name]]` slide property to give it a name that can be used to identify it:

```markdown
name: agenda

# Agenda
```

This will set the `div.content`'s `id` to `slide-agenda`, so that is becomes `div#slide-agenda.content`.

To target one or more `div.content` elements, you create a CSS class and then use use the `[[class|Slide-Properties#wiki-class]]` slide property to assign the class to a slide:

```markdown
class: middle, center

# Slide title
```

This will add the `middle` and `center` classes to the `div.content`, so that it becomes `div.content.middle.center`.