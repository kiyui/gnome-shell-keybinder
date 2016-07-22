# gnome-shell-keybinder

GNOME Shell extension utility for binding keys on-the-fly.

GNOME Shell can only apply new configuration entries from a compiled schema
file. When applying the keybinds, a schema is generated and compiled with the
`glib-compile-schemas` executable, then loaded and applied.

## Building

This module uses ES6 classes, exports and template literals. To use in an
extension, use a transpiler like Babel and a module bundler like Webpack.

## Usage

```javascript
import Keybinder from 'gnome-shell-keybinder';

const keybinder = new Keybinder('my-extension');
keybinder.add('hello-world', '<Super>j', () => print('Hello World!'));

function enable() {
  keybinder.apply();
}

function disable() {
  keybinder.unapply();
}
```

## Documentation

For now, the JSDoc annotations in the source.
