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

#### `ready`

The `ready` event is emitted when the slideshow creation is complete, at which point all Markdown content has been converted into slides.

```javascript
remark.on('ready', function () { ... });
```

#### `slidein`

The `slidein` event is emitted when the slide is coming into view and is supplied with two arguments: slide element and slide index (0-based).

#### `slideout`

The `slideout` event is emitted when the slide is coming out of the view and is supplied with two arguments: slide element and slide index (0-based).