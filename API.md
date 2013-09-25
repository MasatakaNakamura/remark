This page documents the current API, which may still change radically until a version 1.0 is reached.

## Slideshow

#### <a name="general">Creation</a>

To create a slideshow, you use the `remark.create` function as follows:

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

This should all go in a `<script>` block __in the end__ of your `<body>` tag.

Check out the list of [[configuration options|Configuration-Options]].

#### Navigation

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

// Suspend/resume remarks process of keyboard and touch events for custom builds, etc...
slideshow.pause();
slideshow.resume();
```

Read more about [[naming slides|Slide-Properties#wiki-name]].

#### Events

Upon navigation (and later, other stuff as well), events are emitted from the slideshow:

```javascript
slideshow.on('showSlide', function (slide) {
  // Slide is the slide being navigated to
});

slideshow.on('hideSlide', function (slide) {
  // Slide is the slide being navigated away from
});
```

Alternatives include `beforeShowSlide`, `afterShowSlide`, `beforeHideSlide`, and `afterHideSlide` which trigger before or after changes are actually made to the DOM.  Please see below for more information on the `slide` parameter.

## Slide

A slide has the following format:

```javascript
{
  // Function returning the slides number (1..N, where N is the number of slides)
  getSlideNo: function (),

  // The notes for the slide
  notes: <string>,

  // The slide properties extracted from the Markdown
  properties: {
    class: "center, middle",
    name: "agenda",
    ...
  },
  
  // The Markdown representing the slide
  source: <string>
}
```