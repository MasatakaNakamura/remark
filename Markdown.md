Markdown is a plain text formatting syntax that easily lets you write next to plain text with special formatting to signalize textual elements like headings, bullet lists, links and so on. 

Have a look at the [Markdown website](http://daringfireball.net/projects/markdown/) if you're not familiar with Markdown formatting.

## Slide Separators

All regular Markdown formatting rules apply with only a single exception:

* A line containing three dashes constitutes a new slide (not a horizontal rule, `<hr />`)

Thus, a simple Markdown text like the one below represents a slideshow with two slides:

```
# Slide 1
This is slide 1

---

# Slide 2
This is slide 2
```

### Incremental Slides

To split parts of a slide into steps, use `--`. For instance

```
# Slide

- bullet 1

--

- bullet 2
```

will show 

### Slide
- bullet 1

on one slide, and 

### Slide 
- bullet 1
- bullet 2

on the next slide.