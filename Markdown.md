Markdown is a plain text formatting syntax that easily lets you write next to plain text with special formatting to signalize textual elements like headings, bullet lists, links and so on. 

Have a look at the [Markdown website](http://daringfireball.net/projects/markdown/) if you're not familiar with Markdown formatting.

## Slide Separators

A line containing three dashes, represents a slide separator (not a horizontal rule, `<hr />`, like in regular Markdown). Thus, a simple Markdown text like the one below represents a slideshow with two slides:

```
# Slide 1
This is slide 1
---
# Slide 2
This is slide 2
```

### Incremental Slides

To avoid having to duplicate content if a slide is going to add to the previous one, using only two dashes to separate slides will make a slide inherit the content of the previous one:

```
# Slide

- bullet 1
--

- bullet 2
```

The above text expands into the following:

```
# Slide

- bullet 1
---

# Slide

- bullet 1
- bullet 2
``` 

Empty lines before and after the two dashes are of significance as the preceding newline character is omitted to enable adding to the last line of the previous slide. Thus, as the extra bullet point in the above example needs to go on a separate line, an extra line is added after the two dashes to force a newline. Without the extra line, the resulting text would have been `- bullet 1- bullet 2`.

## Slide Properties

Initial lines containing key-value pairs are extracted as slide properties:

```markdown
name: agenda
class: middle, center
background-image: url(remarkable.jpg)

# Agenda

The name of this slide is {{ name }}.
```

Slide properties serve multiple purposes:

 - Naming and styling slides using properties [[name|Slide-properties#wiki-name]] and [[class|Slide-properties#wiki-class]].
 - Using slides as templates using properties [[template|Slide-properties#wiki-template]] and [[layout|Slide-properties#wiki-layout]].
 - Expansion of `{{ property }}` expressions to property values

Check out the [[list of supported slide properties|Slide-Properties]].