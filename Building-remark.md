#### Prerequisites

Building remark requires you to have the following software installed:
  * [`git`](http://git-scm.com/)
  * [`node`](http://nodejs.org/) (and `npm`, which is included in recent node versions)

#### Downloading source and installing dependencies

In addition to cloning the remark repository, it's git sub modules and node package dependencies must be installed as well:

```sh
git clone https://github.com/gnab/remark.git
cd remark
git submodule update --init --recursive
npm install
```

#### Building remark

To build remark, there's one final command to execute:

```sh
node make
```

This will trigger the `all` target in the Makefile-like [make.js](https://github.com/gnab/remark/blob/master/make.js) file created using the excellent [ShellJS](https://github.com/arturadib/shelljs) library.

The `all` target comprises the targets `lint`, `test`, `bundle` and `minify`. If all targets succeed you'll end up with a [remark.js](https://github.com/gnab/remark/blob/master/remark.js) and a minified [remark.min.js](https://github.com/gnab/remark/blob/master/remark.min.js).

#### Building remark highlighter

In addition to building remark itself, there's an additional `highlighter` target that will bundle [Highlight.js](http://softwaremaniacs.org/soft/highlight/en/) into the [src/remark/highlighter.js](https://github.com/gnab/remark/blob/master/src/remark/highlighter.js) file.

```sh
node make highlighter
```

This will bundle [Highlight.js](http://softwaremaniacs.org/soft/highlight/en/) itself, its styles (with a few exceptions), and the languages specified in the [package.json](https://github.com/gnab/remark/blob/master/package.json) file:

```json
{
  ...
  "config": {
    "highlighter": {
       "languages": [
         "javascript",
         "ruby",
         ...
       ]
    }
  }
}
```