# html

[![Analytics](https://ga-beacon.appspot.com/UA-24619548-7/html/readme)](https://github.com/igrigorik/ga-beacon)

A [RequireJS](http://requirejs.org)/AMD loader plugin for loading html fragments
from plain text html files.

Known to work in RequireJS, but should work in other AMD loaders that support
the same loader plugin API.

It requires [text plugin](https://github.com/requirejs/text) from requirejs to work.

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

All template engines are reinventing the weel. DOM is powerfull enough to work
with templates. For client you can use jquery or modern browser methods manipulate
you documentFragment generated by the html.

For the server side is possible to use [domjs](https://github.com/medikoo/domjs).

## Docs

No docs yet.

## Latest release

The latest release is always available from [the "latest" tag](https://raw.github.com/gartz/html/latest/html.js).

It can also be installed using [volo](https://github.com/volojs/volo):

    volo add gartz/html
