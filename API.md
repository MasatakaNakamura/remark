### <a name="general">Creation</a>

To create a slideshow, you use the 'create` function as follows:

```javascript
var slideshow = remark.create();
```

Optionally, you can pass in a number of configuration options:

```javascript
var slideshow = remark.create({
  highlightLanguage: 'javascript',
  highlightStyle: 'monokai',
  ...
});
```

Check out the list of [[configuration options|Configuration-Options]].

### Navigation

After creating your slideshow, a number of functions are available for navigating:

```javascript
// Navigate to the beginning and end of the slideshow
slideshow.gotoFirstSlide();
slideshow.gotoLastSlide();

// Navigate a single slide forward and backward
slideshow.gotoNextSlide();
slideshow.gotoPreviousSlide();

// Navigate to a specific slide, either by slide number or name
slideshow.gotoSlide(5);
slideshow.gotoSlide('agenda');
```

Read more about [[naming slides|Slide-Properties#wiki-name]].

### Events

(TODO)