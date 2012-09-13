Several Markdown extensions have been implemented to help out with slide layout and formatting.

### Slide Properties
Initial lines containing key-value pairs are extracted as slide properties:

```markdown
name: agenda
class: middle, center

# Agenda

The name of this slide is {{ name }}.
```

Slide properties serve multiple purposes:

 - Naming and styling slides using properties `name` and `class`
 - Using slides as templates using properties `template` and `layout`
 - Expansion of `{{ property }}` expressions to property values

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

Inline code is not automatically highlighted (unless [configured to](Configuration) by setting the `highlightInline` configuration option) and must be supplied a language class to be highlighted:

    Inline code: `.ruby a = 5`

The default language for code may be [configured](Configuration) using the `highlightLanguage` configuration option. To disable syntax highlighting, use the class `no-highlight`.