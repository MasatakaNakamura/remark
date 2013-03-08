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

#### `class` slide property

Besides writing your own CSS targeting the above DOM hierarchy in a general fashion, CSS classes can be assigned on a per-slide basis using the `[[class|Slide-Properties#wiki-class]]` slide property:

```markdown
class: middle, center

# Slide title
```

This will extend the `div.content` to `div.content.middle.center`.