# Deep playground

Deep playground is an interactive visualization of neural networks, written in typescript using d3.js.
We use github issues for tracking new requests and bugs. Your feedback is highly appreciated!

**If you'd like to contribute, be sure to review the [contribution
guidelines](CONTRIBUTING).**

## Development

To run the visualization locally you just need a server to serve all the files from the `playground/dist/` directory. If you've previously used npm and node with d3, you can run `npm install` then `npm run serve` from the `playground/` directory. This will launch a node server at the URI `http://localhost:8080/` where you can play in your playground.

If you've not run npm and node on your environment yet, then you'll need to install some OS-specific packages first:

### Mac

I don't own a Mac, but I imagine this might work:

```bash
brew install nodejs
brew install npm
npm install d3
```

### Linux

```bash
sudo apt-get install nodejs nodejs-legacy npm
npm install d3
```

In both cases you may want to then run `sudo npm install typings --global` and `npm install d3` to have the typings tool ready in case you need it and get the latest d3 (though `npm install` may take care of this).

When developing, use `npm run serve-watch` rather than `npm run serve`.
This will start an http server as well as watchers to automatically recompile the typescript, html and css files and put them in `dist/` whenever any source files change.

### Deploymennt

To produce a minified javascript file for production, run `npm run build`.

To push to production (on a github.io server): `git subtree push --prefix dist origin gh-pages`.

This is not an official Google product.
