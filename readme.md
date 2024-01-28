# Context2D

> An ergonomic HTML canvas wrapper geared towards animation frames.

## Usage

```html
<script type="module">
  import { Context2D } from 'https://unpkg.com/context2d';

  const draw = ({ ctx, w, h, oscillate, memoize }) => {
    ...
  }

  const context2d = new Context2D();

  context2d.draw(draw);
</script>
```

## API

### Context2D(options?)
Returns an instance of Context2D, which has one public method: `draw` (see below)

#### options

Type: `object`

##### width

Type: `number`
Default: `window.innerWidth`

The canvas width.

##### height

Type: `number`
Default: `window.innerHeight`

The canvas height.

##### rootElement

Type: `HTMLElement`
Default: `document.body`

The element to which the canvas will be appended.

### context2d.draw(param => void)

#### param

Type: `object`

##### ctx

type: `CanvasRenderingContext2D`

The canvas context.

##### w

type: `number`

The canvas width.

##### h

type: `number`

The canvas height.

##### memoize(fn)

type: `Function`

Memoizes the provided fn. Re-runs fn when window is resized.

##### oscillate(oscillateOptions)

type: `Function`

Returns a sine wave.

#### oscillateOptions

type : `obect`

##### min

type: `number`

The min pixels that the oscillate fn will return. Default is -1.

##### max

type: `number`

The max pixels that the oscillate fn will return. Default is -1.

##### frequency

type: `number`

The number of milliseconds for one waveform to complete.

##### offset

type: `number`

