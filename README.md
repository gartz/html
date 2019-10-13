# require-html

A [RequireJS](http://requirejs.org)/AMD loader plugin for loading html fragments
from plain text html files.

Known to work in RequireJS, but should work in other AMD loaders that support
the same loader plugin API.

It requires [text plugin](https://github.com/requirejs/text) from requirejs to work.

## Install

    npm install require-html

It can also be installed using [volo](https://github.com/volojs/volo):

    volo add gartz/html

## Usage

Use very like `text` plugin from requirejs, and it will return `documentFragment`

```javascript
require(["html!some/module.html"],
    function(html) {
        console.log(html); // documentFragment
        document.body.appendChild(html);
        console.log(html); // empty documentFragment
        html.stash(); // documentFragment restored
        console.log(html.path) // some/module.html
        console.log(html.source) // source code from some/module.html
    }
);
```

## License

Dual-licensed -- new BSD or MIT.

## History

##history

For the server side is possible to use [domjs](https://github.com/medikoo/domjs).

## Latest release

The latest release is always available from [the "latest" tag](https://raw.github.com/gartz/html/latest/html.js).

