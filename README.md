# amator

Tiny animation library.

# usage

Work in progress for better documentation.

``` js
var animate = require('amator')
var from = { x: 0 }
var to = { x: 42 }
// This will animate from.x from 0 to 42 in 400ms, using cubic bezier easing
// function (same effect as default CSS `ease` function)
animate(from, to)

// More options
var animation = animate(from, to, {
  duration: 800, // change duration from 400ms to 800ms
  easing: 'linear', // Use linear easing
  step: function(object) {
    // print value on each animation frame
    console.log(object.x)
  },
  done: function() {
    console.log('All done')
  }
})

// if for some reason you don't need animation to continue, you can cancel it:
animation.cancel()
```

# license

MIT
