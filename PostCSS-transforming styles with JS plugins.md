[](#postcss-)PostCSS [![Gitter](https://camo.githubusercontent.com/6523581eec3346cf93db830add93cdc96b28bb8f32ca4a7a98a710ab449fadd3/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4769747465722d4a6f696e5f7468655f506f73744353535f636861742d627269676874677265656e2e737667)](https://gitter.im/postcss/postcss)
===========================================================================================================================================================================================================================================================================================================================

[![Philosopher’s stone, logo of PostCSS](https://camo.githubusercontent.com/a2ebaaedf9af41416a2717b3a28f405b39535397f4463c5c5119146c84c240f9/68747470733a2f2f706f73746373732e6f72672f6c6f676f2e737667)](https://camo.githubusercontent.com/a2ebaaedf9af41416a2717b3a28f405b39535397f4463c5c5119146c84c240f9/68747470733a2f2f706f73746373732e6f72672f6c6f676f2e737667)

PostCSS is a tool for transforming styles with JS plugins. These plugins can lint your CSS, support variables and mixins, transpile future CSS syntax, inline images, and more.

PostCSS is used by industry leaders including Wikipedia, Twitter, Alibaba, and JetBrains. The [Autoprefixer](https://github.com/postcss/autoprefixer) PostCSS plugin is one of the most popular CSS processors.

PostCSS takes a CSS file and provides an API to analyze and modify its rules (by transforming them into an [Abstract Syntax Tree](https://en.wikipedia.org/wiki/Abstract_syntax_tree)). This API can then be used by [plugins](https://github.com/postcss/postcss#plugins) to do a lot of useful things, e.g., to find errors automatically, or to insert vendor prefixes.

**Support / Discussion:** [Gitter](https://gitter.im/postcss/postcss)  
**Twitter account:** [@postcss](https://twitter.com/postcss)  
**VK.com page:** [postcss](https://vk.com/postcss)  
**中文翻译**: [`docs/README-cn.md`](/postcss/postcss/blob/main/docs/README-cn.md)

For PostCSS commercial support (consulting, improving the front-end culture of your company, PostCSS plugins), contact [Evil Martians](https://evilmartians.com/?utm_source=postcss) at [postcss@evilmartians.com](mailto:postcss@evilmartians.com).

[![Sponsored by Evil Martians](https://camo.githubusercontent.com/e3313339ea3cb39c90da1e389af3b31b3ab754f9e06a115f8bab411854ea460e/68747470733a2f2f6576696c6d61727469616e732e636f6d2f6261646765732f73706f6e736f7265642d62792d6576696c2d6d61727469616e732e737667)](https://evilmartians.com/?utm_source=postcss)

[](#sponsorship)Sponsorship
---------------------------

PostCSS needs your support. We are accepting donations [at Open Collective](https://opencollective.com/postcss/).

 [![Sponsored by Tailwind CSS](https://camo.githubusercontent.com/53b9876cd8e38928387c6824043b0e2772b15b1bfdb7f42d0864216abbf3dfe8/68747470733a2f2f7265666163746f72696e6775692e6e7963332e63646e2e6469676974616c6f6365616e7370616365732e636f6d2f7461696c77696e642d6c6f676f2e737667)](https://tailwindcss.com/)       [![Sponsored by ThemeIsle](https://camo.githubusercontent.com/2943776340da2fc7899541b793285efbddbe5a3ff961326947751e4b75de7102/68747470733a2f2f6d6c6c6a326a387876666c302e692e6f7074696d6f6c652e636f6d2f6430634f5857412e333937307e33373361642f773a6175746f2f683a6175746f2f713a39302f68747470733a2f2f7333303234362e7063646e2e636f2f77702d636f6e74656e742f75706c6f6164732f323031392f30332f6c6f676f2e706e67)](https://themeisle.com/)

[](#plugins)Plugins
-------------------

Currently, PostCSS has more than 200 plugins. You can find all of the plugins in the [plugins list](https://github.com/postcss/postcss/blob/main/docs/plugins.md) or in the [searchable catalog](https://www.postcss.parts/). Below is a list of our favorite plugins — the best demonstrations of what can be built on top of PostCSS.

If you have any new ideas, [PostCSS plugin development](https://github.com/postcss/postcss/blob/main/docs/writing-a-plugin.md) is really easy.

### [](#solve-global-css-problem)Solve Global CSS Problem

*   [`postcss-use`](https://github.com/postcss/postcss-use) allows you to explicitly set PostCSS plugins within CSS and execute them only for the current file.
*   [`postcss-modules`](https://github.com/outpunk/postcss-modules) and [`react-css-modules`](https://github.com/gajus/react-css-modules) automatically isolate selectors within components.
*   [`postcss-autoreset`](https://github.com/maximkoretskiy/postcss-autoreset) is an alternative to using a global reset that is better for isolatable components.
*   [`postcss-initial`](https://github.com/maximkoretskiy/postcss-initial) adds `all: initial` support, which resets all inherited styles.
*   [`cq-prolyfill`](https://github.com/ausi/cq-prolyfill) adds container query support, allowing styles that respond to the width of the parent.

### [](#use-future-css-today)Use Future CSS, Today

*   [`autoprefixer`](https://github.com/postcss/autoprefixer) adds vendor prefixes, using data from Can I Use.
*   [`postcss-preset-env`](https://github.com/jonathantneal/postcss-preset-env) allows you to use future CSS features today.

### [](#better-css-readability)Better CSS Readability

*   [`postcss-nested`](https://github.com/postcss/postcss-nested) unwraps nested rules the way Sass does.
*   [`postcss-sorting`](https://github.com/hudochenkov/postcss-sorting) sorts the content of rules and at-rules.
*   [`postcss-utilities`](https://github.com/ismamz/postcss-utilities) includes the most commonly used shortcuts and helpers.
*   [`short`](https://github.com/jonathantneal/postcss-short) adds and extends numerous shorthand properties.

### [](#images-and-fonts)Images and Fonts

*   [`postcss-assets`](https://github.com/assetsjs/postcss-assets) inserts image dimensions and inlines files.
*   [`postcss-sprites`](https://github.com/2createStudio/postcss-sprites) generates image sprites.
*   [`font-magician`](https://github.com/jonathantneal/postcss-font-magician) generates all the `@font-face` rules needed in CSS.
*   [`postcss-inline-svg`](https://github.com/TrySound/postcss-inline-svg) allows you to inline SVG and customize its styles.
*   [`postcss-write-svg`](https://github.com/jonathantneal/postcss-write-svg) allows you to write simple SVG directly in your CSS.
*   [`webp-in-css`](https://github.com/ai/webp-in-css) to use WebP image format in CSS background.
*   [`avif-in-css`](https://github.com/nucliweb/avif-in-css) to use AVIF image format in CSS background.

### [](#linters)Linters

*   [`stylelint`](https://github.com/stylelint/stylelint) is a modular stylesheet linter.
*   [`stylefmt`](https://github.com/morishitter/stylefmt) is a tool that automatically formats CSS according `stylelint` rules.
*   [`doiuse`](https://github.com/anandthakker/doiuse) lints CSS for browser support, using data from Can I Use.
*   [`colorguard`](https://github.com/SlexAxton/css-colorguard) helps you maintain a consistent color palette.

### [](#other)Other

*   [`postcss-rtl`](https://github.com/vkalinichev/postcss-rtl) combines both-directional (left-to-right and right-to-left) styles in one CSS file.
*   [`cssnano`](https://cssnano.co/) is a modular CSS minifier.
*   [`lost`](https://github.com/peterramsing/lost) is a feature-rich `calc()` grid system.
*   [`rtlcss`](https://github.com/MohammadYounes/rtlcss) mirrors styles for right-to-left locales.

[](#syntaxes)Syntaxes
---------------------

PostCSS can transform styles in any syntax, not just CSS. If there is not yet support for your favorite syntax, you can write a parser and/or stringifier to extend PostCSS.

*   [`sugarss`](https://github.com/postcss/sugarss) is a indent-based syntax like Sass or Stylus.
*   [`postcss-syntax`](https://github.com/gucong3000/postcss-syntax) switch syntax automatically by file extensions.
*   [`postcss-html`](https://github.com/gucong3000/postcss-html) parsing styles in `<style>` tags of HTML-like files.
*   [`postcss-markdown`](https://github.com/gucong3000/postcss-markdown) parsing styles in code blocks of Markdown files.
*   [`postcss-jsx`](https://github.com/gucong3000/postcss-jsx) parsing CSS in template / object literals of source files.
*   [`postcss-styled`](https://github.com/gucong3000/postcss-styled) parsing CSS in template literals of source files.
*   [`postcss-scss`](https://github.com/postcss/postcss-scss) allows you to work with SCSS _(but does not compile SCSS to CSS)_.
*   [`postcss-sass`](https://github.com/AleshaOleg/postcss-sass) allows you to work with Sass _(but does not compile Sass to CSS)_.
*   [`postcss-less`](https://github.com/webschik/postcss-less) allows you to work with Less _(but does not compile LESS to CSS)_.
*   [`postcss-less-engine`](https://github.com/Crunch/postcss-less) allows you to work with Less _(and DOES compile LESS to CSS using true Less.js evaluation)_.
*   [`postcss-js`](https://github.com/postcss/postcss-js) allows you to write styles in JS or transform React Inline Styles, Radium or JSS.
*   [`postcss-safe-parser`](https://github.com/postcss/postcss-safe-parser) finds and fixes CSS syntax errors.
*   [`midas`](https://github.com/ben-eb/midas) converts a CSS string to highlighted HTML.

[](#articles)Articles
---------------------

*   [Some things you may think about PostCSS… and you might be wrong](http://julian.io/some-things-you-may-think-about-postcss-and-you-might-be-wrong)
*   [What PostCSS Really Is; What It Really Does](https://davidtheclark.com/its-time-for-everyone-to-learn-about-postcss/)
*   [PostCSS Guides](https://webdesign.tutsplus.com/series/postcss-deep-dive--cms-889)

More articles and videos you can find on [awesome-postcss](https://github.com/jjaderg/awesome-postcss) list.

[](#books)Books
---------------

*   [Mastering PostCSS for Web Design](https://www.packtpub.com/web-development/mastering-postcss-web-design) by Alex Libby, Packt. (June 2016)

[](#usage)Usage
---------------

You can start using PostCSS in just two steps:

1.  Find and add PostCSS extensions for your build tool.
2.  [Select plugins](https://www.postcss.parts/) and add them to your PostCSS process.

### [](#css-in-js)CSS-in-JS

The best way to use PostCSS with CSS-in-JS is [`astroturf`](https://github.com/4Catalyzer/astroturf). Add its loader to your `webpack.config.js`:

module.exports \= {
  module: {
    rules: \[
      {
        test: /\\.css$/,
        use: \['style-loader', 'postcss-loader'\],
      },
      {
        test: /\\.jsx?$/,
        use: \['babel-loader', 'astroturf/loader'\],
      }
    \]
  }
}

Then create `postcss.config.js`:

module.exports \= {
  plugins: \[
    require('autoprefixer'),
    require('postcss-nested')
  \]
}

### [](#parcel)Parcel

[Parcel](https://parceljs.org) has built-in PostCSS support. It already uses Autoprefixer and cssnano. If you want to change plugins, create `postcss.config.js` in project’s root:

module.exports \= {
  plugins: \[
    require('autoprefixer'),
    require('postcss-nested')
  \]
}

Parcel will even automatically install these plugins for you.

> Please, be aware of [the several issues in Version 1](https://github.com/parcel-bundler/parcel/labels/CSS%20Preprocessing). Notice, [Version 2](https://github.com/parcel-bundler/parcel/projects/5) may resolve the issues via [issue #2157](https://github.com/parcel-bundler/parcel/issues/2157).

### [](#webpack)Webpack

Use [`postcss-loader`](https://github.com/postcss/postcss-loader) in `webpack.config.js`:

module.exports \= {
  module: {
    rules: \[
      {
        test: /\\.css$/,
        exclude: /node\_modules/,
        use: \[
          {
            loader: 'style-loader',
          },
          {
            loader: 'css-loader',
            options: {
              importLoaders: 1,
            }
          },
          {
            loader: 'postcss-loader'
          }
        \]
      }
    \]
  }
}

Then create `postcss.config.js`:

module.exports \= {
  plugins: \[
    require('autoprefixer'),
    require('postcss-nested')
  \]
}

### [](#gulp)Gulp

Use [`gulp-postcss`](https://github.com/postcss/gulp-postcss) and [`gulp-sourcemaps`](https://github.com/floridoo/gulp-sourcemaps).

gulp.task('css', () \=> {
  const postcss    \= require('gulp-postcss')
  const sourcemaps \= require('gulp-sourcemaps')

  return gulp.src('src/\*\*/\*.css')
    .pipe( sourcemaps.init() )
    .pipe( postcss(\[ require('autoprefixer'), require('postcss-nested') \]) )
    .pipe( sourcemaps.write('.') )
    .pipe( gulp.dest('build/') )
})

### [](#npm-scripts)npm Scripts

To use PostCSS from your command-line interface or with npm scripts there is [`postcss-cli`](https://github.com/postcss/postcss-cli).

postcss --use autoprefixer -o main.css css/\*.css

### [](#browser)Browser

If you want to compile CSS string in browser (for instance, in live edit tools like CodePen), just use [Browserify](http://browserify.org/) or [webpack](https://webpack.github.io/). They will pack PostCSS and plugins files into a single file.

To apply PostCSS plugins to React Inline Styles, JSS, Radium and other [CSS-in-JS](https://github.com/MicheleBertoli/css-in-js), you can use [`postcss-js`](https://github.com/postcss/postcss-js) and transforms style objects.

const postcss  \= require('postcss-js')
const prefixer \= postcss.sync(\[ require('autoprefixer') \])

prefixer({ display: 'flex' }) //=> { display: \['-webkit-box', '-webkit-flex', '-ms-flexbox', 'flex'\] }

### [](#deno)Deno

PostCSS also supports [Deno](https://deno.land/):

import postcss from 'https://deno.land/x/postcss/mod.js'
import autoprefixer from 'https://jspm.dev/autoprefixer'

const result \= await postcss(\[autoprefixer\]).process(css)

### [](#runners)Runners

*   **Grunt**: [`@lodder/grunt-postcss`](https://github.com/C-Lodder/grunt-postcss)
*   **HTML**: [`posthtml-postcss`](https://github.com/posthtml/posthtml-postcss)
*   **Stylus**: [`poststylus`](https://github.com/seaneking/poststylus)
*   **Rollup**: [`rollup-plugin-postcss`](https://github.com/egoist/rollup-plugin-postcss)
*   **Brunch**: [`postcss-brunch`](https://github.com/brunch/postcss-brunch)
*   **Broccoli**: [`broccoli-postcss`](https://github.com/jeffjewiss/broccoli-postcss)
*   **Meteor**: [`postcss`](https://atmospherejs.com/juliancwirko/postcss)
*   **ENB**: [`enb-postcss`](https://github.com/awinogradov/enb-postcss)
*   **Taskr**: [`taskr-postcss`](https://github.com/lukeed/taskr/tree/master/packages/postcss)
*   **Start**: [`start-postcss`](https://github.com/start-runner/postcss)
*   **Connect/Express**: [`postcss-middleware`](https://github.com/jedmao/postcss-middleware)
*   **Svelte Preprocessor**: [`svelte-preprocess`](https://github.com/sveltejs/svelte-preprocess/blob/main/docs/preprocessing.md#postcss-sugarss)

### [](#js-api)JS API

For other environments, you can use the JS API:

const autoprefixer \= require('autoprefixer')
const postcss \= require('postcss')
const postcssNested \= require('postcss-nested')
const fs \= require('fs')

fs.readFile('src/app.css', (err, css) \=> {
  postcss(\[autoprefixer, postcssNested\])
    .process(css, { from: 'src/app.css', to: 'dest/app.css' })
    .then(result \=> {
      fs.writeFile('dest/app.css', result.css, () \=> true)
      if ( result.map ) {
        fs.writeFile('dest/app.css.map', result.map.toString(), () \=> true)
      }
    })
})

Read the [PostCSS API documentation](https://postcss.org/api/) for more details about the JS API.

All PostCSS runners should pass [PostCSS Runner Guidelines](https://github.com/postcss/postcss/blob/main/docs/guidelines/runner.md).

### [](#options)Options

Most PostCSS runners accept two parameters:

*   An array of plugins.
*   An object of options.

Common options:

*   `syntax`: an object providing a syntax parser and a stringifier.
*   `parser`: a special syntax parser (for example, [SCSS](https://github.com/postcss/postcss-scss)).
*   `stringifier`: a special syntax output generator (for example, [Midas](https://github.com/ben-eb/midas)).
*   `map`: [source map options](https://postcss.org/api/#sourcemapoptions).
*   `from`: the input file name (most runners set it automatically).
*   `to`: the output file name (most runners set it automatically).

### [](#treat-warnings-as-errors)Treat Warnings as Errors

In some situations it might be helpful to fail the build on any warning from PostCSS or one of its plugins. This guarantees that no warnings go unnoticed, and helps to avoid bugs. While there is no option to enable treating warnings as errors, it can easily be done by adding `postcss-fail-on-warn` plugin in the end of PostCSS plugins:

module.exports \= {
  plugins: \[
    require('autoprefixer'),
    require('postcss-fail-on-warn')
  \]
}

[](#editors--ide-integration)Editors & IDE Integration
------------------------------------------------------

### [](#vs-code)VS Code

*   [`mhmadhamster.postcss-language`](https://marketplace.visualstudio.com/items?itemName=mhmadhamster.postcss-language) adds PostCSS and SugarSS support.

### [](#atom)Atom

*   [`language-postcss`](https://atom.io/packages/language-postcss) adds PostCSS and [SugarSS](https://github.com/postcss/sugarss) highlight.
*   [`source-preview-postcss`](https://atom.io/packages/source-preview-postcss) previews your output CSS in a separate, live pane.

### [](#sublime-text)Sublime Text

*   [`Syntax-highlighting-for-PostCSS`](https://github.com/hudochenkov/Syntax-highlighting-for-PostCSS) adds PostCSS highlight.

### [](#vim)Vim

*   [`postcss.vim`](https://github.com/stephenway/postcss.vim) adds PostCSS highlight.

### [](#webstorm)WebStorm

To get support for PostCSS in WebStorm and other JetBrains IDEs you need to install [this plugin](https://plugins.jetbrains.com/plugin/8578-postcss).

[](#security-contact)Security Contact
-------------------------------------

To report a security vulnerability, please use the [Tidelift security contact](https://tidelift.com/security). Tidelift will coordinate the fix and disclosure.

[](#for-enterprise)For Enterprise
---------------------------------

Available as part of the Tidelift Subscription.

The maintainers of `postcss` and thousands of other packages are working with Tidelift to deliver commercial support and maintenance for the open source dependencies you use to build your applications. Save time, reduce risk, and improve code health, while paying the maintainers of the exact dependencies you use. [Learn more.](https://tidelift.com/subscription/pkg/npm-postcss?utm_source=npm-postcss&utm_medium=referral&utm_campaign=enterprise&utm_term=repo)