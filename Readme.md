
# rework-mixins

  Rework CSS mixins

## Example

  Using all mixing:

```js
var rework = require('rework');
var mixins = require('rework-mixins');

var css = rework('some css here')
  .use(rework.mixin(mixins))
  .toString();
```

  Or specific mixing:

```js
var rework = require('rework');
var mixins = require('rework-mixins');

var css = rework('some css here')
  .use(rework.mixin({
    overflow: mixins.overflow
  }))
  .toString();
```

## overflow: ellipsis

  `mixins.overflow`:

```css
h1 {
  overflow: ellipsis
}
```

yields:

```css
h1 {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis
}
```

## border-radius

  `mixins.border-radius`:

```css
button {
  border-radius: top 5px bottom 10px
}
```

yields:

```css
button {
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
}
```

## License 

  MIT
