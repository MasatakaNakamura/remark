### DOM hierarchy

Below is a visualization of the DOM hierachy of a slideshow:

```markdown
html
 | - body
      | - div#slideshow                    # Slideshow container
               | - div.slide               # First slide container
               |      | - div.content      # First slide content
               | - div.slide               # Second slide
               ...
```

Every slide is represented by a separate `div.slide` that is visible when it's the current slide and hidden when not. The `div.slide` has `display: table`, and contains a `div.content` with `display: table-cell` that holds the actual slide content.

The default styles are defined using [LESS](http://lesscss.org/) in [remark.less](https://github.com/gnab/remark/blob/master/src/remark.less).

### Styling slides

You can use regular CSS to style slides. It's primarily the `div.content` element that should be styled, as its ancestors are more or less the slideshow framework itself, visually speaking.

To target a specific slide's `div.content` element, you can use the `[[name|Slide-Properties#wiki-name]]` slide property to give it a name that can be used to identify it:

```markdown
name: agenda

# Agenda
```

This will set the `div.content`'s `id` to `slide-agenda`, so that is becomes `div#slide-agenda.content`.

To target one or more `div.content` elements, you can create a CSS class and then use the `[[class|Slide-Properties#wiki-class]]` slide property to assign the class to every slide you want to target:

```markdown
class: middle, center

# Slide title
```

This will add the `middle` and `center` classes to the `div.content`, so that it becomes `div.content.middle.center`.

### Styling slide content

While the `[[name|Slide-Properties#wiki-name]]` and `[[class|Slide-Properties#wiki-class]]` slide properties  identify and apply CSS classes to entire slides, there's also [[content classes|Markdown-Extensions#wiki-content-classes]] for styling specific content of a slide:

```markdown
# Slide title

.red[Words] .yellow[in] .green[different] .blue[colors].
```

This will substitute the content of the square brackets with a `<span>` tag with the CSS class name(es) specified applied to it:

```markdown
# Slide title

<span class="red">Words</span> <span class="yellow">in</span> <span class="green">different</span> <span class="blue">colors</span.>
```

If the content of the square brackets contain a newline character, a `<div>` tag will be used instead of a `<span>` tag.