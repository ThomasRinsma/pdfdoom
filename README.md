# PDF Doom

Only works in PDFium (PDF viewer in Chromium-based browsers) for now.

See also: [PDF Tetris](https://github.com/ThomasRinsma/pdftris).

Makes heavy use of [doom-ascii](https://github.com/wojciech-graj/doom-ascii) which uses the lovely [doomgeneric](https://github.com/ozkl/doomgeneric).

## Building

First build `doom-ascii`:

```sh
cd doom-ascii/src
make
```

This produces `doom-ascii/doom_ascii/doom_ascii.js` (if you have emscripten installed, see paths in `Makefile`)

Then run the python script to embed the JS into the PDF template:
```sh
./build.py doom.pdf.template doom-ascii/doom_ascii/doom_ascii.js doom.pdf
```