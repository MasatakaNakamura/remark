Several Markdown extensions have been implemented to help out with slide layout and formatting.

### Slide Classes
A line containing one or more dotted CSS class names is extracted, and the specified classes are applied to the current slide:

    .center.middle

    # Slide with content centered in both dimensions

Resulting HTML extract:

    <div id="slideshow">
      <div class="slide">
        <div class="content center middle">
          <h1>Slide with content centered in both dimensions</h1>

Slide classes available include `left`, `center`, `right`, `top`, `middle` and `bottom`.

### Content Classes

Any occurences of one or more dotted CSS class names followed by square brackets are replaced with the contents of the brackets with the specified classes applied:

    .footnote[.red.bold[*] At least browsers try their best]

Resulting HTML extract:

    <span class="footnote">
      <span class="red bold">*</span> At least browsers try their best
    </span>

Content classes available include `left`, `center` and `right`.

### Language Classes

If the language automatically detected for a code block is incorrect, you may specify the language to use by adding a dotted language class on the first line of code:

    Code:

        .ruby
        def add(a, b)
          a + b
        end

Inline code is not automatically highlighted unless [configured to](Configuration), and must be supplied a language class to be highlighted:

    Inline code: `.ruby a = 5`

To disable syntax highlighting, use the class `no-highlight`.