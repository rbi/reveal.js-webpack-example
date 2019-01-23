# reveal.js with Webpack
This repository contains a minimal example showing how to create a [reveal.js](https://github.com/hakimel/reveal.js) presentation using NPM and Webpack to download and bundle reveal.js with your presentation content.
The [offical documentation](https://github.com/hakimel/reveal.js#installation) tells you do clone or download the whole reveal.js library and add your presentation content next to the code of the library.
This is bad for separation of concerns and not how third-party libraries are used most times.

In this example reveal.js is just an NPM dependency in the `package.json` like any other third-party library.
The `index.html` contains almost only the content of the presentation.
The `src/index.js` configures the presentation e.g. by setting the theme
and `webpack.config.js` is used to configure Webpack to bundle your presentation and the library code.
This example still contains boilerplate but the boilerplate to presentation content ratio is greatly improved compared to the official approach.

# How to Build
To build the presentation run

~~~
npm run build
~~~

To automatically build the presenation when code changes run

~~~
npm run watch
~~~

This doesn't use the Webpack devserver so you have to press F5 in the browser to see the updated results.
