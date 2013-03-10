Several Markdown extensions have been implemented to help out with slide layout and formatting.

### Slide Properties
Initial lines containing key-value pairs are extracted as slide properties:

```markdown
name: agenda
class: middle, center
background-image: url(remarkable.jpg)

# Agenda

The name of this slide is {{ name }}.
```

Slide properties serve multiple purposes:

 - Naming and styling slides using properties `[[name|Slide-properties#wiki-name]]` and `[[class|Slide-properties#wiki-class]]`
 - Using slides as templates using properties `[[template|Slide-properties#wiki-template]]` and `[[layout|Slide-properties#wiki-layout]]`
 - Expansion of `{{ property }}` expressions to property values

Check out the [[list of supported slide properties|Slide-Properties]].

### <a name="content-classes">Content Classes</a>

Any occurences of one or more dotted CSS class names followed by square brackets are replaced with the contents of the brackets with the specified classes applied:

    .footnote[.red.bold[*] Important footnote]

Resulting HTML extract:

    <span class="footnote">
      <span class="red bold">*</span> Important footnote
    </span>

Content classes available include `left`, `center` and `right`.

### Syntax Highlighting

Both indented code blocks and Github Flavored Markdown ([GFM](http://github.github.com/github-flavored-markdown/)) fenced code blocks are supported, optionally overriding the automatically detected language:

    Code:

        .ruby
        def add(a, b)
          a + b
        end

<pre>
Code:

```ruby
def add(a,b)
  a + b
end
```</pre>


Inline code is not automatically highlighted (unless configured using the `[[highlightInline|Configuration-Options#wiki-highlighting]]` configuration option) and must be supplied a language to be highlighted:

    Inline code: `.ruby a = 5`

The default language for code may be configured using the `[[highlightLanguage|Configuration-Options#wiki-highlighting]]` configuration option. To disable syntax highlighting, use the class `no-highlight`.