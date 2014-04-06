The following configuration options are currently available:

### <a name="general">General</a>

```javascript
var slideshow = remark.create({
  // Set the slideshow display ratio
  // Default: '4:3'
  // Alternatives: '16:9', ...
  ratio: '4:3',

  // Navigation options
  navigation: {
    // Enable or disable navigating using scroll
    // Default: true
    // Alternatives: false
    scroll: true,

    // Enable or disable navigation using touch
    // Default: true
    // Alternatives: false
    touch: true
  }
}); 
```

### <a name="highlighting">Highlighting</a>

Highlighting is done using [Highlight.js](http://softwaremaniacs.org/soft/highlight/en/). Check out the demo/test page for the [available styles and languages](http://softwaremaniacs.org/media/soft/highlight/test.html). 

Please note that **only the styles and languages listed below** are embedded in the standard remark build.

* `highlightLanguage`
  * Set default language for syntax highlighting
  * Default: - (no highlighting)
  * Alternatives: `javascript`, `ruby`, `python`, `bash`, `java`, `php`, `perl`, `cpp`, `objectivec`, `cs`, `sql`, `xml`, `css`, `scala`, `coffeescript`, `lisp`, `clojure`, `http`.
  * To disable automatic highlighting, use `no-highlight`
<br /><br />
* `highlightStyle`
  * Set highlight style for syntax highlighting
  * Default: `default`
  * Alternatives: `arta`, `ascetic`, `dark`, `default`, `far`, `github`, `googlecode`, `idea`, `ir_black`, `magula`, `monokai`, `rainbow`, `solarized_dark`, `solarized_light`, `sunburst`, `tomorrow`, `tomorrow-night-blue`, `tomorrow-night-bright`, `tomorrow-night`, `tomorrow-night-eighties`, `vs`, `zenburn`.