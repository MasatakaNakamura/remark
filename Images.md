### Regular images

Regular images are inserted using normal Markdown [image syntax](http://daringfireball.net/projects/markdown/syntax#img), and are treated like regular content that can be places inside [[content classes|Markdown-extensions#wiki-content-classes]], i.e. to be [[aligned|Text-alignment#wiki-block]]:

```markdown
# Images

![Default-aligned image](image.jpg)

.right[![Right-aligned image](image.jpg)]
```

### Background images

The [[background-image|Slide-properties#wiki-background-image]] slide property lets you set the [background-image](http://www.w3schools.com/cssref/pr_background-image.asp) CSS property for the slide:

```markdown
background-image: url(image.jpg)

# Slide with background image
```

The background image will by default be centered both horizontally and vertically on the slide, and scaled down to fit if it is larger than the slide.