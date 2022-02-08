# Deck.gl

 
deck.gl is a WebGL-powered framework for visual exploratory data analysis of large datasets.


A Layered Approach to Data Visualization
deck.gl allows complex visualizations to be constructed by composing existing layers, and makes it easy to package and share new visualizations as reusable layers. We already offer a catalog of proven layers and we have many more in the works.

High-Precision Computations in the GPU
By emulating 64 bit floating point computations in the GPU, deck.gl renders datasets with unparalleled accuracy and performance.

React Friendly
deck.gl APIs are designed to reflect the reactive programming paradigm. Whether using Vanilla JS or the React interface, it can handle efficient WebGL rendering under heavy data load.

Integration with Base Map Providers
While deck.gl works standalone without a base map, it plays nicely with your favorite base map providers such as Google Maps, Mapbox, ArcGIS and more. Where the base map library permits, deck.gl may interleave with 3D map layers to create seamless visualizations.



 [![version](https://camo.githubusercontent.com/3fca7d4437a435dd277e111e5b7d27b5eee6123e514703d684963f92c7d9b47c/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f762f6465636b2e676c2e7376673f7374796c653d666c61742d737175617265)](https://npmjs.org/package/deck.gl) [ ![build](https://github.com/visgl/deck.gl/workflows/test/badge.svg?branch=master) ](https://github.com/visgl/deck.gl/actions?query=workflow%3Atest+branch%3Amaster) [ ![downloads](https://camo.githubusercontent.com/ec0e56f15df08cec8a571b3f517d925f7289370033655a2b17596d6554c5e5f1/68747470733a2f2f696d672e736869656c64732e696f2f6e706d2f646d2f406465636b2e676c2f636f72652e7376673f7374796c653d666c61742d737175617265) ](https://npmjs.org/package/deck.gl) [![Coverage Status](https://camo.githubusercontent.com/5b2437382e17c022ed40c534afeaab022a456bff9892ca6ff45fcdf097f0509e/68747470733a2f2f696d672e736869656c64732e696f2f636f766572616c6c732f766973676c2f6465636b2e676c2e7376673f7374796c653d666c61742d737175617265)](https://coveralls.io/github/visgl/deck.gl?branch=master) 

[](#deckgl--website)deck.gl | [Website](https://deck.gl)
========================================================

##### [](#-webgl2-powered-highly-performant-large-scale-data-visualization)WebGL2-powered, highly performant large-scale data visualization

[![docs](https://camo.githubusercontent.com/f09fe19cef75577a67899233ef61eb58294bf305ceb6ea7ac7845d8bdc9cc6ec/687474703a2f2f692e696d6775722e636f6d2f6d7666766766302e6a7067)](https://visgl.github.io/deck.gl)

deck.gl is designed to simplify high-performance, WebGL-based visualization of large data sets. Users can quickly get impressive visual results with minimal effort by composing existing layers, or leverage deck.gl's extensible architecture to address custom needs.

deck.gl maps **data** (usually an array of JSON objects) into a stack of visual **layers** - e.g. icons, polygons, texts; and look at them with **views**: e.g. map, first-person, orthographic.

deck.gl handles a number of challenges out of the box:

*   Performant rendering and updating of large data sets
*   Interactive event handling such as picking, highlighting and filtering
*   Cartographic projections and integration with major basemap providers
*   A catalog of proven, well-tested layers

Deck.gl is designed to be highly customizable. All layers come with flexible APIs to allow programmatic control of each aspect of the rendering. All core classes such are easily extendable by the users to address custom use cases.

[](#flavors)Flavors
-------------------

### [](#script-tag)Script Tag

<script src\="https://unpkg.com/deck.gl@latest/dist.min.js"\></script\>

*   [Get started](/visgl/deck.gl/blob/master/docs/get-started/using-standalone.md#using-the-scripting-api)
*   [Full examples](https://github.com/visgl/deck.gl/tree/master/examples/get-started/scripting)

### [](#npm-module)NPM Module

npm install deck.gl

#### [](#pure-js)Pure JS

*   [Get started](/visgl/deck.gl/blob/master/docs/get-started/using-standalone.md)
*   [Full examples](/visgl/deck.gl/blob/master/examples/get-started/pure-js)

#### [](#react)React

*   [Get started](/visgl/deck.gl/blob/master/docs/get-started/using-with-react.md)
*   [Full examples](/visgl/deck.gl/blob/master/examples/get-started/react)

### [](#python)Python

pip install pydeck

*   [Get started](https://pydeck.gl/installation.html)
*   [Examples](https://pydeck.gl/)

### [](#third-party-bindings)Third-Party Bindings

*   [deckgl-typings](https://github.com/danmarshall/deckgl-typings) (Typescript)
*   [mapdeck](https://symbolixau.github.io/mapdeck/articles/mapdeck.html) (R)
*   [vega-deck.gl](https://github.com/microsoft/SandDance/tree/master/packages/vega-deck.gl) ([Vega](https://vega.github.io/))
*   [earthengine-layers](https://earthengine-layers.com/) ([Google Earth Engine](https://earthengine.google.com/))
*   [deck.gl-native](https://github.com/UnfoldedInc/deck.gl-native) (C++)

[](#learning-resources)Learning Resources
-----------------------------------------

*   [API documentation](https://deck.gl/#/documentation) for the latest release
*   [Website demos](https://deck.gl/#/examples) with links to source
*   [Interactive playground](https://deck.gl/playground)
*   [deck.gl Codepen demos](https://codepen.io/vis-gl/)
*   [deck.gl Observable demos](https://beta.observablehq.com/@pessimistress)
*   [vis.gl Medium blog](https://medium.com/vis-gl)
*   [deck.gl Slack workspace](https://join.slack.com/t/deckgl/shared_invite/zt-7oeoqie8-NQqzSp5SLTFMDeNSPxi7eg)

[](#contributing)Contributing
-----------------------------

deck.gl is part of vis.gl, a [Urban Computing Foundation](https://uc.foundation/) project. Read the [contribution guidelines](/visgl/deck.gl/blob/master/CONTRIBUTING.md) if you are intrested in contributing.

[](#attributions)Attributions
-----------------------------

#### [](#data-sources)Data sources

Data sources are listed in each example.

#### [](#the-deckgl-project-is-supported-by)The deck.gl project is supported by

[![](https://raw.githubusercontent.com/visgl/deck.gl-data/master/images/branding/unfolded.png)](https://www.unfolded.ai) [![](https://raw.githubusercontent.com/visgl/deck.gl-data/master/images/branding/fsq.svg)](https://www.foursquare.com)

[![](https://raw.githubusercontent.com/visgl/deck.gl-data/master/images/branding/carto.svg)](https://www.carto.com)

[![](https://raw.githubusercontent.com/visgl/deck.gl-data/master/images/branding/mapbox.svg)](https://www.mapbox.com) [![](https://raw.githubusercontent.com/visgl/deck.gl-data/master/images/branding/uber.png)](https://www.uber.com)

[![BrowserStack](https://camo.githubusercontent.com/b4a198118539b82e453c52003d284e8ad9ed635a5b3cf1f2b0020665f3f7ad65/68747470733a2f2f643938623874316e6e756c6b352e636c6f756466726f6e742e6e65742f70726f64756374696f6e2f696d616765732f7374617469632f6c6f676f2e737667)](https://www.browserstack.com/)



Script Tag
<script src="https://unpkg.com/deck.gl@latest/dist.min.js"></script>
Get started
Full examples
NPM Module
npm install deck.gl
Pure JS
Get started
Full examples
React
Get started
Full examples
Python
pip install pydeck
Get started
Examples
Third-Party Bindings
deckgl-typings (Typescript)
mapdeck (R)
vega-deck.gl (Vega)
earthengine-layers (Google Earth Engine)
deck.gl-native (C++)
Learning Resources
API documentation for the latest release
Website demos with links to source
Interactive playground
deck.gl Codepen demos
deck.gl Observable demos
vis.gl Medium blog
deck.gl Slack workspace
