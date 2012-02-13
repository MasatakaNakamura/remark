Configuration is done either by setting configuration options directly in the `<script>` tag or by calling the `remark.config` method.

### Setting options in the `<script>` tag

This method is convenient if you don't need any other JavaScript in your slideshow, as it saves you the trouble of creating that extra `<script>` tag:

    <script src="remark.js" language="text/javascript">
      { "option": "value" }
    </script>

Please notice that the configuration option-value object must be valid JSON, i.e. quotation marks must be used for keys and value strings instead of single quotes.

### Setting options by calling `remark.config` method

This method uses ordinary JavaScript by calling the `remark.config` method, accepting the same configuration option-value object mentioned above:

    remark.config({ "option": "value" });

If you've already got some JavaScript in your slideshow, this is the preferred way.

## Options

The following configuration options are currently available:

### Highlighting

Highlighting is done using [Highlight.js](http://softwaremaniacs.org/soft/highlight/en/). Check out the demo/test page for the [available styles and languages](http://softwaremaniacs.org/media/soft/highlight/test.html).

* `highlightInline`
  * Highlight inline code blocks automatically
  * Default: `false`
  * Alternatives: `true`, `false`

* `highlightLanguage`
  * Set default language for syntax highlighting
  * Default: -
  * Alternatives: `python`, `profile`, `ruby`, `perl`, `php`, `scala`, `go`, `xml`, `django`, `css`, `javascript`, `vbscript`, `lua`, `delphi`, `java`, `cpp`, `objectivec`, `vala`, `cs`, `rsl`, `rib`, `mel`, `sql`, `smalltalk`, `lisp`, `ini`, `apache`, `nginx`, `diff`, `dos`, `bash`, `cmake`, `axapta`, `1c`, `avrasm`, `vhdl`, `parser3`, `tex`, `haskell`, `erlang`, `erlang_repl`

* `highlightStyle`
  * Set highlight style for syntax highlighting
  * Default: `default`
  * Alternatives: `arta`, `ascetic`, `dark`, `default`, `far`, `github`, `idea`, `ir_black`, `magula`, `solarized_dark`, `solarized_light`, `sunburst`, `vs`, `zenburn`.