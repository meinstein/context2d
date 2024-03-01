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
Default: Root element's `offsetWidth`

The canvas width.

##### height

Type: `number`
Default: Root element's `offsetHeight`

The canvas height.

##### rootElement

Type: `string` | `HTMLElement`
Default: `document.body`

The element or element ID to which the canvas will be appended.

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

##### from

type: `number`

The from pixels that the oscillate fn will return. Default is -1.

##### to

type: `number`

The to pixels that the oscillate fn will return. Default is -1.

##### speed

type: `number`

Speed is in Hz, so 1 is one cycle per second.

##### offset

type: `number`

