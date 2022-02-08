# DOM
The Document Object Model (DOM) is a cross-platform and language-independent interface that treats an XML or HTML document as a tree structure wherein each node is an object representing a part of the document. The DOM represents a document with a logical tree. Each branch of the tree ends in a node, and each node contains objects. DOM methods allow programmatic access to the tree; with them one can change the structure, style or content of a document. Nodes can have event handlers attached to them. Once an event is triggered, the event handlers get executed.[2]

The principal standardization of the DOM was handled by the World Wide Web Consortium (W3C), which last developed a recommendation in 2004. WHATWG took over the development of the standard, publishing it as a living document. The W3C now publishes stable snapshots of the WHATWG standard.

# Virtual DOM

A virtual DOM is a lightweight JavaScript representation of the DOM used in declarative web frameworks such as React, Vue.js, and Elm.[1] Updating the virtual DOM is comparatively faster than updating the actual DOM (via js). Thus, the framework is free to make unnecessary changes to the virtual DOM relatively cheaply. The framework then finds the differences between the previous virtual DOM and the current one, and only makes the necessary changes to the actual DOM.[2][3]

Svelte does not have a virtual DOM, and its creator Rich Harris calls the virtual DOM "pure overhead".[4]

Related techniques include Ember.js' Glimmer and Angular's incremental DOM.[5][6]


[](#awesome-virtual-dom)awesome-virtual-dom
===========================================

Modules & resources related to the virtual-dom module.

[![Awesome](https://camo.githubusercontent.com/abb97269de2982c379cbc128bba93ba724d8822bfbe082737772bd4feb59cb54/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f643733303566333864323966656437386661383536353265336136336531353464643865383832392f6d656469612f62616467652e737667)](https://github.com/sindresorhus/awesome)

[](#modules)Modules
-------------------

*   [virtual-dom](https://www.npmjs.com/package/virtual-dom) – A JavaScript DOM model supporting element creation, diff computation and patch operations for efficient re-rendering

### [](#loops)Loops

*   [virtual-raf](https://www.npmjs.com/package/virtual-raf) – Create a requestAnimationFrame loop for virtual-dom
*   [main-loop](https://www.npmjs.com/package/main-loop) – A rendering loop for diffable UIs

### [](#hooks)Hooks

*   [virtual-hook](https://github.com/yoshuawuyts/virtual-hook) – virtual-dom hook constructor. Allows access to the constructed DOM Node, property names and values
*   [virtual-hyperscript-hook](https://www.npmjs.com/package/virtual-hyperscript-hook) – Instead of adding hook/unhook lifecycle events on a per-property basis with a hook instance, this package lets you define simple `hook` and `unhook` properties as ordinary functions
*   [virtual-hyperscript-mount](https://github.com/substack/virtual-hyperscript-mount) – Register mount/unmount lifecycle hooks for virtual-dom

### [](#widgets)Widgets

*   [virtual-widget](https://github.com/yoshuawuyts/virtual-widget) – Create a virtual-dom widget

### [](#building-virtual-hyperscript)Building virtual-hyperscript

*   [hyperx](https://github.com/substack/hyperx) – tagged template string virtual dom builder

### [](#converting-to-and-from-virtual-dom)Converting to and from virtual-dom

*   [vdom-parser](https://www.npmjs.com/package/vdom-parser)
*   [vdom-to-html](https://www.npmjs.com/package/vdom-to-html)
*   [to-virtual-dom](https://www.npmjs.com/package/to-virtual-dom)

### [](#components)Components

*   [sheet-router](https://github.com/yoshuawuyts/sheet-router)
*   [virtual-loading-dots](https://github.com/chinedufn/virtual-loading-dots)
*   [virtual-markdown](https://github.com/yoshuawuyts/virtual-markdown)
*   [virtual-progress-bar](https://github.com/chinedufn/virtual-progress-bar)
*   [virtual-sidebar](https://github.com/yoshuawuyts/virtual-sidebar)
*   [virtual-streamgraph](https://github.com/yoshuawuyts/virtual-streamgraph)
*   [zip-input](https://github.com/bendrucker/zip-input)
*   [virtual-webtorrent](https://github.com/yoshuawuyts/virtual-webtorrent) - Webtorrent video element for virtual-dom

### [](#frameworks--libraries-that-depend-on-virtual-dom)Frameworks / libraries that depend on virtual-dom

*   [cycle.js](https://github.com/cyclejs)
*   [virtual-app](http://github.com/sethvincent/virtual-app)
*   [mercury](https://github.com/Raynos/mercury)

[](#build-tools)Build tools
---------------------------

*   [hyperxify](https://github.com/substack/hyperxify) – browserify transform for hyperx
*   [jsx-virtual-hyperscript-loader](https://www.npmjs.com/package/jsx-virtual-hyperscript-loader) – Webpack loader transpiling jsx into virtual-hyperscript javascript, using jsx-transform

[](#resources)Resources
-----------------------

### [](#articles)Articles

*   [What is Virtual DOM?](http://jbi.sh/what-is-virtual-dom/)
*   [We Don't Need No Stinkin' Frameworks: Writing Web Apps with Bacon.js and virtual-dom](http://blog.javascripting.com/2015/03/11/we-dont-need-no-stinkin-frameworks/)

### [](#talks)Talks

*   [Pocket-sized JS](https://www.youtube.com/watch?v=okk0BGV9oY0)

[](#alternate-virtual-dom-implementations)Alternate Virtual DOM implementations
-------------------------------------------------------------------------------

`virtual-dom` isn't the only module for diffing, patching, and creating elements. Here are some other projects that implement the Virtual DOM approach:

*   [basic-virtual-dom](https://www.npmjs.com/package/basic-virtual-dom)
*   [React](https://github.com/facebook/react)
*   [Preact](https://github.com/developit/preact)
*   [Deku](https://github.com/dekujs/deku)
*   [Snabbdom](https://github.com/paldepind/snabbdom)

[](#license)License
-------------------

[CC0 v1](/sethvincent/awesome-virtual-dom/blob/master/LICENSE)