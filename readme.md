# Context2D

> An ergonomic HTML canvas wrapper geared towards animating frames.

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
