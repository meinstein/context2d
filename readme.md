# Context2D

> An ergonomic HTML canvas wrapper geared towards animation frames.

## Install

```
npm install context2d
```

## Usage

```html
<script type="module">
  import { Context2D } from 'context2d';

  const draw = ({ ctx, w, h, oscillate }) => {
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

##### oscillate(options)

type: `Functions`

Returns a sine wave.

#### options

type : `obect`

##### amplitude

type: `number`

The pixel distance from the top of the wave to the center.

##### frequency

type: `number`

The number of milliseconds for one waveform to complete.

##### offset

type: `number`

