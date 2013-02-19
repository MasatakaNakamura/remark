As requested in issue "[MathJax support](https://github.com/gnab/remark/issues/25)", [joshbode](https://github.com/joshbode) supplied the following [gist](https://gist.github.com/joshbode/4065848), utilizing the remark [ready event](API):

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Title</title>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
    <script type="text/javascript" src="https://github.com/downloads/gnab/remark/remark-0.4.2.min.js"></script>
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js"></script>
    <script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML&delayStartupUntil=configured">
      remark.on('ready', function () {
        MathJax.Hub.Config({
          tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre']
          }
        });
        MathJax.Hub.Queue(function() {
          $(MathJax.Hub.getAllJax()).map(function(index, elem) {
            return(elem.SourceElement());
          }).parent().addClass('has-jax');
        });
        MathJax.Hub.Configured();
      });
    </script>
    <style type="text/css" media="screen">
      code.has-jax {font: inherit; font-size: 100%; background: inherit; border: inherit;}
    </style>
  </head>
  <body>
    <textarea id="source">
 
class: center, middle
 
# `\(\LaTeX{}\)` in remark
 
---
 
# Display and Inline
 
1. This is an inline integral: `\(\int_a^bf(x)dx\)`
2. More `\(x={a \over b}\)` formulae.
 
Display formula:
    $$e^{i\pi} + 1 = 0$$
 
    </textarea>
    <div id="slideshow" />
  </body>
</html>
```