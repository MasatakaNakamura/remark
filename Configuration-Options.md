The following configuration options are currently available:

### <a name="general">General</a>

* `ratio`
  * Set the slideshow display ratio.
  * Default: `4:3`
  * Alternatives: `16:9`, ...

### <a name="highlighting">Highlighting</a>

Highlighting is done using [Highlight.js](http://softwaremaniacs.org/soft/highlight/en/). Check out the demo/test page for the [available styles and languages](http://softwaremaniacs.org/media/soft/highlight/test.html). 

Please note that only the styles and languages listed below are embedded in the standard remark build.

* `highlightInline`
  * Highlight inline code blocks automatically
  * Default: `false`
  * Alternatives: `true`, `false`
<br /><br />
* `highlightLanguage`
  * Set default language for syntax highlighting
  * Default: - (automatically determined)
  * Alternatives: `javascript`, `ruby`, `python`, `bash`, `java`, `php`, `perl`, `cpp`, `objectivec`, `cs`, `sql`, `xml`, `css`, `scala`, `coffeescript`, `lisp`, `clojure`, `http`.
<br /><br />
* `highlightStyle`
  * Set highlight style for syntax highlighting
  * Default: `default`
  * Alternatives: `arta`, `ascetic`, `dark`, `default`, `far`, `github`, `googlecode`, `idea`, `ir_black`, `magula`, `monokai`, `rainbow`, `solarized_dark`, `solarized_light`, `sunburst`, `tomorrow`, `tomorrow-night-blue`, `tomorrow-night-bright`, `tomorrow-night`, `tomorrow-night-eighties`, `vs`, `zenburn`.