 .d88888b.  8888888b.  d8b                                 888b    888               888
d88P" "Y88b 888   Y88b Y8P                                 8888b   888               888
888     888 888    888                                     88888b  888               888
888     888 888   d88P 888  .d88b.  888  888 .d8888b       888Y88b 888  .d88b.   .d88888  .d88b.
888     888 8888888P"  888 d88""88b 888  888 88K           888 Y88b888 d88""88b d88" 888 d8P  Y8b
888 Y8b 888 888 T88b   888 888  888 888  888 "Y8888b.      888  Y88888 888  888 888  888 88888888
Y88b.Y8b88P 888  T88b  888 Y88..88P Y88b 888      X88      888   Y8888 Y88..88P Y88b 888 Y8b.
 "Y888888"  888   T88b 888  "Y88P"   "Y88888  88888P'      888    Y888  "Y88P"   "Y88888  "Y8888
       Y8b

[QRious Node](https://github.com/neocotic/node-qrious) is a [Node.js](https://nodejs.org) module for QR code generation
that uses the [QRious Core](https://github.com/neocotic/qrious-core) engine.

[![Chat](https://img.shields.io/gitter/room/neocotic/qrious.svg?style=flat-square)](https://gitter.im/neocotic/qrious)
[![Build Status](https://img.shields.io/travis/neocotic/node-qrious/develop.svg?style=flat-square)](https://travis-ci.org/neocotic/node-qrious)
[![Dependency Status](https://img.shields.io/david/neocotic/node-qrious.svg?style=flat-square)](https://david-dm.org/neocotic/node-qrious)
[![Dev Dependency Status](https://img.shields.io/david/dev/neocotic/node-qrious.svg?style=flat-square)](https://david-dm.org/neocotic/node-qrious?type=dev)
[![License](https://img.shields.io/npm/l/node-qrious.svg?style=flat-square)](https://github.com/neocotic/node-qrious/blob/master/LICENSE.md)
[![Release](https://img.shields.io/npm/v/node-qrious.svg?style=flat-square)](https://www.npmjs.com/package/node-qrious)

* [Prerequisites](#prerequisites)
* [Install](#install)
* [Examples](#examples)
* [API](#api)
* [Bugs](#bugs)
* [Contributors](#contributors)
* [License](#license)

## Prerequisites

QRious Node depends on [node-canvas](https://github.com/Automattic/node-canvas) to provide HTML5 canvas support within
the Node.js environment. The catch is that the module is entirely dependant on [Cairo](http://cairographics.org) being
installed as an external dependency, so QRious Node won't work without it. Sorry. Please see their wiki on steps on how
to do this on various platforms:

https://github.com/LearnBoost/node-canvas/wiki/_pages

## Install

Install using `npm`:

``` bash
$ npm install --save node-qrious
```

Check out [qrious](https://github.com/neocotic/qrious) if you want to install it for use within the browser.

## Examples

var express = require('express');
var QRious = require('node-qrious');

var app = express();

app.get('/qr', function(req, res) {
  var qr = new QRious({ value: 'https://github.com/neocotic/node-qrious' });

  res.end(new Buffer(qr.toDataURL(), 'base64'));
});

app.listen(3000);

## API

You will find documentation for the API on [QRious](https://github.com/neocotic/qrious).

## Bugs

If you have any problems with QRious Node or would like to see changes currently in development you can do so
[here](https://github.com/neocotic/node-qrious/issues). Core features and issues are maintained separately
[here](https://github.com/neocotic/qrious-core/issues).

## Contributors

If you want to contribute, you're a legend! Information on how you can do so can be found in
[CONTRIBUTING.md](https://github.com/neocotic/node-qrious/blob/master/CONTRIBUTING.md). We want your suggestions and
pull requests!

A list of QRious Node contributors can be found in
[AUTHORS.md](https://github.com/neocotic/node-qrious/blob/master/AUTHORS.md).

## License

Copyright © 2017 Alasdair Mercer  
Copyright © 2010 Tom Zerucha

See [LICENSE.md](https://github.com/neocotic/node-qrious/blob/master/LICENSE.md) for more information on our GPLv3
license.
