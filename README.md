# progress-control

[node-progress](https://github.com/tj/node-progress) wrapper to control bar from keyboard

## Install

```
$ npm install progress-control --save
```

## Usage

```javascript
var value = 0.5;

var bar = require('progress-control')('Use up/down arrows [:bar]', { total: 10 }, {
  'up': function() {
    value = Math.min(Math.round((value + 0.1) * 10) / 10, 1);
    bar.update(value);
  },
  'down': function() {
    value = Math.max(Math.round((value - 0.1) * 10) / 10, 0);
    bar.update(value);
  }
});

bar.update(value);
```

## License

MIT © [ewnd9](http://ewnd9.com)
