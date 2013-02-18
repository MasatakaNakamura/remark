Configuration is done either by setting configuration options directly in the `<script>` tag or by calling the `remark.config` method.

### Setting options in the `<script>` tag

This method is convenient if you don't need any other JavaScript in your slideshow, as it saves you the trouble of creating that extra `<script>` tag:

    <script src="remark.js" language="text/javascript">
      { "option": "value" }
    </script>

Please notice that the configuration option-value object must be valid JSON, i.e. quotation marks must be used for keys and value strings instead of single quotes.

### Setting options by calling `remark.config` method

This method uses ordinary JavaScript by calling the `remark.config` [API](API) method, accepting the same configuration option-value object mentioned above:

    remark.config({ "option": "value" });

If you've already got some JavaScript in your slideshow, this is the preferred way.

## Options

The following configuration options are currently available:

### <a name="highlighting">Highlighting</a>

Highlighting is done using [Highlight.js](http://softwaremaniacs.org/soft/highlight/en/). Check out the demo/test page for the [available styles and languages](http://softwaremaniacs.org/media/soft/highlight/test.html). 

Please note that only the styles and languages listed below are embedded in the standard remark build.

* `highlightInline`
  * Highlight inline code blocks automatically
  * Default: `false`
  * Alternatives: `true`, `false`

* `highlightLanguage`
  * Set default language for syntax highlighting
  * Default: - (automatically determined)
  * Alternatives: `javascript`, `ruby`, `python`, `bash`, `java`, `php`, `perl`, `cpp`, `objectivec`, `cs`, `sql`, `xml`, `css`, `scala`, `coffeescript`, `lisp`, `clojure`.

* `highlightStyle`
  * Set highlight style for syntax highlighting
  * Default: `default`
  * Alternatives: `arta`, `ascetic`, `dark`, `default`, `far`, `github`, `googlecode`, `idea`, `ir_black`, `magula`, `monokai`, `rainbow`, `solarized_dark`, `solarized_light`, `sunburst`, `tomorrow`, `tomorrow-night-blue`, `tomorrow-night-bright`, `tomorrow-night`, `tomorrow-night-eighties`, `vs`, `zenburn`.