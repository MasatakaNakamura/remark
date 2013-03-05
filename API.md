Work in progress.

### Configuration

The following code block shows the API functions available for configuring the slideshow:

```javascript
// Set slideshow ratio to 16:9
remark.config({ratio: '16:9'});
```

Read more about the alternative ways to [[configure|Configuration]] a slideshow and the [[configuration options|Configuration-Options]] available.

### Navigation

The following code block shows the API functions available for navigating the slideshow:

```javascript
// Navigate to the beginning and end of the slideshow
remark.gotoFirstSlide();
remark.gotoLastSlide();

// Navigate a single slide forward and backward
remark.gotoNextSlide();
remark.gotoPreviousSlide();

// Navigate to a specific slide, either by slide number or name
remark.gotoSlide(5);
remark.gotoSlide('agenda');
```

Read more about [[naming slides|Slide-Properties#name]].

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