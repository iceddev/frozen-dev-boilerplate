# {NAME}

## Getting started

To get your environment set up, you need `node` and `npm`

Install [`volo`](http://volojs.org/)

```bash
> npm install -g volo
```

Then use `volo create` to start a new project

```bash
> volo create new_project iceddev/frozen-dev-boilerplate
```

## Development

During development, an error will be thrown because `dist/game.js` doesn't exist

However, we check to see if it is loaded and use the dojo loader if it isn't

We also note in the console that is happening

During development, work in the `src/` directory and make small modules

You can start a development server with linting and auto-reload using the `volo grunt` command in your terminal, which will open your default browser to 0.0.0.0:8000

Your browser will auto-reload when you make changes to files

## Building

Once you are ready to deploy your project, you can build with the `volo grunt build` command

This command will crawl your dependency tree, starting with `src/game.js` and build a single file `dist/game.js.uncompressed.js`

It will also minify your file with Google Closure Compiler into `dist/game.js`

You shouldn't have to make any changes to your `index.html` for this file to start working

## Removing Build and/or Dependencies

You can remove the files generated by the `volo grunt dojo` (`dist/` and `libs/`) by running `volo grunt clean:dist`

You can remove `deps/` and `node_modules/` by running `volo grunt clean:deps`

You can remove `dist/`, `libs/`, `deps/`, and `node_modules/` by running `volo grunt clean:all`

## License

The MIT License (MIT)

Copyright (c) 2013 Iced Development, LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.