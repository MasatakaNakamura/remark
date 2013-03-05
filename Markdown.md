Markdown is a plain text formatting syntax that easily lets you write next to plain text with special formatting to signalize textual elements like headings, bullet lists, links and so on.

Have a look at the [Markdown website]((http://daringfireball.net/projects/markdown/) if you're not familiar with Markdown formatting.

### Markdown in remark

Basically, remark transforms a Markdown-formatted chunk of text into individual slides in a slideshow. What differentiates remark from similar tools, is that it does all of its work using nothing but JavaScript, running locally in your browser.

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