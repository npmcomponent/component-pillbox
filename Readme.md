*This repository is a mirror of the [component](http://component.io) module [component/pillbox](http://github.com/component/pillbox). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-pillbox`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# Pillbox

  Pillbox input component, a fork of [tomerdmnt/tag-input](https://github.com/tomerdmnt/tag-input).

  ![Tags Input](http://f.cl.ly/items/0S262y000s1y441m0Z1l/Screen%20Shot%202012-10-12%20at%205.25.16%20PM.png)

## Install

```
$ component install component/pillbox
```

## Example

``` javascript
var Pillbox = require('pillbox');

var input = Pillbox(document.getElementById('tags'))

input.on('add', function(tag){
  console.log(tag + ' added');
});

input.on('remove', function(tag){
  console.log(tag + ' removed');
});
```

## Events

 - `add` (tag)
 - `remove` (tag)

## API

### Pillbox(input, options)

  Initialize with the given `input` element and `options`. Available options include:

  * `lowercase`: all added tags get converted to lowercase.
  * `allowSpace`: allow spaces in tags.
  * `space`: inverse of allowSpace (backwards support).

### Pillbox#add(tag)

  Add `tag` string if it does not already exist.

### Pillbox#remove(tag)

  Remove `tag` string if it exists.

### Pillbox#values([array])

  Set / Get the tags.

# License

  MIT
