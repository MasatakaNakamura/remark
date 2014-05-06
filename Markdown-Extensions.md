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

 - Naming and styling slides using properties [[name|Slide-properties#wiki-name]] and [[class|Slide-properties#wiki-class]].
 - Using slides as templates using properties [[template|Slide-properties#wiki-template]] and [[layout|Slide-properties#wiki-layout]].
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

Github Flavored Markdown ([GFM](http://github.github.com/github-flavored-markdown/)) fenced code blocks are the preferred way of creating code blocks, easily letting you specify the highlighting language:

<pre>
Code:

```ruby
def add(a,b)
  a + b
end
```</pre>

A default highlighting language may be configured using the [[highlightLanguage|Configuration-Options#wiki-highlighting]] configuration option. Specifying a language on a code block will override the default.

Lines prefixed with `*` will automatically get highlighted with a yellow background, which can be handy for
bringing attention to specific parts of code snippets, i.e.:

<pre>
Implicit return statment:

```ruby
def add(a,b)
*  a + b
end

Notice how there is no return statement.
```</pre>