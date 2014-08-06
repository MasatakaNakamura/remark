## Alignment

### Whole-slide text alignment

The [[class|Markdown#class]] slide property lets you assign CSS classes to a slide, and remark comes with a set of classes for setting horizontal and vertical text alignment:

```markdown
class: middle, center

# Centered vertically and horizontally
```

The classes available for _vertically_ aligning text are:
* `top` (default)
* `middle`
* `bottom`

The classes available for _horizontally_ aligning text are:

* `left` (default)
* `center`
* `right`

### Text block alignment

[[Content classes|Markdown#content-classes]] let you assign CSS classes to a text block, and remark comes with a set of classes for setting horizontal text alignment:

```markdown
# Text alignment

.left[Left-aligned text]

.center[Centered text]

.right[Right-aligned text]
```

The classes available for _horizontally_ aligning text are:

* `left` (default)
* `center`
* `right`

## Images

### Regular images

Regular images are inserted using normal Markdown [image syntax](http://daringfireball.net/projects/markdown/syntax#img), and are treated like regular content that can be placed inside [[content classes|Markdown#content-classes]], e.g. to be [[aligned|Formatting#text-block-alignment]]:

```markdown
# Images

![Default-aligned image](image.jpg)

.right[![Right-aligned image](image.jpg)]
```

### Background images

The [[background-image|Markdown#background-image]] slide property lets you set the [background-image](http://www.w3schools.com/cssref/pr_background-image.asp) CSS property for the slide:

```markdown
background-image: url(image.jpg)

# Slide with background image
```

The background image will by default be centered both horizontally and vertically on the slide, and scaled down to fit if it is larger than the slide.