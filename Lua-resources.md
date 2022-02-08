# Lua

Lua (/ˈluːə/ LOO-ə; from Portuguese: lua [ˈlu.(w)ɐ] meaning moon) is a lightweight, high-level, multi-paradigm programming language designed primarily for embedded use in applications.[3] Lua is cross-platform, since the interpreter of compiled bytecode is written in ANSI C,[4] and Lua has a relatively simple C API to embed it into applications.[5]

Lua was originally designed in 1993 as a language for extending software applications to meet the increasing demand for customization at the time. It provided the basic facilities of most procedural programming languages, but more complicated or domain-specific features were not included; rather, it included mechanisms for extending the language, allowing programmers to implement such features. As Lua was intended to be a general embeddable extension language, the designers of Lua focused on improving its speed, portability, extensibility, and ease-of-use in

  
[](#packages)Packages
---------------------

*   [Implementations, Interpreters, and Bindings](#implementations-interpreters-and-bindings)
*   [Package Managers](#package-managers)
*   [Build Tools and Standalone Makers](#build-tools-and-standalone-makers)
*   [Debugging and Profiling](#debugging-and-profiling)
*   [IDEs and Plugins](#ides-and-plugins)
*   [Utility Belts](#utility-belts)
*   [Game Engines](#game-engines)
*   [Game Development](#game-development)
*   [Logging](#logging)
*   [Web/Networking Platforms](#webnetworking-platforms)
*   [OpenResty](#openresty)
*   [Command-line Utilities](#command-line-utilities)
*   [Concurrency and Multithreading](#concurrency-and-multithreading)
*   [Templating](#templating)
*   [Documentation](#documentation)
*   [Object-oriented Programming](#object-oriented-programming)
*   [File system and OS](#file-system-and-os)
*   [Time and Date](#time-and-date)
*   [Image Manipulation](#image-manipulation)
*   [Digital Signal Processing](#digital-signal-processing)
*   [Hardware and Embedded Systems](###hardware-and-embedded-systems)
*   [Math and Scientific Computing](#math-and-scientific-computing)
*   [Parsing and Serialization](#parsing-and-serialization)
*   [Humanize](#humanize)
*   [Compression](#compression)
*   [Cryptography](#cryptography)
*   [Network](#network)
*   [Data Stores](#data-stores)
*   [Message Brokers](#message-brokers)
*   [Testing](#testing)
*   [Foreign Function Interfaces](#foreign-function-interfaces)
*   [Analysis Tools and ASTs](#analysis-tools-and-asts)
*   [Experimental, etc](#experimental-etc)
*   [Scriptable by Lua](#scriptable-by-lua)
*   [Miscellaneous](#miscellaneous)

[](#resources)Resources
-----------------------

*   [Community](#community)
*   [References](#references)
*   [Style Guides](#style-guides)
*   [Tutorials](#tutorials)
*   [Articles](#articles)
*   [Talks & Slides](#talks--slides)
*   [Books](#books)
*   [Other Lists](#other-lists)

### [](#implementations-interpreters-and-bindings)Implementations, Interpreters, and Bindings

*   [Lua](http://www.lua.org/download.html) - Lua's original ANSI C interpreter.
    *   [Lua Repo](https://github.com/lua/lua) - The official Lua repo, as seen by the Lua team, mirrored to GitHub.
*   [LuaJIT](http://luajit.org/luajit.html) - High-performance Just-In-Time compiler for Lua.
*   [LLVM-Lua](https://github.com/neopallium/llvm-lua) - Compiles Lua to LLVM.
*   [lua.vm.js](https://github.com/daurnimator/lua.vm.js) - Lua VM on the web; a direct port of the C interpreter via LLVM, emscripten, and asm.js.
*   [Moonshine](https://github.com/gamesys/moonshine) - A Lua VM implemented in JavaScript. Slower than lua.vm.js, but with better docs, examples, and JS interfacing.
*   [Fengari](https://fengari.io/) - The Lua VM rewritten in Javascript with seamless JS and DOM interoperability.
*   [MoonSharp](https://github.com/xanathar/moonsharp) - A Lua interpreter written entirely in C# for the .NET, Mono and Unity platforms.
*   [UniLua](https://github.com/xebecnan/UniLua) - A pure C# implementation of Lua 5.2, focused on compatibility with the Unity game engine.
*   [lupa](https://github.com/scoder/lupa) - Python bindings to LuaJIT2.
*   [golua](https://github.com/aarzilli/golua) - Golang bindings to the Lua C API.
*   [GopherLua](https://github.com/yuin/gopher-lua) - Lua 5.1 VM and compiler implemented in Go with Go APIs.
*   [LuaBridge](https://github.com/vinniefalco/LuaBridge) - A lightweight library for mapping data, functions, and classes back and forth between C++ and Lua.

Note: From LuaJIT to Lua to lua.vm.js to Moonshine, a basic benchmark sees performance drop by roughly a factor of 6 with each hop.

### [](#package-managers)Package Managers

*   [LuaRocks](https://luarocks.org/) - De-facto tool for installing Lua modules as packages called "rocks", plus public rock repository and website. Much like npm or pip.

### [](#build-tools-and-standalone-makers)Build Tools and Standalone Makers

*   [Lake](https://github.com/stevedonovan/Lake) - A build engine written in Lua, similar to Ruby's rake.
*   [Luabuild](https://github.com/stevedonovan/luabuild) - Highly customizable Lua 5.2 build system.
*   [luastatic](https://github.com/ers35/luastatic) - Simple tool for turning Lua programs into standalone executables.
*   [omnia](https://github.com/tongson/omnia) - A batteries-included creator of standalone executables, built on top of luastatic.

### [](#debugging-and-profiling)Debugging and Profiling

*   [ProFi](https://gist.github.com/perky/2838755) - Simple profiler that works with LuaJIT and produces a report file.
*   [luatrace](https://github.com/geoffleyland/luatrace) - Toolset for tracing/analyzing/profiling script execution and generating detailed reports.
*   [StackTracePlus](https://github.com/ignacio/StackTracePlus) - Drop-in upgrade to Lua's stack traces which adds local context and improves readability.
*   [MobDebug](https://github.com/pkulchenko/MobDebug) - Powerful remote debugger with breakpoints and stack inspection. Used by ZeroBraneStudio.
*   [lovebird](https://github.com/rxi/lovebird) - Browser-based debug console. Originally made for LÖVE, but works in any project with LuaSocket support.

### [](#ides-and-plugins)IDEs and Plugins

*   [Lua Development Tools](https://eclipse.org/ldt/) - Eclipse plugin which provides code completion, debugging, and more. Built on Metalua.
*   [Lua for IDEA](https://bitbucket.org/sylvanaar2/lua-for-idea/wiki/Home) - IntelliJ IDEA plugin which, among other things, provides code completion, smart highlighting, and experimental debugging.
*   [ZeroBraneStudio](https://studio.zerobrane.com/) - Lightweight, customizable, cross-platform Lua-dedicated IDE with code completion and analysis, written in Lua. Has broad debugging support for numerous Lua engines.
*   [BabeLua](https://archive.codeplex.com/?p=babelua) - Lua editor/debugger extension for VS2012-13 with highlighting, auto-completion, linting, and formatting capabilities.
*   [lua-mode](https://github.com/immerrr/lua-mode) - Emacs major mode for editing Lua.
*   [vscode-lua](https://github.com/trixnz/vscode-lua) - VSCode intellisense and linting.

### [](#utility-belts)Utility Belts

*   [Lua Fun](https://github.com/luafun/luafun) - High-performance functional programming library designed for LuaJIT.
*   [Moses](https://github.com/Yonaba/Moses) - Functional programming utility belt, inspired by Underscore.js.
*   [Penlight](https://github.com/stevedonovan/Penlight) - Broad, heavyweight utility library, inspired by Python's standard libs. Provides the batteries that Lua doesn't.
*   [lua-stdlib](https://github.com/lua-stdlib/lua-stdlib) - Middle-weight standard library extension; adds some useful data structures, utility functions, and basic functional stuff.
*   [Microlight](https://github.com/stevedonovan/Microlight) - A little library of useful Lua functions; the 'extra light' version of Penlight.
*   [compat53](https://luarocks.org/modules/siffiejoe/compat53) - Compatibility module providing Lua-5.3-style APIs for Lua 5.2 and 5.1.
*   [RxLua](https://github.com/bjornbytes/RxLua) - Reactive Extensions, Observables, etc.

### [](#game-engines)Game Engines

*   [LÖVE 2D](http://love2d.org/) - Desktop game development platform. Cross-platform, feature-complete, well-adopted.
*   [Corona SDK](https://coronalabs.com/) - Development platform for iOS and Android. Proprietary, but used by numerous top games and apps, totaling over 150 million downloads.
*   [MOAI](http://getmoai.com/) - Open source, cross-platform, mobile game development framework. Minimalist C++ engine powered by Lua scripting.
*   [Drystal](https://drystal.github.io/) - Open source, games can run on Linux or on any platform with a recent web browser.
*   [Amulet](http://www.amulet.xyz/) - Open source, audio/visual toolkit suitable for small games and experimentation. It runs on Windows, Mac, Linux, HTML5 and iOS.
*   [LÖVR](https://lovr.org) - 3D framework for creating virtual reality experiences, inspired by LÖVE 2D.

### [](#game-development)Game Development

*   Corona
    *   [Coronium](https://develephant.github.io/coronium-core-docs/) - Simple cloud platform supporting analytics, data objects, user management, and more.
*   LÖVE
    *   [awesome-love2d](https://github.com/love2d-community/awesome-love2d) - A list like this one, but focused on game dev and the LÖVE platform.
    *   [lurker](https://github.com/rxi/lurker) - Shortens the iteration cycle by auto-swapping changed Lua files in a running LÖVE project.
    *   [HUMP](http://vrld.github.io/hump/) - A set of lightweight helpers for LÖVE; a game-oriented utility belt.
*   MOAI
    *   [moaifiddle](https://moaifiddle.com) - Edit and share short scripts for the MOAI game engine and run them in the browser using WebGL.
*   [Jumper](https://github.com/Yonaba/Jumper) - Fast, lightweight, and easy-to-use pathfinding library for grid-based games.
*   [lume](https://github.com/rxi/lume/) - Utility belt library geared toward game development.
*   [NoobHub](https://github.com/Overtorment/NoobHub) - Network multiplayer for Corona, LÖVE, and more, following a simple pub-sub model.
*   Collision detection
    *   [bump.lua](https://github.com/kikito/bump.lua) - Minimal rectangle-based collision detection which handles tunnelling and basic collision resolution.
    *   [HardonCollider](http://vrld.github.io/HardonCollider/) - Detect collisions between arbitrarily positioned and rotated shapes of any type.
*   Tweening
    *   [flux](https://github.com/rxi/flux) - A fast, lightweight tweening library for Lua with easing functions and the ability to group tweens together.
    *   [tween.lua](https://github.com/kikito/tween.lua) - Small library for tweening, with several easing functions.
*   Examples
    *   [termtris](https://github.com/tylerneylon/termtris) - A tetris clone, written in literate style with "an emphasis on learn-from-ability".
    *   [PacPac](https://github.com/tylerneylon/pacpac) - A Pac-man clone, made with LÖVE.
    *   [Mari0](https://github.com/Stabyourself/mari0) - Fusion of Mario and Portal, made with LÖVE. See also its [wikipedia entry](https://en.wikipedia.org/wiki/Mari0).
    *   [Journey to the Center of Hawkthorne](https://github.com/hawkthorne/hawkthorne-journey) - 2D platformer based on Community's [Digital Estate Planning](https://en.wikipedia.org/wiki/Digital_Estate_Planning) episode, made with LÖVE.

### [](#logging)Logging

*   [lua-log](https://github.com/moteus/lua-log) - Asynchronous logging library with pluggable writers for file system, network, ZeroMQ, and more.
*   [LuaLogging](https://github.com/Neopallium/lualogging) - Log4j-inspired logging library supporting various appenders.
*   [luasyslog](https://luarocks.org/modules/luarocks/luasyslog) - Log to syslog, based on LuaLogging.

### [](#webnetworking-platforms)Web/Networking Platforms

*   [OpenResty](http://openresty.org/en/) - A fast and scalable web application platform created by extending Nginx with Lua. Today's de-facto Lua web platform, used heavily by Cloudflare, Taobao, Tencent, and others.
*   [turbo](https://turbo.readthedocs.io/en/latest/) - Event-driven, non-blocking, LuaJIT-based networking suite and framework, inspired by Tornado.
*   [Kepler Project](https://github.com/keplerproject) - A collection of web-oriented projects using a common set of standards and components.
*   [Pegasus.lua](https://github.com/EvandroLG/pegasus.lua) - Pegasus.lua is a http server to work with web applications written in Lua language.

### [](#openresty)OpenResty

*   [awesome-resty](https://github.com/bungle/awesome-resty) - A list like this one, but focused on OpenResty.
*   Core platform
    *   [ngx\_lua](https://www.nginx.com/resources/wiki/modules/lua/) - The core piece of OpenResty. Embeds Lua in Nginx and exposes, among other things, the cosocket API for non-blocking sockets (compatible with LuaSocket's API).
    *   [OpenResty GitHub Organization](https://github.com/openresty) - Home of the repositories for ngx\_lua, ngx\_openresty, and many related modules.
*   Third-party modules
    *   [lua-resty-http](https://github.com/pintsized/lua-resty-http) - Lua HTTP client driver, built on the cosocket API.
*   Frameworks & tools
    *   [Lapis](http://leafo.net/lapis/) - Full-stack framework for Lua and OpenResty. Like the Django or Rails of Lua. Supports Moonscript.
    *   [ledge](https://github.com/pintsized/ledge) - Lua module providing scriptable, RFC-compliant HTTP cache functionality.
    *   [Sailor](https://github.com/sailorproject/sailor) — An MVC web framework compatible with OpenResty, Apache and other webservers.
    *   [Kong](https://github.com/Kong/kong) - Microservice & API Management Layer.

Search this page for 'OpenResty' to find related packages under other categories (data stores in particular).

### [](#command-line-utilities)Command-line Utilities

*   [ansicolors](https://github.com/kikito/ansicolors.lua) - Simple function for printing to the console in color.
*   [cliargs](https://github.com/amireh/lua_cliargs) - A simple command-line argument parsing module.
*   [lua-term](https://github.com/hoelzro/lua-term) - Terminal operations and manipulations.
*   [argparse](https://github.com/mpeterv/argparse) - A feature-rich command line parser inspired by argparse for Python.

### [](#concurrency-and-multithreading)Concurrency and Multithreading

*   Coroutine-based multitasking:
    *   [Lumen](https://github.com/xopxe/Lumen) - Simple concurrent task scheduling.
    *   [ConcurrentLua](https://github.com/lefcha/concurrentlua) - Implements an Erlang-style message-passing concurrency model.
    *   [cqueues](http://25thandclement.com/~william/projects/cqueues.html) - Library for managing sockets, signals, and threads based on an event loop with coroutines.
*   Multithreading:
    *   [llthreads](https://github.com/Neopallium/lua-llthreads) - A simple wrapper for low-level pthreads & WIN32 threads.
    *   [llthreads2](https://github.com/moteus/lua-llthreads2) - Newer rewrite of llthreads.
    *   [lanes](https://github.com/LuaLanes/lanes) - Library implementing a message passing model with one OS thread per Lua thread.
    *   [luaproc](https://github.com/askyrme/luaproc) - Message-passing model which allows multiple threads per OS thread and easily generalizes across a network. See also [the paper](http://www.inf.puc-rio.br/~roberto/docs/ry08-05.pdf) where it originated.

For more on the differences (particularly between `lanes` and `luaproc`), see this [comparison](http://www.luteus.biz/Download/LoriotPro_Doc/LUA/LUA_For_Windows/lanes/comparison.html) of options; somewhat dated, but covers how each one works and the significant differences.

### [](#templating)Templating

*   [lustache](http://olivinelabs.com/lustache/) - Mustache template implementation.
*   [etlua](https://github.com/leafo/etlua) - Embedded Lua templates, ERB-style.
*   [lua-resty-template](https://github.com/bungle/lua-resty-template) - Lua-oriented template engine for OpenResty, somewhat Jinja-like.

### [](#documentation)Documentation

*   [LDoc](http://stevedonovan.github.io/ldoc/) - Documentation generator which modernizes and extends [LuaDoc](http://keplerproject.github.io/luadoc/).
*   [Locco](http://rgieseke.github.io/locco/) - Lua port of [Docco](http://ashkenas.com/docco/), the "quick-and-dirty, hundred-line-long, literate-programming-style documentation generator".
*   [docroc](https://github.com/bjornbytes/docroc) - Parse comments into a Lua table to generate documentation.

### [](#object-oriented-programming)Object-oriented Programming

*   [30log](https://github.com/Yonaba/30log) - Minimalist OOP library with basic classes, inheritance, and mixins in 30 lines.
*   [middleclass](https://github.com/kikito/middleclass) - Simple but robust OOP library with inheritance, methods, metamethods, class variables and mixins.

### [](#file-system-and-os)File system and OS

*   [LuaFileSystem](http://keplerproject.github.io/luafilesystem/) - Extends and complements Lua's built-in set of file system functions.
*   [luaposix](https://github.com/luaposix/luaposix) - Bindings for POSIX APIs, including curses.
*   [lunix](http://25thandclement.com/~william/projects/lunix.html) - Bindings to common Unix system APIs, striving for thread-safety.
*   [lua-path](https://github.com/moteus/lua-path) - File system path manipulation library.

### [](#time-and-date)Time and Date

*   [LuaDate](https://github.com/Tieske/date) - Date and time module with parsing, formatting, addition/subtraction, localization, and ISO 8601 support.
*   [cron.lua](https://github.com/kikito/cron.lua) - Time-related functions for Lua, inspired by JavaScript's setTimeout and setInterval.
*   [luatx](https://github.com/daurnimator/luatz) - Time, date, and timezone library.

### [](#image-manipulation)Image Manipulation

*   [magick](https://github.com/leafo/magick) - Lua bindings to ImageMagick for LuaJIT using FFI.

### [](#digital-signal-processing)Digital Signal Processing

*   [LuaFFT](https://github.com/h4rm/luafft) - An easy to use Fast Fourier Transformation package in pure Lua.
*   [Worp](http://worp.zevv.nl/about.html) - Sound/music/DSP engine written for LuaJIT.

### [](#hardware-and-embedded-systems)Hardware and Embedded Systems

*   [eLua](http://www.eluaproject.net/) - Lua, extended with optimizations and specific features for efficient and portable embedded software development.

### [](#math-and-scientific-computing)Math and Scientific Computing

*   [SciLua](http://scilua.org/) - Numerical/scientific computing framework built on LuaJIT, with an interface to R.
*   [Torch7](http://torch.ch/) - Scientific computing framework with wide support for machine learning algorithms, used by Facebook, Google, and more.
*   [lhf's Lua Tools](http://webserver2.tecgraf.puc-rio.br/~lhf/ftp/lua/) - Assorted libraries and tools, many math- or data-related.

### [](#parsing-and-serialization)Parsing and Serialization

*   JSON
    *   [lua-cjson](https://github.com/mpx/lua-cjson/) - Blazing fast JSON encoding/decoding implemented in C and exposed to Lua.
    *   [luajson](https://github.com/harningt/luajson) - JSON encoder/decoder implemented in Lua on top of LPeg.
    *   [dkjson](http://dkolf.de/src/dkjson-lua.fsl/home) - JSON encoder/decoder implemented in pure Lua.
    *   [json.lua](https://github.com/rxi/json.lua) - A fast and tiny JSON library in pure Lua.
*   XML
    *   [LuaExpat](https://matthewwild.co.uk/projects/luaexpat/) - SAX XML parser via binding to the Expat library.
    *   [SLAXML](https://github.com/Phrogz/SLAXML) - Pure Lua SAX-like streaming XML parser.
*   MessagePack
    *   [lua-MessagePack](https://github.com/fperrad/lua-MessagePack) - Pure Lua implementation of MessagePack.
    *   [lua-cmsgpack](https://github.com/antirez/lua-cmsgpack) - A MessagePack C implementation with Lua bindings, as used by Redis.=
*   LPeg
    *   [LPeg](http://www.inf.puc-rio.br/~roberto/lpeg/) - A pattern-matching library for Lua, based on Parsing Expression Grammars.
    *   [lpeg\_patterns](https://github.com/daurnimator/lpeg_patterns) - A collection of LPeg patterns.
    *   [LuLPeg](https://github.com/pygy/LuLPeg) - A pure Lua implementation of LPeg v0.12.
    *   [LPegLJ](https://github.com/sacek/LPegLJ) - A pure LuaJIT implementation of LPeg v1.0.
    *   [LPegLabel](https://github.com/sqmedeiros/lpeglabel) - An extension of LPeg adding support for labeled failures.
*   [lyaml](https://github.com/gvvaughan/lyaml) - YAML encoding/decoding via binding to LibYAML.
*   [lunamark](https://github.com/jgm/lunamark) - Converts Markdown to other textual formats including HTML and LaTeX. Uses LPeg for fast parsing.
*   [LXSH](https://github.com/xolox/lua-lxsh) - A collection of lexers and syntax highlighters written with LPeg.
*   [lua-pb](https://github.com/Neopallium/lua-pb) - Protocol Buffers implementation.

### [](#humanize)Humanize

*   [i18n.lua](https://github.com/kikito/i18n.lua) - Internationalization library with locales, formatting, and pluralization.
*   [inspect.lua](https://github.com/kikito/inspect.lua) - Human-readable representation of Lua tables.
*   [serpent](https://github.com/pkulchenko/serpent) - Serializer and pretty printer.
*   [Ser](https://github.com/gvx/Ser) - Dead simple serializer with good performance.
*   [say](https://github.com/Olivine-Labs/say) - Simple string key-value store for i18n.

### [](#compression)Compression

*   [lua-zlib](https://github.com/brimworks/lua-zlib) - Simple streaming interface to zlib for gzip/gunzip.
*   [lua-zip](https://github.com/brimworks/lua-zip) - Lua binding to libzip. Reads and writes zip files.

### [](#cryptography)Cryptography

*   [LuaCrypto](https://github.com/mkottman/luacrypto) - Lua bindings to OpenSSL.
*   [lua-lockbox](https://github.com/somesocks/lua-lockbox) - A collection of cryptographic primitives written in pure Lua.
*   [luatweetnacl](https://github.com/philanc/luatweetnacl) - Bindings to tweetnacl, modern high-security cryptographic library.
*   [luaossl](https://github.com/wahern/luaossl) - "Most comprehensive OpenSSL module in the Lua universe" - used by lapis, kong, and lua-http.

### [](#network)Network

*   [LuaSocket](https://github.com/diegonehab/luasocket) - Networking extension which provides a socket API for TCP and UDP, and implements HTTP, FTP, and SMTP.
*   [lua-websockets](https://github.com/lipp/lua-websockets) - WebSocket client and server modules. Webserver-agnostic, implemented in Lua on top of LuaSocket.
*   [lua-cURLv3](https://github.com/Lua-cURL/Lua-cURLv3) - Lua binding to libcurl.
*   [lua-http](https://github.com/daurnimator/lua-http) - Asynchronous HTTP and WebSocket library with client and server APIs, TLS, and HTTP/2; based on cqueues.

### [](#data-stores)Data Stores

*   [LuaSQL](http://keplerproject.github.io/luasql/) - Simple interface for connecting to ODBC, ADO, Oracle, MySQL, SQLite and PostgreSQL.
*   [pgmoon](https://github.com/leafo/pgmoon) - Lua PostgreSQL driver for OpenResty, LuaSocket, and cqueues.
*   [lua-resty-mysql](https://github.com/openresty/lua-resty-mysql) - Lua MySQL driver for OpenResty.
*   [lua-resty-cassandra](https://github.com/jbochi/lua-resty-cassandra) - Lua Cassandra client driver for OpenResty and others.
*   Redis
    *   [redis-lua](https://github.com/nrk/redis-lua) - Pure Lua client library for Redis.
    *   [lua-resty-redis](https://github.com/openresty/lua-resty-redis) - Lua Redis client driver for OpenResty.
    *   [lredis](https://github.com/daurnimator/lredis) - Asynchronous Redis client with pipelining and Pub/Sub support; based on cqueues.

### [](#message-brokers)Message Brokers

*   [lua-zmq](https://github.com/Neopallium/lua-zmq) - Lua bindings to ZeroMQ.
*   [lzmq](https://github.com/zeromq/lzmq) - A newer Lua binding to ZeroMQ.
*   [lua-resty-kafka](https://github.com/doujiang24/lua-resty-kafka) - Kafka client driver based on OpenResty cosockets.
*   [lua-resty-rabbitmqstomp](https://github.com/wingify/lua-resty-rabbitmqstomp) - RabbitMQ client library based on OpenResty cosockets.

### [](#testing)Testing

*   [busted](http://olivinelabs.com/busted/) - BDD-style unit testing framework with great docs and Moonscript support.
*   [telescope](https://github.com/norman/telescope) - Flexible and highly customizable testing library.
*   [luassert](https://github.com/Olivine-Labs/luassert) - Assertion library extending Lua's built-in assertions.
*   [lust](https://github.com/bjornbytes/lust) - Minimal test framework.

### [](#foreign-function-interfaces)Foreign Function Interfaces

*   [LuaJIT FFI](http://luajit.org/ext_ffi.html) - LuaJIT's mechanism for calling external C functions and using C data structures from pure Lua code.
*   [luaffi](https://github.com/jmckaskill/luaffi) - Standalone FFI library, compatible with the LuaJIT FFI interface.

### [](#analysis-tools-and-asts)Analysis Tools and ASTs

*   [luadec51](https://github.com/sztupy/luadec51) - Lua Decompiler for Lua version 5.1.
*   [luacov](http://keplerproject.github.io/luacov/) - Simple coverage analyzer, used by busted and telescope for checking test coverage.
    *   [luacov-coveralls](https://github.com/moteus/luacov-coveralls) - LuaCov reporter for coveralls.io.
*   [luacheck](https://github.com/mpeterv/luacheck) - Simple static analyzer which detects accidental globals and undefined or shadowed locals.
*   [Metalua](https://github.com/fab13n/metalua) - Pure Lua parser and compiler, used for generating ASTs. A number of other tools make use of the Metalua parser in this way.
*   [LuaInspect](https://github.com/davidm/lua-inspect) - Lua's most powerful code analysis and linting tool, built on Metalua. Used by ZeroBraneStudio, among others.
*   [LuaMinify](https://github.com/stravant/LuaMinify) - Minifier which also brings its own static analysis tools, lexer, and parser.
*   [Typed Lua](https://github.com/andremm/typedlua) - A typed superset of Lua that compiles to plain Lua.
*   [lua-parser](https://github.com/andremm/lua-parser) - A Lua 5.3 parser written using LPegLabel, with improved error messages.

### [](#experimental-etc)Experimental, etc

*   [punchdrunk.js](https://github.com/TannerRogalsky/punchdrunk) - Moonshine + LÖVE API reimplementation = run LÖVE games in the browser.
*   [luvit](https://github.com/luvit/luvit) - Node.js's underlying architecture (libUV) with Lua on top instead of JavaScript.
*   [graphql-lua](https://github.com/bjornbytes/graphql-lua) - Lua implementation of [GraphQL](http://graphql.org/).

### [](#scriptable-by-lua)Scriptable by Lua

*   [luakit](https://luakit.github.io/luakit/) - Fast, small, webkit based browser framework extensible by Lua.
*   [Hammerspoon](http://www.hammerspoon.org) - A powerful, extensible OS X automation tool. A community-maintained fork of [Mjolnir](http://www.mjolnir.io/).
*   [kpie](https://github.com/skx/kpie) - A scripting utility to juggle windows.
*   [lumail](https://lumail.org/) - A console-based mail client, with extensive scripting capabilities.
*   [AwesomeWM](https://awesomewm.org/) - A highly configurable and extensible window manager for X, scripted and configured by Lua.
*   [Textadept](https://foicica.com/textadept/) - Extremely lightweight, customizable, cross-platform editor, written (mostly) in (and scripted by) Lua.
*   [KoReader](https://github.com/koreader/koreader) - An ebook reader application supports PDF, DJVU, EPUB, FB2 and much more, running on Kindle, Kobo, PocketBook and Android devices.

### [](#miscellaneous)Miscellaneous

*   [MoonScript](http://moonscript.org/) - Moonscript is a dynamic scripting language that compiles to Lua. It reduces verbosity and provides a rich set of features like comprehensions and classes. Its author calls it 'CoffeeScript for Lua'.
*   [sitegen](http://leafo.net/sitegen/) - A static site generator which uses MoonScript and supports HTML and Markdown, page grouping, and plugins.

[](#resources-1)Resources
-------------------------

### [](#community)Community

*   [lua-l](http://www.lua.org/lua-l.html) - The official Lua mailing list, and one of the focal points of the Lua community.
*   [Lua.Space](http://lua.space/) - The Lua community blog.
*   [Lua Users Foundation](https://github.com/lua-users-foundation) - An association of individuals with the mission of supporting and promoting Lua and its community and ecosystems.
*   [lua-users.org](http://lua-users.org/) - A site for and by users of Lua, featuring an IRC channel, a web archive of lua-l, and a large wiki.
*   Conferences/Meetups
    *   [Lua Workshop](https://www.lua.org/community.html#workshop) - Annual 2-day meeting of the Lua community, in rotating locations.
    *   [Lua Conf](http://luaconf.com/) - Annual 1-day Lua conference in Brazil.
    *   [FOSDEM](https://fosdem.org/) - Annual 2-day gathering of F/OSS developers in Brussels which sometimes has a "Lua devroom".

### [](#references)References

*   [Reference Manual](http://www.lua.org/manual/5.3/) - The official definition of the Lua language.
*   [lua-users wiki](http://lua-users.org/wiki/) - A large community-maintained collection of Lua information and resources, supplementing the official website.
*   [Lua Unofficial FAQ](http://www.luafaq.org/) - Answers all sorts of Lua-related questions, including many of the form 'How to \_\_\_?'.

### [](#glossaries)Glossaries

*   [Lua 5.3 Glossary](https://rawgit.com/dlaurie/lua-notes/master/glossary.html) - A glossary of some essential Lua terms.

### [](#style-guides)Style Guides

*   [Lua-users style guide](http://lua-users.org/wiki/LuaStyleGuide) - A general, high-level style guide; unopinionated, easily agreed on.
*   [Olivine style guide](https://github.com/Olivine-Labs/lua-style-guide) - A more opinionated and specific, and therefore more rigorous, guide.

### [](#tutorials)Tutorials

*   [Lua Crash Course](http://www.coppeliarobotics.com/helpFiles/en/luaCrashCourse.htm) - Short crash course readover, or reference for when you forget the basics.
*   [Learn Lua in 15 Minutes](http://tylerneylon.com/a/learn-lua/) - A well-commented example file which covers the basics.
*   [Learning Lua from JS](http://phrogz.net/lua/LearningLua_FromJS.html) - An overview of the similarities and differences between Lua and JS; a great start for JavaScript folks looking to pick up Lua.
*   [lua-users tutorial](http://lua-users.org/wiki/LuaTutorial) - In-depth collection of tutorials aimed at newcomers.
*   [Lua Missions](https://github.com/kikito/lua_missions) - A series of 'Missions' to work through which are designed to teach aspects of Lua along the way.
*   [Creating an Image Server](http://leafo.net/posts/creating_an_image_server.html) - Walks through setting up and using OpenResty to build a simple image processing server; a great starting point for playing with OpenResty.

### [](#articles)Articles

*   [Embedding Lua in C](https://debian-administration.org/article/264/Embedding_a_scripting_language_inside_your_C/C_code) - An introductory walkthrough of embedding Lua in a C program. A bit dated, but still a great walkthrough.
*   [Lua: Good, bad, and ugly parts](http://notebook.kulchenko.com/programming/lua-good-different-bad-and-ugly-parts) - A thorough summary of the good, different, bad, and ugly aspects of Lua, including many subtle quirks, by the author of ZeroBraneStudio.
*   [Lua states, libraries, coroutines and memory](http://www.thijsschreijer.nl/blog/?p=693) - Diagrams and explains some more advanced concepts of the Lua VM, particularly when interfacing with C.

### [](#talks--slides)Talks & Slides

*   [Roberto's Talks](http://www.inf.puc-rio.br/~roberto/talks/index.html) - History of talks given by Lua's chief architect, with slides for each.
*   [Lua Workshop Talks](http://www.lua.org/wshop14.html#abstracts) - High-quality talks are given at each ~annual Lua Workshop, and a history of them is online, slides included.

### [](#books)Books

*   [Programming in Lua](http://www.lua.org/pil/) - The authoritative intro to all aspects of Lua programming, written by Lua's chief architect. Three editions released; first edition available online.
*   [Lua Quick Reference](https://foicica.com/lua/) - A quick reference on how to program in and embed Lua 5.1 through 5.3, by the creator of Textadept.
*   [Programming Gems](http://www.lua.org/gems/) - A collection of articles covering existing wisdom and practices on programming well in Lua, in a broad variety of use cases.
*   [Lua Programming](https://en.wikibooks.org/wiki/Lua_Programming) - A shorter overview of the language, up to date for Lua 5.2, and available online.

### [](#other-lists)Other Lists

*   [awesome-resty](https://github.com/bungle/awesome-resty) - A list like this one, but focused on OpenResty.
*   [awesome-love2d](https://github.com/love2d-community/awesome-love2d) - A list like this one, but focused on game dev and the LÖVE platform.
*   [Where Lua is Used](https://sites.google.com/site/marbux/home/where-lua-is-used) - A comprehensive list of stand-alone programs written in or extensible using Lua.
 

*   [apache/apisix](https://github.com/apache/apisix) - The Cloud-Native API Gateway
*   [NvChad/NvChad](https://github.com/NvChad/NvChad) - An attempt to make neovim cli as functional as an IDE while being very beautiful, blazing fast.
*   [LunarVim/LunarVim](https://github.com/LunarVim/LunarVim) - An IDE layer for Neovim with sane defaults. Completely free and community driven.
*   [rxi/lite](https://github.com/rxi/lite) - A lightweight text editor written in Lua
*   [nmap/nmap](https://github.com/nmap/nmap) - Nmap - the Network Mapper. Github mirror of official SVN repository.
*   [alexazhou/VeryNginx](https://github.com/alexazhou/VeryNginx) - A very powerful and friendly nginx base on lua-nginx-module( openresty ) which provide WAF, Control Panel, and Dashboards.
*   [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim) - Find, Filter, Preview, Pick. All lua, all the time.
*   [awesomeWM/awesome](https://github.com/awesomeWM/awesome) - awesome window manager
*   [loveshell/ngx\_lua\_waf](https://github.com/loveshell/ngx_lua_waf) - ngx\_lua\_waf是一个基于lua-nginx-module(openresty)的web应用防火墙
*   [luvit/luvit](https://github.com/luvit/luvit) - Lua + libUV + jIT = pure awesomesauce
*   [tarantool/tarantool](https://github.com/tarantool/tarantool) - Get your data in RAM. Get compute close to data. Enjoy the performance.
*   [leafo/moonscript](https://github.com/leafo/moonscript) - ![crescent_moon](https://github.githubassets.com/images/icons/emoji/unicode/1f319.png) A language that compiles to Lua
*   [lcpz/awesome-copycats](https://github.com/lcpz/awesome-copycats) - Awesome WM themes
*   [luarocks/luarocks](https://github.com/luarocks/luarocks) - LuaRocks is the package manager for the Lua programming language.
*   [OpenNMT/OpenNMT](https://github.com/OpenNMT/OpenNMT) - Open Source Neural Machine Translation in Torch (deprecated)
*   [scipag/vulscan](https://github.com/scipag/vulscan) - Advanced vulnerability scanning with Nmap NSE
*   [pkulchenko/ZeroBraneStudio](https://github.com/pkulchenko/ZeroBraneStudio) - Lightweight Lua-based IDE for Lua with code completion, syntax highlighting, live coding, remote debugger, and code analyzer; supports Lua 5.1, 5.2, 5.3, 5.4, LuaJIT and other Lua interpreters on Windows, macOS, and Linux
*   [skywind3000/z.lua](https://github.com/skywind3000/z.lua) - ![zap](https://github.githubassets.com/images/icons/emoji/unicode/26a1.png) A new cd command that helps you navigate faster by learning your habits.
*   [wbthomason/packer.nvim](https://github.com/wbthomason/packer.nvim) - A use-package inspired plugin manager for Neovim. Uses native packages, supports Luarocks dependencies, written in Lua, allows for expressive config
*   [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp) - A completion plugin for neovim coded in Lua.
*   [lite-xl/lite-xl](https://github.com/lite-xl/lite-xl) - A lightweight text editor written in Lua
*   [nvim-neorg/neorg](https://github.com/nvim-neorg/neorg) - Modernity meets insane extensibility. The future of organizing your life in Neovim.
*   [auto-ssl/lua-resty-auto-ssl](https://github.com/auto-ssl/lua-resty-auto-ssl) - On the fly (and free) SSL registration and renewal inside OpenResty/nginx with Let's Encrypt.
*   [yuanfengyun/qipai\_algorithm](https://github.com/yuanfengyun/qipai_algorithm) - 棋牌的胡牌算法，包括麻将、跑胡子、扑克。实现 lua 、c++ 、c# 、golang 、js 、java 、python 版本。( Mahjong algorithm )
*   [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua) - A file explorer tree for neovim written in lua
*   [luafun/luafun](https://github.com/luafun/luafun) - Lua Fun is a high-performance functional programming library for Lua designed with LuaJIT's trace compiler in mind.
*   [ledgetech/lua-resty-http](https://github.com/ledgetech/lua-resty-http) - Lua HTTP client cosocket driver for OpenResty / ngx\_lua.
*   [openresty/lua-resty-redis](https://github.com/openresty/lua-resty-redis) - Lua redis client driver for the ngx\_lua based on the cosocket API
*   [luakit/luakit](https://github.com/luakit/luakit) - Fast, small, webkit based browser framework extensible by Lua.
*   [mpeterv/luacheck](https://github.com/mpeterv/luacheck) - A tool for linting and static analysis of Lua code.
*   [kikito/middleclass](https://github.com/kikito/middleclass) - Object-orientation for Lua
*   [lunarmodules/Penlight](https://github.com/lunarmodules/Penlight) - A set of pure Lua libraries focusing on input data handling (such as reading configuration files), functional programming (such as map, reduce, placeholder expressions,etc), and OS path management. Much of the functionality is inspired by the Python standard libraries.
*   [hrsh7th/nvim-compe](https://github.com/hrsh7th/nvim-compe) - Auto completion Lua plugin for nvim
*   [starwing/lua-protobuf](https://github.com/starwing/lua-protobuf) - A Lua module to work with Google protobuf
*   [a327ex/BYTEPATH](https://github.com/a327ex/BYTEPATH) - A replayable arcade shooter with a focus on build theorycrafting.
*   [folke/trouble.nvim](https://github.com/folke/trouble.nvim) - ![vertical_traffic_light](https://github.githubassets.com/images/icons/emoji/unicode/1f6a6.png) A pretty diagnostics, references, telescope results, quickfix and location list to help you solve all the trouble your code is causing.
*   [rxi/json.lua](https://github.com/rxi/json.lua) - A lightweight JSON library for Lua
*   [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim) - A blazing fast and easy to configure neovim statusline plugin written in pure lua.
*   [sile-typesetter/sile](https://github.com/sile-typesetter/sile) - Simon’s Improved Layout Engine
*   [sumneko/lua-language-server](https://github.com/sumneko/lua-language-server) - Lua Language Server coded by Lua
*   [nvim-orgmode/orgmode](https://github.com/nvim-orgmode/orgmode) - Orgmode clone written in Lua for Neovim 0.5+.
*   [knyar/nginx-lua-prometheus](https://github.com/knyar/nginx-lua-prometheus) - Prometheus metric library for Nginx written in Lua
*   [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim) - Git integration for buffers
*   [Olivine-Labs/busted](https://github.com/Olivine-Labs/busted) - Elegant Lua unit testing.
*   [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim) - ![cityscape](https://github.githubassets.com/images/icons/emoji/unicode/1f3d9.png) A clean, dark Neovim theme written in Lua, with support for lsp, treesitter and lots of plugins. Includes additional themes for Kitty, Alacritty, iTerm and Fish.
*   [unixhot/waf](https://github.com/unixhot/waf) - 使用Nginx+Lua实现的WAF（版本v1.0）
*   [starjun/openstar](https://github.com/starjun/openstar) - lua waf,nginx+lua,openresty,luajit,waf+,cdn,nginx
*   [teal-language/tl](https://github.com/teal-language/tl) - The compiler for Teal, a typed dialect of Lua
*   [norcalli/nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua) - The fastest Neovim colorizer.
*   [folke/which-key.nvim](https://github.com/folke/which-key.nvim) - ![boom](https://github.githubassets.com/images/icons/emoji/unicode/1f4a5.png) Create key bindings that stick. WhichKey is a lua plugin for Neovim 0.5 that displays a popup with possible keybindings of the command you started typing.
*   [nvim-lua/completion-nvim](https://github.com/nvim-lua/completion-nvim) - A async completion framework aims to provide completion to neovim's built in LSP written in Lua
*   [liuhaopen/UnityMMO](https://github.com/liuhaopen/UnityMMO) - an unity mmo demo, base on ecs(game play), xlua(ui)
*   [kikito/inspect.lua](https://github.com/kikito/inspect.lua) - Human-readable representation of Lua tables
*   [edubart/nelua-lang](https://github.com/edubart/nelua-lang) - Minimal, efficient, statically-typed and meta-programmable systems programming language heavily inspired by Lua, which compiles to C and native code.
*   [sumory/lor](https://github.com/sumory/lor) - a fast, minimalist web framework for lua based on OpenResty
*   [a327ex/SNKRX](https://github.com/a327ex/SNKRX) - A replayable arcade shooter where you control a snake of heroes.
*   [Tencent/LuaPanda](https://github.com/Tencent/LuaPanda) - lua debug and code tools for VS Code
*   [cardwing/Codes-for-Lane-Detection](https://github.com/cardwing/Codes-for-Lane-Detection) - Learning Lightweight Lane Detection CNNs by Self Attention Distillation (ICCV 2019)
*   [LIKO-12/LIKO-12](https://github.com/LIKO-12/LIKO-12) - LIKO-12 is an open source fantasy computer made using LÖVE.
*   [sailorproject/sailor](https://github.com/sailorproject/sailor) - A Lua MVC Web Framework.
*   [emmericp/MoonGen](https://github.com/emmericp/MoonGen) - MoonGen is a fully scriptable high-speed packet generator built on DPDK and LuaJIT. It can saturate a 10 Gbit/s connection with 64 byte packets on a single CPU core while executing user-provided Lua scripts for each packet. Multi-core support allows for even higher rates. It also features precise and accurate timestamping and rate control.
*   [lcpz/lain](https://github.com/lcpz/lain) - Awesome WM complements
*   [Tinywan/lua-nginx-redis](https://github.com/Tinywan/lua-nginx-redis) - ![hibiscus](https://github.githubassets.com/images/icons/emoji/unicode/1f33a.png) Redis、Lua、Nginx、OpenResty 笔记和资料
*   [WeakAuras/WeakAuras2](https://github.com/WeakAuras/WeakAuras2) - World of Warcraft addon that provides a powerful framework to display customizable graphics on your screen.
*   [cldrn/nmap-nse-scripts](https://github.com/cldrn/nmap-nse-scripts) - My collection of nmap NSE scripts
*   [bungle/lua-resty-template](https://github.com/bungle/lua-resty-template) - Templating Engine (HTML) for Lua and OpenResty.
*   [akinsho/bufferline.nvim](https://github.com/akinsho/bufferline.nvim) - A snazzy bufferline for Neovim
*   [viruscamp/luadec](https://github.com/viruscamp/luadec) - Lua Decompiler for lua 5.1 , 5.2 and 5.3
*   [jose-elias-alvarez/null-ls.nvim](https://github.com/jose-elias-alvarez/null-ls.nvim) - Use Neovim as a language server to inject LSP diagnostics, code actions, and more via Lua.
*   [kiccer/Soldier76](https://github.com/kiccer/Soldier76) - PUBG - 罗技鼠标宏 | 兴趣使然的项目，完虐收费宏！点个Star支持一下作者！\[PUBG - Logitech mouse macro | Support 12 kinds of guns without recoil!\]
*   [pkulchenko/MobDebug](https://github.com/pkulchenko/MobDebug) - Remote debugger for Lua.
*   [kikito/bump.lua](https://github.com/kikito/bump.lua) - A collision detection library for Lua
*   [zmartzone/lua-resty-openidc](https://github.com/zmartzone/lua-resty-openidc) - OpenID Connect Relying Party and OAuth 2.0 Resource Server implementation in Lua for NGINX / OpenResty
*   [openresty/lua-resty-limit-traffic](https://github.com/openresty/lua-resty-limit-traffic) - Lua library for limiting and controlling traffic in OpenResty/ngx\_lua
*   [doujiang24/lua-resty-kafka](https://github.com/doujiang24/lua-resty-kafka) - Lua kafka client driver for the Openresty based on the cosocket API
*   [glepnir/galaxyline.nvim](https://github.com/glepnir/galaxyline.nvim) - neovim statusline plugin written in lua
*   [artart222/CodeArt](https://github.com/artart222/CodeArt) - Use NeoVim as general purpose IDE
*   [nrk/redis-lua](https://github.com/nrk/redis-lua) - A Lua client library for the redis key value storage system.
*   [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs) - autopairs for neovim written by lua
*   [akinsho/toggleterm.nvim](https://github.com/akinsho/toggleterm.nvim) - A neovim lua plugin to help easily manage multiple terminal windows
*   [openresty/lua-resty-core](https://github.com/openresty/lua-resty-core) - New FFI-based API for lua-nginx-module
*   [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim) - plenary: full; complete; entire; absolute; unqualified. All the lua functions I don't want to write twice.
*   [rxi/lume](https://github.com/rxi/lume) - Lua functions geared towards gamedev
*   [WillPower3309/awesome-dotfiles](https://github.com/WillPower3309/awesome-dotfiles) - Dotfiles for awesome people using the awesomewm linux environment
*   [Planimeter/grid-sdk](https://github.com/Planimeter/grid-sdk) - The Grid SDK - Game engine for Lua
*   [openresty/lua-resty-mysql](https://github.com/openresty/lua-resty-mysql) - Nonblocking Lua MySQL driver library for ngx\_lua or OpenResty
*   [facebookarchive/fblualib](https://github.com/facebookarchive/fblualib) - Facebook libraries and utilities for Lua
*   [sean-lin/protoc-gen-lua](https://github.com/sean-lin/protoc-gen-lua) - Google's Protocol Buffers project, ported to Lua
*   [rktjmp/lush.nvim](https://github.com/rktjmp/lush.nvim) - Define Neovim themes as a DSL in lua, with real-time feedback.
*   [daurnimator/lua-http](https://github.com/daurnimator/lua-http) - HTTP Library for Lua. Supports HTTP(S) 1.0, 1.1 and 2.0; client and server.
*   [ers35/luastatic](https://github.com/ers35/luastatic) - Build a standalone executable from a Lua program.
*   [Yonaba/Moses](https://github.com/Yonaba/Moses) - Utility library for functional programming in Lua
*   [rxi/classic](https://github.com/rxi/classic) - Tiny class module for Lua
*   [projekt0n/github-nvim-theme](https://github.com/projekt0n/github-nvim-theme) - Github theme for Neovim, kitty, iTerm, Konsole, tmux and Alacritty written in Lua
*   [franko/luajit-lang-toolkit](https://github.com/franko/luajit-lang-toolkit) - A Lua bytecode compiler written in Lua itself for didactic purposes or for new language implementations
*   [jbyuki/instant.nvim](https://github.com/jbyuki/instant.nvim) - collaborative editing in Neovim using built-in capabilities
*   [Yonaba/Jumper](https://github.com/Yonaba/Jumper) - Fast, lightweight and easy-to-use pathfinding library for grid-based games
*   [lunarmodules/LDoc](https://github.com/lunarmodules/LDoc) - LDoc is a LuaDoc-compatible documentation generator which can also process C extension source. Markdown may be optionally used to render comments, as well as integrated readme documentation and pretty-printed example files.
*   [picolove/picolove](https://github.com/picolove/picolove) - PICO-8 Reimplementation in Love2D. Chat: [https://discord.gg/jGEMUse6RM](https://discord.gg/jGEMUse6RM)
*   [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip) - Snippet Engine for Neovim written in Lua.
*   [games50/pong](https://github.com/games50/pong) - Atari's 1972 classic, implemented in Lua with LÖVE
*   [vsergeev/luaradio](https://github.com/vsergeev/luaradio) - A lightweight, embeddable software-defined radio framework built on LuaJIT
*   [ray-x/navigator.lua](https://github.com/ray-x/navigator.lua) - Navigate codes like a breeze![wind_chime](https://github.githubassets.com/images/icons/emoji/unicode/1f390.png). Exploring LSP and ![evergreen_tree](https://github.githubassets.com/images/icons/emoji/unicode/1f332.png)Treesitter symbols a piece of ![cake](https://github.githubassets.com/images/icons/emoji/unicode/1f370.png). Control codes like a boss ![gorilla](https://github.githubassets.com/images/icons/emoji/unicode/1f98d.png).
*   [kabouzeid/nvim-lspinstall](https://github.com/kabouzeid/nvim-lspinstall) - Provides the missing :LspInstall for nvim-lspconfig
*   [slembcke/debugger.lua](https://github.com/slembcke/debugger.lua) - A dependency free, embeddable debugger for Lua in a single file (.lua or .c)
*   [andremm/typedlua](https://github.com/andremm/typedlua) - An Optional Type System for Lua
*   [kevinhwang91/nvim-bqf](https://github.com/kevinhwang91/nvim-bqf) - Better quickfix window in Neovim, polish old quickfix window.
*   [feline-nvim/feline.nvim](https://github.com/feline-nvim/feline.nvim) - A minimal, stylish and customizable statusline for Neovim written in Lua
*   [upyun/slardar](https://github.com/upyun/slardar) - Updating your upstream list and run lua scripts without reloading Nginx.
*   [kernelsauce/turbo](https://github.com/kernelsauce/turbo) - Turbo is a framework built for LuaJIT 2 to simplify the task of building fast and scalable network applications. It uses a event-driven, non-blocking, no thread design to deliver excellent performance and minimal footprint to high-load applications while also providing excellent support for embedded uses.
*   [gamesys/moonshine](https://github.com/gamesys/moonshine) - A lightweight Lua VM for the browser
*   [deepmind/dqn](https://github.com/deepmind/dqn) - Lua/Torch implementation of DQN (Nature, 2015)
*   [TheAMM/mpv\_thumbnail\_script](https://github.com/TheAMM/mpv_thumbnail_script) - A Lua script to show preview thumbnails in mpv's OSC seekbar, sans external dependencies
*   [EmmyLua/VSCode-EmmyLua](https://github.com/EmmyLua/VSCode-EmmyLua) - Lua IDE/Debugger Plugin for VSCode
*   [b3nj5m1n/kommentary](https://github.com/b3nj5m1n/kommentary) - Neovim commenting plugin, written in lua.
*   [NTBBloodbath/doom-nvim](https://github.com/NTBBloodbath/doom-nvim) - A Neovim configuration for the advanced martian hacker
*   [EdenEast/nightfox.nvim](https://github.com/EdenEast/nightfox.nvim) - ![fox_face](https://github.githubassets.com/images/icons/emoji/unicode/1f98a.png)A soft dark, fully customizable (Neo)Vim theme, with support for lsp, treesitter and a variety of plugins.
*   [kikito/tween.lua](https://github.com/kikito/tween.lua) - Tweening/Easing/Interpolating functions for lua. Inspired on jQuery's animate method.
*   [bjornbytes/RxLua](https://github.com/bjornbytes/RxLua) - Reactive Extensions for Lua
*   [openresty/lua-resty-upstream-healthcheck](https://github.com/openresty/lua-resty-upstream-healthcheck) - Health Checker for Nginx Upstream Servers in Pure Lua
*   [openresty/lua-resty-websocket](https://github.com/openresty/lua-resty-websocket) - WebSocket support for the ngx\_lua module (and OpenResty)
*   [SinisterRectus/Discordia](https://github.com/SinisterRectus/Discordia) - Discord API library written in Lua for the Luvit runtime environment
*   [bakpakin/tiny-ecs](https://github.com/bakpakin/tiny-ecs) - ECS for Lua
*   [ledgetech/ledge](https://github.com/ledgetech/ledge) - An RFC compliant and ESI capable HTTP cache for Nginx / OpenResty, backed by Redis
*   [group-butler/GroupButler](https://github.com/group-butler/GroupButler) - This bot can help you in managing your group with rules, anti-flood, description, custom triggers, and much more!
*   [lewis6991/impatient.nvim](https://github.com/lewis6991/impatient.nvim) - Improve startup time for Neovim
*   [422658476/MPV-EASY-Player](https://github.com/422658476/MPV-EASY-Player) - MPV-EASY Player - A modern video player based on mpv
*   [pkulchenko/serpent](https://github.com/pkulchenko/serpent) - Lua serializer and pretty printer.
*   [C0nw0nk/Nginx-Lua-Anti-DDoS](https://github.com/C0nw0nk/Nginx-Lua-Anti-DDoS) - A Anti-DDoS script to protect Nginx web servers using Lua with a HTML Javascript based authentication puzzle inspired by Cloudflare I am under attack mode an Anti-DDoS authentication page protect yourself from every attack type All Layer 7 Attacks Mitigating Historic Attacks DoS DoS Implications DDoS All Brute Force Attacks Zero day exploits Social Engineering Rainbow Tables Password Cracking Tools Password Lists Dictionary Attacks Time Delay Any Hosting Provider Any CMS or Custom Website Unlimited Attempt Frequency Search Attacks HTTP Basic Authentication HTTP Digest Authentication HTML Form Based Authentication Mask Attacks Rule-Based Search Attacks Combinator Attacks Botnet Attacks Unauthorized IPs IP Whitelisting Bruter THC Hydra John the Ripper Brutus Ophcrack unauthorized logins Injection Broken Authentication and Session Management Sensitive Data Exposure XML External Entities (XXE) Broken Access Control Security Misconfiguration Cross-Site Scripting (XSS) Insecure Deserialization Using Components with Known Vulnerabilities Insufficient Logging & Monitoring Drupal WordPress Joomla Flash Magento PHP Plone WHMCS Atlassian Products malicious traffic Adult video script avs KVS Kernel Video Sharing Clip Bucket Tube sites Content Management Systems Social networks scripts backends proxy proxies PHP Python Porn sites xxx adult gaming networks servers sites forums vbulletin phpbb mybb smf simple machines forum xenforo web hosting video streaming buffering ldap upstream downstream download upload rtmp vod video over dl hls dash hds mss livestream drm mp4 mp3 swf css js html php python sex m3u zip rar archive compressed mitigation code source sourcecode chan 4chan 4chan.org 8chan.net 8ch 8ch.net infinite chan 8kun 8kun.net anonymous anon tor services .onion torproject.org nginx.org nginx.com openresty.org darknet dark net deepweb deep web darkweb dark web mirror vpn reddit reddit.com adobe flash hackthissite.org dreamhack hack hacked hacking hacker hackers hackerz hackz hacks code coding script scripting scripter source leaks leaked leaking cve vulnerability great firewall china america japan russia .gov government http1 http2 http3 quic q3 litespeedtech litespeed apache torrents torrent torrenting webtorrent bittorrent bitorrent bit-torrent cyberlocker cyberlockers cyber locker cyberbunker warez keygen key generator free irc internet relay chat peer-to-peer p2p cryptocurrency crypto bitcoin miner browser xmr monero coinhive coin hive coin-hive litecoin ethereum cpu cycles popads pop-ads advert advertisement networks banner ads protect ovh blazingfast.io amazon steampowered valve store.steampowered.com steamcommunity thepiratebay lulzsec antisec xhamster pornhub porn.com pornhub.com xhamster.com xvideos xvdideos.com xnxx xnxx.com popads popcash cpm ppc
*   [p00f/nvim-ts-rainbow](https://github.com/p00f/nvim-ts-rainbow) - ![rainbow](https://github.githubassets.com/images/icons/emoji/unicode/1f308.png) Rainbow parentheses for neovim using tree-sitter ![rainbow](https://github.githubassets.com/images/icons/emoji/unicode/1f308.png)
*   [MisterDA/love-release](https://github.com/MisterDA/love-release) - ![love_letter](https://github.githubassets.com/images/icons/emoji/unicode/1f48c.png) Lua script that makes LÖVE game release easier
*   [cloudflare/nginx-google-oauth](https://github.com/cloudflare/nginx-google-oauth) - Lua module to add Google OAuth to nginx
*   [bluebird75/luaunit](https://github.com/bluebird75/luaunit) - LuaUnit is a popular unit-testing framework for Lua, with an interface typical of xUnit libraries (Python unittest, Junit, NUnit, ...). It supports several output formats (Text, TAP, JUnit, ...) to be used directly or work with Continuous Integration platforms (Jenkins, Maven, ...).
*   [ignacio/LuaNode](https://github.com/ignacio/LuaNode) - Asynchronous I/O for Lua
*   [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons) - lua `fork` of vim-web-devicons for neovim
*   [nvim-lua/lsp-status.nvim](https://github.com/nvim-lua/lsp-status.nvim) - Utility functions for getting diagnostic status and progress messages from LSP servers, for use in the Neovim statusline
*   [Kamikaze94/WolfHUD](https://github.com/Kamikaze94/WolfHUD) - Payday 2 HUD
*   [glepnir/nvim](https://github.com/glepnir/nvim) - neovim configuration written in lua
*   [onsails/lspkind-nvim](https://github.com/onsails/lspkind-nvim) - vscode-like pictograms for neovim lsp completion items
*   [savq/paq-nvim](https://github.com/savq/paq-nvim) - ![new_moon_with_face](https://github.githubassets.com/images/icons/emoji/unicode/1f31a.png) Neovim package manager
*   [betaflight/betaflight-tx-lua-scripts](https://github.com/betaflight/betaflight-tx-lua-scripts) - Collection of scripts to configure Betaflight from your TX (currently only supported in OpenTx)
*   [mirven/underscore.lua](https://github.com/mirven/underscore.lua) - A utility library for Lua
*   [yaukeywang/LuaMemorySnapshotDump](https://github.com/yaukeywang/LuaMemorySnapshotDump) - Lua memory snapshot dump utility, used for memory leak detection。
*   [zeta0134/LuaGB](https://github.com/zeta0134/LuaGB) - A gameboy emulator written in pure Lua. Work in progress.
*   [marcoskirsch/nodemcu-httpserver](https://github.com/marcoskirsch/nodemcu-httpserver) - A (very) simple web server written in Lua for the ESP8266 firmware NodeMCU.
*   [chipsenkbeil/distant.nvim](https://github.com/chipsenkbeil/distant.nvim) - ![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png) (Alpha stage software) Edit files, run programs, and work with LSP on a remote machine from the comfort of your local environment ![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)
*   [openresty/lua-resty-string](https://github.com/openresty/lua-resty-string) - String utilities and common hash functions for ngx\_lua and LuaJIT
*   [openresty/lua-resty-lrucache](https://github.com/openresty/lua-resty-lrucache) - Lua-land LRU Cache based on LuaJIT FFI
*   [JoosepAlviste/nvim-ts-context-commentstring](https://github.com/JoosepAlviste/nvim-ts-context-commentstring) - Neovim treesitter plugin for setting the commentstring based on the cursor location in a file.
*   [apioak/apioak](https://github.com/apioak/apioak) - Full Lifecycle Management API Gateway.
*   [dualface/gbc-core](https://github.com/dualface/gbc-core) - GameBox Cloud Core - The Game Server Framework based on Lua and OpenResty.
*   [ayamir/nvimdots](https://github.com/ayamir/nvimdots) - A well configured and structured Neovim.
*   [dbalatero/VimMode.spoon](https://github.com/dbalatero/VimMode.spoon) - Adds vim keybindings to all OS X inputs
*   [Pocco81/TrueZen.nvim](https://github.com/Pocco81/TrueZen.nvim) - ![raccoon](https://github.githubassets.com/images/icons/emoji/unicode/1f99d.png) Clean and elegant distraction-free writing for NeoVim
*   [openresty/lua-resty-upload](https://github.com/openresty/lua-resty-upload) - Streaming reader and parser for http file uploading based on ngx\_lua cosocket
*   [folke/twilight.nvim](https://github.com/folke/twilight.nvim) - ![sunrise](https://github.githubassets.com/images/icons/emoji/unicode/1f305.png) Twilight is a Lua plugin for Neovim 0.5 that dims inactive portions of the code you're editing using TreeSitter.
*   [torhve/weechat-matrix-protocol-script](https://github.com/torhve/weechat-matrix-protocol-script) - A WeeChat script in Lua that implements the matrix.org chat protocol
*   [marko-cerovac/material.nvim](https://github.com/marko-cerovac/material.nvim) - ![trident](https://github.githubassets.com/images/icons/emoji/unicode/1f531.png) Material colorscheme for NeoVim written in Lua with built-in support for native LSP, TreeSitter and many more plugins
*   [pandoc/lua-filters](https://github.com/pandoc/lua-filters) - A collection of lua filters for pandoc
*   [Yonaba/30log](https://github.com/Yonaba/30log) - 30 lines library for object orientation in Lua
*   [hkupty/nvimux](https://github.com/hkupty/nvimux) - Neovim as a TMUX replacement
*   [lipp/lua-websockets](https://github.com/lipp/lua-websockets) - Websockets for Lua.
*   [ellisonleao/glow.nvim](https://github.com/ellisonleao/glow.nvim) - A markdown preview directly in your neovim.
*   [MunifTanjim/nui.nvim](https://github.com/MunifTanjim/nui.nvim) - UI Component Library for Neovim.
*   [leafo/magick](https://github.com/leafo/magick) - Lua bindings to ImageMagick for LuaJIT using FFI
*   [karb94/neoscroll.nvim](https://github.com/karb94/neoscroll.nvim) - Smooth scrolling neovim plugin written in lua
*   [TACC/Lmod](https://github.com/TACC/Lmod) - Lmod: An Environment Module System based on Lua, Reads TCL Modules, Supports a Software Hierarchy
*   [tversteeg/registers.nvim](https://github.com/tversteeg/registers.nvim) - ![bookmark_tabs](https://github.githubassets.com/images/icons/emoji/unicode/1f4d1.png) Neovim plugin to preview the contents of the registers
*   [Roblox/roact](https://github.com/Roblox/roact) - A view management library for Roblox Lua similar to React
*   [tylerneylon/pacpac](https://github.com/tylerneylon/pacpac) - A lua-based Pac-Man clone.
*   [wube/factorio-data](https://github.com/wube/factorio-data) - Tracks changes of the lua prototype definitions in factorio inbetween releases.
*   [pavouk/lgi](https://github.com/pavouk/lgi) - Dynamic Lua binding to GObject libraries using GObject-Introspection
*   [rmagatti/auto-session](https://github.com/rmagatti/auto-session) - A small automated session manager for Neovim
*   [numToStr/FTerm.nvim](https://github.com/numToStr/FTerm.nvim) - ![fire](https://github.githubassets.com/images/icons/emoji/unicode/1f525.png) No-nonsense floating terminal plugin for neovim ![fire](https://github.githubassets.com/images/icons/emoji/unicode/1f525.png)
*   [airstruck/knife](https://github.com/airstruck/knife) - A collection of useful micro-modules for Lua.
*   [Igalia/pflua](https://github.com/Igalia/pflua) - Packet filtering in Lua
*   [svermeulen/vimpeccable](https://github.com/svermeulen/vimpeccable) - Neovim plugin that allows you to easily map keys directly to lua code inside your init.lua
*   [ibhagwan/fzf-lua](https://github.com/ibhagwan/fzf-lua) - Improved fzf.vim written in lua
*   [Bambooir/TeleSeed](https://github.com/Bambooir/TeleSeed) - A Telegram-CLI Administration Telgram bot in Lua
*   [stijnwop/guidanceSteering](https://github.com/stijnwop/guidanceSteering) - Guidance Steering (AutoTrack) for Farming Simulator 22.
*   [AckslD/nvim-neoclip.lua](https://github.com/AckslD/nvim-neoclip.lua) - Clipboard manager neovim plugin with telescope integration
*   [giann/croissant](https://github.com/giann/croissant) - ![croissant](https://github.githubassets.com/images/icons/emoji/unicode/1f950.png) A Lua REPL and debugger
*   [somesocks/lua-lockbox](https://github.com/somesocks/lua-lockbox) - A collection of cryptographic primitives written in pure Lua
*   [meric/l2l](https://github.com/meric/l2l) - Lisp is Lisp. Lua is Lua. Lisp and Lua as One.
*   [kikito/lua\_missions](https://github.com/kikito/lua_missions) - Lua Koans, minus the Zen stuff
*   [CosmicNvim/CosmicNvim](https://github.com/CosmicNvim/CosmicNvim) - CosmicNvim is a lightweight and opinionated Neovim config for web development, specifically designed to provide a ![dizzy](https://github.githubassets.com/images/icons/emoji/unicode/1f4ab.png) COSMIC programming experience!
*   [yaapu/FrskyTelemetryScript](https://github.com/yaapu/FrskyTelemetryScript) - A LUA telemetry script and widget for the Horus X10(S),X12 and Taranis X9D+,X9E,QX7 and X-Lite radios using ArduPilot frsky passthru protocol
*   [actboy168/lua-debug](https://github.com/actboy168/lua-debug) - Lua Debug Adapter for Visual Studio Code
*   [a327ex/windfield](https://github.com/a327ex/windfield) - Physics module for LÖVE
*   [EvandroLG/pegasus.lua](https://github.com/EvandroLG/pegasus.lua) - ![rocket](https://github.githubassets.com/images/icons/emoji/unicode/1f680.png) Pegasus.lua is an http server to work with web applications written in Lua language.
*   [Hammerspoon/Spoons](https://github.com/Hammerspoon/Spoons) - The official repository of Spoon plugins
*   [iresty/Mio](https://github.com/iresty/Mio) - API statistics/summary and health datas in NGINX based on OpenResty/ngx\_lua, just like NGINX Plus
*   [vicious-widgets/vicious](https://github.com/vicious-widgets/vicious) - Vicious is a modular widget library for the "awesome" window manager.
*   [openresty/lua-resty-dns](https://github.com/openresty/lua-resty-dns) - DNS resolver for the nginx lua module
*   [aleju/face-generator](https://github.com/aleju/face-generator) - Generate human faces with neural networks
*   [kingluo/luajit.io](https://github.com/kingluo/luajit.io) - luajit io framework
*   [ellisonleao/gruvbox.nvim](https://github.com/ellisonleao/gruvbox.nvim) - Lua port of the most famous vim colorscheme
*   [ElvUI-WotLK/ElvUI](https://github.com/ElvUI-WotLK/ElvUI) - ElvUI for World of Warcraft - Wrath of the Lich King (3.3.5a)
*   [oberblastmeister/neuron.nvim](https://github.com/oberblastmeister/neuron.nvim) - Make neovim the best note taking application
*   [Neopallium/lua-pb](https://github.com/Neopallium/lua-pb) - Lua Protocol Buffers
*   [29988122/Fate-Grand-Order\_Lua](https://github.com/29988122/Fate-Grand-Order_Lua) - Fate Grand Order auto battle script - no root needed, for Android use only
*   [openresty/lua-resty-lock](https://github.com/openresty/lua-resty-lock) - Simple nonblocking lock API for ngx\_lua based on shared memory dictionaries
*   [libmoon/libmoon](https://github.com/libmoon/libmoon) - libmoon is a library for fast and flexible packet processing with DPDK and LuaJIT.
*   [lovetoys/lovetoys](https://github.com/lovetoys/lovetoys) - ![banana](https://github.githubassets.com/images/icons/emoji/unicode/1f34c.png) a full-featured Entity-Component-System framework for making games with lua
*   [openresty/lua-resty-balancer](https://github.com/openresty/lua-resty-balancer) - A generic consistent hash implementation for OpenResty/Lua
*   [VapourNvim/VapourNvim](https://github.com/VapourNvim/VapourNvim) - A NeoVim config for THE ULTIMATE vim IDE-like experience.
*   [yosamrath/kyoto.nvim](https://github.com/yosamrath/kyoto.nvim) - kyoto.nvim is a functional, beautiful, and highly customizable neovim configuration
*   [tanvirtin/vgit.nvim](https://github.com/tanvirtin/vgit.nvim) - Visual Git Plugin for Neovim
*   [kikito/md5.lua](https://github.com/kikito/md5.lua) - MD5 sum in pure Lua, with no C and no external dependencies
*   [craigmj/json4lua](https://github.com/craigmj/json4lua) - JSON (Javascript Object Notation - [http://www.json.org](http://www.json.org)) encoding / decoding module for Lua, and very basic JSON RPC module (requiring socket 2.0).Module requires compat-5.1 if using Lua 5.0.This repository was converted from a CVS repository on luaforge.net on Jan. 20, 2010.
*   [rxi/flux](https://github.com/rxi/flux) - A fast, lightweight tweening library for Lua
*   [rose-pine/neovim](https://github.com/rose-pine/neovim) - Soho vibes for Neovim
*   [bungle/lua-resty-session](https://github.com/bungle/lua-resty-session) - Session library for OpenResty – flexible and secure
*   [Overtorment/NoobHub](https://github.com/Overtorment/NoobHub) - ![globe_with_meridians](https://github.githubassets.com/images/icons/emoji/unicode/1f310.png)![fire](https://github.githubassets.com/images/icons/emoji/unicode/1f525.png) Network multiplayer and messaging for CoronaSDK, Moai, Gideros, LÖVE & Defold
*   [folke/lua-dev.nvim](https://github.com/folke/lua-dev.nvim) - ![computer](https://github.githubassets.com/images/icons/emoji/unicode/1f4bb.png) Dev setup for init.lua and plugin development with full signature help, docs and completion for the nvim lua API.
*   [shaunsingh/nord.nvim](https://github.com/shaunsingh/nord.nvim) - Neovim theme based off of the Nord Color Palette, written in lua with tree sitter support
*   [kyleconroy/lua-state-machine](https://github.com/kyleconroy/lua-state-machine) - A finite state machine lua micro framework
*   [kevinhwang91/nvim-hlslens](https://github.com/kevinhwang91/nvim-hlslens) - Hlsearch Lens for Neovim
*   [teckel12/LuaTelemetry](https://github.com/teckel12/LuaTelemetry) - FrSky SmartPort(S.Port), D-series, F.Port and TBS Crossfire telemetry on all Taranis and Horus transmitters
*   [ray-x/go.nvim](https://github.com/ray-x/go.nvim) - Modern Go development plugin for Neovim, based on nvim-lsp, treesitter and Dap.
*   [mongrel2/Tir](https://github.com/mongrel2/Tir) - A Simple Lua Web Framework For Mongrel2
*   [kdheepak/lazygit.nvim](https://github.com/kdheepak/lazygit.nvim) - Plugin for calling lazygit from within neovim.
*   [Aviana/LunaUnitFrames](https://github.com/Aviana/LunaUnitFrames) - Unit Frames for WoW Classic
*   [NTBBloodbath/rest.nvim](https://github.com/NTBBloodbath/rest.nvim) - A fast Neovim http client written in Lua
*   [vladimir-kotikov/clink-completions](https://github.com/vladimir-kotikov/clink-completions) - Completion files to clink util
*   [upyun/lua-resty-checkups](https://github.com/upyun/lua-resty-checkups) - Manage Nginx upstreams in pure Lua.
*   [cfadmin-cn/cfadmin](https://github.com/cfadmin-cn/cfadmin) - A lua web network framework.
*   [Alloyed/lua-lsp](https://github.com/Alloyed/lua-lsp) - A Lua language server
*   [rafcamlet/nvim-luapad](https://github.com/rafcamlet/nvim-luapad) - Interactive real time neovim scratchpad for embedded lua engine - type and watch!
*   [f-person/git-blame.nvim](https://github.com/f-person/git-blame.nvim) - Git Blame plugin for Neovim written in Lua
*   [lua-stdlib/lua-stdlib](https://github.com/lua-stdlib/lua-stdlib) - General Lua libraries
*   [hack0z/luject](https://github.com/hack0z/luject) - ![tropical_drink](https://github.githubassets.com/images/icons/emoji/unicode/1f379.png)A static injector of dynamic library for application (android, iphoneos, macOS, windows, linux)
*   [appwilldev/moochine](https://github.com/appwilldev/moochine) - MOOCHINE - A simple and lightweight web framework based on OpenResty(ngx\_lua, [http://openresty.org](http://openresty.org)).
*   [goolord/alpha-nvim](https://github.com/goolord/alpha-nvim) - a lua powered greeter like vim-startify / dashboard-nvim
*   [letoram/safespaces](https://github.com/letoram/safespaces) - 3D/VR Desktop built for Arcan
*   [blackCauldron7/surround.nvim](https://github.com/blackCauldron7/surround.nvim) - A surround text object plugin for neovim written in lua.
*   [shagu/pfUI](https://github.com/shagu/pfUI) - A User Interface Replacement for World of Warcraft: Vanilla & TBC
*   [windwp/windline.nvim](https://github.com/windwp/windline.nvim) - Animation statusline, floating window statusline. Use lua + luv make some wind
*   [torch/threads](https://github.com/torch/threads) - Threads for Lua and LuaJIT. Transparent exchange of data between threads is allowed thanks to torch serialization.
*   [harningt/luajson](https://github.com/harningt/luajson) - JSON parser/encoder for Lua Parses JSON using LPEG for speed and flexibility. Depending on parser/encoder options, various values are preserved as best as possible.
*   [libremesh/lime-packages](https://github.com/libremesh/lime-packages) - OpenWrt packages composing LibreMesh meta-firmware for wireless mesh networking
*   [ostinelli/gin](https://github.com/ostinelli/gin) - A LUA fast, low-latency, low-memory footprint, web JSON-API framework with Test Driven Development helpers and patterns.
*   [rxi/log.lua](https://github.com/rxi/log.lua) - A tiny logging module for Lua
*   [a327ex/STALKER-X](https://github.com/a327ex/STALKER-X) - Camera module for LÖVE
*   [jonniek/mpv-playlistmanager](https://github.com/jonniek/mpv-playlistmanager) - Mpv lua script to create and manage playlists
*   [groverburger/g3d](https://github.com/groverburger/g3d) - Simple and easy 3D engine for LÖVE.
*   [daogangtang/bamboo](https://github.com/daogangtang/bamboo) - Bamboo is the web framework of Lua based on Mongrel2, ZeroMQ and NoSQL database.
*   [sidebar-nvim/sidebar.nvim](https://github.com/sidebar-nvim/sidebar.nvim) - A generic and modular lua sidebar for Neovim
*   [keplerproject/luacov](https://github.com/keplerproject/luacov) - LuaCov is a simple coverage analyzer for Lua code.
*   [spacewander/lua-resty-rsa](https://github.com/spacewander/lua-resty-rsa) - RSA encrypt/decrypt & sign/verify for OpenResty/LuaJIT
*   [orbitalquark/textadept](https://github.com/orbitalquark/textadept) - Textadept is a fast, minimalist, and remarkably extensible cross-platform text editor for programmers.
*   [adamqqqplay/dota2ai](https://github.com/adamqqqplay/dota2ai) - This project is a improved Dota2 Bot script based on Valve's default AI. Relase on steam workshop as Ranked Matchmaking AI. This script has more than 1 million current subscribers on Steam Workshop.
*   [LukeZGD/DDLC-LOVE](https://github.com/LukeZGD/DDLC-LOVE) - An unofficial Doki Doki Literature Club port to Lua for the PS Vita and other game consoles
*   [rxi/lurker](https://github.com/rxi/lurker) - Auto-swaps changed Lua files in a running LÖVE project
*   [crivotz/nv-ide](https://github.com/crivotz/nv-ide) - Neovim custom configuration, oriented for full stack developers (rails, ruby, php, html, css, SCSS, javascript)
*   [zserge/luash](https://github.com/zserge/luash) - Tiny lua module to write shell scripts with lua (inspired by Python's sh module)
*   [love2d-community/love-api](https://github.com/love2d-community/love-api) - The whole LÖVE wiki in a Lua table.
*   [occivink/mpv-scripts](https://github.com/occivink/mpv-scripts) - Various scripts for mpv
*   [lujian101/LuaTableOptimizer](https://github.com/lujian101/LuaTableOptimizer) - simple readonly lua table optimizer
*   [rmagatti/goto-preview](https://github.com/rmagatti/goto-preview) - A small Neovim plugin for previewing definitions using floating windows.
*   [beauwilliams/focus.nvim](https://github.com/beauwilliams/focus.nvim) - Auto-Focusing and Auto-Resizing Splits/Windows for Neovim written in Lua. A full suite of window management enhancements. Vim splits on steroids!
*   [tjdevries/nlua.nvim](https://github.com/tjdevries/nlua.nvim) - Lua Development for Neovim
*   [stravant/LuaMinify](https://github.com/stravant/LuaMinify) - Lua source code minifier.
*   [davidm/lua2c](https://github.com/davidm/lua2c) - convert Lua source code into an equivalent C source code written in terms of Lua C API calls
*   [vijaymarupudi/nvim-fzf](https://github.com/vijaymarupudi/nvim-fzf) - A Lua API for using fzf in neovim.
*   [efrederickson/LuaAssemblyTools](https://github.com/efrederickson/LuaAssemblyTools) - Lua Assembly/Bytecode Tools. Has functions for virtually all aspects of LASM, including reading/writing, verifying, stripping debug info, LASM decompilation, and LASM parsing.
*   [tickbh/tdengine](https://github.com/tickbh/tdengine) - game server for Rust + Lua
*   [abecodes/tabout.nvim](https://github.com/abecodes/tabout.nvim) - tabout plugin for neovim
*   [pygy/LuLPeg](https://github.com/pygy/LuLPeg) - A port of LPeg 100% written in Lua.
*   [Tieske/date](https://github.com/Tieske/date) - Date & Time module for Lua 5.x
*   [terrortylor/nvim-comment](https://github.com/terrortylor/nvim-comment) - A comment toggler for Neovim, written in Lua
*   [tanema/light\_world.lua](https://github.com/tanema/light_world.lua) - A lighting model made for love 2d
*   [paulofmandown/rotLove](https://github.com/paulofmandown/rotLove) - Roguelike Toolkit in Love. A Love2D/lua port of rot.js
*   [ledgetech/lua-resty-redis-connector](https://github.com/ledgetech/lua-resty-redis-connector) - Connection utilities for lua-resty-redis
*   [echasnovski/mini.nvim](https://github.com/echasnovski/mini.nvim) - Neovim plugin with collection of minimal, independent, and fast Lua modules dedicated to improve Neovim (version 0.5 and higher) experience
*   [YunoHost/SSOwat](https://github.com/YunoHost/SSOwat) - A simple SSO for NGINX, written in Lua
*   [zhaojh329/wifidog-ng](https://github.com/zhaojh329/wifidog-ng) - Next generation WifiDog implemented in Lua.
*   [advanced-threat-research/CVE-2020-16898](https://github.com/advanced-threat-research/CVE-2020-16898) - CVE-2020-16898 (Bad Neighbor) Microsoft Windows TCP/IP Vulnerability Detection Logic and Rule
*   [JaapBraam/LoRaWanGateway](https://github.com/JaapBraam/LoRaWanGateway) - A LoRaWan Gateway in LUA
*   [richardhundt/shine](https://github.com/richardhundt/shine) - A Shiny Lua Dialect
*   [golgote/neturl](https://github.com/golgote/neturl) - URL and Query string parser, builder, normalizer for Lua
*   [edluffy/hologram.nvim](https://github.com/edluffy/hologram.nvim) - ![ghost](https://github.githubassets.com/images/icons/emoji/unicode/1f47b.png) A cross platform terminal image viewer for Neovim. Extensible and fast, written in Lua and C. Works on macOS and Linux.
*   [openresty/lua-resty-memcached](https://github.com/openresty/lua-resty-memcached) - Lua memcached client driver for the ngx\_lua based on the cosocket API
*   [openLuat/Luat\_2G\_RDA\_8955](https://github.com/openLuat/Luat_2G_RDA_8955) - Luat 2G开源项目，适用于Air202、Air800、Air201等，持续维护
*   [luukvbaal/stabilize.nvim](https://github.com/luukvbaal/stabilize.nvim) - Neovim plugin to stabilize window open/close events.
*   [kikito/i18n.lua](https://github.com/kikito/i18n.lua) - A very complete i18n lib for Lua
*   [renoise/xrnx](https://github.com/renoise/xrnx) - The official Renoise Lua Scripting repository
*   [navarasu/onedark.nvim](https://github.com/navarasu/onedark.nvim) - One Dark Theme for Neovim >= 0.5.0 written in lua based on Atom's One Dark UI Theme. Additionally, it comes with 5 color variant styles
*   [edluffy/specs.nvim](https://github.com/edluffy/specs.nvim) - ![eyeglasses](https://github.githubassets.com/images/icons/emoji/unicode/1f453.png) A fast and lightweight Neovim lua plugin to keep an eye on where your cursor has jumped.
*   [Argon-/mpv-stats](https://github.com/Argon-/mpv-stats) - Display file statistics in mpv.
*   [oUF-wow/oUF](https://github.com/oUF-wow/oUF) - WoW AddOn - Unit frame framework.
*   [pkulchenko/ZeroBranePackage](https://github.com/pkulchenko/ZeroBranePackage) - Packages for ZeroBrane Studio ([https://studio.zerobrane.com](https://studio.zerobrane.com))
*   [andweeb/presence.nvim](https://github.com/andweeb/presence.nvim) - Discord Rich Presence for Neovim
*   [kurapica/PLoop](https://github.com/kurapica/PLoop) - Prototype Lua object-oriented program system and frameworks.
*   [yamatsum/nvim-nonicons](https://github.com/yamatsum/nvim-nonicons) - Icon set using nonicons for neovim plugins and settings
*   [tami5/sqlite.lua](https://github.com/tami5/sqlite.lua) - SQLite/LuaJIT binding for lua and neovim
*   [lukas-reineke/format.nvim](https://github.com/lukas-reineke/format.nvim) - Neovim lua plugin to format the current buffer with external executables
*   [cloudwu/lua-bgfx](https://github.com/cloudwu/lua-bgfx) - Yet another bgfx lua binding
*   [Quenty/NevermoreEngine](https://github.com/Quenty/NevermoreEngine) - ModuleScript loader with reusable and easy unified server-client modules for faster game development on Roblox
*   [APItools/router.lua](https://github.com/APItools/router.lua) - A barebones router for Lua. It matches urls and executes lua functions.
*   [Olivine-Labs/lustache](https://github.com/Olivine-Labs/lustache) - Mustache templates for Lua
*   [zserge/lua-promises](https://github.com/zserge/lua-promises) - A+ promises in Lua
*   [luvit/lit](https://github.com/luvit/lit) - Toolkit for developing, sharing, and running luvit/lua programs and libraries.
*   [liseen/lua-resty-http](https://github.com/liseen/lua-resty-http) - Lua http client driver for the ngx\_lua based on the cosocket API
*   [pguillory/luajit-libuv](https://github.com/pguillory/luajit-libuv) - LuaJIT FFI binding for libuv
*   [mpeterv/argparse](https://github.com/mpeterv/argparse) - Feature-rich command line parser for Lua
*   [glepnir/zephyr-nvim](https://github.com/glepnir/zephyr-nvim) - A dark neovim colorscheme written in lua
*   [Fizzadar/Luapress](https://github.com/Fizzadar/Luapress) - ![newspaper](https://github.githubassets.com/images/icons/emoji/unicode/1f4f0.png) Static site/blog generator written in Lua.
*   [zzamboni/dot-hammerspoon](https://github.com/zzamboni/dot-hammerspoon) - My personal Hammerspoon configuration - mirrored from GitLab
*   [wingify/lua-resty-rabbitmqstomp](https://github.com/wingify/lua-resty-rabbitmqstomp) - Opinionated Lua RabbitMQ client library for the ngx\_lua apps based on the cosocket API
*   [Kadoba/Advanced-Tiled-Loader](https://github.com/Kadoba/Advanced-Tiled-Loader) - Imports Tiled maps into Lua for the LÖVE game engine. (NO LONGER IN DEVELOPMENT)
*   [savq/melange](https://github.com/savq/melange) - ![dagger](https://github.githubassets.com/images/icons/emoji/unicode/1f5e1.png) Warm color scheme for Neovim and beyond
*   [vlipco/srv-router](https://github.com/vlipco/srv-router) - OpenResty (nginx+lua) that discovers upstream servers from SRV records
*   [leegao/LuaInLua](https://github.com/leegao/LuaInLua) - A self-hosting compiler for the Lua language.
*   [facebookresearch/CParser](https://github.com/facebookresearch/CParser) - A compact C preprocessor and declaration parser written in pure Lua
*   [manoelcampos/xml2lua](https://github.com/manoelcampos/xml2lua) - XML Parser written entirely in Lua that works for Lua 5.1+. Convert XML to and from Lua Tables ![waning_gibbous_moon](https://github.githubassets.com/images/icons/emoji/unicode/1f316.png)![currency_exchange](https://github.githubassets.com/images/icons/emoji/unicode/1f4b1.png)
*   [JakobGreen/lua-requests](https://github.com/JakobGreen/lua-requests) - Requests for Lua!
*   [msva/lua-htmlparser](https://github.com/msva/lua-htmlparser) - An HTML parser for lua.
*   [FlightControl-Master/MOOSE](https://github.com/FlightControl-Master/MOOSE) - Mission Object Oriented Scripting Environment (MOOSE) for lua mission scripting design in DCS World
*   [nicknlsn/MarioKart64NEAT](https://github.com/nicknlsn/MarioKart64NEAT) - NEAT implementation in Lua for Mario Kart 64 and the BizHawk emulator
*   [ignacio/StackTracePlus](https://github.com/ignacio/StackTracePlus) - StackTracePlus provides enhanced stack traces for Lua.
*   [CommandPost/CommandPost](https://github.com/CommandPost/CommandPost) - Workflow Enhancements for Creatives
*   [CapsAdmin/goluwa](https://github.com/CapsAdmin/goluwa) - game engine and framework written in luajit
*   [leafo/etlua](https://github.com/leafo/etlua) - Embedded Lua templates
*   [Kampfkarren/Roblox](https://github.com/Kampfkarren/Roblox) - Scripts and stuff I wrote for Roblox. Documentation is little to none as these are just stuff I took from my game that I thought I could share.
*   [sunjon/Shade.nvim](https://github.com/sunjon/Shade.nvim) - An Nvim lua plugin that dims your inactive windows
*   [posenhuang/NPMT](https://github.com/posenhuang/NPMT) - Towards Neural Phrase-based Machine Translation
*   [weshoke/Lust](https://github.com/weshoke/Lust) - Lua String Templates
*   [topkecleon/otouto](https://github.com/topkecleon/otouto) - A Lua-based Telegram bot with plugins.
*   [hpxl/nginx-lua-fastdfs-GraphicsMagick](https://github.com/hpxl/nginx-lua-fastdfs-GraphicsMagick) - nginx+lua+fastdfs+GraphicsMagick 动态生成缩略图
*   [tjdevries/express\_line.nvim](https://github.com/tjdevries/express_line.nvim) - WIP: Statusline written in pure lua. Supports co-routines, functions and jobs.
*   [saks/lua-resty-repl](https://github.com/saks/lua-resty-repl) - Interactive console (REPL) for Openresty and luajit code
*   [flingo64/PhotoStation-Upload-Lr-Plugin](https://github.com/flingo64/PhotoStation-Upload-Lr-Plugin) - Photo StatLr (aka PhotoStation Upload) is a Lightroom Publish and Export Service Plugin that enables the export /publishing of photos and videos from Lr to a Synology Photo Station. It uploads the photos/videos and all required thumbnails. It can download comments and ratings and do a real two-way synch of various metadata (tags, ratings, labels).
*   [Windower/Lua](https://github.com/Windower/Lua) - Lua Addons and Scripts
*   [evaera/Cmdr](https://github.com/evaera/Cmdr) - Extensible command console for Roblox developers
*   [yamatsum/nvim-cursorline](https://github.com/yamatsum/nvim-cursorline) - A plugin for neovim that highlights cursor words and lines
*   [paulcuth/starlight](https://github.com/paulcuth/starlight) - A Lua to ES6 transpiler.
*   [jamestthompson3/nvim-remote-containers](https://github.com/jamestthompson3/nvim-remote-containers) - Develop inside docker containers, just like VSCode
*   [hanks-zyh/hydrogenApp](https://github.com/hanks-zyh/hydrogenApp) - hydrogen is a pluggable android app
*   [bungle/lua-resty-nettle](https://github.com/bungle/lua-resty-nettle) - LuaJIT FFI bindings for Nettle (a low-level cryptographic library)
*   [ms-jpq/lua-async-await](https://github.com/ms-jpq/lua-async-await) - Async Await in 90 lines of code.
*   [keplerproject/xavante](https://github.com/keplerproject/xavante) - Xavante is a Lua HTTP 1.1 Web server that uses a modular architecture based on URI mapped handlers.
*   [trixnz/lua-fmt](https://github.com/trixnz/lua-fmt) - lua-fmt is pretty-printer for Lua code
*   [bjornbytes/graphql-lua](https://github.com/bjornbytes/graphql-lua) - GraphQL implementation in Lua
*   [torhve/LuaWeb](https://github.com/torhve/LuaWeb) - A very simple blog engine using openresty, nginx, lua, markdown, git and redis
*   [brainfucksec/neovim-lua](https://github.com/brainfucksec/neovim-lua) - My Neovim configuration with Lua
*   [adobe-apiplatform/api-gateway-aws](https://github.com/adobe-apiplatform/api-gateway-aws) - AWS SDK for NGINX with Lua
*   [theganyo/lua2go](https://github.com/theganyo/lua2go) - Easy access to your Go (Golang) modules from Lua and NGINX!
*   [davidm/lua-inspect](https://github.com/davidm/lua-inspect) - Lua code analysis, with plugins for HTML and SciTE
*   [zrong/lua](https://github.com/zrong/lua) - A lua library by zengrong.net
*   [128technology/protobuf\_dissector](https://github.com/128technology/protobuf_dissector) - A Wireshark Lua plugin for decoding Google protobuf packets
*   [lefcha/concurrentlua](https://github.com/lefcha/concurrentlua) - Concurrency oriented programming in Lua
*   [Kong/lua-resty-worker-events](https://github.com/Kong/lua-resty-worker-events) - Cross Worker Events for Nginx in Pure Lua
*   [tamago324/lir.nvim](https://github.com/tamago324/lir.nvim) - ![file_cabinet](https://github.githubassets.com/images/icons/emoji/unicode/1f5c4.png) A simple file explorer
*   [bakpakin/binser](https://github.com/bakpakin/binser) - Customizable Lua Serializer
*   [adelarsq/neoline.vim](https://github.com/adelarsq/neoline.vim) - Status Line for Neovim focused on beauty and performance ![white_check_mark](https://github.githubassets.com/images/icons/emoji/unicode/2705.png)
*   [appwilldev/moochine-demo](https://github.com/appwilldev/moochine-demo) - OpenResty(ngx\_lua, [http://openresty.org](http://openresty.org) )+Moochine 完整实例
*   [OTCv8/otclientv8](https://github.com/OTCv8/otclientv8) - Clean, ready to use version of OTClientV8 - Alternative, highly optimized Tibia client
*   [DeadlyBossMods/DBM-Retail](https://github.com/DeadlyBossMods/DBM-Retail) - The ultimate encounter helper (for Retail) to give you fight info that's easy to process at a glance. DBM aims to focus on what's happening to you, and what YOU need to do about it.
*   [CapsAdmin/pac3](https://github.com/CapsAdmin/pac3) - advanced avatar customization for garrysmod
*   [monaqa/dial.nvim](https://github.com/monaqa/dial.nvim) - enhanced increment/decrement plugin for Neovim.
*   [geoffleyland/luatrace](https://github.com/geoffleyland/luatrace) - A tool for tracing Lua script execution and analysing time profiles and coverage
*   [jirutka/ngx-oauth](https://github.com/jirutka/ngx-oauth) - OAuth 2.0 proxy for nginx written in Lua.
*   [jirutka/luapak](https://github.com/jirutka/luapak) - Easily build a standalone executable for any Lua program
*   [eddyekofo94/gruvbox-flat.nvim](https://github.com/eddyekofo94/gruvbox-flat.nvim) - Another attempt of a flat Gruvbox theme for Neovim
*   [tiagovla/tokyodark.nvim](https://github.com/tiagovla/tokyodark.nvim) - A clean dark theme written in lua for neovim 0.5.
*   [stevedonovan/Microlight](https://github.com/stevedonovan/Microlight) - A little library of useful Lua functions, intended as the 'light' version of Penlight
*   [danymat/neogen](https://github.com/danymat/neogen) - A better annotation generator. Supports multiple languages and annotation conventions.
*   [DhavalKapil/elasticsearch-lua](https://github.com/DhavalKapil/elasticsearch-lua) - Lua client for Elasticsearch
*   [ruifm/gitlinker.nvim](https://github.com/ruifm/gitlinker.nvim) - A lua neovim plugin to generate shareable file permalinks (with line ranges) for several git web frontend hosts. Inspired by tpope/vim-fugitive's :GBrowse
*   [asqbtcupid/lua\_hotupdate](https://github.com/asqbtcupid/lua_hotupdate) - my lua hotudpate(hot swap) implement
*   [kikito/stateful.lua](https://github.com/kikito/stateful.lua) - Stateful classes for Lua
*   [gvvaughan/lyaml](https://github.com/gvvaughan/lyaml) - LibYAML binding for Lua.
*   [cloudflare/loom](https://github.com/cloudflare/loom) - Easier to read LuaJIT dumps
*   [andremm/lua-parser](https://github.com/andremm/lua-parser) - A Lua 5.3 parser written with LPegLabel
*   [norman/telescope](https://github.com/norman/telescope) - A highly customizable test library for Lua that allows declarative tests with nested contexts.
*   [igrigorik/tokyo-recipes](https://github.com/igrigorik/tokyo-recipes) - Lean & mean Tokyo Cabinet recipes (with Lua)
*   [Roblox/rodux](https://github.com/Roblox/rodux) - A state management library for Roblox Lua inspired by Redux
*   [Neopallium/lualogging](https://github.com/Neopallium/lualogging) - New maintainer at: [https://github.com/lunarmodules/lualogging](https://github.com/lunarmodules/lualogging)
*   [haringsrob/nvim\_context\_vt](https://github.com/haringsrob/nvim_context_vt) - Virtual text context for neovim treesitter
*   [a327ex/boipushy](https://github.com/a327ex/boipushy) - Input module for LÖVE
*   [Afforess/Factorio-Stdlib](https://github.com/Afforess/Factorio-Stdlib) - Factorio Standard Library Project
*   [occivink/mpv-image-viewer](https://github.com/occivink/mpv-image-viewer) - Configuration, scripts and tips for using mpv as an image viewer
*   [tokers/lua-resty-requests](https://github.com/tokers/lua-resty-requests) - Yet Another HTTP library for OpenResty - For human beings!
*   [matiasah/shadows](https://github.com/matiasah/shadows) - Shädows - A Shadows & Lights engine for löve
*   [agoragames/nginx-google-oauth](https://github.com/agoragames/nginx-google-oauth) - Lua module to add Google OAuth to nginx
*   [nvonahsen/jitsi-token-moderation-plugin](https://github.com/nvonahsen/jitsi-token-moderation-plugin) - Lua plugin for jitsi which determines whether users are moderator or not based on token contents
*   [silentbicycle/tamale](https://github.com/silentbicycle/tamale) - TAble MAtching Lua Extension - An Erlang-style pattern-matching library for Lua
*   [kikito/cron.lua](https://github.com/kikito/cron.lua) - Time-related functions for Lua, inspired in javascript's setTimeout and setInterval
*   [bfredl/nvim-luadev](https://github.com/bfredl/nvim-luadev) - REPL/debug console for nvim lua plugins
*   [tullamods/Bagnon](https://github.com/tullamods/Bagnon) - Single window displays for you items
*   [hythloday/VenturePlanSoDMissions](https://github.com/hythloday/VenturePlanSoDMissions) - Addon to bring VenturePlan up to date with the 9.1 missions
*   [bungle/lua-resty-validation](https://github.com/bungle/lua-resty-validation) - Validation Library (Input Validation and Filtering) for Lua and OpenResty.
*   [hoelzro/lua-repl](https://github.com/hoelzro/lua-repl) - A Lua REPL implemented in Lua for embedding in other programs
*   [evaera/roblox-lua-promise](https://github.com/evaera/roblox-lua-promise) - Promise implementation for Roblox
*   [majek/lua-channels](https://github.com/majek/lua-channels) - Go style channels in pure Lua
*   [geekscape/mqtt\_lua](https://github.com/geekscape/mqtt_lua) - MQTT Client library for the Lua language
*   [fjolnir/TLC](https://github.com/fjolnir/TLC) - The Tiny Lua Cocoa Bridge
*   [camchenry/sock.lua](https://github.com/camchenry/sock.lua) - A Lua networking library for LÖVE games.
*   [RedisLabs/geo.lua](https://github.com/RedisLabs/geo.lua) - A helper library for Redis geospatial indices
*   [luastar/luastar](https://github.com/luastar/luastar) - 一个基于openresty的http接口和web开发框架
*   [benglard/waffle](https://github.com/benglard/waffle) - Fast, asynchronous web framework for Lua/Torch
*   [Skycrab/skynet\_websocket](https://github.com/Skycrab/skynet_websocket) - skynet websocket(lua)
*   [Cluain/Lua-Simple-XML-Parser](https://github.com/Cluain/Lua-Simple-XML-Parser) - Read simple XML easily
*   [nshen/learn-neovim-lua](https://github.com/nshen/learn-neovim-lua) - ![scroll](https://github.githubassets.com/images/icons/emoji/unicode/1f4dc.png) 学习 Neovim 全配置， 逃离 VSCode。
*   [Phrogz/SLAXML](https://github.com/Phrogz/SLAXML) - SAX-like streaming XML parser for Lua
*   [Iron-E/nvim-highlite](https://github.com/Iron-E/nvim-highlite) - A colorscheme template that is "lite" on logic for the developer.
*   [rmehri01/onenord.nvim](https://github.com/rmehri01/onenord.nvim) - ![mountain_snow](https://github.githubassets.com/images/icons/emoji/unicode/1f3d4.png) A Neovim theme that combines the Nord and Atom One Dark color palettes for a more vibrant programming experience.
*   [filipdutescu/renamer.nvim](https://github.com/filipdutescu/renamer.nvim) - VS Code-like renaming UI for Neovim, writen in Lua.
*   [cloudwu/luareload](https://github.com/cloudwu/luareload) - reload a lua module
*   [SpringCloud/nginx-zuul-dynamic-lb](https://github.com/SpringCloud/nginx-zuul-dynamic-lb) - ![maple_leaf](https://github.githubassets.com/images/icons/emoji/unicode/1f341.png) 基于Lua的Spring Cloud网关高可用通用Ngnix插件
*   [zheng-ji/ngx\_lua\_reqstatus](https://github.com/zheng-ji/ngx_lua_reqstatus) - 实时统计 nginx 状态的 lua 拓展
*   [NTBBloodbath/cheovim](https://github.com/NTBBloodbath/cheovim) - Neovim configuration switcher written in Lua. Inspired by chemacs.
*   [xopxe/lumen](https://github.com/xopxe/lumen) - Lua Multitasking Environment.
*   [ful1e5/onedark.nvim](https://github.com/ful1e5/onedark.nvim) - Atom's iconic One Dark theme for Neovim, written in Lua
*   [SavedInstances/SavedInstances](https://github.com/SavedInstances/SavedInstances) - Addon that keeps track of the instance/raid lockouts saved against your characters, and related currencies and cooldowns.
*   [1bardesign/batteries](https://github.com/1bardesign/batteries) - Reusable dependencies for games made with lua (especially with love)
*   [xfbs/PiL3](https://github.com/xfbs/PiL3) - My solutions to the exercises from the book "Programming in Lua 3" by Roberto Ierusalimschy
*   [mtourne/nginx\_log\_by\_lua](https://github.com/mtourne/nginx_log_by_lua) - Simple example of aggregated logging using log\_by\_lua hooks
*   [4ban/awesome-ban](https://github.com/4ban/awesome-ban) - Awesome WM 4.x theme configs
*   [renerocksai/telekasten.nvim](https://github.com/renerocksai/telekasten.nvim) - A Neovim (lua) plugin for working with a markdown zettelkasten / wiki and mixing it with a journal, based on telescope.nvim
*   [juce/lua-resty-shell](https://github.com/juce/lua-resty-shell) - tiny subprocess/shell library to use with OpenResty application server
*   [Kong/lua-resty-dns-client](https://github.com/Kong/lua-resty-dns-client) - Lua DNS client, load balancer, and utility library
*   [peanode/simple-url-shorten](https://github.com/peanode/simple-url-shorten) - 基于Openresty的lua模块开发的简单网址缩短系统，特点是使用Nginx+lua+redis，性能非常高；具有域名黑名单、白名单，支持简单认证；支持自定义短网址；支持自定义短URL长度；支持自定义短网址字符前缀后缀等等
*   [mam91/neat-genetic-mario](https://github.com/mam91/neat-genetic-mario) - Update of Seth Bling's MarI/O
*   [FAForever/fa](https://github.com/FAForever/fa) - Lua code for FAF
*   [EmmanuelOga/easing](https://github.com/EmmanuelOga/easing) - Easing functions implemented in lua (Functions from [http://www.robertpenner.com/easing/](http://www.robertpenner.com/easing/) )
*   [gvx/bitser](https://github.com/gvx/bitser) - Serializes and deserializes Lua values with LuaJIT
*   [tjdevries/vim9jit](https://github.com/tjdevries/vim9jit) - Ok, hear me out. vim9script... but in lua... so fast
*   [sonoro1234/LuaJIT-ImGui](https://github.com/sonoro1234/LuaJIT-ImGui) - LuaJIT ffi binding for imgui, backends and extension widgets
*   [davidde/mpv-autosub](https://github.com/davidde/mpv-autosub) - Fully automatic subtitle downloading for the MPV media player
*   [cloudwu/lua-trace](https://github.com/cloudwu/lua-trace) - Trace for debug lua
*   [stevedonovan/LuaMacro](https://github.com/stevedonovan/LuaMacro) - An extended Lua macro preprocessor
*   [jmcnamara/xlsxwriter.lua](https://github.com/jmcnamara/xlsxwriter.lua) - A lua module for creating Excel XLSX files.
*   [clementfarabet/graphicsmagick](https://github.com/clementfarabet/graphicsmagick) - A simple Lua wrapper to graphicsmagick.
*   [leandromoreira/nginx-lua-redis-rate-measuring](https://github.com/leandromoreira/nginx-lua-redis-rate-measuring) - A lua library to provide distributed rate measurement using nginx + redis, you can use it to do a throttling system within many nodes.
*   [jtarchie/underscore-lua](https://github.com/jtarchie/underscore-lua) - Underscore is a utility-belt library for Lua
*   [apache/skywalking-nginx-lua](https://github.com/apache/skywalking-nginx-lua) - The Nginx Lua agent for Apache SkyWalking
*   [weibocom/motan-openresty](https://github.com/weibocom/motan-openresty) - A cross-language RPC framework for rapid development of high performance distributed services based on OpenResty.
*   [LuaDist/squish](https://github.com/LuaDist/squish) - Squish Lua libraries and apps into a single compact file.
*   [tamton-aquib/staline.nvim](https://github.com/tamton-aquib/staline.nvim) - A modern lightweight statusline and bufferline for neovim in lua. Mainly uses unicode symbols for showing info.
*   [disrupted/dotfiles](https://github.com/disrupted/dotfiles) - 👨🏻‍💻 My personal Neovim config entirely written in Lua (requires nightly), ZSH with zinit plugin manager & powerlevel10k prompt, and other dotfiles I am adding over time
*   [stevedonovan/Lake](https://github.com/stevedonovan/Lake) - A Lua-based Build Tool
*   [iryont/lua-struct](https://github.com/iryont/lua-struct) - Implementation of binary packing/unpacking in pure lua
*   [olimorris/onedarkpro.nvim](https://github.com/olimorris/onedarkpro.nvim) - ![art](https://github.githubassets.com/images/icons/emoji/unicode/1f3a8.png) One Dark Pro for Neovim with dark and light themes. Completely customisable colors, styles and highlights. Written in Lua
*   [nixuehan/Belial](https://github.com/nixuehan/Belial) - 基于nginx lua module 的一个 waf .
*   [mwSora/payday-2-luajit](https://github.com/mwSora/payday-2-luajit) - Decompiled Lua of PAYDAY 2.
*   [lspcontainers/lspcontainers.nvim](https://github.com/lspcontainers/lspcontainers.nvim) - Neovim plugin for lspcontainers.
*   [jameshiew/nvim-magic](https://github.com/jameshiew/nvim-magic) - ![genie](https://github.githubassets.com/images/icons/emoji/unicode/1f9de.png) Pluggable framework for using AI code assistance in Neovim
*   [zeromq/lzmq](https://github.com/zeromq/lzmq) - Lua binding to ZeroMQ
*   [wrxck/mattata](https://github.com/wrxck/mattata) - A powerful, plugin-based, multi-purpose Telegram bot designed to serve a wide variety of purposes
*   [pltanton/net\_widgets](https://github.com/pltanton/net_widgets) - Network widgets for Awesome WM
*   [iresty/lua-resty-test](https://github.com/iresty/lua-resty-test) - Lua test frame for the ngx\_lua based on Openresty
*   [philanc/plc](https://github.com/philanc/plc) - Pure Lua Crypto
*   [cocos-creator/deprecated-creator-lua](https://github.com/cocos-creator/deprecated-creator-lua) - Cocos Creator 的 Lua 支持
*   [b0o/mapx.nvim](https://github.com/b0o/mapx.nvim) - ![world_map](https://github.githubassets.com/images/icons/emoji/unicode/1f5fa.png) A better way to create key mappings in Neovim.
*   [grafi-tt/lunajson](https://github.com/grafi-tt/lunajson) - A strict and fast JSON parser/decoder/encoder written in pure Lua.
*   [deepmind/classic](https://github.com/deepmind/classic) - A class system for Lua.
*   [Mofiqul/vscode.nvim](https://github.com/Mofiqul/vscode.nvim) - Neovim/Vim color scheme inspired by Dark+ and Light+ theme in Visual Studio Code
*   [numToStr/Navigator.nvim](https://github.com/numToStr/Navigator.nvim) - ![sparkles](https://github.githubassets.com/images/icons/emoji/unicode/2728.png) Smoothly navigate between neovim splits and tmux panes ![sparkles](https://github.githubassets.com/images/icons/emoji/unicode/2728.png)
*   [lvim-tech/lvim](https://github.com/lvim-tech/lvim) - LVIM IDE is a modular Neovim configuration written in LUA with full customization.
*   [esoui/esoui](https://github.com/esoui/esoui) - ESOUI is the Lua source code of the ZenimaxOnline's MMORPG "The Elder Scrolls Online"
*   [diegofn/TuneIn-Radio-VLC](https://github.com/diegofn/TuneIn-Radio-VLC) - TuneIn Radio LUA Script for VLC 2.x. and 3.x. Its compatible with VLC for Windows, Linux and Mac
*   [Yagua/nebulous.nvim](https://github.com/Yagua/nebulous.nvim) - Minimalist Collection of Colorschemes Written in Lua
*   [EsreverWoW/ShestakUI\_Classic](https://github.com/EsreverWoW/ShestakUI_Classic) - ShestakUI for WoW Classic (1.14.0) and Burning Crusade Classic (2.5.2)
*   [wrxck/telegram-bot-lua](https://github.com/wrxck/telegram-bot-lua) - A simple yet extensive Lua library for the Telegram bot API.
*   [umegaya/lua-aws](https://github.com/umegaya/lua-aws) - pure-lua implementation of aws REST APIs
*   [jinq0123/grpc-lua](https://github.com/jinq0123/grpc-lua) - The Lua gRPC binding. HTTP/2 based RPC [http://grpc.io](http://grpc.io)
*   [Tieske/uuid](https://github.com/Tieske/uuid) - A pure Lua uuid generator (modified from a Rackspace module)
*   [luukvbaal/nnn.nvim](https://github.com/luukvbaal/nnn.nvim) - File manager for Neovim powered by nnn.
*   [Olivine-Labs/luassert](https://github.com/Olivine-Labs/luassert) - Assertion library for Lua
*   [Creckeryop/NOBORU](https://github.com/Creckeryop/NOBORU) - Application for PlayStation Vita to read manga or comics
*   [stepelu/lua-sci](https://github.com/stepelu/lua-sci) - SciLua: Scientific Computing with LuaJIT
*   [petertriho/cmp-git](https://github.com/petertriho/cmp-git) - Git source for nvim-cmp
*   [multitheftauto/mtasa-resources](https://github.com/multitheftauto/mtasa-resources) - This project maintains a list of up-to-date resources that come with Multi Theft Auto.
*   [BeamMP/BeamMP](https://github.com/BeamMP/BeamMP) - A LUA implementation at attempting to bring local network multiplayer to BeamNG.drive
*   [noib3/nvim-cokeline](https://github.com/noib3/nvim-cokeline) - ![nose](https://github.githubassets.com/images/icons/emoji/unicode/1f443.png) A Neovim bufferline for people with addictive personalities
*   [kikito/love-loader](https://github.com/kikito/love-loader) - Threaded resource loading for LÖVE
*   [efrederickson/XFuscator](https://github.com/efrederickson/XFuscator) - Most advanced Lua obfuscator 3V4R
*   [TeamUlysses/ulx](https://github.com/TeamUlysses/ulx) - ULX: A powerful administration addon for Garry's Mod
*   [Stepets/utf8.lua](https://github.com/Stepets/utf8.lua) - pure-lua 5.3 regex library
*   [xchopin/FiveM-RP-Boilerplate](https://github.com/xchopin/FiveM-RP-Boilerplate) - ![gun](https://github.githubassets.com/images/icons/emoji/unicode/1f52b.png) Boilerplate for FiveM Roleplay servers. Save time and focus on your real project.
*   [davidm/lua-matrix](https://github.com/davidm/lua-matrix) - Matrices and vectors of are real, complex, and symbolic elements, implemented as Lua tables.
*   [SiENcE/astray](https://github.com/SiENcE/astray) - Astray is a lua based maze, room and dungeon generation library for dungeon crawlers and rougelike video games
*   [speedata/luaqrcode](https://github.com/speedata/luaqrcode) - Pure Lua qrcode library
*   [numToStr/dotfiles](https://github.com/numToStr/dotfiles) - ~/.dotfiles. Includes configs for neovim, tmux, zsh, alacrity, kitty, and more | Managed by GNU stow
*   [tanema/behaviourtree.lua](https://github.com/tanema/behaviourtree.lua) - a simple behaviour tree library for lua ported from javascript
*   [max397574/better-escape.nvim](https://github.com/max397574/better-escape.nvim) - Escape from insert mode without delay when typing
*   [lukas-reineke/headlines.nvim](https://github.com/lukas-reineke/headlines.nvim) - This plugin adds 3 kind of horizontal highlights for text filetypes, like `markdown`, `vimwiki` and `orgmode`
*   [keplerproject/orbit](https://github.com/keplerproject/orbit) - Orbit is an MVC web framework for Lua.
*   [jbyuki/one-small-step-for-vimkind](https://github.com/jbyuki/one-small-step-for-vimkind) - Debug adapter for Neovim plugins
*   [ignacio/LuaOAuth](https://github.com/ignacio/LuaOAuth) - A OAuth client library for Lua
*   [b0o/SchemaStore.nvim](https://github.com/b0o/SchemaStore.nvim) - A Neovim plugin that provides access to the SchemaStore catalog.
*   [Egor-Skriptunoff/pure\_lua\_SHA](https://github.com/Egor-Skriptunoff/pure_lua_SHA) - SHA1, SHA2, SHA3 and BLAKE2 functions written in pure Lua and optimized for speed
*   [isage/lua-resty-moongoo](https://github.com/isage/lua-resty-moongoo) - MongoDB library for OpenResty
*   [Roblox/testez](https://github.com/Roblox/testez) - BDD-style test and assertion library for Roblox Lua
*   [NightrainsRbx/RobloxLsp](https://github.com/NightrainsRbx/RobloxLsp) - Roblox Luau Language Server forked from Lua by sumneko.
*   [DengSir/tdBattlePetScript](https://github.com/DengSir/tdBattlePetScript) - Battle pet combat script for wow.
*   [occivink/mpv-gallery-view](https://github.com/occivink/mpv-gallery-view) - Gallery-view scripts for mpv
*   [hoelzro/lua-term](https://github.com/hoelzro/lua-term) - Terminal operations for Lua
*   [ldb/lua-telegram-bot](https://github.com/ldb/lua-telegram-bot) - Lua Library for the Telegram Bot API
*   [MutePuker/TeleMute](https://github.com/MutePuker/TeleMute) - A Telegram-CLI Administration Telgram bot in Lua - New TG
*   [HDoujinDownloader/HDoujinDownloader](https://github.com/HDoujinDownloader/HDoujinDownloader) - An easy-to-use manga and dōjinshi downloader supporting 800+ different websites
*   [psamim/telegram-cli-backup](https://github.com/psamim/telegram-cli-backup) - A simple Lua script to backup Telegram messages into a CSV or sqlite database
*   [daurnimator/lpeg\_patterns](https://github.com/daurnimator/lpeg_patterns) - A collection of LPEG patterns
*   [IronsDu/Joynet](https://github.com/IronsDu/Joynet) - high performance network (tcp socket) library for lua, based on [https://github.com/IronsDu/brynet](https://github.com/IronsDu/brynet) and lua coroutine.
*   [cloudflare/raven-lua](https://github.com/cloudflare/raven-lua) - A Lua interface to Sentry
*   [anjia0532/lua-resty-redis-util](https://github.com/anjia0532/lua-resty-redis-util) - openresty/lua-resty-redis 封装工具类
*   [Olivine-Labs/lusty](https://github.com/Olivine-Labs/lusty) - Lua RESTful Web Application Framework
*   [Neopallium/lua-handlers](https://github.com/Neopallium/lua-handlers) - Provides a set of async. callback based handlers for working with raw TCP/UDP socket, ZeroMQ sockets, or HTTP client/server.
*   [Ketho/BlizzardInterfaceResources](https://github.com/Ketho/BlizzardInterfaceResources) - Development resources from World of Warcraft
*   [Elfansoer/dota-2-lua-abilities](https://github.com/Elfansoer/dota-2-lua-abilities) - A repository for creating Dota 2 Lua abilities.
*   [saadparwaiz1/cmp\_luasnip](https://github.com/saadparwaiz1/cmp_luasnip) - luasnip completion source for nvim-cmp
*   [huyvohcmc/dotfiles](https://github.com/huyvohcmc/dotfiles) - backup or it didn't exist
*   [X-Raym/REAPER-ReaScripts](https://github.com/X-Raym/REAPER-ReaScripts) - X-Raym's Free and Open Source Scripts for Cockos REAPER.
*   [thegrb93/StarfallEx](https://github.com/thegrb93/StarfallEx) - Starfall, but with active development and more features. Write Garry's mod chips similar to E2, but in lua
*   [piXelicidio/locas-ants](https://github.com/piXelicidio/locas-ants) - A modern Lua+Löve2D remake of my Ant Colony Simulation
*   [thomasgoldstein/zabuyaki](https://github.com/thomasgoldstein/zabuyaki) - Zabuyaki, old-school side-scrolling beat 'em up
*   [thibaultcha/lua-cassandra](https://github.com/thibaultcha/lua-cassandra) - Pure Lua driver for Apache Cassandra
*   [daurnimator/luatz](https://github.com/daurnimator/luatz) - Time, Date and Timezone library for lua
*   [Ruin0x11/OpenNefia](https://github.com/Ruin0x11/OpenNefia) - (Archived) Moddable engine reimplementation of the Japanese roguelike Elona.
*   [mnabila/nvimrc](https://github.com/mnabila/nvimrc) - vimrc for neovim written in lua
*   [LazyZhu/lua-resty-ssdb](https://github.com/LazyZhu/lua-resty-ssdb) - Lua ssdb client driver for the ngx\_lua based on the cosocket API, SSDB is a leveldb server.
*   [APItools/sandbox.lua](https://github.com/APItools/sandbox.lua) - A lua sandbox for executing non-trusted code
*   [norcalli/nvim-terminal.lua](https://github.com/norcalli/nvim-terminal.lua) - A high performance filetype mode for Neovim which leverages conceal and highlights your buffer with the correct color codes.
*   [matbme/JABS.nvim](https://github.com/matbme/JABS.nvim) - Just Another Buffer Switcher for Neovim
*   [luapower/dynasm](https://github.com/luapower/dynasm) - DynASM with Lua mode
*   [horan-geeker/nana](https://github.com/horan-geeker/nana) - Lua http api framework
*   [flwmxd/PharaohStroy](https://github.com/flwmxd/PharaohStroy) - A maplestory IDE which can develop the multi-platform maplestory game
*   [clementfarabet/lua---nnx](https://github.com/clementfarabet/lua---nnx) - An extension to Torch7's nn package.
*   [ElvUI-TBC/ElvUI](https://github.com/ElvUI-TBC/ElvUI) - ElvUI for World of Warcraft - The Burning Crusade (2.4.3)
*   [tietang/ngx-lua-zuul](https://github.com/tietang/ngx-lua-zuul) - 基于Nginx&Lua 和Netflix Eureka的微服务网关。请看看：[https://github.com/tietang/zebra](https://github.com/tietang/zebra)
*   [tanvirtin/monokai.nvim](https://github.com/tanvirtin/monokai.nvim) - Monokai theme for Neovim written in Lua.
*   [lithammer/NeavUI](https://github.com/lithammer/NeavUI) - Development branch of Neav UI
*   [kenshohara/3D-ResNets](https://github.com/kenshohara/3D-ResNets) - 3D ResNets for Action Recognition
*   [gilzoide/godot-lua-pluginscript](https://github.com/gilzoide/godot-lua-pluginscript) - Godot PluginScript for the Lua language, currently based on LuaJIT's FFI
*   [beauwilliams/statusline.lua](https://github.com/beauwilliams/statusline.lua) - A zero-config minimal statusline for neovim written in lua featuring awesome integrations and blazing speed!
*   [alvarosevilla95/luatab.nvim](https://github.com/alvarosevilla95/luatab.nvim) - Tabline lua plugin for neovim
*   [David-Kunz/treesitter-unit](https://github.com/David-Kunz/treesitter-unit) - A Neovim plugin to deal with treesitter units
*   [xolox/vim-lua-inspect](https://github.com/xolox/vim-lua-inspect) - Semantic highlighting for Lua in Vim
*   [nucular/sfxrlua](https://github.com/nucular/sfxrlua) - A port of the sfxr sound effect synthesizer to Lua
*   [mkafrin/PolyZone](https://github.com/mkafrin/PolyZone) - PolyZone is a FiveM mod to define zones of different shapes and test whether a point is inside or outside of the zone
*   [alec-gibson/nvim-tetris](https://github.com/alec-gibson/nvim-tetris) - Bringing emacs' greatest feature to neovim - Tetris!
*   [Open-Markets-Initiative/wireshark-lua](https://github.com/Open-Markets-Initiative/wireshark-lua) - Source generated cross platform wireshark dissectors
*   [winston0410/commented.nvim](https://github.com/winston0410/commented.nvim) - Neovim commenting plugin in Lua. Support operator, motions and more than 60 languages! ![fire](https://github.githubassets.com/images/icons/emoji/unicode/1f525.png)
*   [serprex/luwa](https://github.com/serprex/luwa) - WIP jit lua to wasm
*   [jonniek/mpv-scripts](https://github.com/jonniek/mpv-scripts) - A collection of mpv scripts
*   [daxliar/submerger](https://github.com/daxliar/submerger) - SRT Subtitles Merger
*   [solso/api-aggregator](https://github.com/solso/api-aggregator) - Aggregate REST API calls easily on a sandboxed Nginx+Lua env
*   [orts/server](https://github.com/orts/server) - A real map datapack based on TFS 1.2 engine
*   [fffonion/lua-resty-acme](https://github.com/fffonion/lua-resty-acme) - Automatic Let's Encrypt certificate serving and Lua implementation of ACMEv2 procotol
*   [clementfarabet/lua---parallel](https://github.com/clementfarabet/lua---parallel) - A (simple) parallel computing framework for Lua
*   [ToxicFrog/vstruct](https://github.com/ToxicFrog/vstruct) - A Lua library for packing and unpacking binary data, supporting arbitrary (byte-aligned) widths, named fields, and repetition.
*   [yashguptaz/calvera-dark.nvim](https://github.com/yashguptaz/calvera-dark.nvim) - Calvera Dark Colorscheme for Neovim written in Lua with built-in support for native LSP, TreeSitter and many more plugins
*   [rmagatti/session-lens](https://github.com/rmagatti/session-lens) - A session-switcher extension for rmagatti/auto-session using Telescope.nvim
*   [koreader/koreader-base](https://github.com/koreader/koreader-base) - Base framework offering a Lua scriptable environment for creating document readers
*   [hopesoft/nginx-lua-image-module](https://github.com/hopesoft/nginx-lua-image-module) - A nginx module to resize, crop images
*   [xHasKx/luamqtt](https://github.com/xHasKx/luamqtt) - luamqtt - Pure-lua MQTT v3.1.1 and v5.0 client
*   [whatsthatsmell/dots](https://github.com/whatsthatsmell/dots) - Code Smell Dotfiles
*   [scipag/httprecon-nse](https://github.com/scipag/httprecon-nse) - Advanced web server fingerprinting for Nmap
*   [moteus/lua-log](https://github.com/moteus/lua-log) - Asynchronous logging library for Lua
*   [hnlq715/nginx-prometheus-metrics](https://github.com/hnlq715/nginx-prometheus-metrics) - A production demo to collect prometheus metrics for nginx with lua embedded.
*   [boyliang/lua\_badboy](https://github.com/boyliang/lua_badboy) - Some useful tools for lua
*   [SimonLarsen/duckmarines](https://github.com/SimonLarsen/duckmarines) - Free software ChuChu Rocket remake for PC
*   [osyrisrblx/t](https://github.com/osyrisrblx/t) - A Runtime Typechecker for Roblox
*   [cloudwu/ldebug](https://github.com/cloudwu/ldebug) - A Lua Remote Debugger
*   [amireh/lua\_cliargs](https://github.com/amireh/lua_cliargs) - A command-line argument parsing module for Lua.
*   [AdiAddons/AdiBags](https://github.com/AdiAddons/AdiBags) - WoW Addon — Adirelle's bag addon.
*   [pianocomposer321/yabs.nvim](https://github.com/pianocomposer321/yabs.nvim) - Yet Another Build System/Code Runner for Neovim, written in lua
*   [ekickx/clipboard-image.nvim](https://github.com/ekickx/clipboard-image.nvim) - Neovim Lua plugin to paste image from clipboard.
*   [bungle/lua-resty-route](https://github.com/bungle/lua-resty-route) - URL Routing Library for OpenResty Supporting Pluggable Matching Engines
*   [siffiejoe/lua-amalg](https://github.com/siffiejoe/lua-amalg) - Amalgamation of Lua modules/scripts
*   [kyleschaub/udemy-love2d](https://github.com/kyleschaub/udemy-love2d) - Full source code for all projects from my course on Lua and Love2D
*   [kikito/beholder.lua](https://github.com/kikito/beholder.lua) - Minimal observer pattern for Lua, with a couple twists
*   [Neopallium/LuaNativeObjects](https://github.com/Neopallium/LuaNativeObjects) - A Lua bindings generator written in Lua.
*   [CRAG666/code\_runner.nvim](https://github.com/CRAG666/code_runner.nvim) - The best code runner you could have, it is like the one in vscode but with super powers, it manages projects like in intellij but without being slow
*   [libvips/lua-vips](https://github.com/libvips/lua-vips) - Lua binding for the libvips image processing library
*   [ledgetech/lua-resty-qless](https://github.com/ledgetech/lua-resty-qless) - Lua binding to Qless (Queue / Pipeline management) for OpenResty / Redis
*   [andersevenrud/nordic.nvim](https://github.com/andersevenrud/nordic.nvim) - A nord-esque colorscheme for neovim
*   [Kong/lua-resty-healthcheck](https://github.com/Kong/lua-resty-healthcheck) - Healthcheck library for OpenResty to validate upstream service status
*   [sumneko/vscode-lua](https://github.com/sumneko/vscode-lua) - Release lua-language-server for VSCode
*   [ishan9299/modus-theme-vim](https://github.com/ishan9299/modus-theme-vim) - Port of modus-themes in neovim
*   [gamax92/OCEmu](https://github.com/gamax92/OCEmu) - OpenComputers Emulator in Lua. Depreciated
*   [bighil/aeslua](https://github.com/bighil/aeslua) - Implementation of aes in nearly pure lua (bitlib is required)
*   [seblindfors/ConsolePort](https://github.com/seblindfors/ConsolePort) - ConsolePort - Game Controller Addon for World of Warcraft
*   [leegao/see.lua](https://github.com/leegao/see.lua) - A Lua 5.x/LuaJIT introspection library for humans
*   [brymer-meneses/grammar-guard.nvim](https://github.com/brymer-meneses/grammar-guard.nvim) - Grammar Guard is a Neovim plugin that checks your grammar as you write your LaTeX, Markdown or plain text document.
*   [RedisLabs/redis-lua-debugger](https://github.com/RedisLabs/redis-lua-debugger) - A Redis Lua script for debugging Redis Lua scripts
*   [wtsnjp/llmk](https://github.com/wtsnjp/llmk) - Light LaTeX Make
*   [monsonjeremy/onedark.nvim](https://github.com/monsonjeremy/onedark.nvim) - OneDark NeoVim theme written in Lua
*   [lubyk/dub](https://github.com/lubyk/dub) - A Lua bindings generator that uses Doxygen to parse C/C++ headers.
*   [liuhaopen/SkynetMMO](https://github.com/liuhaopen/SkynetMMO) - a skynet implementation of MMO, server side of UnityMMO
*   [ittner/lua-iconv](https://github.com/ittner/lua-iconv) - Lua bindings for POSIX iconv
*   [guysv/ilua](https://github.com/guysv/ilua) - Portable Lua kernel for Jupyter
*   [Mofiqul/dracula.nvim](https://github.com/Mofiqul/dracula.nvim) - Dracula colorscheme for neovim written in Lua
*   [pintsized/lua-resty-rack](https://github.com/pintsized/lua-resty-rack) - A simple and extensible HTTP server framework for OpenResty.
*   [mailru/tntlua](https://github.com/mailru/tntlua) - Tarantool 1.5 Lua stored procedures
*   [duhoobo/lua-resty-smtp](https://github.com/duhoobo/lua-resty-smtp) - I must be crazy trying to send mail with Nginx.
*   [dingshukai/lua-oop](https://github.com/dingshukai/lua-oop) - Lua Object Oriented Programming Framework. WOW!
*   [azurewang/lua-resty-fastdfs](https://github.com/azurewang/lua-resty-fastdfs) - Nonblocking Lua FastDFS driver library for ngx\_lua
*   [albingroen/quick.nvim](https://github.com/albingroen/quick.nvim) - A very fast Lua based Neovim configuration that uses coc.nvim for intellisense
*   [RishabhRD/nvim-cheat.sh](https://github.com/RishabhRD/nvim-cheat.sh) - cheat.sh integration for neovim in elegant way
*   [DeadlyBossMods/DBM-Classic](https://github.com/DeadlyBossMods/DBM-Classic) - The ultimate encounter helper (for Classic) to give you fight info that's easy to process at a glance. DBM aims to focus on what's happening to you, and what YOU need to do about it.
*   [vovolie/lua-nginx-prometheus](https://github.com/vovolie/lua-nginx-prometheus) - Monitoring nginx using prometheus
*   [ray-x/nvim](https://github.com/ray-x/nvim) - Blazing fast neovim setup with 120 plugins.
*   [pixeltailgames/cinema](https://github.com/pixeltailgames/cinema) - ![movie_camera](https://github.githubassets.com/images/icons/emoji/unicode/1f3a5.png) Gamemode for Garry's Mod featuring multiplayer video streaming
*   [philips/lualint](https://github.com/philips/lualint) - lua linter
*   [mfcc64/mpv-scripts](https://github.com/mfcc64/mpv-scripts) - mpv lua scripts
*   [lattejed/a-star-lua](https://github.com/lattejed/a-star-lua) - A clean, simple implementation of the A\* pathfinding algorithm for Lua.
*   [ethanholz/nvim-lastplace](https://github.com/ethanholz/nvim-lastplace) - A Lua rewrite of vim-lastplace
*   [Enfernuz/quik-lua-rpc](https://github.com/Enfernuz/quik-lua-rpc) - RPC-сервис для вызова API Lua-библиотеки торгового терминала QUIK (ARQA Technologies)
*   [DNS-OARC/drool](https://github.com/DNS-OARC/drool) - DNS Replay Tool
*   [tullamods/OmniCC](https://github.com/tullamods/OmniCC) - Cooldown count for everything
*   [torch/trepl](https://github.com/torch/trepl) - A pure Lua-based, lightweight REPL for Torch.
*   [openresty/lua-ssl-nginx-module](https://github.com/openresty/lua-ssl-nginx-module) - NGINX C module that extends ngx\_http\_lua\_module for enhanced SSL/TLS capabilities
*   [rrfeng/lua-resty-upstream-etcd](https://github.com/rrfeng/lua-resty-upstream-etcd) - An OpenResty lua module that can use upstream config in etcd and Kubernetes.
*   [karai17/lapis-chan](https://github.com/karai17/lapis-chan) - Image board software written in Lua using the Lapis web framework.
*   [SimonLarsen/sienna](https://github.com/SimonLarsen/sienna) - Fast-paced one button platformer
*   [Jigoku/boxclip](https://github.com/Jigoku/boxclip) - 2D platformer engine using LÖVE and Lua
*   [DarkEnergyProcessor/livesim2](https://github.com/DarkEnergyProcessor/livesim2) - Love Live! School Idol Festival Live Simulator
*   [leafo/heroku-openresty](https://github.com/leafo/heroku-openresty) - Run OpenResty on Heroku with the Lua buildpack
*   [katono/rogue.vim](https://github.com/katono/rogue.vim) - Porting of Rogue-clone II for Vim
*   [jamores/eth-ws-someip](https://github.com/jamores/eth-ws-someip) - Automotive Ethernet SOME/IP-SD Wireshark LUA dissectors (Autosar 4.2)
*   [giann/sirocco](https://github.com/giann/sirocco) - ![parrot](https://github.githubassets.com/images/icons/emoji/unicode/1f99c.png) A collection of interactive command line prompts for Lua
*   [fffonion/lua-resty-sniproxy](https://github.com/fffonion/lua-resty-sniproxy) - SNI Proxy based on stream-lua-nginx-module
*   [VolatilePulse/PoB-Item-Tester](https://github.com/VolatilePulse/PoB-Item-Tester) - AHK and Lua script to automate comparing PoE items from in game or trade sites against your current build with the power of PoB
*   [NodeUSB/nodemcu-ide](https://github.com/NodeUSB/nodemcu-ide) - Browser based Lua IDE for ESP8266 SoC
*   [shagu/pfQuest](https://github.com/shagu/pfQuest) - A Questhelper and Database Addon for World of Warcraft: Vanilla & TBC
*   [rxi/tick](https://github.com/rxi/tick) - Lua module for delaying function calls
*   [medcl/lua-resty-weedfs](https://github.com/medcl/lua-resty-weedfs) - weefs,lua,nginx and file post processing with ffmpeg and graphicsmagick
*   [kikito/memoize.lua](https://github.com/kikito/memoize.lua) - memoized functions in lua
*   [jose-elias-alvarez/buftabline.nvim](https://github.com/jose-elias-alvarez/buftabline.nvim) - A low-config, minimalistic buffer tabline Neovim plugin written in Lua.
*   [iqiyi/lua-resty-couchbase](https://github.com/iqiyi/lua-resty-couchbase) - Lua couchbase client driver for the ngx\_lua based on the cosocket API / 使用cosocket纯lua实现的couchbase的client，已经在爱奇艺重要的服务播放服务稳定运行5年多
*   [graue/luasynth](https://github.com/graue/luasynth) - Audio framework in Lua
*   [cniw/mpv-discordRPC](https://github.com/cniw/mpv-discordRPC) - Discord Rich Presence integration for mpv Media Player
*   [Xuyuanp/yanil](https://github.com/Xuyuanp/yanil) - Yet Another Nerdtree In Lua
*   [NobleRobot/NobleEngine](https://github.com/NobleRobot/NobleEngine) - A li'l game engine for Playdate.
*   [xfguo/luactor](https://github.com/xfguo/luactor) - A pure Lua (at least for now) Actor Model framework.
*   [ubergarm/openresty-nginx-jwt](https://github.com/ubergarm/openresty-nginx-jwt) - JWT Bearer Token authorization with nginx, openresty, and lua-resty-jwt.
*   [sniper00/entitas-lua](https://github.com/sniper00/entitas-lua) - Entitas ECS implementation in Lua.
*   [sailorproject/valua](https://github.com/sailorproject/valua) - Validation for lua! A module for making chained validations. Create your objects, append your tests, use and reuse it!
*   [netxfly/nginx\_lua\_security](https://github.com/netxfly/nginx_lua_security) - 浅谈nginx+lua在安全中的应用
*   [keplerproject/luadoc](https://github.com/keplerproject/luadoc) - LuaDoc is obsolete, use LDoc instead →
*   [javieryanez/nodemcu-modules](https://github.com/javieryanez/nodemcu-modules) - Modules for nodeMcu (LUA intepreter for ESP8266)
*   [hiwoshixiaoyu/FruitSlot](https://github.com/hiwoshixiaoyu/FruitSlot) - 老虎机,水果机,游戏,cocos2d-lua,go网络版水果机
*   [api7/jsonschema](https://github.com/api7/jsonschema) - Pure Lua JSON schema validator for Lua/LuaJIT
*   [ahmedkhalf/lsp-rooter.nvim](https://github.com/ahmedkhalf/lsp-rooter.nvim) - lsp-rooter.nvim is a neovim plugin written in lua to change the current working directory to the project's root directory automagically using nvim native lsp.
*   [ysugimoto/lua-resty-grpc-gateway](https://github.com/ysugimoto/lua-resty-grpc-gateway) - REST <-> gRPC gateway library implementation with OpenResty
*   [romgrk/fzy-lua-native](https://github.com/romgrk/fzy-lua-native) - Luajit FFI bindings to FZY
*   [kikito/semver.lua](https://github.com/kikito/semver.lua) - Semantic versioning for Lua
*   [itdxer/4DaysORM](https://github.com/itdxer/4DaysORM) - Lua 4Days ORM for sqlite3 and mysql
*   [MArpogaus/awesome-ayu](https://github.com/MArpogaus/awesome-ayu) - Minimalistic awesome window manager theme using the gorgeous ayu color palette.
*   [starius/lua-lru](https://github.com/starius/lua-lru) - LRU cache in Lua
*   [neovim/lua-client](https://github.com/neovim/lua-client) - Nvim Lua client
*   [Mogara/LuaSkillsForQSGS](https://github.com/Mogara/LuaSkillsForQSGS) - 新版太阳神三国杀武将技能代码速查手册（Lua版）
*   [MikuAuahDark/lily](https://github.com/MikuAuahDark/lily) - LÖVE Async Asset Loader
*   [AckslD/nvim-revJ.lua](https://github.com/AckslD/nvim-revJ.lua) - Nvim-plugin for doing the opposite of join-line (J) of arguments written in lua.
*   [trisulnsm/trisul-scripts](https://github.com/trisulnsm/trisul-scripts) - Ready to run scripts for network analysis
*   [sundream/ggApp](https://github.com/sundream/ggApp) - A game server example,base on gg+skynet
*   [silentbicycle/lunatest](https://github.com/silentbicycle/lunatest) - xUnit-style + randomized unit testing framework for Lua (and C projects using Lua, etc.)
*   [rgieseke/locco](https://github.com/rgieseke/locco) - Locco is Docco in Lua.
*   [haproxytech/haproxy-lua-oauth](https://github.com/haproxytech/haproxy-lua-oauth) - JWT Validation implementation for HAProxy Lua host
*   [freeioe/freeioe](https://github.com/freeioe/freeioe) - FreeIOE is a framework for building IOE (Internet Of Everything) edge-computing gateway 开源的边缘计算网关框架. 讨论群: 291292378
*   [api7/lua-resty-ipmatcher](https://github.com/api7/lua-resty-ipmatcher) - High-performance match IP address for Nginx + Lua
*   [TeamUlysses/ulib](https://github.com/TeamUlysses/ulib) - ULib: A Lua library for more rapid development on Garry's Mod servers
*   [yuri/sputnik](https://github.com/yuri/sputnik) - An Extensible Wiki/CMS in Lua
*   [nekonako/xresources-nvim](https://github.com/nekonako/xresources-nvim) - ![art](https://github.githubassets.com/images/icons/emoji/unicode/1f3a8.png) Neovim colorscheme based on your xresources color
*   [mindreframer/ProFi.lua](https://github.com/mindreframer/ProFi.lua) - a non-official git mirror for ProFi, a Lua profiler
*   [mfenner/pandoc-jats](https://github.com/mfenner/pandoc-jats) - A Lua custom writer for Pandoc generating JATS XML
*   [lua-nucleo/lua-nucleo](https://github.com/lua-nucleo/lua-nucleo) - A random collection of core and utility level Lua libraries
*   [catwell/luajit-msgpack-pure](https://github.com/catwell/luajit-msgpack-pure) - MessagePack for LuaJIT (using FFI, no bindings, V4 API)
*   [wilhantian/catui](https://github.com/wilhantian/catui) - A very light-weight GUI library for the Löve2D
*   [onsails/diaglist.nvim](https://github.com/onsails/diaglist.nvim) - Live render workspace diagnostics in quickfix with current buf errors on top, buffer diagnostics in loclist
*   [kikito/sha1.lua](https://github.com/kikito/sha1.lua) - (Deprecated Repo) SHA-1 secure hash computation, and HMAC-SHA1 signature computation in Lua (5.1)
*   [kepler155c/opus](https://github.com/kepler155c/opus) - ComputerCraft OS
*   [grasses/nginx-lua-static-merger](https://github.com/grasses/nginx-lua-static-merger) - Static files merger base on openresty
*   [aiq/basexx](https://github.com/aiq/basexx) - A Lua library which provides base2(bitfield), base16(hex), base32(crockford/rfc), base64(rfc/url), base85(z85) decoding and encoding.
*   [RealUI/RealUI](https://github.com/RealUI/RealUI) - A minimalistic UI for World of Warcraft designed to be functional, yet also efficient and elegant.
*   [JoepVanlier/Hackey-Trackey](https://github.com/JoepVanlier/Hackey-Trackey) - A LUA tracker plugin for REAPER 5.x and up. Designed to mimick the pattern editor in Jeskola Buzz.
*   [Grouflon/3rd\_training\_lua](https://github.com/Grouflon/3rd_training_lua) - Training mode for Street Fighter III 3rd Strike (Japan 990512), on Fightcade
*   [wiiaboo/mpv-scripts](https://github.com/wiiaboo/mpv-scripts) - Scripts I've made or adapted from others
*   [keplerproject/wsapi](https://github.com/keplerproject/wsapi) - WSAPI is an API that abstracts the web server from Lua web applications.
*   [henix/slt2](https://github.com/henix/slt2) - a simple Lua template processor
*   [gvx/Ser](https://github.com/gvx/Ser) - A fast, robust, richly-featured table serialisation library for Lua
*   [LandSandBoat/server](https://github.com/LandSandBoat/server) - ![boat](https://github.githubassets.com/images/icons/emoji/unicode/26f5.png) LandSandBoat - a server emulator for Final Fantasy XI. Just an X-34 landspeeder out for a drive.
*   [tsbohc/zest.nvim](https://github.com/tsbohc/zest.nvim) - macros to configure neovim in fennel
*   [shawndumas/adventure.lua](https://github.com/shawndumas/adventure.lua) - Lua Text Adventure Engine
*   [nvim-neo-tree/neo-tree.nvim](https://github.com/nvim-neo-tree/neo-tree.nvim) - Neovim plugin to manage the file system and other tree like structures.
*   [ishan9299/nvim-solarized-lua](https://github.com/ishan9299/nvim-solarized-lua) - solarized colorscheme in lua for nvim 0.5
*   [arthurealike/turtle.lua](https://github.com/arthurealike/turtle.lua) - Turtle graphics library for LÖVE.
*   [Yelp/casper](https://github.com/Yelp/casper) - Yelp's internal caching proxy, powered by Nginx and OpenResty at its core
*   [ThymonA/menuv](https://github.com/ThymonA/menuv) - FiveM menu library for creating menu's with NUI
*   [NTBBloodbath/doom-one.nvim](https://github.com/NTBBloodbath/doom-one.nvim) - doom-emacs' doom-one Lua port for Neovim
*   [LinArcX/telescope-command-palette.nvim](https://github.com/LinArcX/telescope-command-palette.nvim) - Create key-bindings and watch them with telescope ![telescope](https://github.githubassets.com/images/icons/emoji/unicode/1f52d.png)
*   [torch/xlua](https://github.com/torch/xlua) - A set of useful functions to extend Lua (string, table, ...).
*   [tokers/lua-resty-http2](https://github.com/tokers/lua-resty-http2) - The HTTP/2 Protocol (Client Side) Implementation for OpenResty.
*   [tjdevries/tree-sitter-lua](https://github.com/tjdevries/tree-sitter-lua) - Neovim Tree Sitter Lua Grammar & Library
*   [rdlaitila/LURE](https://github.com/rdlaitila/LURE) - Lua User Interface Rendering engine
*   [mozilla-services/lua\_sandbox\_extensions](https://github.com/mozilla-services/lua_sandbox_extensions) - Extension packages (sandboxes and modules) for the lua\_sandbox project
*   [moteus/lua-llthreads2](https://github.com/moteus/lua-llthreads2) - `llthreads` library rewritten without `LuaNativeObjects` code generator
*   [itsyourbedtime/orca](https://github.com/itsyourbedtime/orca) - Lua port of @neauoire orca for monome norns
*   [calio/lua-capnproto](https://github.com/calio/lua-capnproto) - Lua-capnp is a pure lua implementation of capnproto based on luajit.
*   [anjia0532/lua-resty-maxminddb](https://github.com/anjia0532/lua-resty-maxminddb) - A Lua library for reading MaxMind's Geolocation database
*   [KSDaemon/wiola](https://github.com/KSDaemon/wiola) - WAMP implementation in Lua
*   [torch/class](https://github.com/torch/class) - Oriented Object Programming for Lua
*   [mirven/luaspec](https://github.com/mirven/luaspec) - A specification framework for lua
*   [mcclure/emu-coop](https://github.com/mcclure/emu-coop) - Lua scripts for turning 1-player games into 2-player games using inventory sharing.
*   [jbochi/lua-resty-cassandra](https://github.com/jbochi/lua-resty-cassandra) - Pure Lua Cassandra client using CQL binary protocol
*   [andycai/kodelua](https://github.com/andycai/kodelua) - Kode is a free Open Source Model-View-Controller framework using Lua.
*   [abzcoding/lvim](https://github.com/abzcoding/lvim) - Bloated LunarVim
*   [xolox/lua-lxsh](https://github.com/xolox/lua-lxsh) - Lexing & Syntax Highlighting in Lua (using LPeg)
*   [tullamods/Dominos](https://github.com/tullamods/Dominos) - A main actionbar replacement
*   [torhve/lua-resty-letsencrypt](https://github.com/torhve/lua-resty-letsencrypt) - Lua script for Nginx to automatically get certificates from LetsEncrypt CA
*   [rossy/mpv-repl](https://github.com/rossy/mpv-repl) - A graphical REPL for mpv input commands
*   [optimizacija/neovim-config](https://github.com/optimizacija/neovim-config) - Modern NeoVim config for IDE-like development
*   [nanomsg/luajit-nanomsg](https://github.com/nanomsg/luajit-nanomsg) - LuaJIT FFI binding to the nanomsg library
*   [jagt/pprint.lua](https://github.com/jagt/pprint.lua) - yet another lua pretty printer
*   [elihugarret/Moonlet](https://github.com/elihugarret/Moonlet) - Live coding with Lua.
*   [bjornbytes/lust](https://github.com/bjornbytes/lust) - Lightweight Lua test framework
*   [RishabhRD/popfix](https://github.com/RishabhRD/popfix) - Neovim lua API for highly extensible popup window
*   [Eroica-cpp/dota2scripts](https://github.com/Eroica-cpp/dota2scripts) - Lua scripts for DotA2.
*   [vislee/lua-resty-dns-server](https://github.com/vislee/lua-resty-dns-server) - Lua DNS server driver for OpenResty
*   [ttwings/wuxiaLove2d](https://github.com/ttwings/wuxiaLove2d) - 武侠与江湖 养成类武侠游戏
*   [superzazu/denver.lua](https://github.com/superzazu/denver.lua) - a simple library to help you play custom waveforms with LÖVE
*   [jaawerth/fennel-nvim](https://github.com/jaawerth/fennel-nvim) - running fennel-lang natively in neovim
*   [frederic2ec/onsetrp](https://github.com/frederic2ec/onsetrp) - \[OUTDATED\] OnsetRP framework
*   [ejmr/Luvent](https://github.com/ejmr/Luvent) - Simple Event Library for Lua
*   [azurewang/lua-resty-postgres](https://github.com/azurewang/lua-resty-postgres) - Nonblocking Lua PostgreSQL driver library for ngx\_lua
*   [LPGhatguy/luajit-request](https://github.com/LPGhatguy/luajit-request) - Simple HTTPS for LuaJIT!
*   [HTV04/funkin-rewritten](https://github.com/HTV04/funkin-rewritten) - Rewrite of Friday Night Funkin' built on LÖVE
*   [wardz/ClassicCastbars](https://github.com/wardz/ClassicCastbars) - WoW Classic addon that brings back the target & nameplate castbars.
*   [spro/simon](https://github.com/spro/simon) - Dynamic routing/vhosts with nginx + Lua + Redis
*   [petertriho/nvim-scrollbar](https://github.com/petertriho/nvim-scrollbar) - Extensible Neovim Scrollbar
*   [nvim-treesitter/highlight.lua](https://github.com/nvim-treesitter/highlight.lua) - a neovim syntax highlighter using treesitter
*   [lusis/lua-httpclient](https://github.com/lusis/lua-httpclient) - A unified http/s client library for lua
*   [leafo/image-server-tutorial](https://github.com/leafo/image-server-tutorial) - An example of an image processing server in OpenResty and Lua
*   [iopass4/behavior3-lua](https://github.com/iopass4/behavior3-lua) - behavior3-lua
*   [hrsh7th/cmp-nvim-lua](https://github.com/hrsh7th/cmp-nvim-lua) - nvim-cmp source for nvim lua
*   [handsomematt/3d2d-vgui](https://github.com/handsomematt/3d2d-vgui) - ![eyes](https://github.githubassets.com/images/icons/emoji/unicode/1f440.png) Render and control 2D VGUI in 3D world space for Garry's Mod
*   [geekscape/nodemcu\_esp8266](https://github.com/geekscape/nodemcu_esp8266) - NodeMCU Lua examples for the ESP8266 Wi-Fi module
*   [davisdude/mlib](https://github.com/davisdude/mlib) - A math and collisions library for Lua.
*   [Roblox/roact-rodux](https://github.com/Roblox/roact-rodux) - A connector between Roact and Rodux, similar to react-redux
*   [timotta/wrk-scripts](https://github.com/timotta/wrk-scripts) - Script Lua to work better with wrk
*   [prettier/plugin-lua](https://github.com/prettier/plugin-lua) - Prettier Lua Plugin (WIP)
*   [pkulchenko/ZeroBraneEduPack](https://github.com/pkulchenko/ZeroBraneEduPack) - A collection of simple lessons, scripts, and demos in Lua, suitable for learning programming concepts.
*   [dhruvmanila/telescope-bookmarks.nvim](https://github.com/dhruvmanila/telescope-bookmarks.nvim) - A Neovim Telescope extension to open your browser bookmarks right from the editor!
*   [davidm/lua-fish](https://github.com/davidm/lua-fish) - Parses Lua to abstract syntax tree (AST) using LPeg.
*   [anuvyklack/pretty-fold.nvim](https://github.com/anuvyklack/pretty-fold.nvim) - Foldtext customization and folded region preview in Neovim.
*   [MINIONBOTS/FFXIVMinion](https://github.com/MINIONBOTS/FFXIVMinion) - The LUA-Bot-Module for FFXIVMinion, from MMOMinion.com
*   [ElvUI-Vanilla/ElvUI](https://github.com/ElvUI-Vanilla/ElvUI) - ElvUI for World of Warcraft - Vanilla (1.12.1)
*   [Aviana/YaHT](https://github.com/Aviana/YaHT) - Yet another Hunter Timer for WoW Classic
*   [zrbcool/prometheus-lua-nginx](https://github.com/zrbcool/prometheus-lua-nginx) - API Gateway monitoring tools, out-of-box dashboard helps you find out performance issue,help improve SLA.
*   [x25/luajwt](https://github.com/x25/luajwt) - JSON Web Tokens for Lua
*   [jvgrootveld/telescope-zoxide](https://github.com/jvgrootveld/telescope-zoxide) - An extension for telescope.nvim that allows you operate zoxide within Neovim.
*   [hunzsig-warcraft3/h-lua](https://github.com/hunzsig-warcraft3/h-lua) - H-Lua SDK. This project has been stopped.
*   [emilk/sol](https://github.com/emilk/sol) - Lua + Typesafety = Sol
*   [davidm/lua-bit-numberlua](https://github.com/davidm/lua-bit-numberlua) - Bitwise operators in pure Lua using Lua numbers
*   [PedroAlvesV/AbsTK](https://github.com/PedroAlvesV/AbsTK) - The Abstract Toolkit – a widget toolkit for GUI and text-mode applications.
*   [Isotarge/ScriptHawk](https://github.com/Isotarge/ScriptHawk) - A collection of Lua scripts and RAM watches for BizHawk.
*   [Ellypse/IntelliJ-IDEA-Lua-IDE-WoW-API](https://github.com/Ellypse/IntelliJ-IDEA-Lua-IDE-WoW-API) - WoW Lua API to use with the Lua IDE plugin for IntelliJ IDEA
*   [songweihang/knight](https://github.com/songweihang/knight) - Nginx Http 集群api 统计监控、灰度发布、频率控制
*   [moneymanagerex/general-reports](https://github.com/moneymanagerex/general-reports) - Bunch of general reports for Money Manager Ex
*   [jonstoler/class.lua](https://github.com/jonstoler/class.lua) - object-oriented library for lua
*   [fffonion/lua-resty-openssl](https://github.com/fffonion/lua-resty-openssl) - FFI-based OpenSSL binding for OpenResty
*   [brimworks/lua-http-parser](https://github.com/brimworks/lua-http-parser) - Lua binding to Ryan Dahl's "http-parser".
*   [andrewmcwatters/lclass](https://github.com/andrewmcwatters/lclass) - Lua with Classes
*   [actboy168/MoeHero](https://github.com/actboy168/MoeHero) - 我的英雄不可能那么萌
*   [Yonaba/Lua-Class-System](https://github.com/Yonaba/Lua-Class-System) - Lua Class System (LCS) is a small library which offers a clean, minimalistic but powerful API for (Pseudo) Object Oriented programming style using Lua.
*   [MiaadTeam/lesvim](https://github.com/MiaadTeam/lesvim) - Nvim config focus on Javascript, Typescript, Rust and Lua - ![rocket](https://github.githubassets.com/images/icons/emoji/unicode/1f680.png) ![muscle](https://github.githubassets.com/images/icons/emoji/unicode/1f4aa.png) ( Fast and Powerfull ) - Deno and other typescript LSP working well together
*   [mebens/strong](https://github.com/mebens/strong) - A Lua library that makes your strings stronger!
*   [hishamhm/f-strings](https://github.com/hishamhm/f-strings) - String interpolation for Lua
*   [dcampos/nvim-snippy](https://github.com/dcampos/nvim-snippy) - Snippet plugin for Neovim
*   [bungle/lua-resty-uuid](https://github.com/bungle/lua-resty-uuid) - LuaJIT FFI bindings for libuuid, a DCE compatible Universally Unique Identifier library.
*   [IUdalov/u-test](https://github.com/IUdalov/u-test) - Sane and simple unit testing framework for Lua
*   [rlch/github-notifications.nvim](https://github.com/rlch/github-notifications.nvim) - Statusline + Telescope integration for viewing and interacting with GitHub notifications
*   [Theory-of-Everything/nii-nvim](https://github.com/Theory-of-Everything/nii-nvim) - A minimal neovim configuration
*   [RealTadango/FrSky](https://github.com/RealTadango/FrSky) - My S.Port sensors and OpenTX Lua scripts
*   [symphony-of-empires/symphony-of-empires](https://github.com/symphony-of-empires/symphony-of-empires) - Symphony of the Empires is a RTS strategy game and map game.
*   [love2d-community/splashes](https://github.com/love2d-community/splashes) - A collection of splash screens for LÖVE
*   [iskolbin/lbase64](https://github.com/iskolbin/lbase64) - Lua base64 decoder/encoder
*   [hjjpku/Action\_Detection\_DQN](https://github.com/hjjpku/Action_Detection_DQN) - Lua
*   [ddonline/nginx-lua-waf](https://github.com/ddonline/nginx-lua-waf) - Nginx-Lua-WAF是一款基于Nginx的使用Lua语言开发的灵活高效的Web应用层防火墙
*   [danielnehrig/nvim](https://github.com/danielnehrig/nvim) - neovim lua cfg
*   [charlesmallah/lua-profiler](https://github.com/charlesmallah/lua-profiler) - Fast function profiling for use with Lua
*   [arkav/lualine-lsp-progress](https://github.com/arkav/lualine-lsp-progress) - LSP Progress lualine componenet
*   [akshendra/Serene-Conky](https://github.com/akshendra/Serene-Conky) - Nice and clean conky theme, made using lua and cairo
*   [Playermet/luajit-tcc](https://github.com/Playermet/luajit-tcc) - Tiny C Compiler 0.9.26 binding for LuaJIT
*   [Heerozh/LuaAsio](https://github.com/Heerozh/LuaAsio) - Simple transparent non-blocking TCP I/O for LuaJIT, Based on Boost.Asio and Lua coroutine.
*   [GUI/lua-resty-mail](https://github.com/GUI/lua-resty-mail) - A high-level, easy to use, and non-blocking email and SMTP library for OpenResty.
*   [Avimitin/nvim](https://github.com/Avimitin/nvim) - Superfast NeoVIM configuration
*   [woothee/lua-resty-woothee](https://github.com/woothee/lua-resty-woothee) - Woothee Lua-Openresty implementation
*   [unindented/lua-fsm](https://github.com/unindented/lua-fsm) - A simple finite-state machine implementation for Lua.
*   [kikito/lua-sandbox](https://github.com/kikito/lua-sandbox) - A lua sandbox for executing non-trusted code
*   [isage/lua-imagick](https://github.com/isage/lua-imagick) - Lua pure-c bindings to ImageMagick
*   [is0n/fm-nvim](https://github.com/is0n/fm-nvim) - ![card_index_dividers](https://github.githubassets.com/images/icons/emoji/unicode/1f5c2.png) Neovim plugin that lets you use your favorite terminal file managers (and fuzzy finders) from within Neovim.
*   [dvv/nodemcu-thingies](https://github.com/dvv/nodemcu-thingies) - Assorted set of small Lua modules for nodemcu-firmware
*   [JoebRogers/PICO-Tween](https://github.com/JoebRogers/PICO-Tween) - A small library of tweening/easing functions for use in the PICO-8 fantasy console, inspired by Robert Penner's easing functions.
*   [Iron-E/nvim-libmodal](https://github.com/Iron-E/nvim-libmodal) - Create new "modes" for Neovim!
*   [ChristianChiarulli/lvim](https://github.com/ChristianChiarulli/lvim) - My config for LunarVim
*   [williamwen1986/flutter\_luakit\_demo](https://github.com/williamwen1986/flutter_luakit_demo) - show how to use flutter\_luakit\_plugin with flutter project
*   [tjdevries/vlog.nvim](https://github.com/tjdevries/vlog.nvim) - Single file, no dependency, easy copy & paste log file to add to your neovim lua plugins
*   [sroccaserra/object-lua](https://github.com/sroccaserra/object-lua) - \[Deprecated\] A class-oriented OOP module for Lua
*   [philer/polycore](https://github.com/philer/polycore) - A conky config and library of Lua widgets
*   [mthnglac/dotfiles](https://github.com/mthnglac/dotfiles) - This is what I use to get things done!
*   [jonstoler/lua-toml](https://github.com/jonstoler/lua-toml) - toml decoder/encoder for Lua
*   [jinq0123/hotfix](https://github.com/jinq0123/hotfix) - Lua 5.2/5.3 hotfix. Hot update functions and keep old data.
*   [hiili/WindowsTorch](https://github.com/hiili/WindowsTorch) - Windows binary build of the Torch machine learning framework
*   [bakpakin/Splash.lua](https://github.com/bakpakin/Splash.lua) - 2D Spatial Hashing in Lua
*   [ThemerCorp/themer.lua](https://github.com/ThemerCorp/themer.lua) - A simple, minimal highlighter plugin for neovim
*   [AndrewFarley/Taranis-XLite-Q7-Lua-Dashboard](https://github.com/AndrewFarley/Taranis-XLite-Q7-Lua-Dashboard) - A simple lua-based dashboard for the OpenTX XLite/QX7 Transmitters
*   [woshihuo12/LuaDesignPattern](https://github.com/woshihuo12/LuaDesignPattern) - lua design pattern example code
*   [weshoke/DSL](https://github.com/weshoke/DSL) - Domain Specific Language generator for Lua
*   [rrpgfirecast/firecast](https://github.com/rrpgfirecast/firecast) - OpenSource side of RRPG Firecast =)
*   [cuducos/yaml.nvim](https://github.com/cuducos/yaml.nvim) - ![cherries](https://github.githubassets.com/images/icons/emoji/unicode/1f352.png) YAML toolkit for Neovim users
*   [andersevenrud/cmp-tmux](https://github.com/andersevenrud/cmp-tmux) - Tmux completion source for nvim-cmp and nvim-compe
*   [adriweb/EEPro-for-Nspire](https://github.com/adriweb/EEPro-for-Nspire) - FormulaPro: An open-source EEPro-like application for the TI-Nspire, written in Lua.
*   [Wiladams/LAPHLibs](https://github.com/Wiladams/LAPHLibs) - Lua Application Programming Helper Libraries
*   [LPGhatguy/luanoid](https://github.com/LPGhatguy/luanoid) - Alternative to Roblox Humanoids written entirely in Lua
*   [CharLemAznable/lua-resty-wechat](https://github.com/CharLemAznable/lua-resty-wechat) - 使用Lua编写的nginx服务器微信公众平台代理.
*   [BlueMountainsIO/OnsetLuaScripts](https://github.com/BlueMountainsIO/OnsetLuaScripts) - Example Lua scripts for Onset for you to learn from.
*   [rizaumami/merbot](https://github.com/rizaumami/merbot) - Telegram Group Administration Bot
*   [oniietzschan/erogodic](https://github.com/oniietzschan/erogodic) - A library for scripting branching interactive narrative in Lua.
*   [nvim-lua/nvim-lua-plugin-template](https://github.com/nvim-lua/nvim-lua-plugin-template) - A starter template for a Neovim plugin written in Lua
*   [nick-nh/qlua](https://github.com/nick-nh/qlua) - Quik Lua indicators
*   [icowan/lua-resty-17mon](https://github.com/icowan/lua-resty-17mon) - IP数据库之openresty版
*   [hoelzro/obvious](https://github.com/hoelzro/obvious) - Widget library for the awesome window manager
*   [fffonion/lua-resty-multiplexer](https://github.com/fffonion/lua-resty-multiplexer) - Transparent port service multiplexer for stream subsystem
*   [chen0040/lua-algorithms](https://github.com/chen0040/lua-algorithms) - Lua algorithms library that covers commonly used data structures and algorithms
*   [catwell/cw-lua](https://github.com/catwell/cw-lua) - Catwell's Lua playground
*   [Metastruct/garrysmod-chatsounds](https://github.com/Metastruct/garrysmod-chatsounds) - Community Uploaded Ingame Chat Reaction Sounds
*   [KURANADO2/hammerspoon-kuranado](https://github.com/KURANADO2/hammerspoon-kuranado) - Hammerspoon 配置
*   [AckslD/nvim-whichkey-setup.lua](https://github.com/AckslD/nvim-whichkey-setup.lua) - Nvim-plugin what wraps vim-which-key to simplify setup in lua
*   [williamwilling/luagui](https://github.com/williamwilling/luagui) - An easy-to-use library for creating GUIs with Lua.
*   [teal-language/teal-types](https://github.com/teal-language/teal-types) - Teal type definitions of Lua libraries!
*   [stevedonovan/luaish](https://github.com/stevedonovan/luaish) - A Lua REPL with global name tab-completion and a shell sub-mode
*   [spacewander/luafilesystem](https://github.com/spacewander/luafilesystem) - Reimplement luafilesystem via LuaJIT FFI
*   [sharpobject/panel-attack](https://github.com/sharpobject/panel-attack) - Tetris Attack/Panel de Pon clone in lua with LOVE
*   [rxi/coil](https://github.com/rxi/coil) - A tiny cooperative threading module for Lua
*   [rizaumami/tdcli.lua](https://github.com/rizaumami/tdcli.lua) - A simple Lua library for the telegram-cli
*   [jprjr/lua-resty-exec](https://github.com/jprjr/lua-resty-exec) - Run external programs in OpenResty without spawning a shell or blocking
*   [bungle/lua-resty-random](https://github.com/bungle/lua-resty-random) - LuaJIT FFI-based Random Library for OpenResty.
*   [Solor/FreeUI](https://github.com/Solor/FreeUI) - A user interface replacement for World of Warcraft.
*   [Rerumu/FiOne](https://github.com/Rerumu/FiOne) - Lua 5.1 bytecode interpreter, in Lua
*   [DawnAngel/lua-nats](https://github.com/DawnAngel/lua-nats) - LUA client for NATS messaging system. [https://nats.io](https://nats.io)
*   [David-Kunz/cmp-npm](https://github.com/David-Kunz/cmp-npm) - An additional source for nvim-cmp to autocomplete packages and its versions
*   [torch/argcheck](https://github.com/torch/argcheck) - A powerful (and blazing fast) argument checker and function overloading system for Lua or LuaJIT
*   [tomasguisasola/luasoap](https://github.com/tomasguisasola/luasoap) - LuaSOAP provides a very simple API that convert Lua tables to and from XML documents
*   [svof/svof](https://github.com/svof/svof) - Svof is an AI system for Achaea, an online MUD. It has advanced and adaptable curing capabilities, defence raising, and addons.
*   [pygy/strung.lua](https://github.com/pygy/strung.lua) - Lua string patterns rewritten in Lua + FFI, for LuaJIT.
*   [projekt0n/circles.nvim](https://github.com/projekt0n/circles.nvim) - uniform icons for neovim
*   [lipp/tango](https://github.com/lipp/tango) - A simple and transparent RPC module for Lua.
*   [leihog/hashids.lua](https://github.com/leihog/hashids.lua) - A Lua implementation of [http://www.hashids.org](http://www.hashids.org)
*   [jirutka/luasrcdiet](https://github.com/jirutka/luasrcdiet) - Compresses Lua source code by removing unnecessary characters (maintained fork of [http://luasrcdiet.luaforge.net/](http://luasrcdiet.luaforge.net/))
*   [iwiniwin/LuaKit](https://github.com/iwiniwin/LuaKit) - Lua核心工具包，包含对面向对象，组件系统（灵活的绑定解绑模式），mvc分模块加载，事件分发系统等常用模式的封装。同时提供打印，内存泄漏检测，性能分析等常用工具类。
*   [heroiclabs/nakama-defold](https://github.com/heroiclabs/nakama-defold) - Defold client for Nakama server.
*   [danielmgmi/lodash.lua](https://github.com/danielmgmi/lodash.lua) - lodash inspired library for lua
*   [bungle/lua-resty-libcjson](https://github.com/bungle/lua-resty-libcjson) - LuaJIT FFI-based cJSON library for OpenResty.
*   [britzl/defnet](https://github.com/britzl/defnet) - Defold networking examples
*   [EvandroLG/array.lua](https://github.com/EvandroLG/array.lua) - A small library with useful methods to handle Lua's table when it's working like an Array
*   [vavrusa/luajit-bpf](https://github.com/vavrusa/luajit-bpf) - This has been merged to to [https://github.com/iovisor/bcc](https://github.com/iovisor/bcc)
*   [sonoro1234/Lua2SC](https://github.com/sonoro1234/Lua2SC) - Lua client for supercollider scsynth and supernova
*   [simenkid/lua-events](https://github.com/simenkid/lua-events) - A Lua EventEmitter class in node.js style.
*   [poga/spacer](https://github.com/poga/spacer) - ![rocket](https://github.githubassets.com/images/icons/emoji/unicode/1f680.png)Serverless function platform for Lua
*   [peter4431/LuaSoar](https://github.com/peter4431/LuaSoar) - A lua debugger
*   [norman/lua-haml](https://github.com/norman/lua-haml) - Haml for Lua
*   [kengonakajima/lua-msgpack](https://github.com/kengonakajima/lua-msgpack) - msgpack implementation by pure Lua (5.1) works without LuajJIT and FFI.
*   [astrochili/narrator](https://github.com/astrochili/narrator) - The Ink language parser and runtime implementation in Lua.
*   [ZehMatt/Lambda](https://github.com/ZehMatt/Lambda) - Half-Life 2 series Co-Op Gamemode
*   [Shadorain/shadovim](https://github.com/Shadorain/shadovim) - A neovim setup for the shadow warriors. Speed through the light with the power of shadovim built on the new Lua based neovim! With the highly overpowered native LSP, built in auto-completion, snippets, menus and so much more, you will unleash the power of a hundred million shadows!
*   [JakobOvrum/LuaIRC](https://github.com/JakobOvrum/LuaIRC) - IRC library for Lua
*   [Hoizame/AtlasLootClassic](https://github.com/Hoizame/AtlasLootClassic) - AtlasLootClassic
*   [AbyssEngine/OpenDiablo2](https://github.com/AbyssEngine/OpenDiablo2) - An implementation of Diablo 2 in AbyssEngine.
*   [xlibor/lxlib](https://github.com/xlibor/lxlib) - a web application framework based on OpenResty(ngx+lua)
*   [rm-code/love-IDEA-plugin](https://github.com/rm-code/love-IDEA-plugin) - A LÖVE-Plugin for IntelliJ IDEA and PHPStorm. (Looking for new maintainer!)
*   [rhgao/Im2Flow](https://github.com/rhgao/Im2Flow) - Im2Flow: Motion Hallucination from Static Images for Action Recognition (CVPR 2018)
*   [rafamadriz/dotfiles](https://github.com/rafamadriz/dotfiles) - There's lots of configurations out there, but this one is mine.
*   [pfirsich/lua-discordRPC](https://github.com/pfirsich/lua-discordRPC) - LuaJIT FFI Wrapper for the Discord Rich Presence API
*   [nczempin/Turres-Monacorum](https://github.com/nczempin/Turres-Monacorum) - scifi tower defense made with löve2d and lua
*   [najsword/serverOne](https://github.com/najsword/serverOne) - 标签：lua skynet 大厅+房间+匹配模式 推荐理由：skynet模块少，有很多用c封装的底层接口，对个人学习底层核心功能实现有指导作用。
*   [detailyang/lua-resty-cors](https://github.com/detailyang/lua-resty-cors) - It's the implement of CORS on OpenResty
*   [chen0040/lua-graph](https://github.com/chen0040/lua-graph) - Graph algorithms in lua
*   [calio/luaflow](https://github.com/calio/luaflow) - A tool like GNU cflow but for Lua programming language
*   [Humbedooh/server-status](https://github.com/Humbedooh/server-status) - mod\_lua version of the Apache httpd's mod\_status using dynamic charts
*   [osa1/language-lua](https://github.com/osa1/language-lua) - Lua parser and pretty-printer
*   [lloydzhou/lua-resty-cache](https://github.com/lloydzhou/lua-resty-cache) - http cache to redis, can server stale response, and using "lua-resty-lock" only allow one request to populate a new cache
*   [leafo/web\_sanitize](https://github.com/leafo/web_sanitize) - Lua library for sanitizing untrusted HTML
*   [detailyang/lua-resty-socks5-server](https://github.com/detailyang/lua-resty-socks5-server) - This is an implementation of the SOCKS v5 server in the OpenResty
*   [bungle/lua-resty-reqargs](https://github.com/bungle/lua-resty-reqargs) - Read application/x-www-form-urlencoded, multipart/form-data, and application/json request args
*   [Playermet/luajit-glfw](https://github.com/Playermet/luajit-glfw) - GLFW bindings for LuaJIT
*   [famiu/feline.nvim](https://github.com/famiu/feline.nvim) - A minimal, stylish and customizable statusline for Neovim written in Lua
*   [samrathchadha/kyoto.nvim](https://github.com/samrathchadha/kyoto.nvim) - kyoto.nvim is a functional, beautiful, and highly customizable neovim configuration
*   [shaunsingh/nix-darwin-dotfiles](https://github.com/shaunsingh/nix-darwin-dotfiles) - Dotfiles managed via Nix-Darwin and Mk-Darwin-System, for schoolwork and kotlin, lua, and rust programming
*   [ojroques/nvim-hardline](https://github.com/ojroques/nvim-hardline) - A simple Neovim statusline written in Lua
*   [mebens/ammo](https://github.com/mebens/ammo) - A simple, flexible organisational library for use with the LÖVE game engine.
*   [WetDesertRock/vivid](https://github.com/WetDesertRock/vivid) - Vivid is a simple lua library for dealing with simple color math.
*   [zhengguo07q/UnityLuaFramework](https://github.com/zhengguo07q/UnityLuaFramework) - 一个用LUA写的框架游戏框架
*   [sniper00/BallGame](https://github.com/sniper00/BallGame) - moon game server的一个使用示例，搭建简单的服务器框架
*   [kevinlekiller/mpv\_scripts](https://github.com/kevinlekiller/mpv_scripts) - Various lua scripts for the [http://mpv.io](http://mpv.io) video player.
*   [hylun/lua-resty-yii](https://github.com/hylun/lua-resty-yii) - A network framework based on OpenResty Imitation Yii2
*   [bjornbytes/maf](https://github.com/bjornbytes/maf) - 3D math library for Lua
*   [aconbere/vert](https://github.com/aconbere/vert) - Virtual Environments For Lua
*   [SLMP-Team/SLMP](https://github.com/SLMP-Team/SLMP) - OpenSource GTA: San Andreas Multiplayer based on Lua Language
*   [FPtje/Sublime-GLua-Highlight](https://github.com/FPtje/Sublime-GLua-Highlight) - GMod Lua syntax highlighting for Sublime Text 2 and 3
*   [DoubleSpout/lua-resty-aries](https://github.com/DoubleSpout/lua-resty-aries) - openresty and lua multi-function template
*   [luakit/luakit-plugins](https://github.com/luakit/luakit-plugins) - Version control for various luakit plugins.
*   [cloudwu/luacc](https://github.com/cloudwu/luacc) - LUACC allows you write C code in lua
*   [kristijanhusak/orgmode.nvim](https://github.com/kristijanhusak/orgmode.nvim) - Orgmode clone written in Lua for Neovim 0.5+.
*   [samrath2007/kyoto.nvim](https://github.com/samrath2007/kyoto.nvim) - kyoto.nvim is a functional, beautiful, and highly customizable neovim configuration
*   [mattleong/CosmicNvim](https://github.com/mattleong/CosmicNvim) - CosmicNvim is a lightweight and opinionated Neovim config for web development, specifically designed to provide a ![dizzy](https://github.githubassets.com/images/icons/emoji/unicode/1f4ab.png) COSMIC programming experience!
*   [benbusby/earthbound-themes](https://github.com/benbusby/earthbound-themes) - A unique color theme generator for Vim, VSCode, Atom, and Sublime
*   [noib3/cokeline.nvim](https://github.com/noib3/cokeline.nvim) - ![nose](https://github.githubassets.com/images/icons/emoji/unicode/1f443.png) A neovim bufferline for people with addictive personalities
*   [doujiang24/lua-resty-ini](https://github.com/doujiang24/lua-resty-ini) - lua-resty-ini - ini parser for OpenResty
*   [clementfarabet/lua---csv](https://github.com/clementfarabet/lua---csv) - A package to read and write CSV. Provides high-level database-like handlers.
*   [svermeulen/nvim-moonmaker](https://github.com/svermeulen/nvim-moonmaker) - Moonscript plugin support for neovim
*   [robmiracle/Simple-Table-Load-Save-Functions-for-Corona-SDK](https://github.com/robmiracle/Simple-Table-Load-Save-Functions-for-Corona-SDK) - Two very simple load and save function to store a Lua Table and Read it back in. Requires the Corona SDK JSON Library
*   [maxiwell/conky-seamod](https://github.com/maxiwell/conky-seamod) - Seamod theme for conky 1.10 (lua config)
*   [hnakamur/luajit-examples](https://github.com/hnakamur/luajit-examples) - my example codes for LuaJIT
*   [gamax92/midi2pico](https://github.com/gamax92/midi2pico) - Midi to PICO-8 converter
*   [davidm/lua-compress-deflatelua](https://github.com/davidm/lua-compress-deflatelua) - DEFLATE (RFC1951)/gunzip implemented in pure Lua
*   [bakpakin/moonmint](https://github.com/bakpakin/moonmint) - A Web Framework for Lua
*   [CasimirKaPazi/Voxelgarden](https://github.com/CasimirKaPazi/Voxelgarden) - Subgame for Minetest
*   [LIKO-12/Legacy](https://github.com/LIKO-12/Legacy) - LIKO-12 is an open source fantasy computer made using LÖVE.
*   [CandyMi/cfadmin](https://github.com/CandyMi/cfadmin) - A lua web network framework.
*   [mrjones2014/dash.nvim](https://github.com/mrjones2014/dash.nvim) - ![telescope](https://github.githubassets.com/images/icons/emoji/unicode/1f52d.png) Search Dash.app from Neovim with Telescope. Built with Lua and Rust ![crab](https://github.githubassets.com/images/icons/emoji/unicode/1f980.png)
*   [kikito/sandbox.lua](https://github.com/kikito/sandbox.lua) - A lua sandbox for executing non-trusted code
*   [MinecraftU/mcu-curriculum](https://github.com/MinecraftU/mcu-curriculum) - Minecraft U Curriculum
*   [tbastos/lift](https://github.com/tbastos/lift) - Lua automation tool and scripting framework
*   [starwing/luaiter](https://github.com/starwing/luaiter) - A iteration library for Lua
*   [qwe7989199/Lyric-Importer-for-Aegisub](https://github.com/qwe7989199/Lyric-Importer-for-Aegisub) - Lua scripts for importing .krc .qrc .lrc to Aegisub
*   [moteus/luacov-coveralls](https://github.com/moteus/luacov-coveralls) - LuaCov reporter for coveralls.io service
*   [moteus/lua-path](https://github.com/moteus/lua-path) - File system path manipulation library
*   [liuxq/kbengine\_unity3d\_lua\_plugins](https://github.com/liuxq/kbengine_unity3d_lua_plugins) - kbengine的lua版unity客户端插件
*   [iamaleksey/lua-zmq](https://github.com/iamaleksey/lua-zmq) - Lua zeromq2 binding
*   [aiq/luazdf](https://github.com/aiq/luazdf) - LuaZDF - Lua Zero Dependency Functions
*   [VideoOS/VideoOS-lua-app](https://github.com/VideoOS/VideoOS-lua-app) - VideoOS 官方实现的 lua 小程序：[http://store.videojj.com](http://store.videojj.com)
*   [GUI/lua-libcidr-ffi](https://github.com/GUI/lua-libcidr-ffi) - LuaJIT FFI bindings to libcidr. Provides CIDR calculations for IPv4 and IPv6.
*   [zym2014/MoonWarriors-lua](https://github.com/zym2014/MoonWarriors-lua) - 《雷电战机》游戏-Lua移植版
*   [xinmingyao/skynet\_web](https://github.com/xinmingyao/skynet_web) - http websocket support lua skynet
*   [unanimated/luaegisub](https://github.com/unanimated/luaegisub) - Aegisub automation scripts
*   [mpeterv/markdown](https://github.com/mpeterv/markdown) - An implementation of the Markdown text-to-html markup system in pure Lua.
*   [luapower/winapi](https://github.com/luapower/winapi) - winapi Lua+ffi binding
*   [keplerproject/lua-compat-5.2](https://github.com/keplerproject/lua-compat-5.2) - Compatibility module providing Lua-5.2-style APIs for Lua 5.1
*   [gityf/ngx\_lua\_thrift](https://github.com/gityf/ngx_lua_thrift) - thrift lua for nginx.
*   [devyte/nodemcu-platform](https://github.com/devyte/nodemcu-platform) - A platform to serve as a base for nodemcu-firmware Lua applications
*   [FourierTransformer/ftcsv](https://github.com/FourierTransformer/ftcsv) - a fast csv library written in pure Lua
*   [hoob3rt/lualine.nvim](https://github.com/hoob3rt/lualine.nvim) - A blazing fast and easy to configure neovim statusline plugin written in pure lua.
*   [shiguredo/luli](https://github.com/shiguredo/luli) - A static analysis and linter tool for Lua
*   [artemshein/luv](https://github.com/artemshein/luv) - \[abandoned\] Lua MVC web-framework
*   [25A0/Quadtastic](https://github.com/25A0/Quadtastic) - A tool to manage sprite sheets and color palettes
*   [wudi/nlgm](https://github.com/wudi/nlgm) - NLGM (Nginx Lua GraphicsMagick) 提供一种实时处理图片的思路
*   [rxi/shash](https://github.com/rxi/shash) - A simple, lightweight spatial hash for Lua
*   [rktjmp/fwatch.nvim](https://github.com/rktjmp/fwatch.nvim) - fwatch.nvim lets you watch files or directories for changes and then run vim commands or lua functions.
*   [ppissanetzky/AndThen](https://github.com/ppissanetzky/AndThen) - Lua Promises library inspired by Q
*   [jonniek/mpv-filenavigator](https://github.com/jonniek/mpv-filenavigator) - Navigate and open your local files in mpv
*   [asamy/forgottenmapeditor](https://github.com/asamy/forgottenmapeditor) - Map editor written in lua for Open Tibia. Written with OtClient's framework.
*   [a327ex/chrono](https://github.com/a327ex/chrono) - Timer module for LÖVE
*   [Oarcinae/FactorioScenarioMultiplayerSpawn](https://github.com/Oarcinae/FactorioScenarioMultiplayerSpawn) - A custom scenario for Factorio which provides each player a unique starting spawn point in a multiplayer game.
*   [MarkoPaul0/WireBait](https://github.com/MarkoPaul0/WireBait) - Run and test your Lua Wireshark dissector without Wireshark or capture data.
*   [Kong/lua-multipart](https://github.com/Kong/lua-multipart) - Multipart Parser for Lua
*   [IrcDirk/Carbonite-Classic](https://github.com/IrcDirk/Carbonite-Classic) - Carbonite + Modules for WoW Classic
*   [EvandroLG/computer\_science\_in\_lua](https://github.com/EvandroLG/computer_science_in_lua) - ![first_quarter_moon_with_face](https://github.githubassets.com/images/icons/emoji/unicode/1f31b.png) Implementation of some classic data structures and algorithms in Lua
*   [catwell/lua-multipart-post](https://github.com/catwell/lua-multipart-post) - HTTP Multipart Post helper that does just that.
*   [vhyrro/neorg](https://github.com/vhyrro/neorg) - Modernity meets insane extensibility. The future of organizing your life in Neovim.
*   [Olical/aniseed](https://github.com/Olical/aniseed) - Neovim configuration and plugins in Fennel (Lisp compiled to Lua)
*   [DeadlyBossMods/DeadlyBossMods](https://github.com/DeadlyBossMods/DeadlyBossMods) - The ultimate encounter helper (for Retail) to give you fight info that's easy to process at a glance. DBM aims to focus on what's happening to you, and what YOU need to do about it.
*   [hackorum/VapourNvim](https://github.com/hackorum/VapourNvim) - A NeoVim config for THE ULTIMATE vim IDE-like experience.
*   [Vicious-wow/XIV\_Databar](https://github.com/Vicious-wow/XIV_Databar) - AddOn for WoW that displays a databar at the bottom/top of the screen with several modules and customization options.
*   [vsbenas/parser-gen](https://github.com/vsbenas/parser-gen) - A parser generator in Lua using PEG syntax.
*   [akinsho/nvim-toggleterm.lua](https://github.com/akinsho/nvim-toggleterm.lua) - A neovim lua plugin to help easily manage multiple terminal windows
*   [npxbr/glow.nvim](https://github.com/npxbr/glow.nvim) - A markdown preview directly in your neovim.
*   [npxbr/gruvbox.nvim](https://github.com/npxbr/gruvbox.nvim) - Lua port of the most famous vim colorscheme
*   [tami5/sql.nvim](https://github.com/tami5/sql.nvim) - SQLite/LuaJIT binding for lua and neovim
*   [tullamods/Combuctor](https://github.com/tullamods/Combuctor) - Single window displays for you items
*   [tongtzeho/HearthSprite](https://github.com/tongtzeho/HearthSprite) - Android炉石传说脚本
*   [robotboy655/gmod-lua-menu](https://github.com/robotboy655/gmod-lua-menu) - A Lua powered ( No HTML ) main menu for Garry's Mod.
*   [chudongjingling/open\_code](https://github.com/chudongjingling/open_code) - 开源脚本，持续更新~触动 Lua 开发交流 QQ 群：187139891
*   [erogol/seg-torch](https://github.com/erogol/seg-torch) - Segmentation with deep learning
*   [siduck76/neovim-dotfiles](https://github.com/siduck76/neovim-dotfiles) - beautiful neovim setup configured in lua
*   [franko/lite-xl](https://github.com/franko/lite-xl) - A lightweight text editor written in Lua
*   [xjdrew/levent](https://github.com/xjdrew/levent) - lua concurrency library based on libev, similar with gevent
*   [kdav5758/TrueZen.nvim](https://github.com/kdav5758/TrueZen.nvim) - ![feather](https://github.githubassets.com/images/icons/emoji/unicode/1fab6.png) Clean and elegant distraction-free writing for NeoVim.
*   [tongson/LadyLua](https://github.com/tongson/LadyLua) - Single executable(static), batteries included, Lua 5.1 interpreter.
*   [ellisonleao/dotfiles](https://github.com/ellisonleao/dotfiles) - ![floppy_disk](https://github.githubassets.com/images/icons/emoji/unicode/1f4be.png) personal configuration files
*   [zorggn/LoveTracker](https://github.com/zorggn/LoveTracker) - A module tracker written in lua/LöVE.
*   [tdy/awesome](https://github.com/tdy/awesome) - Configs for awesomeWM
*   [pirogoeth/lsso](https://github.com/pirogoeth/lsso) - Nginx SSO middleware for protecting your internets.
*   [kennethreitz/super-sphere](https://github.com/kennethreitz/super-sphere) - A minimal action game by Kenneth Reitz.
*   [jasonsantos/remdebug](https://github.com/jasonsantos/remdebug) - Remote debugger for Lua using LuaSocket. RemDebug offers breakpoints, inspection, step into, step over and watch expressions using a simple command-line controller. The protocol allows the use of the debugger engine with other client interfaces.
*   [mkottman/lua-git](https://github.com/mkottman/lua-git) - An attempt to implement the basics of Git in pure Lua
*   [kmarkus/rFSM](https://github.com/kmarkus/rFSM) - rFSM is a lightweight Statechart implementation in Lua
*   [LukeMS/lua-namegen](https://github.com/LukeMS/lua-namegen) - Lua Name Generator
*   [siduck76/chad-nvim](https://github.com/siduck76/chad-nvim) - beautiful neovim setup configured in lua
*   [JavaCafe01/dotfiles](https://github.com/JavaCafe01/dotfiles) - Configuration files I use on my main machine
*   [folke/lsp-trouble.nvim](https://github.com/folke/lsp-trouble.nvim) - ![vertical_traffic_light](https://github.githubassets.com/images/icons/emoji/unicode/1f6a6.png) A pretty diagnostics list to help you solve all the trouble your code is causing.
*   [haproxytech/haproxy-lua-jwt](https://github.com/haproxytech/haproxy-lua-jwt) - JWT Validation implementation for HAProxy Lua host
*   [ojdon/pico8-boilerplate](https://github.com/ojdon/pico8-boilerplate) - ![joystick](https://github.githubassets.com/images/icons/emoji/unicode/1f579.png) A game starter template for Pico-8 developers!
*   [upyun/lua-resty-sync](https://github.com/upyun/lua-resty-sync) - Synchronizing data based on version changes
*   [tarantool/mqtt](https://github.com/tarantool/mqtt) - Tarantool MQTT client
*   [lipp/nodish](https://github.com/lipp/nodish) - A Lightweight Lua equivalent to Node.js
*   [hishamhm/tabular](https://github.com/hishamhm/tabular) - Tabular representation of Lua data
*   [Eonblast/fleece-lite](https://github.com/Eonblast/fleece-lite) - Fast Lua to JSON
*   [CloudSixteen/Clockwork](https://github.com/CloudSixteen/Clockwork) - A roleplaying framework developed by Cloud Sixteen for the people.
*   [robmiracle/Corona-SDK-RSS-Reader](https://github.com/robmiracle/Corona-SDK-RSS-Reader) - A way to read RSS feeds using Lua and Corona SDK
*   [mangoszero/LuaScripts](https://github.com/mangoszero/LuaScripts) - Eluna Scripts for MangosZero
*   [bsm/fakengx](https://github.com/bsm/fakengx) - Library for testing Lua scripts embedded into Nginx
*   [ToddWegner/clidebugger](https://github.com/ToddWegner/clidebugger) - A simple command line interface debugger for Lua 5.1 written in pure Lua. Its not dependent on anything other than the standard Lua 5.1 libraries. It was inspired by RemDebug but does not have its remote facilities.
*   [LuaDevelopmentTools/luaformatter](https://github.com/LuaDevelopmentTools/luaformatter) - Beautifies Lua code
*   [DelusionalLogic/pngLua](https://github.com/DelusionalLogic/pngLua) - A pure lua implementation of a PNG decoder
*   [siduck76/neovim-dots](https://github.com/siduck76/neovim-dots) - beautiful neovim setup configured in lua
*   [openresty/lua-tablepool](https://github.com/openresty/lua-tablepool) - Lua table recycling pools for LuaJIT
*   [incinirate/Riko4](https://github.com/incinirate/Riko4) - A Fantasy Console intended as a tool for pixel art game development.
*   [kenreitz42/super-sphere](https://github.com/kenreitz42/super-sphere) - A minimal action game by Kenneth Reitz.
*   [tonetheman/love\_shaders](https://github.com/tonetheman/love_shaders) - some shaders that work for love lua 0.9.1
*   [lunarlang/lunar](https://github.com/lunarlang/lunar) - Lunar is a superset programming language of Lua 5.1 with optional static typing, inspired by TypeScript and Ruby.
*   [SPR-CPU-ORG/F80](https://github.com/SPR-CPU-ORG/F80) - A Professional Telegram-Bot Based On valtman.name/telegram-cli
*   [upvalue/love-repl](https://github.com/upvalue/love-repl) - Magic-free in-game REPL for the Love game engine
*   [pygy/require.lua](https://github.com/pygy/require.lua) - `require()` rewritten in plain Lua
*   [nly/SingleLua](https://github.com/nly/SingleLua) - Simple but powerful ngx\_lua web framework
*   [lewei50/lua-on-nodemcu](https://github.com/lewei50/lua-on-nodemcu) - Lua lib for lewei50(iot) platform
*   [leeyiw/ngx\_lua\_anticc](https://github.com/leeyiw/ngx_lua_anticc) - HTTP flood attacks mitigation tool for Nginx
*   [ireaderlab/lua\_nsc](https://github.com/ireaderlab/lua_nsc) - dynamic upstream control on nginx
*   [hkupty/impromptu.nvim](https://github.com/hkupty/impromptu.nvim) - Create prompts fast and easy
*   [fsantanna/luagravity](https://github.com/fsantanna/luagravity) - LuaGravity is a reactive language that implements the synchronous approach for concurrency.
*   [creationix/lua-git](https://github.com/creationix/lua-git) - Git implementation in pure lua for luvit.
*   [benanders/LuaIDE](https://github.com/benanders/LuaIDE) - An in-game IDE for ComputerCraft
*   [agentzh/lua-resty-multipart-parser](https://github.com/agentzh/lua-resty-multipart-parser) - Simple multipart data parser for OpenResty/Lua
*   [LinkedInAttic/dmarc-msys](https://github.com/LinkedInAttic/dmarc-msys) - This set of scripts in Lua implements DMARC policy checking and reporting for the Message Systems MTA products, a popular extendable commercial MTA.
*   [liuhaopen/LuaECS](https://github.com/liuhaopen/LuaECS) - unity ecs framework implemented by Lua
*   [kieselsteini/msgpack](https://github.com/kieselsteini/msgpack) - A MessagePack implementation for Lua 5.3 - msgpack.org\[Lua\]
*   [denglf/FormatLua](https://github.com/denglf/FormatLua) - Formatting lua to a more readable form by using Lua Development Tools library.
*   [cornelisse/LuaFSM](https://github.com/cornelisse/LuaFSM) - Finite State Machine library for Lua
*   [jamesmarlowe/lua-resty-s3](https://github.com/jamesmarlowe/lua-resty-s3) - Lua driver for uploading content to amazon s3
*   [unXedDani/Artal](https://github.com/unXedDani/Artal) - A .PSD parsing library for LÖVE
*   [nrk/hige](https://github.com/nrk/hige) - {{growing mustaches in your templates with Lua}}
*   [kikito/passion](https://github.com/kikito/passion) - An object-oriented LÖVE game engine
*   [kaytotes/ImprovedBlizzardUI](https://github.com/kaytotes/ImprovedBlizzardUI) - General improvements to the Blizzard UI
*   [jie123108/lua-resty-stats](https://github.com/jie123108/lua-resty-stats) - lua-resty-stats - is a statistical module for nginx base on ngx\_lua, Statistical key and values are configurable, can use the nginx core's variables and this module's variables. The statistical result store in mongodb.
*   [Sorroko/cclite](https://github.com/Sorroko/cclite) - A cc emulator written in lua
*   [KSDaemon/Loowy](https://github.com/KSDaemon/Loowy) - Lua WAMP client
*   [eugeneia/s-lua](https://github.com/eugeneia/s-lua) - S-Lua, S-expressions and Macros for Lua
*   [dannote/lua-template](https://github.com/dannote/lua-template) - The simplest Lua template engine
*   [apache/incubator-apisix](https://github.com/apache/incubator-apisix) - The Cloud-Native API Gateway
*   [chetannaik/learning\_torch](https://github.com/chetannaik/learning_torch) - Learning to program in Lua using "Torch" and other useful libraries
*   [starius/lua-resty-socks5](https://github.com/starius/lua-resty-socks5) - Lua SOCKS5 client for the ngx\_lua based on the cosocket API
*   [robinef/ua-lua](https://github.com/robinef/ua-lua) - LUA User-Agent detector
*   [noma4i/lua-api-client](https://github.com/noma4i/lua-api-client) - Lua REST API Client
*   [mistsv/luardkafka](https://github.com/mistsv/luardkafka) - WARNING: this repo is not maintained anymore
*   [luoxinliang/pomelo\_quick\_x](https://github.com/luoxinliang/pomelo_quick_x) - pomelo lua(quick-cocos2d-x) client.
*   [HridayHS/aimware\_lua\_scripts](https://github.com/HridayHS/aimware_lua_scripts) - Lua scripts for AIMWARE Counter Strike: Global Offensive hack.
*   [ErnieE5/ee5\_base64](https://github.com/ErnieE5/ee5_base64) - Lua base64 encoding
*   [SquidDev-CC/CC-Tweaked](https://github.com/SquidDev-CC/CC-Tweaked) - Just another ComputerCraft fork
*   [lanoox/luject](https://github.com/lanoox/luject) - A static injector of dynamic library for application (android, iphoneos, macOS, windows, linux)
*   [presidentbeef/brat](https://github.com/presidentbeef/brat) - Brat is a little language for people who don't like to be told what to do.
*   [wbthomason/lsp-status.nvim](https://github.com/wbthomason/lsp-status.nvim) - Utility functions for getting diagnostic status and progress messages from LSP servers, for use in the Neovim statusline
*   [Vigemus/nvimux](https://github.com/Vigemus/nvimux) - Neovim as a TMUX replacement
*   [adnzzzzZ/windfield](https://github.com/adnzzzzZ/windfield) - Physics module for LÖVE
*   [steve0511/resty-redis-cluster](https://github.com/steve0511/resty-redis-cluster) - Openresty lua client for redis cluster.
*   [adnzzzzZ/STALKER-X](https://github.com/adnzzzzZ/STALKER-X) - Camera module for LÖVE
*   [adnzzzzZ/boipushy](https://github.com/adnzzzzZ/boipushy) - Input module for LÖVE
*   [Kong/kong](https://github.com/Kong/kong) - ![gorilla](https://github.githubassets.com/images/icons/emoji/unicode/1f98d.png) The Cloud-Native API Gateway
*   [GUI/lua-resty-auto-ssl](https://github.com/GUI/lua-resty-auto-ssl) - On the fly (and free) SSL registration and renewal inside OpenResty/nginx with Let's Encrypt.