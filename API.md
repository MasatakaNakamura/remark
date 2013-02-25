Work in progress.

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
