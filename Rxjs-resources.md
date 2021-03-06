# RxJS  

https://rxjs.dev/

RxJS is a library for composing asynchronous and event-based programs by using observable sequences. It provides one core type, the Observable, satellite types (Observer, Schedulers, Subjects) and operators inspired by Array#extras (map, filter, reduce, every, etc) to allow handling asynchronous events as collections.

Think of RxJS as Lodash for events.

ReactiveX combines the Observer pattern with the Iterator pattern and functional programming with collections to fill the need for an ideal way of managing sequences of events.

The essential concepts in RxJS which solve async event management are:

Observable: represents the idea of an invokable collection of future values or events.
Observer: is a collection of callbacks that knows how to listen to values delivered by the Observable.
Subscription: represents the execution of an Observable, is primarily useful for cancelling the execution.
Operators: are pure functions that enable a functional programming style of dealing with collections with operations like map, filter, concat, reduce, etc.
Subject: is equivalent to an EventEmitter, and the only way of multicasting a value or event to multiple Observers.
Schedulers: are centralized dispatchers to control concurrency, allowing us to coordinate when computation happens on e.g. setTimeout or requestAnimationFrame or others.


Reactive Extensions Library for JavaScript


*   [Getting Started](#getting-started)
*   [Beyond the Basics](#beyond-the-basics)
*   [Hot vs Cold Observables](#hot-vs-cold-observables)
*   [RxJS 5 vs RxJS 4](#rxjs-5-vs-rxjs-4)
*   [Libraries Built with RxJS](#libraries-built-with-rxjs)
*   [Talks](#talks)
*   [Articles](#articles)
*   [Examples](#examples)
*   [Testing](#testing)
*   [References](#references)
*   [People](#people)
*   [Community](#community)
*   [React & RxJS](#react--rxjs)
*   [Angular2 & RxJS](#angular2--rxjs)
*   [Other Reactive Programming Libraries](#other-reactive-programming-libraries)
*   [Sources](#sources)

[](#getting-started)Getting Started
-----------------------------------

*   [The introduction to Reactive Programming you've been missing](https://gist.github.com/staltz/868e7e9bc2a7b8c1f754)
*   [Learnrx interactive operator tutorial](http://reactivex.io/learnrx/)
*   [Introduction to Reactive Programming](https://egghead.io/series/introduction-to-reactive-programming) - Egghead series by Andr?? Staltz for _brand new_ to reactive programming
*   [Step-by-Step Async JavaScript with RxJS](https://egghead.io/series/step-by-step-async-javascript-with-rxjs) - Egghead series by John Lindquist
*   [Introducing the Observable](https://egghead.io/lessons/javascript-introducing-the-observable) - Egghead Series by Jafar Husain
*   [The Two Pillars of JavaScript ??? Pt 2: Functional Programming](https://medium.com/javascript-scene/the-two-pillars-of-javascript-pt-2-functional-programming-a63aa53a41a4#.cn22tmqmm)
*   [RxJS, Kefir and Bacon are "inspired by" FRP but not strict functional](https://twitter.com/conal/status/468875014461468677) - Conal Elliott
*   [What is FRP aka. Functional Reactive Programming Specification](http://stackoverflow.com/questions/5875929/specification-for-a-functional-reactive-programming-language/5878525#5878525) - Conal Elliott
*   [Interactive diagrams of Rx Observables](http://rxmarbles.com/) - Andr?? Staltz
*   [Rx Visualizer](https://rxviz.com) - Animated playground for Rx Observables by Misha Moroshko
*   [Learn RxJS](http://learnrxjs.io) - RxJS 5 descriptions, examples, and resources by Brian Troncone
*   [Reactive.how](https://reactive.how/) - Animated cards to learn Reactive Programming by C??dric Soulas

[](#beyond-the-basics)Beyond the Basics
---------------------------------------

*   [RxJS Beyond the Basics: Creating Observables from scratch](https://egghead.io/series/rxjs-beyond-the-basics-creating-observables-from-scratch) - Egghead series by Andr?? Staltz
*   [RxJS Beyond the Basics: Operators in Depth](https://egghead.io/series/rxjs-beyond-the-basics-operators-in-depth) - Egghead series by Andr?? Staltz

[](#hot-vs-cold-observables)Hot vs Cold Observables
---------------------------------------------------

[Paul Taylor](https://twitter.com/trxcllnt) (RxJS 5 Contributor) with the best explanation of Hot & Cold Observables yet. [https://github.com/ReactiveX/RxJS/issues/1121#issuecomment-169568428](https://github.com/ReactiveX/RxJS/issues/1121#issuecomment-169568428)

> ... "cold" and "hot" don't refer to unicast vs. multicast, they refer to the state of the computation. An Observable represents an asynchronous computation (aka, it's a function that can return multiple values between now and infinity).

> "Cold" Observables are just like functions which haven't been called (subscribed to) yet. Each time you call it (aka, subscribe to it), you're re-running whatever calculation the Observable performs.

> "Hot" Observables are just regular cold Observables that you've shoved a Subject between you and the cold Observable source. When you subscribe to it, you're really subscribing to the Subject over and over. Subjects can have any number of Observers (just like EventEmitter, etc.), but the original cold source has only one Observer (the Subject that's sitting between you and the source).

[](#rxjs-5-vs-rxjs-4)RxJS 5 vs RxJS 4
-------------------------------------

[ReactiveX/RxJS](https://github.com/ReactiveX/RxJS) - (RxJS 5)

> This rewrite is meant to have better performance, better modularity, better debuggable call stacks, while staying mostly backwards compatible, with some breaking changes that reduce the API surface.

[Reactive-Extensions/RxJS](https://github.com/Reactive-Extensions/RxJS) - (RxJS 4)

> ...is a set of libraries to compose asynchronous and event-based programs using observable collections and Array#extras style composition in JavaScript

[](#libraries-built-with-rxjs)Libraries Built with RxJS
-------------------------------------------------------

*   [arkverse/lell](https://github.com/arkverse/lell) - Reactive state, no boilerplate, just init and subscribe
*   [Cycle.js](https://cycle.js.org) - A fully reactive JavaScript framework for Human-Computer Interaction.
*   [ds300/derivablesjs](https://github.com/ds300/derivablejs) - Functional Reactive State for JavaScript and TypeScript
*   [WebRx](https://webrx.org) - The Browser-based MVVM-Framework for ReactiveX-powered Single Page Applications.
*   [Angular2](https://angular.io/) - Angular is a development platform for building mobile and desktop applications
*   [garbles/yolk](https://github.com/garbles/yolk) - ![egg](https://github.githubassets.com/images/icons/emoji/unicode/1f95a.png) A library for building asynchronous user interfaces.
*   [bcoop713/routerx](https://github.com/bcoop713/routerx) - A Router for RxJS and Cycle.js applcations
*   [ngrx/store](https://github.com/ngrx/store) - RxJS powered state management inspired by Redux for Angular2

[](#talks)Talks
---------------

*   [Reactive JavaScript at Netflix, Microsoft and the World](https://www.youtube.com/watch?v=KOOT7BArVHQ) - Matthew Podwysocki (Dec 2015)
*   [What if the user was a function?](https://www.youtube.com/watch?v=1zj7M1LnJV4) - Andre Staltz (Jun 2015)
*   [Controlling Time and Space: understanding the many formulations of FRP](https://www.youtube.com/watch?v=Agu6jipKfYw) - Evan Czaplicki (Sep 2014)

[](#articles)Articles
---------------------

*   [Containers Are Dead. Long Live Observable Combinators](https://medium.com/@milankinen/containers-are-dead-long-live-observable-combinators-2cb0c1f06c96#.4e639jlf5) - Matti Lankinen (Nov 2015)
*   [Angular - Introduction to Reactive Extensions (RxJS)](https://medium.com/google-developer-experts/angular-introduction-to-reactive-extensions-rxjs-a86a7430a61f#.4xdsm88gq) - gsans (Sep 2015)
*   [A Dead-Simple Todo List with RxJS](http://blog.edanschwartz.com/2015/09/18/dead-simple-rxjs-todo-list) - Edan Schwartz (Sep 2015)
*   [Imposs??vel errar com RxJS e Redux](https://medium.com/@tiagosemoh/imposs%C3%ADvel-errar-com-rxjs-e-redux-7876459c0044) (pt-BR) Tiago Miranda (Mar 2018)

[](#examples)Examples
---------------------

*   [Awesome example of combineLatest](https://jsbin.com/padutujasu/edit?js,output) from [@xgrommx](https://twitter.com/xgrommx)

[](#testing)Testing
-------------------

*   [How To Debug RxJS Code](http://staltz.com/how-to-debug-rxjs-code.html) - Andre Staltz (Dec 2015)
*   [Testing reactive code](https://glebbahmutov.com/blog/testing-reactive-code/) - Dr. Gleb Bahmutov (Feb 2016)
*   [Testing your Rx application](https://github.com/Reactive-Extensions/RxJS/blob/master/doc/gettingstarted/testing.md) - RxJS documentation
*   [RxJs Testing in Real World Applications](https://blog.hyphe.me/rxjs-testing-in-real-world-applications/) - Simon Jentsch (Feb 2016)

[](#references)References
-------------------------

*   [Online gitbook rx-book](https://xgrommx.github.io/rx-book/index.html)
*   [xgrommx/awesome-functional-programming](https://github.com/xgrommx/awesome-functional-programming)

[](#people)People
-----------------

*   [Ben Lesh @BenLesh](https://twitter.com/BenLesh) - Lead Maintainer of RxJS 5
*   [Andr?? Staltz @andrestaltz](https://twitter.com/andrestaltz) - Creator of Cycle.js
*   [Jafar Husain @jhusain](https://twitter.com/jhusain) - Technical Lead at Netflix, used to work at microsoft on Rx
*   [Matt Podwysocki @mattpodwysocki](https://twitter.com/mattpodwysocki) - Works at Netflix with Jafar on ReactiveX stuff
*   [Erik Meijer @headinthebox](https://twitter.com/headinthebox) - Functional Programming Wizard
*   [ReactiveX Offical Twitter](https://twitter.com/ReactiveX) - Official ReactiveX/Rx twitter
*   [David Sheldrick @djsheldrick](https://twitter.com/djsheldrick) - Creator of Derivables.js
*   [Paul Taylor](https://twitter.com/trxcllnt) - RxJS 5 Contributor

[](#community)Community
-----------------------

*   [RxJS Gitter](https://gitter.im/Reactive-Extensions/RxJS)
*   [RxJS StackOverflow](https://stackoverflow.com/questions/tagged/rxjs)

[](#react--rxjs)React & RxJS
----------------------------

*   [https://github.com/jas-chen/thisless-react](https://github.com/jas-chen/thisless-react)
*   [FrintJS](https://frint.js.org): Build reactive and scalable applications with RxJS and React

[](#angular2--rxjs)Angular2 & RxJS
----------------------------------

*   [http://blog.lambda-it.ch/reactive-data-flow-in-angular-2/](http://blog.lambda-it.ch/reactive-data-flow-in-angular-2/)
*   [https://coryrylan.com/blog/angular-2-observable-data-services](https://coryrylan.com/blog/angular-2-observable-data-services)

[](#other-reactive-programming-libraries)Other Reactive Programming Libraries
-----------------------------------------------------------------------------

*   [baconjs/bacon.js](https://github.com/baconjs/bacon.js) - FRP (functional reactive programming) library for Javascript.
*   [pozadi/kefir](https://github.com/pozadi/kefir) - FRP library for JavaScript inspired by Bacon.js and RxJS with focus on high performance and low memory consumption.
*   \[Highland.js\] ([http://highlandjs.org/](http://highlandjs.org/)) - Re-thinking the JavaScript utility belt, Highland manages synchronous and asynchronous code easily, using nothing more than standard JavaScript and Node-like Streams.
*   [cujojs/most](https://github.com/cujojs/most) - high performance FRP library.

[](#sources)Sources
-------------------

### [](#4x)4.x

[https://cdnjs.com/libraries/rxjs/](https://cdnjs.com/libraries/rxjs/)

### [](#5x)5.x

[https://unpkg.com/@reactivex/rxjs@5.0.0-beta.12/dist/global/Rx.js](https://unpkg.com/@reactivex/rxjs@5.0.0-beta.12/dist/global/Rx.js)
 