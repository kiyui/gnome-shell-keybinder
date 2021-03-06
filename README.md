# gnome-shell-keybinder

Forked from https://github.com/rliang/gnome-shell-keybinder, which is no longer available.

GNOME Shell extension utility for binding keys on-the-fly.

GNOME Shell can only apply new configuration entries from a compiled schema
file. When applying the keybinds, a schema is generated and compiled with the
`glib-compile-schemas` executable, then loaded and applied.

## Building

This module's source uses ES6 classes and modules, to build it into an ES5 UMD
module run `npm run build`.

## Usage

To use in an extension, include the UMD module or use a module bundler like
Webpack.

```javascript
import Keybinder from 'gnome-shell-keybinder';

const keybinder = new Keybinder();
keybinder.add('hello-world', '<Super>j', () => print('Hello World!'));

export function enable() {
  keybinder.enable();
}

export function disable() {
  keybinder.disable();
}
```

## Documentation

For now, the JSDoc annotations in the source.
