# NESNES

NESNES (New EcmaScript NES) is a pure JS NES emulator.

## Installation

NESNES can be installed through npm:

```
npm install nesnes
```

## Usage

NESNES can be used as follows:

```js
var NesNes = require("nesnes");

var emulator = new NesNes( canvas );
emulator.load( pathToRom, callback );
```

The parameters can be described as such:
   * ``canvas``: a &lt;canvas&gt; DOM object to which the video output will be rendered
   * ``pathToRom``: the path to an INES rom file (most ROMs found on the internet are in this format)
   * ``callback``: function to be executed once the ROM has been loaded and initialized. If ``true`` true is passed the ROM will automatically start playing

## Build standalone

If you don't use Browserify or Node, you can build a standalone version for browsers:

```
npm install
make
```

This will create ``nesnes.js`` in ``dist/``, which exposes a global NesNes object when included in your page.

## Configuration

Configuration (currently only keyboard input) can be found in ``config.json``.

## Testing

NESNES can be tested as follows:

```
make test
```

This starts an HTTP server at localhost, usually at port 8080 (the script tells you which port it uses). Visit http://localhost:PORT in your browser to be able to run several test ROMs with NESNES.