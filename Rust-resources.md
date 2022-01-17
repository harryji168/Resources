## Rust

Rust is a multi-paradigm, general-purpose programming language designed for performance and safety, especially safe concurrency.[12][13] Rust is syntactically similar to C++,[14] but can guarantee memory safety by using a borrow checker to validate references.[15] Rust achieves memory safety without garbage collection, and reference counting is optional.[16][17] Rust has been called a systems programming language and in addition to high-level features such as functional programming it also offers mechanisms for low-level memory management.

First appearing in 2010, Rust was designed by Graydon Hoare at Mozilla Research,[18] with contributions from Dave Herman, Brendan Eich, and others.[19][20] The designers refined the language while writing the Servo experimental browser engine[21] and the Rust compiler. Rust's major influences include C++, OCaml, Haskell, and Erlang.[5] It has gained increasing use and investment in industry, by companies including Amazon, Discord, Dropbox, Facebook, Google, and Microsoft.

Rust has been voted the "most loved programming language" in the Stack Overflow Developer Survey every year since 2016, and was used by 7% of the respondents in 2021.[22]
 
 

*   [Applications](#applications)
    *   [Audio and Music](#audio-and-music)
    *   [Cryptocurrencies](#cryptocurrencies)
    *   [Database](#database)
    *   [Emulators](#emulators)
    *   [Games](#games)
    *   [Graphics](#graphics)
    *   [Image processing](#image-processing)
    *   [Industrial automation](#industrial-automation)
    *   [Observability](#observability)
    *   [Operating systems](#operating-systems)
    *   [Productivity](#productivity)
    *   [Security tools](#security-tools)
    *   [System tools](#system-tools)
    *   [Task scheduling](#task-scheduling)
    *   [Text editors](#text-editors)
    *   [Text processing](#text-processing)
    *   [Utilities](#utilities)
    *   [Video](#video)
    *   [Virtualization](#virtualization)
    *   [Web](#web)
    *   [Web Servers](#web-servers)
*   [Development tools](#development-tools)
    *   [Build system](#build-system)
    *   [Debugging](#debugging)
    *   [Deployment](#deployment)
    *   [Embedded](#embedded)
    *   [FFI](#ffi)
    *   [IDEs](#ides)
    *   [Pattern recognition](#pattern-recognition)
    *   [Profiling](#profiling)
    *   [Services](#services)
    *   [Static analysis](#static-analysis)
    *   [Testing](#testing)
    *   [Transpiling](#transpiling)
*   [Libraries](#libraries)
    *   [Artificial Intelligence](#artificial-intelligence)
        *   [Genetic algorithms](#genetic-algorithms)
        *   [Machine learning](#machine-learning)
    *   [Astronomy](#astronomy)
    *   [Asynchronous](#asynchronous)
    *   [Audio and Music](#audio-and-music-1)
    *   [Authentication](#authentication)
    *   [Automotive](#automotive)
    *   [Bioinformatics](#bioinformatics)
    *   [Caching](#caching)
    *   [Cloud](#cloud)
    *   [Command-line](#command-line)
    *   [Compression](#compression)
    *   [Computation](#computation)
    *   [Concurrency](#concurrency)
    *   [Configuration](#configuration)
    *   [Cryptography](#cryptography)
    *   [Data processing](#data-processing)
    *   [Data streaming](#data-streaming)
    *   [Data structures](#data-structures)
    *   [Data visualization](#data-visualization)
    *   [Database](#database-1)
    *   [Date and time](#date-and-time)
    *   [Distributed systems](#distributed-systems)
    *   [Domain driven design](#domain-driven-design)
    *   [Email](#email)
    *   [Encoding](#encoding)
    *   [Filesystem](#filesystem)
    *   [Functional Programming](#functional-programming)
    *   [Game development](#game-development)
    *   [Geospatial](#geospatial)
    *   [Graph processing](#graph-processing)
    *   [Graphics](#graphics-1)
    *   [GUI](#gui)
    *   [Image processing](#image-processing)
    *   [Language specification](#language-specification)
    *   [Logging](#logging)
    *   [Macro](#macro)
    *   [Markup language](#markup-language)
    *   [Mobile](#mobile)
    *   [Network programming](#network-programming)
    *   [Packaging formats](#packaging-formats)
    *   [Parsing](#parsing)
    *   [Peripherals](#peripherals)
    *   [Platform specific](#platform-specific)
    *   [Scripting](#scripting)
    *   [Simulation](#simulation)
    *   [Task scheduling](#task-scheduling-1)
    *   [Template engine](#template-engine)
    *   [Text processing](#text-processing-1)
    *   [Text search](#text-search)
    *   [Unsafe](#unsafe)
    *   [Virtualization](#virtualization-1)
    *   [Web programming](#web-programming)
*   [Registries](#registries)
*   [Resources](#resources)
*   [License](#license)

[](#applications)Applications
-----------------------------

See also [Rust — Production](https://www.rust-lang.org/production) organizations running Rust in production.

*   [alacritty](https://github.com/alacritty/alacritty) — A cross-platform, GPU enhanced terminal emulator
*   [andschwa/rust-genetic-algorithm](https://github.com/andschwa/rust-genetic-algorithm) — A genetic algorithm for academic benchmark problems [![build badge](https://camo.githubusercontent.com/24d503dd6b7f2e23dcc6a950b4194acf919b21a8880c7213de039af17cb6d7ad/68747470733a2f2f6170692e7472617669732d63692e6f72672f616e6473636877612f727573742d67656e657469632d616c676f726974686d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/andschwa/rust-genetic-algorithm)
*   [asm-cli-rust](https://github.com/cch123/asm-cli-rust) — An interactive assembly shell written in rust.
*   [cloudflare/boringtun](https://github.com/cloudflare/boringtun) — A Userspace WireGuard VPN Implementation [![build badge](https://camo.githubusercontent.com/f287c0eebbef025799317ca262ba4e872a1ef14da441eaced804ca5301cc2e56/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6372617465732e696f2d76302e322e302d6f72616e67652e737667)](https://crates.io/crates/boringtun)
*   [datafusion](https://github.com/apache/arrow-datafusion) — Apache Arrow DataFusion and Ballista query engines
*   [denoland/deno](https://github.com/denoland/deno) — A secure JavaScript/TypeScript runtime built with V8, Rust, and Tokio [![Build Status](https://github.com/denoland/deno/workflows/ci/badge.svg?branch=master&event=push)](https://github.com/denoland/deno/actions)
*   [Factotum](https://github.com/snowplow/factotum) — [A system to programmatically run data pipelines](https://snowplowanalytics.com/blog/2016/04/09/introducing-factotum-data-pipeline-runner/) [![build badge](https://camo.githubusercontent.com/3116d6aa990fbff365c7b540f84d8e0862f4f9a22bcfa7a8d165412a9e06d5a1/68747470733a2f2f6170692e7472617669732d63692e6f72672f736e6f77706c6f772f666163746f74756d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/snowplow/factotum)
*   [fcsonline/drill](https://github.com/fcsonline/drill) — A HTTP load testing application inspired by Ansible syntax [![build badge](https://camo.githubusercontent.com/df488621566c7f9aeb399ae64a0666c1ccf10ae324d034bec82863d0bdc94af2/68747470733a2f2f6170692e7472617669732d63692e6f72672f6663736f6e6c696e652f6472696c6c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/fcsonline/drill)
*   [Fractalide](https://github.com/fractalide/fractalide) — Simple Rust Microservices
*   [habitat](https://github.com/habitat-sh/habitat) — An tool created by [Chef](https://www.chef.io/) to build, deploy, and manage applications.
*   [Herd](https://github.com/imjacobclark/Herd) — an experimental HTTP load testing application
*   [ivanceras/diwata](https://github.com/ivanceras/diwata) — A database administration tool for postgresql [![build badge](https://camo.githubusercontent.com/fbcc7eda14af70f368b443895f516842e2e9504babe92c67cd1e179655ae921a/68747470733a2f2f6170692e7472617669732d63692e6f72672f6976616e63657261732f6469776174612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ivanceras/diwata)
*   [jedisct1/flowgger](https://github.com/awslabs/flowgger) — A fast, simple and lightweight data collector
*   [kalker](https://github.com/PaddiM8/kalker) - A scientific calculator that supports math-like syntax with user-defined variables, functions, derivation, integration, and complex numbers. Cross platform + WASM support [![Build Status](https://github.com/PaddiM8/kalker/workflows/Release/badge.svg)](https://github.com/PaddiM8/kalker/actions)
*   [kytan](https://github.com/changlan/kytan) — High Performance Peer-to-Peer VPN
*   [linkerd/linkerd2-proxy](https://github.com/linkerd/linkerd2-proxy) — Ultralight service mesh for Kubernetes.
*   [MaidSafe](https://github.com/maidsafe) — A decentralized platform.
*   [mdBook](https://crates.io/crates/mdbook) — A command line utility to create books from markdown files [![Build Status](https://github.com/rust-lang/mdBook/workflows/CI/badge.svg?branch=master)](https://github.com/rust-lang/mdBook/actions)
*   [nicohman/eidolon](https://github.com/nicohman/eidolon) — A steam and drm-free game registry and launcher for linux and macosx [![build badge](https://camo.githubusercontent.com/27ee1cd7ad89a5271f8f570c5cfa820f526628727f95033506661b305aad2288/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e69636f686d616e2f6569646f6c6f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/nicohman/eidolon)
*   [notty](https://github.com/withoutboats/notty) — A new kind of terminal
*   [Pijul](https://pijul.org) — A patch-based distributed version control system
*   [Rudr](https://github.com/oam-dev/rudr) — A Kubernetes implementation of the [Open Application Model](https://oam.dev/) specification [![Build Status](https://github.com/oam-dev/rudr/workflows/Rust/badge.svg?branch=master)](https://github.com/oam-dev/rudr/actions)
*   [rx](https://github.com/cloudhead/rx) — Vi inspired Modern Pixel Art Editor
*   [Servo](https://github.com/servo/servo) — A prototype web browser engine
*   [tiny](https://github.com/osa1/tiny) — A terminal IRC client
*   [trust-dns](https://crates.io/crates/trust-dns) — A DNS-server [![Build Status](https://github.com/bluejekyll/trust-dns/workflows/test/badge.svg?branch=main)](https://github.com/bluejekyll/trust-dns/actions?query=workflow%3Atest)
*   [wasmer](https://github.com/wasmerio/wasmer) — A safe and fast WebAssembly runtime supporting WASI and Emscripten [![Build Status](https://github.com/wasmerio/wasmer/workflows/build/badge.svg?style=flat-square)](https://github.com/wasmerio/wasmer/actions)
*   [Weld](https://github.com/serayuzgur/weld) — Full fake REST API generator [![build badge](https://camo.githubusercontent.com/f857ad152f89a7019df8655afd589443a0df7448787e539eb1a582cae628f07b/68747470733a2f2f6170692e7472617669732d63692e6f72672f7365726179757a6775722f77656c642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/serayuzgur/weld)
*   [wezterm](https://github.com/wez/wezterm) — A GPU-accelerated cross-platform terminal emulator and multiplexer
*   [zellij](https://github.com/zellij-org/zellij) — A terminal multiplexer (workspace) with batteries included

### [](#audio-and-music)Audio and Music

*   [enginesound](https://github.com/DasEtwas/enginesound) — A GUI and command line application used to procedurally generate semi-realistic engine sounds. Featuring in-depth configuration, variable sample rate and a frequency analysis window.
*   [ncspot](https://github.com/hrkfdn/ncspot) - Cross-platform ncurses Spotify client, inspired by ncmpc and the likes. [![build badge](https://github.com/hrkfdn/ncspot/workflows/Build/badge.svg)](https://github.com/hrkfdn/ncspot/actions?query=workflow%3ABuild)
*   [Polaris](https://github.com/agersant/polaris) — A music streaming application. [![build badge](https://camo.githubusercontent.com/2adf114ef5efdbc98d6b50d445be5ada3c29cc8f7a91656fbb58030b85eeb4c5/68747470733a2f2f6170692e7472617669732d63692e6f72672f6167657273616e742f706f6c617269732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/agersant/polaris)
*   [Spotify TUI](https://github.com/Rigellute/spotify-tui) — A Spotify client for the terminal written in Rust. [![Continuous Integration](https://github.com/Rigellute/spotify-tui/workflows/Continuous%20Integration/badge.svg?branch=master)](https://github.com/Rigellute/spotify-tui/workflows/Continuous%20Integration/badge.svg?branch=master)
*   [Spotifyd](https://github.com/Spotifyd/spotifyd) — An open source Spotify client running as a UNIX daemon. [![Continuous Integration](https://github.com/Spotifyd/spotifyd/workflows/Continuous%20Integration/badge.svg?branch=master)](https://github.com/Spotifyd/spotifyd/workflows/Continuous%20Integration/badge.svg?branch=master)

### [](#cryptocurrencies)Cryptocurrencies

*   [Bitcoin Satoshi's Vision](https://github.com/brentongunning/rust-sv) \[[sv](https://crates.io/crates/sv)\] — A Rust library for working with Bitcoin SV .
*   [cardano-cli](https://github.com/input-output-hk/cardano-cli) — Cardano Command Line Interface (CLI)
*   [ChainX](https://github.com/chainx-org/ChainX) — Fully Decentralized Interchain Crypto Asset Management on Polkadot.
*   [CITA](https://github.com/citahub/cita) — A high performance blockchain kernel for enterprise users.
*   [coinbase-pro-rs](https://github.com/inv2004/coinbase-pro-rs) — Coinbase pro client in Rust, supports sync/async/websocket [![build badge](https://camo.githubusercontent.com/065ea5d49f31d37af9d2ca627f8608dff4ee7de055de9e0ec7434850a606a6b9/68747470733a2f2f6170692e7472617669732d63692e6f72672f696e76323030342f636f696e626173652d70726f2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/inv2004/coinbase-pro-rs)
*   [Diem](https://github.com/diem/diem) — Diem’s mission is to enable a simple global currency and financial infrastructure that empowers billions of people.
*   [ethaddrgen](https://github.com/Limeth/ethaddrgen) — Custom Ethereum vanity address generator made in Rust [![build badge](https://camo.githubusercontent.com/cd281751541f06b6dad41f9190a1b51240a22a7812f804ae3c456eafcf6fb320/68747470733a2f2f6170692e7472617669732d63692e6f72672f4c696d6574682f6574686164647267656e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Limeth/ethaddrgen)
*   [Forest](https://github.com/ChainSafe/forest) - Rust Filecoin implementation [![Build Status](https://camo.githubusercontent.com/c0f0e6b9cd4af7a7b5fe0035bfed7689a779764deaa169cd78a9337999d120f7/68747470733a2f2f696d672e736869656c64732e696f2f636972636c6563692f6275696c642f67682f436861696e536166652f666f726573742f6d61696e3f6272616e63683d6d6173746572)](https://app.circleci.com/pipelines/github/ChainSafe/forest?branch=main)
*   [Grin](https://github.com/mimblewimble/grin/) — Evolution of the MimbleWimble protocol
*   [hdwallet](https://github.com/jjyr/hdwallet) \[[hdwallet](https://crates.io/crates/hdwallet)\] — BIP-32 HD wallet related key derivation utilities.
*   [Holochain](https://github.com/holochain/holochain) — Scalable P2P alternative to blockchain for all those distributed apps you always wanted to build. The link to the old repo is [this](https://github.com/holochain/holochain-rust) which is no longer maintained. [![Build Status](https://camo.githubusercontent.com/709d93345c3634163aa1ea0aa22dc1984de10fd63a9bb9a0701b9f2ad28bd3f9/68747470733a2f2f6170692e7472617669732d63692e636f6d2f686f6c6f636861696e2f686f6c6f636861696e2d727573742e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/holochain/holochain-rust)
*   [ibc-rs](https://github.com/informalsystems/ibc-rs) - Rust implementation of the [Interblockchain Communication](https://ibcprotocol.org/) protocol
*   [infincia/bip39-rs](https://github.com/infincia/bip39-rs) \[[bip39](https://crates.io/crates/bip39)\] — Rust implementation of BIP39.
*   [interBTC](https://github.com/interlay/interbtc) — Trustless and fully decentralized Bitcoin bridge to Polkadot and Kusama.
*   [Joystream](https://github.com/Joystream/joystream) — A user governed video platform [![Build Status](https://camo.githubusercontent.com/7ab5f278e1ec9781632dd976f7defbb3ab180fc7cfce71eabb2c6eac2228e49e/68747470733a2f2f6170692e7472617669732d63692e6f72672f4a6f7973747265616d2f6a6f7973747265616d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Joystream/joystream)
*   [Lighthouse](https://github.com/sigp/lighthouse) — Rust Ethereum 2.0 Client [![Build Status](https://github.com/sigp/lighthouse/workflows/test-suite/badge.svg?branch=master)](https://github.com/sigp/lighthouse/actions)
*   [near/nearcore](https://github.com/near/nearcore) — decentralized smart-contract platform for low-end mobile devices.
*   [Nervos CKB](https://github.com/nervosnetwork/ckb) — Nervos CKB is a public permissionless blockchain, the common knowledge layer of Nervos network.
*   [Nimiq](https://github.com/nimiq/core-rs) — Rust implementation of Nimiq node
*   [Parity-Bitcoin](https://github.com/paritytech/parity-bitcoin) — The Parity Bitcoin client [![build badge](https://camo.githubusercontent.com/f356bc1cd0496962327f0508e63254329fc96a24514c791e1b327b6df1bb713d/68747470733a2f2f6170692e7472617669732d63692e6f72672f706172697479746563682f7061726974792d626974636f696e2e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/paritytech/parity-bitcoin)
*   [Parity-Bridge](https://github.com/paritytech/parity-bridge) — Bridge between any two ethereum-based networks
*   [Parity-Ethereum](https://github.com/openethereum/openethereum) — Fast, light, and robust Ethereum client
*   [Parity-Zcash](https://github.com/paritytech/parity-zcash) — Rust implementation of the Zcash protocol
*   [Phala-Network/phala-blockchain](https://github.com/Phala-Network/phala-blockchain) — Confidential smart contract blockchain based on Intel SGX and Substrate
*   [Polkadot](https://github.com/paritytech/polkadot) — Heterogeneous multi‑chain technology with pooled security
*   [rust-bitcoin](https://github.com/rust-bitcoin/rust-bitcoin) — Library with support for de/serialization, parsing and executing on data structures and network messages related to Bitcoin.
*   [rust-cardano](https://github.com/input-output-hk/rust-cardano) — Rust implementation of Cardano primitives, helpers, and related applications
*   [Solana](https://github.com/solana-labs/solana) — Incredibly fast, highly scalable blockchain using Proof-of-History.
*   [Substrate](https://github.com/paritytech/substrate) — Generic modular blockchain template written in Rust
*   [tendermint-rs](https://github.com/informalsystems/tendermint-rs) - Rust implementation of Tendermint blockchain data structures and clients
*   [wagyu](https://github.com/AleoHQ/wagyu) \[[wagyu](https://crates.io/crates/wagyu)\] — Rust library for generating cryptocurrency wallets [![build badge](https://camo.githubusercontent.com/45de61258c92e5953d739be7673969c7dfbb3e8cac3f7c360bb1cb0140f2e241/68747470733a2f2f6170692e7472617669732d63692e636f6d2f416c656f48512f77616779752e7376673f6272616e63683d6d6173746572)](https://api.travis-ci.com/AleoHQ/wagyu.svg?branch=master)
*   [zcash](https://github.com/zcash/zcash) — Zcash is an implementation of the "Zerocash" protocol.

### [](#database)Database

*   [Databend](https://github.com/datafuselabs/databend) - A Modern Real-Time Data Processing & Analytics DBMS with Cloud-Native Architecture [![Release](https://github.com/datafuselabs/databend/actions/workflows/databend-release.yml/badge.svg)](https://github.com/datafuselabs/databend/actions/workflows/databend-release.yml)
*   [indradb](https://crates.io/crates/indradb) — Rust based graph database [![build badge](https://camo.githubusercontent.com/3f8f88ec9065a46279b3f6a776eb8d25a0d1dedad9ab54e8fc279f49cdc94c66/68747470733a2f2f6170692e7472617669732d63692e6f72672f696e64726164622f696e64726164622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/indradb/indradb)
*   [Lucid](https://github.com/lucid-kv/lucid) — High performance and distributed KV store accessible through a HTTP API. [![Build Status](https://github.com/lucid-kv/lucid/workflows/Lucid/badge.svg?branch=master)](https://github.com/lucid-kv/lucid/actions?workflow=Lucid)
*   [Materialize](https://github.com/MaterializeInc/materialize) - Streaming SQL database powered by Timely Dataflow ![heavy_dollar_sign](https://github.githubassets.com/images/icons/emoji/unicode/1f4b2.png) [![Build status](https://camo.githubusercontent.com/0a1221e465f51e15938c3573f391b9ac72bb91b6d6aa71a4c7622cee2af8ea4f/68747470733a2f2f62616467652e6275696c646b6974652e636f6d2f39376436363034653031356266363333643163326131326431363662623436663362343361393237643339353263393939612e7376673f6272616e63683d6d61696e)](https://buildkite.com/materialize/tests)
*   [noria](https://github.com/mit-pdos/noria) \[[noria](https://crates.io/crates/noria)\] — Dynamically changing, partially-stateful data-flow for web application backends [![build badge](https://camo.githubusercontent.com/f20f10fd1d13e56bdc8ca70371fc8f1d89e37ddeeea8a1152f5aa3b9559a42dd/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d69742d70646f732f6e6f7269612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mit-pdos/noria)
*   [ParityDB](https://github.com/paritytech/parity-db) — Fast and reliable database, optimised for read operation
*   [PumpkinDB](https://github.com/PumpkinDB/PumpkinDB) — an event sourcing database engine
*   [seppo0010/rsedis](https://github.com/seppo0010/rsedis) — A Redis reimplementation in Rust [![build badge](https://camo.githubusercontent.com/04dcc4c3584b859396ac7f3b932eafa535008d13f677d63cd7c536f2cd33b6e6/68747470733a2f2f6170692e7472617669732d63692e6f72672f736570706f303031302f7273656469732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/seppo0010/rsedis)
*   [Skytable](https://github.com/skytable/skytable) — A multi-model NoSQL database [![GitHub Workflow Status](https://camo.githubusercontent.com/80e458002e58a234902c0ff2610f5d1ff887dccfac20c545a0bd175545bf43da/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f736b797461626c652f736b797461626c652f54657374733f7374796c653d666c61742d737175617265)](https://camo.githubusercontent.com/80e458002e58a234902c0ff2610f5d1ff887dccfac20c545a0bd175545bf43da/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f736b797461626c652f736b797461626c652f54657374733f7374796c653d666c61742d737175617265)
*   [sled](https://crates.io/crates/sled) — A (beta) modern embedded database [![Build Status](https://github.com/spacejam/sled/workflows/Rust/badge.svg?branch=master)](https://github.com/spacejam/sled/actions?workflow=Rust)
*   [TerminusDB](https://github.com/terminusdb/terminusdb-store) - open source graph database and document store [![Build Status](https://github.com/terminusdb/terminusdb-store/workflows/Build/badge.svg?branch=master)](https://github.com/terminusdb/terminusdb-store/actions)
*   [tikv](https://github.com/tikv/tikv) — A distributed KV database in Rust [![Build Status](https://camo.githubusercontent.com/5fe31d7413bb334f55bd4eba445673bb26f65c01791bf454d9aa42a4cbc801a8/68747470733a2f2f63692e70696e676361702e6e65742f6a6f622f74696b765f676870725f746573742f62616467652f69636f6e)](https://ci.pingcap.net/job/tikv_ghpr_test/)
*   [vorot93/libmdbx-rs](https://github.com/vorot93/libmdbx-rs) \[[mdbx-sys](https://crates.io/crates/mdbx-sys)\] — Rust bindings for MDBX, a "fast, compact, powerful, embedded, transactional key-value database, with permissive license". This is a fork of mozilla/lmdb-rs with patches to make it work with libmdbx.
*   [WooriDB](https://github.com/naomijub/wooridb) - General purpose time serial database inspired by Crux and Datomic.

### [](#emulators)Emulators

See also [crates matching keyword 'emulator'](https://crates.io/keywords/emulator).

*   Commodore 64
    *   [kondrak/rust64](https://github.com/kondrak/rust64) — [![build badge](https://camo.githubusercontent.com/7665171300f56835b0e34c330b2f370fe425d729c8cf2f94afbdf2c1fb2d4c18/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b6f6e6472616b2f7275737436342e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kondrak/rust64)
*   Flash Player
    *   [Ruffle](https://github.com/ruffle-rs/ruffle) — Ruffle is an Adobe Flash Player emulator written in the Rust programming language. Ruffle targets both the desktop and the web using WebAssembly. [![build badge](https://camo.githubusercontent.com/11f9b2705ede6309dae641f1929a40278eba799affdc0c5aa55203720e618d3e/68747470733a2f2f696d672e736869656c64732e696f2f636972636c6563692f6275696c642f6769746875622f727566666c652d72732f727566666c65)](https://app.circleci.com/pipelines/github/ruffle-rs/ruffle)
*   Gameboy
    *   [Gekkio/mooneye-gb](https://github.com/Gekkio/mooneye-gb) — [![build badge](https://camo.githubusercontent.com/86a6bbcc830481d04a32a42192cfa867a70c63ed92787a8b46ba34a42b4b0bf6/68747470733a2f2f6170692e7472617669732d63692e6f72672f47656b6b696f2f6d6f6f6e6579652d67622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Gekkio/mooneye-gb)
    *   [mohanson/gameboy](https://github.com/mohanson/gameboy) — Full featured Cross-platform GameBoy emulator. Forever boys!.
    *   [mvdnes/rboy](https://github.com/mvdnes/rboy) — [![build badge](https://camo.githubusercontent.com/1cd9eecaf83c31ddf8370892a0b62181c032b907426108df08af7e289b745fbd/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d76646e65732f72626f792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mvdnes/rboy)
*   Gameboy Advance
    *   [michelhe/rustboyadvance-ng](https://github.com/michelhe/rustboyadvance-ng) - RustboyAdvance-ng is a Gameboy Advance emulator with desktop, android and [WebAssembly](https://michelhe.github.io/rustboyadvance-ng/) support. [![build badge](https://github.com/michelhe/rustboyadvance-ng/workflows/Deploy/badge.svg?branch=master)](https://github.com/michelhe/rustboyadvance-ng/actions?query=workflow%3ADeploy)
*   Intel 8080 CPU
    *   [mohanson/i8080](https://github.com/mohanson/i8080) — Intel 8080 cpu emulator by Rust
*   NES
    *   [koute/pinky](https://github.com/koute/pinky) — [![build badge](https://camo.githubusercontent.com/268aa32f96fec361961a78839f062038099dae4d547968f95091cda87baa15ad/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b6f7574652f70696e6b792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/koute/pinky)
    *   [pcwalton/sprocketnes](https://github.com/pcwalton/sprocketnes)
*   Virtual Boy
    *   [emu-rs/rustual-boy](https://github.com/emu-rs/rustual-boy) — [![build badge](https://camo.githubusercontent.com/9755f2ff6d4cf9c24ba26cd61e6c17921a81e24221f471d1d207addbef9dd3e6/68747470733a2f2f6170692e7472617669732d63692e6f72672f656d752d72732f7275737475616c2d626f792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/emu-rs/rustual-boy)
*   ZX Spectrum
    *   [pacmancoder/rustzx](https://github.com/pacmancoder/rustzx) — [![build badge](https://camo.githubusercontent.com/f7cca77fd2dd456e95ef8aea8a6761c9b890b2ec7ff00b0d3cdb928122de2bc0/68747470733a2f2f6170692e7472617669732d63692e6f72672f7061636d616e636f6465722f727573747a782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/pacmancoder/rustzx)

### [](#games)Games

See also [Games Made With Piston](https://github.com/PistonDevelopers/piston/wiki/Games-Made-With-Piston).

*   [citybound](https://github.com/citybound/citybound) — The city sim you deserve
*   [cristicbz/rust-doom](https://github.com/cristicbz/rust-doom) — A renderer for Doom, may progress to being a playable game [![build badge](https://camo.githubusercontent.com/a7918d3f4486eb422828299f27b33d3f8d4ad9fed7cba608e2aae88eacfc021f/68747470733a2f2f6170692e7472617669732d63692e6f72672f63726973746963627a2f727573742d646f6f6d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cristicbz/rust-doom)
*   [doukutsu-rs](https://github.com/doukutsu-rs/doukutsu-rs) — A Rust reimplementation of Cave Story engine with some enhancements.
*   [garkimasera/rusted-ruins](https://github.com/garkimasera/rusted-ruins) — Extensible open world rogue like game with pixel art [![build badge](https://camo.githubusercontent.com/313f768ea0635e855302899ba0ba3690efc3666bf06c2095a625f35d4b340426/68747470733a2f2f6170692e7472617669732d63692e6f72672f6761726b696d61736572612f7275737465642d7275696e732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/garkimasera/rusted-ruins)
*   [lifthrasiir/angolmois-rust](https://github.com/lifthrasiir/angolmois-rust) — A minimalistic music video game which supports the BMS format [![build badge](https://camo.githubusercontent.com/d0c9ec57880b3761f83711db598eecbc6111409794168bfae4a9dbf12ca168df/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c696674687261736969722f616e676f6c6d6f69732d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lifthrasiir/angolmois-rust)
*   [ozkriff/zemeroth](https://github.com/ozkriff/zemeroth) — A small 2D turn-based hexagonal strategy game [![build badge](https://camo.githubusercontent.com/16335129fd0d89f15aae476b0da08b2a8293eed2c41a53b212eb3a4057c39f51/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f7a6b726966662f7a656d65726f74682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ozkriff/zemeroth)
*   [rhex](https://github.com/dpc/rhex) — hexagonal ascii roguelike
*   [rsaarelm/magog](https://github.com/rsaarelm/magog) — A roguelike game in Rust
*   [schulke-214/rsnake](https://github.com/schulke-214/rsnake) — Snake written in Rust.
*   [SoftbearStudios/mk48](https://github.com/SoftbearStudios/mk48) — Mk48.io is an online multiplayer naval combat game
*   [swatteau/sokoban-rs](https://github.com/swatteau/sokoban-rs) — A Sokoban implementation
*   [thetawavegame/thetawave-legacy](https://github.com/thetawavegame/thetawave-legacy) - A space shooter game that strives to be an entry point for new game developers to make their first contributions. [![build badge](https://github.com/thetawavegame/thetawave-legacy/actions/workflows/ci.yml/badge.svg?branch=master)](https://github.com/thetawavegame/thetawave-legacy/actions/workflows/ci.yml/badge.svg?branch=master)
*   [Thinkofname/rust-quake](https://github.com/Thinkofname/rust-quake) — Quake map renderer in Rust
*   [Veloren](https://gitlab.com/veloren/veloren) — An open world, open source multiplayer voxel RPG game currently in alpha development [![build badge](https://camo.githubusercontent.com/12770cf46bb3ce8a8a7c62ae7af46f7fda3c49e4dda7a26b55282afd0e96b840/68747470733a2f2f6769746c61622e636f6d2f76656c6f72656e2f76656c6f72656e2f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/veloren/veloren/-/pipelines)
*   [Zone of Control](https://github.com/ozkriff/zoc) — A turn-based hexagonal strategy game [![build badge](https://camo.githubusercontent.com/23e91ba0f7a39e8d98b374891d79e8013ae1cc3e85863c28ff84a128b879b2a3/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f7a6b726966662f7a6f632e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ozkriff/zoc)

### [](#graphics)Graphics

*   [ivanceras/svgbob](https://github.com/ivanceras/svgbob) — converts ASCII diagrams into SVG graphics [![build badge](https://camo.githubusercontent.com/9bbb66fff91fa9c8385490b3af55aae24e0cd9f9fdd1c0515d51feb3148abee3/68747470733a2f2f6170692e7472617669732d63692e6f72672f6976616e63657261732f737667626f622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ivanceras/svgbob)
*   [Limeth/euclider](https://github.com/Limeth/euclider) — A real-time 4D CPU ray tracer [![build badge](https://camo.githubusercontent.com/d3f786fe338095c16738e83b5e8b02b506f964843cba8003491ab08d05740d2b/68747470733a2f2f6170692e7472617669732d63692e6f72672f4c696d6574682f6575636c696465722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Limeth/euclider)
*   [RazrFalcon/resvg](https://github.com/RazrFalcon/resvg) — An SVG rendering library. [![build badge](https://camo.githubusercontent.com/08af0d4ba143260454bdb0d478a96b8c2872555f5dcef55aac0de6109f2c288a/68747470733a2f2f6170692e7472617669732d63692e6f72672f52617a7246616c636f6e2f72657376672e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/RazrFalcon/resvg)
*   [RazrFalcon/svgcleaner](https://github.com/RazrFalcon/svgcleaner) — tidies SVG graphics
*   [turnage/valora](https://crates.io/crates/valora) — A library for generative fine art [![Rust](https://github.com/turnage/valora/workflows/Rust/badge.svg?branch=master)](https://github.com/turnage/valora/workflows/Rust/badge.svg?branch=master)
*   [Twinklebear/tray\_rust](https://github.com/Twinklebear/tray_rust) — A ray tracer [![build badge](https://camo.githubusercontent.com/616ee54b482ae081a62facd74bc264261f1e7623ed4ee6e2a6e5dbe480be1e6d/68747470733a2f2f6170692e7472617669732d63692e6f72672f5477696e6b6c65626561722f747261795f727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Twinklebear/tray_rust)

### [](#image-processing)Image processing

*   [Imager](https://github.com/imager-io/imager) — Automated image optimization.

### [](#industrial-automation)Industrial automation

*   [locka99/opcua](https://github.com/locka99/opcua) — A pure rust [OPC UA](https://opcfoundation.org/about/opc-technologies/opc-ua/) library.
*   [slowtec/tokio-modbus](https://github.com/slowtec/tokio-modbus) — A [tokio](https://tokio.rs)\-based [modbus](https://modbus.org) library. [![Build Status](https://camo.githubusercontent.com/a8d7e718252d31e2d7b42315a9a3ca00330c74daa60a1bcd72368d28fe880d45/68747470733a2f2f6170692e7472617669732d63692e6f72672f736c6f777465632f746f6b696f2d6d6f646275732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/slowtec/tokio-modbus)

### [](#observability)Observability

*   [avito-tech/bioyino](https://github.com/avito-tech/bioyino) — A high-performance scalable StatsD compatible server.
*   [OpenTelemetry](https://crates.io/crates/opentelemetry) — OpenTelemetry provides a single set of APIs, libraries, agents, and collector services to capture distributed traces and metrics from your application. You can analyze them using Prometheus, Jaeger, and other observability tools. [![GitHub Actions CI](https://github.com/open-telemetry/opentelemetry-rust/workflows/CI/badge.svg?branch=master)](https://github.com/open-telemetry/opentelemetry-rust/actions?query=workflow%3ACI+branch%3Amaster)
*   [Scaphandre](https://github.com/hubblo-org/scaphandre) - A power consumption monitoring agent, to track host and each service power consumption and enable designing systems and applications for more sustainability. Designed to fit any monitoring toolchain (already supports prometheus, warp10, riemann...).
*   [vectordotdev/vector](https://github.com/vectordotdev/vector) — A High-Performance, Logs, Metrics, & Events Router.

### [](#operating-systems)Operating systems

See also [A comparison of operating systems written in Rust](https://github.com/flosse/rust-os-comparison).

*   [0x59616e/SteinsOS](https://github.com/0x59616e/SteinsOS) — An OS for armv8-a architecture.
*   [nebulet/nebulet](https://github.com/nebulet/nebulet) — A microkernel that implements a WebAssembly "usermode" that runs in Ring 0.
*   [redox-os/redox](https://gitlab.redox-os.org/redox-os/redox) — [![build badge](https://camo.githubusercontent.com/64bf679aed0255aac50a5993491c5609aafb775601eaef1195b83a0f4d1e534d/68747470733a2f2f6170692e7472617669732d63692e6f72672f7265646f782d6f732f7265646f782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/redox-os/redox)
*   [thepowersgang/rust\_os](https://github.com/thepowersgang/rust_os) — [![build badge](https://camo.githubusercontent.com/ba7405f5afe86d4c3674aa3d551d2afa6d2091ec0ac9caa273a642b2d75c9371/68747470733a2f2f6170692e7472617669732d63692e6f72672f746865706f7765727367616e672f727573745f6f732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/thepowersgang/rust_os)
*   [tock/tock](https://github.com/tock/tock) — A secure embedded operating system for Cortex-M based microcontrollers

### [](#productivity)Productivity

*   [espanso](https://github.com/federico-terzi/espanso) — A cross-platform Text Expander written in Rust [![Build Status](https://camo.githubusercontent.com/bf869bf55541958d0e23e314332a5a0a5c328fb3aa2343c13fc7e13998dd56eb/68747470733a2f2f6465762e617a7572652e636f6d2f667265646479363839362f657370616e736f2f5f617069732f6275696c642f7374617475732f666564657269636f2d7465727a692e657370616e736f3f6272616e63684e616d653d6d6173746572)](https://dev.azure.com/freddy6896/espanso/_build)
*   [eureka](https://crates.io/crates/eureka) — A CLI tool to input and store your ideas without leaving the terminal
*   [pier-cli/pier](https://github.com/pier-cli/pier) — A central repository to manage (add, search metadata, etc.) all your one-liners, scripts, tools, and CLIs

### [](#security-tools)Security tools

*   [arvancloud/libinjection-rs](https://github.com/arvancloud/libinjection-rs) — Rust bindings for [libinjection](https://github.com/client9/libinjection) [![build badge](https://camo.githubusercontent.com/f6b2657157e7fadaeabb472a5e7dec3b05c0491c8fbaa4ed02301cb5d6edecbc/68747470733a2f2f6170692e7472617669732d63692e6f72672f617276616e636c6f75642f6c6962696e6a656374696f6e2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/arvancloud/libinjection-rs)
*   [b23r0/Cliws](https://github.com/b23r0/Cliws) — A bind/reverse PTY shell with Windows&Linux support. [![Build Status](https://camo.githubusercontent.com/4c7e3776736928b2dacc86f0c2fe77fa95cd69d83346000f2bcb0fc11426215f/68747470733a2f2f6170692e7472617669732d63692e636f6d2f62323372302f636c6977732e7376673f6272616e63683d6d61696e)](https://app.travis-ci.com/b23r0/cliws)
*   [epi052/feroxbuster](https://github.com/epi052/feroxbuster) - A simple, fast, recursive content discovery tool written in Rust (
*   [kpcyrd/authoscope](https://github.com/kpcyrd/authoscope) — A scriptable network authentication cracker [![build badge](https://camo.githubusercontent.com/610cfc98c0f7fb7c197ba5f15ec5854c1613f2d29173a3954cf186651a55ef9c/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b70637972642f617574686f73636f70652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kpcyrd/authoscope)
*   [kpcyrd/rshijack](https://github.com/kpcyrd/rshijack) — A TCP connection hijacker, rust rewrite of shijack [![build badge](https://camo.githubusercontent.com/67f2b181c592233d69a7c65a12404f7983c9d1bf24c3e74e835baf1c21a490d9/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b70637972642f727368696a61636b2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kpcyrd/rshijack)
*   [kpcyrd/sn0int](https://github.com/kpcyrd/sn0int) — A semi-automatic OSINT framework and package manager [![build badge](https://camo.githubusercontent.com/15493cf7b391e5f91ffb256abea3cfb9ee70d9d289455ac22b449024b4d51076/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b70637972642f736e30696e742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kpcyrd/sn0int)
*   [kpcyrd/sniffglue](https://github.com/kpcyrd/sniffglue) — A secure multithreaded packet sniffer [![build badge](https://camo.githubusercontent.com/de6d4866434f126f569d6de89ed453f60f6625399f11b2254f82224fc4f61b3d/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b70637972642f736e696666676c75652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kpcyrd/sniffglue)
*   [ObserverWard\_0x727](https://github.com/0x727/ObserverWard_0x727) — Community based web technologies analysis tool.
*   [phra/rustbuster](https://github.com/phra/rustbuster) — A Comprehensive Web Fuzzer and Content Discovery Tool
*   [ripasso](https://github.com/cortex/ripasso/) — A password manager, filesystem compatible with pass
*   [rustscan/rustscan](https://github.com/RustScan/RustScan) — Make Nmap faster with this port scanning tool [![build badge](https://github.com/RustScan/RustScan/workflows/Continuous%20integration/badge.svg?branch=master)](https://github.com/RustScan/RustScan/actions?query=workflow%3A%22Continuous+integration%22)

### [](#system-tools)System tools

*   [ajeetdsouza/zoxide](https://github.com/ajeetdsouza/zoxide/) — A fast alternative to `cd` that learns your habits [![release](https://github.com/ajeetdsouza/zoxide/workflows/.github/workflows/release.yml/badge.svg)](https://github.com/ajeetdsouza/zoxide/actions)
*   [Alonely0/Voila](https://github.com/Alonely0/Voila) — Voila is a domain-specific language launched through CLI tool for operating with files and directories in massive amounts in a fast & reliable way. [![Linux build](https://github.com/Alonely0/Voila/actions/workflows/linux-ci.yml/badge.svg)](https://github.com/Alonely0/Voila/actions/workflows/linux-ci.yml) [![macOS build](https://github.com/Alonely0/Voila/actions/workflows/mac-ci.yml/badge.svg)](https://github.com/Alonely0/Voila/actions/workflows/mac-ci.yml) [![Windows build](https://github.com/Alonely0/Voila/actions/workflows/windows-ci.yml/badge.svg)](https://github.com/Alonely0/Voila/actions/workflows/windows-ci.yml)
*   [b23r0/yaftp](https://github.com/b23r0/yaftp) — A lightweight file transfer CLI tool support with resume broken transfer & reverse mode & largefile. [![Build Status](https://camo.githubusercontent.com/72e176bbab8cfb7f7a8b65442477da3b3efc36e8caa776c346d4d0c689ba1c83/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f62323372302f79616674702f52757374)](https://github.com/b23r0/yaftp/actions/workflows/rust.yml)
*   [bandwhich](https://github.com/imsnif/bandwhich) — Terminal bandwidth utilization tool [![build badge](https://camo.githubusercontent.com/d72ca6f7b6e630ca2d713311288da90649e4de9fd27177ff3ed8fa86f0b955d4/68747470733a2f2f6170692e7472617669732d63692e636f6d2f696d736e69662f62616e6477686963682e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/imsnif/bandwhich)
*   [bottom](https://github.com/ClementTsang/bottom) - Yet another cross-platform graphical process/system monitor. [![GitHub Workflow Status (branch)](https://camo.githubusercontent.com/f3df7f69e3f93b805b6a755608f1769c9c0841d7cdb297673cdd1258392721af/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f436c656d656e745473616e672f626f74746f6d2f63692f6d6173746572)](https://github.com/ClementTsang/bottom/actions?query=branch%3Amaster)
*   [brocode/fblog](https://github.com/brocode/fblog) — Small command-line JSON Log viewer [![build badge](https://camo.githubusercontent.com/622822d8b0b61f572a107b319863267519ed710561f8e587bc1750f04bd1c80a/68747470733a2f2f6170692e7472617669732d63692e6f72672f62726f636f64652f66626c6f672e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/brocode/fblog)
*   [bustd](https://github.com/vrmiguel/bustd) - Lightweight process killer daemon to handle out-of-memory scenarios on Linux. [![GitHub Workflow Status (branch)](https://camo.githubusercontent.com/1d9ee5fdbcb2915f6cbfa5481d25c59ddef82b87ab1a983246cf6915e7e4098d/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f76726d696775656c2f62757374642f6275696c642d616e642d74657374)](https://github.com/vrmiguel/bustd/actions?query=branch%3Amaster)
*   [buster/rrun](https://github.com/buster/rrun) — A command launcher for Linux, similar to gmrun [![build badge](https://camo.githubusercontent.com/5f81b208bb36cc10ee01d4fa9043c02211dd43766cbbf522076f3220561d40f5/68747470733a2f2f6170692e7472617669732d63692e6f72672f6275737465722f7272756e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/buster/rrun)
*   [cantino/mcfly](https://github.com/cantino/mcfly) - Fly through your shell history. Great Scott! [![build badge](https://camo.githubusercontent.com/aa7f9da7200dd8d3d6782bde9ce8e216f76c5f310d93b1a22bfaa3133dfe20c3/68747470733a2f2f6170692e7472617669732d63692e6f72672f63616e74696e6f2f6d63666c792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cantino/mcfly)
*   [crabz](https://github.com/sstadick/crabz) - Multi-threaded compression and decompression CLI tool [![Build Status](https://github.com/sstadick/crabz/workflows/Check/badge.svg)](https://github.com/sstadick/crabz/actions?query=workflow%3ACheck)
*   [cristianoliveira/funzzy](https://github.com/cristianoliveira/funzzy) — A configurable filesystem watcher inspired by [entr](http://eradman.com/entrproject/) [![build badge](https://camo.githubusercontent.com/eb4124e6367addd363ce42dac4c4c3019fc61def132e48357fb59557e3639d83/68747470733a2f2f6170692e7472617669732d63692e6f72672f637269737469616e6f6c6976656972612f66756e7a7a792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cristianoliveira/funzzy)
*   [dalance/procs](https://github.com/dalance/procs) — A modern replacement for 'ps' written by Rust [![Regression](https://github.com/dalance/procs/actions/workflows/regression.yml/badge.svg)](https://github.com/dalance/procs/actions/workflows/regression.yml)
*   [ddh](https://github.com/darakian/ddh) — Fast duplicate file finder [![build badge](https://camo.githubusercontent.com/c70869b4d155a8e93c9742031907403928e9f8be3962f7ee8bf4c1c3d9339184/68747470733a2f2f6170692e7472617669732d63692e6f72672f646172616b69616e2f6464682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/darakian/ddh)
*   [diskonaut](https://github.com/imsnif/diskonaut) — Terminal visual disk space navigator [![build badge](https://camo.githubusercontent.com/f77c40b4cf60a971dc616625f4418e064b530e8e0b6888affe438ba2ffc20812/68747470733a2f2f6170692e7472617669732d63692e636f6d2f696d736e69662f6469736b6f6e6175742e7376673f6272616e63683d6d61696e)](https://app.travis-ci.com/github/imsnif/diskonaut)
*   [dust](https://github.com/bootandy/dust) — A more intuitive version of du
*   [fselect](https://crates.io/crates/fselect) — Find files with SQL-like queries [![build badge](https://camo.githubusercontent.com/26220af0d2d583a6871ac99b5a178bdcdb36b8e9995ff54ba4bb512db60ffe18/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a6873706574657273736f6e2f6673656c6563742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jhspetersson/fselect)
*   [gitui](https://github.com/extrawurst/gitui) - Blazing fast terminal client for git written in Rust. [![build](https://github.com/extrawurst/gitui/workflows/CI/badge.svg?branch=master)](https://github.com/extrawurst/gitui/actions)
*   [k0pernicus/zou](https://github.com/k0pernicus/zou) — A download accelerator
*   [Kondo](https://github.com/tbillington/kondo) - CLI & GUI tool for deleting software project artifacts and reclaiming disk space
*   [lotabout/rargs](https://github.com/lotabout/rargs) \[[rargs](https://crates.io/crates/rargs)\] — xargs + awk with pattern matching support [![build badge](https://camo.githubusercontent.com/4857f04943d68728ddad79dff2b4e70c33d519c8989b6685820f0c5efe418ad1/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c6f7461626f75742f72617267732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lotabout/rargs)
*   [lotabout/skim](https://github.com/lotabout/skim) — A fuzzy finder in pure rust [![build badge](https://camo.githubusercontent.com/45c60c04834bfd55304a5a521738552770fa8b8926472e6c445bf9b3b27859d0/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c6f7461626f75742f736b696d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lotabout/skim)
*   [Luminarys/synapse](https://github.com/Luminarys/synapse) — Flexible and fast BitTorrent daemon. [![Build Status](https://camo.githubusercontent.com/1e131780521e9645c3ed141f88ce76557a17465fc4615bf085751d1dca397a4c/68747470733a2f2f6170692e7472617669732d63692e6f72672f4c756d696e617279732f73796e617073652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Luminarys/synapse)
*   [m4b/bingrep](https://github.com/m4b/bingrep) — Greps through binaries from various OSs and architectures, and colors them. [![build badge](https://camo.githubusercontent.com/507cdbd6cd1b53fe74099c82680ef4a21536baf0702b9786d506774f9a44e49d/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d34622f62696e677265702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/m4b/bingrep)
*   [mitnk/cicada](https://github.com/mitnk/cicada) — A bash-like Unix shell [![build badge](https://camo.githubusercontent.com/8e9a7d42a7454c40205fe3d753336efcf341bada24781601b49b851bd3a3f832/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d69746e6b2f6369636164612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mitnk/cicada)
*   [mmstick/concurr](https://github.com/mmstick/concurr) — Alternative to GNU Parallel w/ a client-server architecture
*   [mmstick/fontfinder](https://github.com/mmstick/fontfinder) — GTK3 application for previewing and installing Google's fonts
*   [mmstick/parallel](https://github.com/mmstick/parallel) — Reimplementation of GNU Parallel
*   [mmstick/tv-renamer](https://github.com/mmstick/tv-renamer) — A tv series renaming application with an optional GTK3 frontend. [![build badge](https://camo.githubusercontent.com/b72485987893104e2cd7638d6baccff4133855cd15928a925415cf70c880bc26/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6d737469636b2f74762d72656e616d65722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mmstick/tv-renamer)
*   [mxseev/logram](https://github.com/mxseev/logram) — Push log files' updates to Telegram
*   [nickgerace/gfold](https://github.com/nickgerace/gfold) \[[gfold](https://crates.io/crates/gfold)\] - CLI tool to help keep track of multiple Git repositories [![build](https://camo.githubusercontent.com/e1da6ada40a8eb1f99cafde114d211871d143959842024756332e52bfadf624b/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f6e69636b6765726163652f67666f6c642f6d657267652f6d61696e)](https://github.com/nickgerace/gfold/actions?query=workflow%3Amerge+branch%3Amain)
*   [nivekuil/rip](https://github.com/nivekuil/rip) - A safe and ergonomic alternative to `rm` [![build badge](https://camo.githubusercontent.com/44e8517a2eafd76e4eb99139553c0b4df06a34fdc7e2b4898f8cb9de37136bc1/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e6976656b75696c2f7269702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/nivekuil/rip)
*   [ogham/exa](https://github.com/ogham/exa) — A replacement for 'ls' [![build badge](https://camo.githubusercontent.com/1b2d6edfc88933edc2ca2c1a814d480c70b45e1fb6667d9a024de398a8db179b/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f6768616d2f6578612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ogham/exa)
*   [orhun/kmon](https://github.com/orhun/kmon) — Linux Kernel Manager and Activity Monitor [![https://github.com/orhun/kmon/actions](https://camo.githubusercontent.com/a03cff318adf9065a7aae360845d181aad931d500988e90da3cda00aeab935a3/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f6f7268756e2f6b6d6f6e2f436f6e74696e756f7573253230496e746567726174696f6e2f6d61737465723f6c6162656c3d6275696c64)](https://camo.githubusercontent.com/a03cff318adf9065a7aae360845d181aad931d500988e90da3cda00aeab935a3/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f6f7268756e2f6b6d6f6e2f436f6e74696e756f7573253230496e746567726174696f6e2f6d61737465723f6c6162656c3d6275696c64)
*   [ouch](https://github.com/ouch-org/ouch) - Painless compression and decompression on the command-line [![GitHub Workflow Status (branch)](https://camo.githubusercontent.com/37bb44f326c315121f19c22048b6294c2f76b71364825f1289dab3106fdd256a/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f6f7563682d6f72672f6f7563682f6275696c642d616e642d74657374)](https://github.com/ouch-org/ouch/actions?query=branch%3Amaster)
*   [Peltoche/lsd](https://github.com/Peltoche/lsd) — An ls with a lot of pretty colors and awesome icons [![build](https://github.com/Peltoche/lsd/workflows/CICD/badge.svg?branch=master)](https://github.com/Peltoche/lsd/actions)
*   [pop-os/popsicle](https://github.com/pop-os/popsicle) — GTK3 & CLI utility for flashing multiple USB devices in parallel
*   [pop-os/system76-power](https://github.com/pop-os/system76-power/) — Linux power management daemon (DBus-interface) with CLI tool.
*   [pueue](https://github.com/nukesor/pueue) — Manage your long running shell commands. [![GitHub Actions Workflow](https://github.com/nukesor/pueue/workflows/Test%20build/badge.svg?branch=master)](https://github.com/Nukesor/pueue/actions)
*   [redox-os/ion](https://github.com/redox-os/ion) — Next-generation system shell [![build badge](https://camo.githubusercontent.com/df808034723b1aeb8cf8ae274036ddbc42b62a842ad5c8eab7580110a7cc8ba9/68747470733a2f2f6170692e7472617669732d63692e6f72672f7265646f782d6f732f696f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/redox-os/ion)
*   [sharkdp/bat](https://github.com/sharkdp/bat) — A cat(1) clone with wings. [![CICD](https://github.com/sharkdp/bat/actions/workflows/CICD.yml/badge.svg?branch=master)](https://github.com/sharkdp/bat/actions/workflows/CICD.yml)
*   [sharkdp/fd](https://github.com/sharkdp/fd) — A simple, fast and user-friendly alternative to find. [![CICD](https://github.com/sharkdp/fd/actions/workflows/CICD.yml/badge.svg)](https://github.com/sharkdp/fd/actions/workflows/CICD.yml)
*   [sitkevij/hex](https://github.com/sitkevij/hex) — A colorized hexdump terminal utility. [![build badge](https://camo.githubusercontent.com/8f4f5f45b5cfe97f0296473d58f7ac7d40db6e49f4873fcfaf162177ad21fafd/68747470733a2f2f6170692e7472617669732d63692e6f72672f7369746b6576696a2f6865782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sitkevij/hex)
*   [uutils/coreutils](https://github.com/uutils/coreutils) — A cross-platform Rust rewrite of the GNU coreutils \[[![CICD](https://github.com/uutils/coreutils/actions/workflows/CICD.yml/badge.svg)](https://github.com/uutils/coreutils/actions/workflows/CICD.yml)
*   [watchexec](https://github.com/watchexec/watchexec) — Executes commands in response to file modifications [![build badge](https://camo.githubusercontent.com/781dba96e3118be27a8b68c060586d4d6f9d3eaa6f6d5eaea4a16377c2ce8346/68747470733a2f2f6170692e7472617669732d63692e6f72672f7761746368657865632f7761746368657865632e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/watchexec/watchexec)
*   [XAMPPRocky/tokei](https://github.com/XAMPPRocky/tokei) — counts the lines of code [![build badge](https://camo.githubusercontent.com/44cd9d427ee5690cd7f77173c7c1e892d8acc3da07c37929a60eab58fe390385/68747470733a2f2f6170692e7472617669732d63692e6f72672f58414d5050526f636b792f746f6b65692e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/XAMPPRocky/tokei)

### [](#task-scheduling)Task scheduling

*   [delicate](https://github.com/BinChengZhao/delicate) — A lightweight and distributed task scheduling platform written in rust. [![Build Status](https://github.com/BinChengZhao/delicate/workflows/CI/badge.svg)](https://github.com/BinChengZhao/delicate/actions)

### [](#text-editors)Text editors

*   [amp](https://amp.rs) — Inspired by Vi/Vim. [![build badge](https://camo.githubusercontent.com/7e358668d86808675c8b97c8419f6cc84beb6a0c6c573f5f84d200bf9f7455f3/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a6d6163646f6e616c642f616d702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jmacdonald/amp)
*   [gchp/iota](https://github.com/gchp/iota) — A simple text editor [![build badge](https://camo.githubusercontent.com/41a30f7f8242dd6accd5e23f7f3af2ec849bb55db8a6b9437fde80ff6c8105e1/68747470733a2f2f6170692e7472617669732d63692e6f72672f676368702f696f74612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/gchp/iota)
*   [helix](https://github.com/helix-editor/helix) — A post-modern modal text editor inspired by Neovim/Kakoune. [![build badge](https://github.com/helix-editor/helix/actions/workflows/build.yml/badge.svg)](https://github.com/helix-editor/helix/actions)
*   [ilai-deutel/kibi](https://github.com/ilai-deutel/kibi) — A tiny (≤1024 LOC) text editor with syntax highlighting, incremental search and more. [![build badge](https://github.com/ilai-deutel/kibi/workflows/CI/badge.svg?branch=master)](https://github.com/ilai-deutel/kibi/actions?query=branch%3Amaster)
*   [mathall/rim](https://github.com/mathall/rim) — Vim-like text editor written in Rust
*   [ox](https://github.com/curlpipe/ox) — An independent Rust text editor that runs in your terminal!
*   [Remacs](https://github.com/remacs/remacs) — A community-driven port of Emacs to Rust. [![build badge](https://camo.githubusercontent.com/9b5d8e7d743d7c5d74c05499fd59b0fbffebef67b67d8e92c535ff38d638f973/68747470733a2f2f6170692e7472617669732d63692e6f72672f72656d6163732f72656d6163732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/remacs/remacs)
*   [vamolessa/pepper](https://github.com/vamolessa/pepper) \[[pepper](https://crates.io/crates/pepper)\] — An opinionated modal editor to simplify code editing from the terminal [![build badge](https://github.com/vamolessa/pepper/workflows/rust/badge.svg?branch=master)](https://github.com/vamolessa/pepper)
*   [xi-editor](https://github.com/xi-editor/xi-editor) — A modern editor with a backend written in Rust.
*   [xray](https://github.com/atom-archive/xray) — An experimental next-generation Electron-based text editor. [![build badge](https://camo.githubusercontent.com/52478278c63130a96390c16b38fab109c8ff18afc9c3c19b72a67ea94e676350/68747470733a2f2f6170692e7472617669732d63692e6f72672f61746f6d2f787261792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/atom/xray)

### [](#text-processing)Text processing

*   [dmerejkowsky/ruplacer](https://github.com/dmerejkowsky/ruplacer) — Find and replace text in source files [![Run tests](https://github.com/dmerejkowsky/ruplacer/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/dmerejkowsky/ruplacer/actions/workflows/test.yml)
*   [grex](https://github.com/pemistahl/grex) — A command-line tool and library for generating regular expressions from user-provided test cases [![build badge](https://camo.githubusercontent.com/982a589b3618bf1a307a1d4bc44b8fb6ffc573c114b6baeba5260cd230df3b33/68747470733a2f2f6170692e7472617669732d63692e6f72672f70656d69737461686c2f677265782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/pemistahl/grex)
*   [Lisprez/so\_stupid\_search](https://github.com/Lisprez/so_stupid_search) — A simple and fast string search tool for human beings
*   [phiresky/ripgrep-all](https://github.com/phiresky/ripgrep-all) — ripgrep, but also search in PDFs, E-Books, Office documents, zip, tar.gz, etc. [![Build Status](https://camo.githubusercontent.com/5ae4b4fcdf531663d61b8c99eed7cd3de16342b2d808f2412eabf66b5b86aa00/68747470733a2f2f6170692e7472617669732d63692e6f72672f7068697265736b792f726970677265702d616c6c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/phiresky/ripgrep-all)
*   [replicadse/complate](https://github.com/replicadse/complate) — An in-terminal text templating tool designed for standardizing messages (like for GIT commits). [![crates.io](https://camo.githubusercontent.com/1abb9d9e3b84d52d68c6c1f3adaebc6843d09cfede1c35a9405ee5a1c0c826c7/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f636f6d706c6174652e737667)](https://crates.io/crates/complate) [![crates.io](https://camo.githubusercontent.com/a9a1c79a604ebd999bf3733a397077617a2fbd173cc39497acbb69eb3df3ebd9/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f636f6d706c6174653f6c6162656c3d6372617465732e696f253230646f776e6c6f616473)](https://crates.io/crates/complate) [![build badge](https://github.com/replicadse/complate/workflows/pipeline/badge.svg?branch=master)](https://github.com/replicadse/complate/actions)
*   [ripgrep](https://crates.io/crates/ripgrep) — combines the usability of The Silver Searcher with the raw speed of grep [![build badge](https://camo.githubusercontent.com/bcb3fb2c0de368fc581481cbcc9fe33581ecc16f60781dcbdc7ad3643fd5c12a/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f726970677265702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/ripgrep)
*   [sd](https://crates.io/crates/sd) — Intuitive find & replace CLI
*   [sstadick/hck](https://github.com/sstadick/hck) - A faster and more featureful drop in replacement for `cut` [![build badge](https://github.com/sstadick/hck/workflows/Check/badge.svg?branch=master)](https://github.com/sstadick/hck)
*   [vishaltelangre/ff](https://github.com/vishaltelangre/ff) — Find files (ff) by name! [![build badge](https://camo.githubusercontent.com/1edd084ed411e2b67ce20b8d2ce3c648057a219253f36f403e1911b484d24491/68747470733a2f2f6170692e7472617669732d63692e6f72672f76697368616c74656c616e6772652f66662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vishaltelangre/ff)
*   [whitfin/bytelines](https://github.com/whitfin/bytelines) \[[bytelines](https://crates.io/crates/bytelines)\] — Read input lines as byte slices for high efficiency.
*   [whitfin/runiq](https://github.com/whitfin/runiq) — an efficient way to filter duplicate lines from unsorted input.
*   [xsv](https://crates.io/crates/xsv) — A fast CSV command line tool (slicing, indexing, selecting, searching, sampling, etc.) [![build badge](https://camo.githubusercontent.com/e433c7427ee3769f812f54a0161baa7c31dcc6c8da4fd237896e4c115d7bf799/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f7873762e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/xsv)

### [](#image-processing-1)Image processing

*   [Imager](https://github.com/imager-io/imager) — Automated image optimization.
*   [shssoichiro/oxipng](https://github.com/shssoichiro/oxipng) \[[oxipng](https://crates.io/crates/oxipng)\] — Multithreaded PNG optimizer written in Rust. [![Build Status](https://github.com/shssoichiro/oxipng/workflows/oxipng/badge.svg)](https://github.com/shssoichiro/oxipng/actions?query=branch%3Amaster) [![Version](https://camo.githubusercontent.com/4dbbbf78d731ca31b9163b368aa10b3ca2fd0a3edbc41bc8a33c9a3832a587ba/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f6f7869706e672e737667)](https://crates.io/crates/oxipng)

### [](#utilities)Utilities

*   [brycx/checkpwn](https://github.com/brycx/checkpwn) — A Have I Been Pwned (HIBP) command-line utility tool that lets you easily check for compromised accounts and passwords.
*   [evansmurithi/cloak](https://github.com/evansmurithi/cloak) — A Command Line OTP (One Time Password) Authenticator application. [![CI](https://github.com/evansmurithi/cloak/workflows/CI/badge.svg)](https://github.com/evansmurithi/cloak/workflows/CI/badge.svg) [![build badge](https://camo.githubusercontent.com/2bd909424f0eea4be786ceeb89e51f1b5890c2deff49d9fe5c6162c8cb88d8b8/68747470733a2f2f63692e6170707665796f722e636f6d2f6170692f70726f6a656374732f7374617475732f396d6c6670667275336e6734633638392f6272616e63682f6d61737465723f7376673d74727565)](https://ci.appveyor.com/project/evansmurithi/cloak)
*   [fcsonline/tmux-thumbs](https://github.com/fcsonline/tmux-thumbs) — A lightning fast version of tmux-fingers written in Rust, copy/pasting tmux like vimium/vimperator.
*   [guoxbin/dtool](https://github.com/guoxbin/dtool) — A useful command-line tool collection to assist development including conversion, codec, hashing, encryption, etc. [![Build Status](https://camo.githubusercontent.com/91d91152c2fe46512c6b46a77d54842f45027b60932afee6c7e74636f0c9104a/68747470733a2f2f6170692e7472617669732d63692e6f72672f67756f7862696e2f64746f6f6c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/guoxbin/dtool)
*   [nomino](https://github.com/yaa110/nomino) — Batch rename utility for developers [![Build Status](https://camo.githubusercontent.com/8a003305e46a62748b57c1665563b6701ac2fbcdbaea1a638fcb529dbeba58cb/68747470733a2f2f6170692e7472617669732d63692e6f72672f7961613131302f6e6f6d696e6f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/yaa110/nomino)
*   [raftario/licensor](https://github.com/raftario/licensor) — write licenses to stdout [![GitHub Actions](https://github.com/raftario/licensor/actions/workflows/build.yml/badge.svg?branch=master)](https://github.com/raftario/licensor/actions/workflows/build.yml)
*   [rustdesk/rustdesk](https://github.com/rustdesk/rustdesk) — A remote desktop software, great alternative to TeamViewer and AnyDesk.
*   [tversteeg/emplace](https://github.com/tversteeg/emplace) — Synchronize installed packages on multiple machines
*   [unrelentingtech/freepass](https://github.com/unrelentingtech/freepass) — The free password manager for power users.
*   [vamolessa/verco](https://github.com/vamolessa/verco) \[[verco](https://crates.io/crates/verco)\] — A simple Git/Hg tui client focused on keyboard shortcuts
*   [vaultwarden](https://github.com/dani-garcia/vaultwarden#readme) [![Build](https://github.com/dani-garcia/vaultwarden/actions/workflows/build.yml/badge.svg)](https://github.com/dani-garcia/vaultwarden/actions/workflows/build.yml) — Alternative implementation of the Bitwarden server API written in Rust
*   [yaa110/cb](https://github.com/yaa110/cb) — Command line interface to manage clipboard [![Build Status](https://camo.githubusercontent.com/3e0b83b33c7cd5b3f3c8ba0143744977e7d4f238c01706a68205d2bbc2ef860b/68747470733a2f2f6170692e7472617669732d63692e6f72672f7961613131302f63622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/yaa110/cb)

### [](#video)Video

*   [dertuxmalwieder/yaydl](https://github.com/dertuxmalwieder/yaydl) \[[yaydl](https://crates.io/crates/yaydl)\] - A simple video downloader
*   [harlanc/xiu](https://github.com/harlanc/xiu) — A powerful and secure live server by pure rust (rtmp/httpflv/hls/relay). [![Build Status](https://camo.githubusercontent.com/403738bd5890adecb4f3b445b77990f75913b190c01f1700dad08da30a77aa64/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6861726c616e632f7869752e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/harlanc/xiu) [![crates.io](https://camo.githubusercontent.com/6719aa7f288429bcf98a3d728188d0cba199dc922c28d07c9caa4b43b4c81041/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f7869752e737667)](https://crates.io/crates/xiu)
*   [xiph/rav1e](https://github.com/xiph/rav1e) — The fastest and safest AV1 encoder. [![build badge](https://camo.githubusercontent.com/8a246340d4ce77638d4ac055ae8d93f741f443d9b130916881c51384ac5a2f90/68747470733a2f2f6170692e7472617669732d63692e6f72672f786970682f72617631652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/xiph/rav1e)

### [](#virtualization)Virtualization

*   [containers/youki](https://github.com/containers/youki) — A container runtime in Rust [![build badge](https://github.com/containers/youki/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/containers/youki/actions)
*   [firecracker-microvm/firecracker](https://github.com/firecracker-microvm/firecracker) — A lightweight virtual machine for container workload [Firecracker Microvm](https://firecracker-microvm.github.io/)
*   [oracle/railcar](https://github.com/oracle/railcar) — Docker-like container OCI runtime implementation in Rust [![wercker status](https://camo.githubusercontent.com/bac1eca13a6ca0d5defdb5390be39a1d15af32afc4d32c236c48b33185e05572/68747470733a2f2f6170702e776572636b65722e636f6d2f7374617475732f37333065383734373732646330326336303035663461653465343262306361342f732f6d6173746572 "wercker status")](https://app.wercker.com/applications/59696a02ee70670100155ae2)
*   [tailhook/vagga](https://github.com/tailhook/vagga) — A containerization tool without daemons [![build badge](https://camo.githubusercontent.com/c3aff567a464a0b5c5b8d998d4212561d8f71d1921217c4ca75cfb015dbbb870/68747470733a2f2f6170692e7472617669732d63692e6f72672f7461696c686f6f6b2f76616767612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tailhook/vagga)

### [](#web)Web

*   [LemmyNet/lemmy](https://github.com/LemmyNet/lemmy) — A link aggregator / reddit clone for the fediverse [![Build Status](https://camo.githubusercontent.com/58003b0473dd3d61dd805e6f0fba624e1de7bd18b298b81a3d94718aebe05e38/68747470733a2f2f636c6f75642e64726f6e652e696f2f6170692f6261646765732f4c656d6d794e65742f6c656d6d792f7374617475732e737667)](https://cloud.drone.io/LemmyNet/lemmy)
*   [MASQ-Project/Node](https://github.com/MASQ-Project/Node) — MASQ Node software provides a decentralized mesh-network of nodes for global users to access normal internet content - next evolution of tech beyond Tor & VPN [![build badge](https://github.com/MASQ-Project/Node/actions/workflows/ci-matrix.yml/badge.svg)](https://github.com/MASQ-Project/Node/actions)
*   [Plume-org/Plume](https://github.com/Plume-org/Plume) — ActivityPub federating blogging application [![build badge](https://camo.githubusercontent.com/8d795cc336347cbe39b7f9dd4683a72a3e63d12238f9420fe83144202e94f8be/68747470733a2f2f6170692e7472617669732d63692e6f72672f506c756d652d6f72672f506c756d652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Plume-org/Plume)
*   [Revolt/delta](https://github.com/revoltchat/delta) - User-first chat platform built with modern web technologies.

### [](#web-servers)Web Servers

*   [joseluisq/static-web-server](https://github.com/joseluisq/static-web-server) — A blazing fast and asynchronous web server for static files-serving. ![zap](https://github.githubassets.com/images/icons/emoji/unicode/26a1.png) [![CI](https://github.com/joseluisq/static-web-server/actions/workflows/devel.yml/badge.svg)](https://github.com/joseluisq/static-web-server/actions/workflows/devel.yml?query=branch%3Amaster)
*   [mufeedvh/binserve](https://github.com/mufeedvh/binserve) — A blazingly fast static web server with routing, templating, and security in a single binary you can set up with zero code [![build badge](https://github.com/mufeedvh/binserve/workflows/CICD/badge.svg?branch=master)](https://github.com/mufeedvh/binserve/actions)
*   [ronanyeah/rust-hasura](https://github.com/ronanyeah/rust-hasura) — A demonstration of how a Rust GraphQL server can be used as a remote schema with [Hasura](https://hasura.io/) [![Rust](https://github.com/ronanyeah/rust-hasura/workflows/Rust/badge.svg?branch=master)](https://github.com/ronanyeah/rust-hasura/workflows/Rust/badge.svg?branch=master)
*   [svenstaro/miniserve](https://github.com/svenstaro/miniserve) — A small, self-contained cross-platform CLI tool that allows you to just grab the binary and serve some file(s) via HTTP [![build badge](https://github.com/svenstaro/miniserve/workflows/CI/badge.svg?branch=master)](https://github.com/svenstaro/miniserve/actions)
*   [thecoshman/http](https://github.com/thecoshman/http) — Host These Things Please — A basic http server for hosting a folder fast and simply [![build badge](https://camo.githubusercontent.com/1b198f58adf4e0fa4afbd516525b3fbba167e60494785bc64fd79ecf93dd9752/68747470733a2f2f6170692e7472617669732d63692e6f72672f746865636f73686d616e2f687474702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/thecoshman/http)
*   [TheWaWaR/simple-http-server](https://github.com/TheWaWaR/simple-http-server) — simple static http server
*   [wyhaya/see](https://github.com/wyhaya/see) — Static HTTP file server [![Build Status](https://camo.githubusercontent.com/409967f3624271428ddf1f06af47a9ed852bccb9721c4de2fe476f4215cfe801/68747470733a2f2f6170692e7472617669732d63692e6f72672f7779686179612f7365652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/wyhaya/see)

[](#development-tools)Development tools
---------------------------------------

*   [artifact](https://github.com/vitiral/artifact) — the design doc tool made for developers [![Build Status](https://camo.githubusercontent.com/5272c441f004ecebbac20103040adf8cbc6a4884ff8d91e3430fd90df0730315/68747470733a2f2f6170692e7472617669732d63692e6f72672f7669746972616c2f61727469666163742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vitiral/artifact)
*   [clippy](https://crates.io/crates/clippy) — Rust lints [![build badge](https://camo.githubusercontent.com/d74a0f1bb12d9b04e12d11a774eaad398fee08deaf4c244568fb2d1bb10b9722/68747470733a2f2f6170692e7472617669732d63692e636f6d2f727573742d6c616e672f727573742d636c697070792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-lang/rust-clippy)
*   [clog-tool/clog-cli](https://github.com/clog-tool/clog-cli) — generates a changelog from git metadata ([conventional changelog](https://blog.thoughtram.io/announcements/tools/2014/09/18/announcing-clog-a-conventional-changelog-generator-for-the-rest-of-us.html)) [![build badge](https://camo.githubusercontent.com/ff4dfb1e22afb5a11db5149ac7dc182168b8895dd64e6a5de1154a7632cbbc0d/68747470733a2f2f6170692e7472617669732d63692e6f72672f636c6f672d746f6f6c2f636c6f672d636c692e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/clog-tool/clog-cli)
*   [dan-t/rusty-tags](https://github.com/dan-t/rusty-tags) — create ctags/etags for a cargo project and all of its dependencies [![build badge](https://camo.githubusercontent.com/906c865b06c7139a8b7e340830f4f903c0cdae4105800d6cf62505e91a7c5c63/68747470733a2f2f6170692e7472617669732d63692e6f72672f64616e2d742f72757374792d746167732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/dan-t/rusty-tags)
*   [datanymizer/datanymizer](https://github.com/datanymizer/datanymizer) - Powerful database anonymizer with flexible rules [![build badge](https://github.com/datanymizer/datanymizer/workflows/CI/badge.svg?branch=main)](https://github.com/datanymizer/datanymizer/actions?query=workflow%3ACI+branch%3Amain)
*   [delta](https://crates.io/crates/git-delta) — A syntax-highlighter for git and diff output[![build badge](https://github.com/dandavison/delta/workflows/Continuous%20Integration/badge.svg)](https://github.com/dandavison/delta//actions)
*   [dotenv-linter](https://github.com/dotenv-linter/dotenv-linter) — Linter for `.env` files [![build badge](https://github.com/dotenv-linter/dotenv-linter/workflows/CI/badge.svg?branch=master)](https://github.com/dotenv-linter/dotenv-linter/actions?query=workflow%3ACI+branch%3Amaster)
*   [fw](https://github.com/brocode/fw) — workspace productivity booster [![Rust](https://github.com/brocode/fw/actions/workflows/rust.yml/badge.svg)](https://github.com/brocode/fw/actions/workflows/rust.yml)
*   [geiger](https://github.com/rust-secure-code/cargo-geiger) — A program that list statistics related to usage of unsafe Rust code in a Rust crate and all its dependencies [![Build Status](https://camo.githubusercontent.com/310803f3bba4b95c7168d8cb191261d4bfc7e5b45e0dc6811f9514d9fbbca6b4/68747470733a2f2f6465762e617a7572652e636f6d2f636172676f2d6765696765722f636172676f2d6765696765722f5f617069732f6275696c642f7374617475732f727573742d7365637572652d636f64652e636172676f2d6765696765723f6272616e63684e616d653d6d6173746572)](https://dev.azure.com/cargo-geiger/cargo-geiger/_build/latest?definitionId=1&branchName=master)
*   [git-journal](https://github.com/saschagrunert/git-journal/) — The Git Commit Message and Changelog Generation Framework [![build badge](https://camo.githubusercontent.com/35ffecf6a10c38ec4feafaa46347bf3533e6ef26ca59b260f7512428bbb3999d/68747470733a2f2f6170692e7472617669732d63692e6f72672f7361736368616772756e6572742f6769742d6a6f75726e616c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/saschagrunert/git-journal)
*   [just](https://github.com/casey/just) — A handy command runner for project-specific tasks [![build badge](https://camo.githubusercontent.com/45485a23220ff8a21d028c09737f26e3fda5b8ee6680111a117e21a213799a97/68747470733a2f2f6170692e7472617669732d63692e6f72672f63617365792f6a7573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/casey/just)
*   [mask](https://github.com/jakedeichert/mask) — A CLI task runner defined by a simple markdown file [![build badge](https://github.com/jakedeichert/mask/workflows/CI/badge.svg?branch=master)](https://github.com/jakedeichert/mask/actions?query=workflow%3ACI)
*   [Module Linker](https://github.com/fiatjaf/module-linker) — Extension that adds `<a>` links to references in `mod`, `use` and `extern crate` statements at GitHub.
*   [ptags](https://github.com/dalance/ptags) — A parallel universal-ctags wrapper for git repository [![Build Status](https://camo.githubusercontent.com/e36db65cf29e4458a5aea4de28dcbedc9accf38339881761f67845ccfd657f9d/68747470733a2f2f6170692e7472617669732d63692e6f72672f64616c616e63652f70746167732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/dalance/ptags)
*   [Racer](https://github.com/racer-rust/racer) — code completion for Rust [![build badge](https://camo.githubusercontent.com/31bf19cfd309a1e3d330c6ba6d1aca098e14df751897a2068148e330b1db9ffa/68747470733a2f2f6170692e7472617669732d63692e6f72672f72616365722d727573742f72616365722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/racer-rust/racer)
*   [Rust Language Server](https://github.com/rust-lang/rls) — A server that runs in the background, providing IDEs, editors, and other tools with information about Rust programs
*   [Rust Search Extension](https://github.com/huhu/rust-search-extension) — A handy browser extension to search crates and docs in address bar (omnibox). [![Build Status](https://github.com/huhu/rust-search-extension/workflows/build/badge.svg?branch=master)](https://github.com/huhu/rust-search-extension/actions)
*   [rust-lang/rustfix](https://github.com/rust-lang/rustfix) — automatically applies the suggestions made by rustc
*   [rustfmt](https://github.com/rust-lang/rustfmt) — A Rust code formatter [![build badge](https://camo.githubusercontent.com/eb08f9eea210788950cb201ebd6bcec3734e91cfe21338c9e9acaa9b6adc2865/68747470733a2f2f6170692e7472617669732d63692e636f6d2f727573742d6c616e672f72757374666d742e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/rust-lang/rustfmt)
*   [Rustup](https://github.com/rust-lang/rustup) — the Rust toolchain installer [![build badge](https://github.com/rust-lang/rustup/workflows/Linux%20(master)/badge.svg?branch=master)](https://github.com/rust-lang/rustup/actions)
*   [scriptisto](https://github.com/igor-petruk/scriptisto) A language-agnostic "shebang interpreter" that enables you to write one file scripts in compiled languages. [![Build Status](https://camo.githubusercontent.com/4f2cefababb4a6967d961ff47b0030907c3a01ef5955b4c2bbe66701cd4e1127/68747470733a2f2f636c6f75642e64726f6e652e696f2f6170692f6261646765732f69676f722d70657472756b2f7363726970746973746f2f7374617475732e737667)](https://cloud.drone.io/igor-petruk/scriptisto)
*   [semantic-rs](https://github.com/semantic-rs/semantic-rs) — automatic crate publishing [![build badge](https://camo.githubusercontent.com/984ca105b23c12d76f646f4deb09972b264d3b551e11304c98badd87e59fe4b3/68747470733a2f2f6170692e7472617669732d63692e6f72672f73656d616e7469632d72732f73656d616e7469632d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/semantic-rs/semantic-rs)
*   [synth](https://github.com/getsynth/synth) — A declarative data generation engine.

### [](#build-system)Build system

*   [Cargo](https://crates.io/) — the Rust package manager
    *   [cargo-benchcmp](https://crates.io/crates/cargo-benchcmp) — A utility to compare Rust micro-benchmarks [![build badge](https://camo.githubusercontent.com/c5c3e8cc4edbe0ee7a9d3e90cc094c2772db2397f993ae2b24e176fd15d77e6b/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f636172676f2d62656e6368636d702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/cargo-benchcmp)
    *   [cargo-bitbake](https://crates.io/crates/cargo-bitbake) — A cargo extension that can generate BitBake recipes utilizing the classes from meta-rust [![build badge](https://camo.githubusercontent.com/e10cf2d19e1851b002f57258bf981a86a2f424d9744c6ea1b84f3a6a94a18610/68747470733a2f2f6170692e7472617669732d63692e6f72672f636172646f652f636172676f2d62697462616b652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cardoe/cargo-bitbake)
    *   [cargo-cache](https://crates.io/crates/cargo-cache) — inspect/manage/clean your cargo cache (`~/.cargo/`/`${CARGO_HOME}`), print sizes etc [![Build Status](https://github.com/matthiaskrgr/cargo-cache/workflows/ci/badge.svg?branch=master)](https://github.com/matthiaskrgr/cargo-cache/actions)
    *   [cargo-check](https://crates.io/crates/cargo-check) — A wrapper around `cargo rustc -- -Zno-trans` which can be helpful for running a faster compile if you only need correctness checks [![build badge](https://camo.githubusercontent.com/3773579866683141eb37975a5f8ada67b615c4c284ac228cb5b17882eb637d42/68747470733a2f2f6170692e7472617669732d63692e6f72672f72736f6c6f6d6f2f636172676f2d636865636b2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rsolomo/cargo-check)
    *   [cargo-count](https://crates.io/crates/cargo-count) — lists source code counts and details about cargo projects, including unsafe statistics [![build badge](https://camo.githubusercontent.com/bb1e3c7cd99daa5b70bde6de2bea473e043eae57e9a14034f6c11bcdefcaff7b/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b626b6e6170702f636172676f2d636f756e742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kbknapp/cargo-count)
    *   [cargo-deb](https://crates.io/crates/cargo-deb) — Generates binary Debian packages [![build badge](https://camo.githubusercontent.com/47e0d9638e077e884f47cf1dc23a38abc7f37639ed70071585c69216d9ac00b7/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6d737469636b2f636172676f2d6465622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mmstick/cargo-deb)
    *   [cargo-deps](https://crates.io/crates/cargo-deps) — build dependency graphs of Rust projects [![build badge](https://camo.githubusercontent.com/4a0371ed7c7310a6b43f34d43990e78eba2443e3c8fb227be61478c15fd2c2f8/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6d2d6361742f636172676f2d646570732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/m-cat/cargo-deps)
    *   [cargo-do](https://crates.io/crates/cargo-do) — run multiple cargo commands in a row [![build badge](https://camo.githubusercontent.com/a47f00cbcebe3e4c6bac0e049cd92d1f0b0320970c95c0f4e1ba2c801f3c58ed/68747470733a2f2f6170692e7472617669732d63692e6f72672f70776f6f6c636f632f636172676f2d646f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/pwoolcoc/cargo-do)
    *   [cargo-ebuild](https://crates.io/crates/cargo-ebuild) — cargo extension that can generate ebuilds using the in-tree eclasses [![build badge](https://camo.githubusercontent.com/f902de843117620d193f85d869c3f028708362b249f47556ed7454232f571f22/68747470733a2f2f6170692e7472617669732d63692e6f72672f636172646f652f636172676f2d656275696c642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cardoe/cargo-ebuild)
    *   [cargo-edit](https://crates.io/crates/cargo-edit) — allows you to add and list dependencies by reading/writing to your Cargo.toml file from the command line [![build badge](https://camo.githubusercontent.com/27181cb53330eee9f1700fec2ff19eff89a7f9a648a67dd0e6f7eeed4f477fcf/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b696c6c65726375702f636172676f2d656469742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/killercup/cargo-edit)
    *   [cargo-generate](https://github.com/cargo-generate/cargo-generate) A generator of a rust project by leveraging a pre-existing git repository as a template.
    *   [cargo-graph](https://crates.io/crates/cargo-graph) — updated fork of `cargo-dot` with additional features. Unmaintained, see `cargo-deps` [![build badge](https://camo.githubusercontent.com/008fc4661e327eae88b70378d28c793d41e3d7072c6007f7de35b1b55bf1b2c3/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b626b6e6170702f636172676f2d67726170682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kbknapp/cargo-graph)
    *   [cargo-info](https://crates.io/crates/cargo-info) — queries crates.io for crates details from command line [![build badge](https://camo.githubusercontent.com/cd8f613f728237ac4c8d4ef6bfa25d1e10c61ff9ebfd2c91acdf1303ec2bcb09/68747470733a2f2f6170692e7472617669732d63692e6f72672f696d702f636172676f2d696e666f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/imp/cargo-info)
    *   [cargo-license](https://crates.io/crates/cargo-license) — A cargo subcommand to quickly view the licenses of all dependencies. [![build badge](https://camo.githubusercontent.com/3074e5aa48ba1255e52281fc63da269caa8dc82a2a4c00ac21f65c60d780984a/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f6e75722f636172676f2d6c6963656e73652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/onur/cargo-license)
    *   [cargo-make](https://crates.io/crates/cargo-make) — Rust task runner and build tool. [![build badge](https://camo.githubusercontent.com/cc9396dfc161f569f8085418a9d633b2de18004901389955a21e5276f838a2cf/68747470733a2f2f6170692e7472617669732d63692e6f72672f73616769656775726172692f636172676f2d6d616b652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sagiegurari/cargo-make)
    *   [cargo-modules](https://crates.io/crates/cargo-modules) — A cargo plugin for showing a tree-like overview of a crate's modules. [![build badge](https://camo.githubusercontent.com/6db758deca605066f21b17cb6818605126f688f1beed4288237dc3571f9505a3/68747470733a2f2f6170692e7472617669732d63692e6f72672f72656765786964656e742f636172676f2d6d6f64756c65732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/regexident/cargo-modules)
    *   [cargo-multi](https://crates.io/crates/cargo-multi) — runs specified cargo command on multiple crates [![build badge](https://camo.githubusercontent.com/5984b24ed85f0f4b48b443f6f6f38891113d598cdb008dabfe10cf1772991303/68747470733a2f2f6170692e7472617669732d63692e6f72672f696d702f636172676f2d6d756c74692e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/imp/cargo-multi)
    *   [cargo-outdated](https://crates.io/crates/cargo-outdated) — displays when newer versions of Rust dependencies are available, or out of date [![build badge](https://camo.githubusercontent.com/7ac4bebd8b77293d8604b06ab8cb82be94ebc484e6f5ccb7f5debe64ea378e77/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b626b6e6170702f636172676f2d6f757464617465642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kbknapp/cargo-outdated)
    *   [cargo-release](https://crates.io/crates/cargo-release) — tool for releasing git-managed cargo project, build, tag, publish, doc and push [![Rust](https://github.com/crate-ci/cargo-release/actions/workflows/ci.yml/badge.svg)](https://github.com/crate-ci/cargo-release/actions/workflows/rust.yml)
    *   [cargo-script](https://crates.io/crates/cargo-script) — lets people quickly and easily run Rust "scripts" which can make use of Cargo's package ecosystem [![build badge](https://camo.githubusercontent.com/8a6533a20320154fea603bdadcf96775626801287955670987f3833f462e753d/68747470733a2f2f6170692e7472617669732d63692e6f72672f44616e69656c4b6565702f636172676f2d7363726970742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/DanielKeep/cargo-script)
    *   [cargo-tree](https://github.com/sfackler/cargo-tree) – Cargo subcommand that visualizes a crate's dependency graph in a tree-like format [![CircleCI](https://camo.githubusercontent.com/5a4c97cc302fb3401936ea113feb7739983732ce4c2dbda4d28becce03912c35/68747470733a2f2f636972636c6563692e636f6d2f67682f736661636b6c65722f636172676f2d747265652e7376673f7374796c653d736869656c64)](https://app.circleci.com/pipelines/github/sfackler/cargo-tree)
    *   [cargo-update](https://crates.io/crates/cargo-update) — cargo subcommand for checking and applying updates to installed executables [![build badge](https://camo.githubusercontent.com/e68b4691b93c3ea9b67ba4c685a189465bb13cea576fe4f522bf3d158b55fbe5/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e6162696a61637a6c6577656c692f636172676f2d7570646174652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/nabijaczleweli/cargo-update)
    *   [cargo-watch](https://crates.io/crates/cargo-watch) — utility for cargo to compile projects when sources change [![build badge](https://camo.githubusercontent.com/601e143b4d2a30625dd9d5ab12729a71cc04e2de352e8c7146b1ccd9b547ed12/68747470733a2f2f6170692e7472617669732d63692e6f72672f70617373636f642f636172676f2d77617463682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/passcod/cargo-watch)
    *   [dtolnay/cargo-expand](https://github.com/dtolnay/cargo-expand) — Expand macros in your source code
*   CMake
    *   [Devolutions/CMakeRust](https://github.com/Devolutions/CMakeRust) — useful for integrating a Rust library into a CMake project
    *   [SiegeLord/RustCMake](https://github.com/SiegeLord/RustCMake) — an example project showing usage of CMake with Rust [![build badge](https://camo.githubusercontent.com/11c013e8015a8c877cfc12a7cf8de002903dd43ad8ee3787f5c790e566943358/68747470733a2f2f6170692e7472617669732d63692e6f72672f53696567654c6f72642f52757374434d616b652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/SiegeLord/RustCMake)
*   Github actions
    *   [icepuma/rust-action](https://github.com/icepuma/rust-action) — rust github action
    *   [peaceiris/actions-mdbook](https://github.com/peaceiris/actions-mdbook) — GitHub Actions for mdBook

### [](#debugging)Debugging

*   GDB
    *   [gdbgui](https://github.com/cs01/gdbgui) — Browser based frontend for gdb to debug C, C++, Rust, and go. [![build badge](https://camo.githubusercontent.com/ff15f1d7ea44900723d5c047c54513322d401af0cf5d8cf66d5926f4f2bf515c/68747470733a2f2f6170692e7472617669732d63692e6f72672f637330312f6764626775692e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cs01/gdbgui)
*   LLDB
    *   [CodeLLDB](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb) — A LLDB extension for [Visual Studio Code](https://code.visualstudio.com/).

### [](#deployment)Deployment

*   Docker
    *   [emk/rust-musl-builder](https://github.com/emk/rust-musl-builder) — Docker images for compiling static Rust binaries using musl-libc and musl-gcc, with static versions of useful C libraries
    *   [kpcyrd/mini-docker-rust](https://github.com/kpcyrd/mini-docker-rust) — An example project for very small rust docker images [![build badge](https://camo.githubusercontent.com/0edacabc20afa569d14ca0124d10fa0d61268f5f1cd448c3b193c32ba69ef6d1/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b70637972642f6d696e692d646f636b65722d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kpcyrd/mini-docker-rust)
    *   [liuchong/docker-rustup](https://github.com/liuchong/docker-rustup) — A multiple version (with musl tools) Rust Docker image
    *   [messense/rust-musl-cross](https://github.com/messense/rust-musl-cross) — Docker images for compiling static Rust binaries using musl-cross [![build badge](https://camo.githubusercontent.com/e223d88821970b9e2f093b08c9413f5be72c6eb5cfefbc053a5df1e39b84e066/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d657373656e73652f727573742d6d75736c2d63726f73732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/messense/rust-musl-cross)
    *   [rust-lang-nursery/docker-rust](https://github.com/rust-lang/docker-rust) — the official Rust Docker image
*   Github Pages
    *   [wasm-template-rust](https://github.com/sn99/wasm-template-rust) — A wasm template for Rust to publish to gh-pages without npm-deploy [![Build Status](https://camo.githubusercontent.com/6fd5ca5d8b2fbb3542f8515f9a3f713e92834690fec27398d581893f534c4b6d/68747470733a2f2f6170692e7472617669732d63692e636f6d2f736e39392f7761736d2d74656d706c6174652d727573742e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/sn99/wasm-template-rust)
*   Heroku
    *   [emk/heroku-buildpack-rust](https://github.com/emk/heroku-buildpack-rust) — A buildpack for Rust applications on Heroku

### [](#embedded)Embedded

[Rust Embedded](https://rust-embedded.org/)

*   Arduino
    *   [avr-rust/ruduino](https://github.com/avr-rust/ruduino) ^\`^t Reusable components for the Arduino Uno.
*   Cross compiling
    *   [japaric/rust-cross](https://github.com/japaric/rust-cross) — everything you need to know about cross compiling Rust programs [![build badge](https://camo.githubusercontent.com/9d758a4af770f993da40ffb773e30c7bdb6023f2e59458bcd7ef7d552b04b6dd/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a6170617269632f727573742d63726f73732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/japaric/rust-cross)
    *   [japaric/xargo](https://github.com/japaric/xargo) — effortless cross compilation of Rust programs to custom bare-metal targets like ARM Cortex-M [![build badge](https://camo.githubusercontent.com/7f508eb4cb9bd80b53246a83dc1a4cbfce906d5f8f99d7519b457b83acb1a3f6/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a6170617269632f786172676f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/japaric/xargo)
*   Raspberry Pi
    *   [Ogeon/rust-on-raspberry-pi](https://github.com/Ogeon/rust-on-raspberry-pi) — instructions for how to cross compile Rust projects for the Raspberry Pi .

### [](#ffi)FFI

See also [Foreign Function Interface](https://doc.rust-lang.org/book/first-edition/ffi.html), [The Rust FFI Omnibus](http://jakegoulding.com/rust-ffi-omnibus/) (a collection of examples of using code written in Rust from other languages) and [FFI examples written in Rust](https://github.com/alexcrichton/rust-ffi-examples).

*   C
    *   [rlhunt/cbindgen](https://github.com/eqrion/cbindgen) — generates C header files from Rust source files. Used in Gecko for WebRender [![build badge](https://camo.githubusercontent.com/a24d5589587503ae34149f076cba04a985bc5dfa57af888dc8fb8969472c78f7/68747470733a2f2f6170692e7472617669732d63692e6f72672f657172696f6e2f6362696e6467656e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/eqrion/cbindgen)
    *   [Sean1708/rusty-cheddar](https://github.com/Sean1708/rusty-cheddar) — generates C header files from Rust source files [![build badge](https://camo.githubusercontent.com/78499a61cd5a55fd3a2c0a59e79602c45a4b0abcb0734c70c5188d6330e609ec/68747470733a2f2f6170692e7472617669732d63692e6f72672f5365616e313730382f72757374792d636865646461722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Sean1708/rusty-cheddar)
*   C++
    *   [dtolnay/cxx](https://github.com/dtolnay/cxx) — Safe interop between Rust and C++ [![build badge](https://camo.githubusercontent.com/9ef5b1489a563da1d57eb8b0f8cb91ac1159b39da1cce9fd24ea793a71086ba6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6769746875622d64746f6c6e61792f6378782d3864613063623f7374796c653d666f722d7468652d6261646765266c6162656c436f6c6f723d353535353535266c6f676f3d676974687562)](https://github.com/dtolnay/cxx)
    *   [rust-cpp](https://crates.io/crates/cpp) - Embed C++ code directly in Rust. [![Build Status](https://camo.githubusercontent.com/7314232f32e388473d76532003436faeabf08de4680723a36fb5e8a0ffc74963/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d7973746f722f727573742d6370702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mystor/rust-cpp) [![Build status](https://camo.githubusercontent.com/c20752b0b6fd7a4e1d688ebdc56b1ca1f17ecc80b3e0a87ec1c69bf76656a01d/68747470733a2f2f63692e6170707665796f722e636f6d2f6170692f70726f6a656374732f7374617475732f75753736766d6372776e6a71726130752f6272616e63682f6d61737465723f7376673d74727565)](https://ci.appveyor.com/project/mystor/rust-cpp/branch/master)
    *   [rust-lang/rust-bindgen](https://github.com/rust-lang/rust-bindgen) — A Rust bindings generator
*   Erlang
    *   [rusterlium/rustler](https://github.com/rusterlium/rustler) — safe Rust bridge for creating Erlang NIF functions [![build badge](https://camo.githubusercontent.com/3ed9d7c82c72fdbbac5fb764ef1843ee54e1ab2d560c2b31c53191444f4ea59d/68747470733a2f2f6170692e7472617669732d63692e6f72672f7275737465726c69756d2f727573746c65722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rusterlium/rustler)
*   Haskell
    *   [mgattozzi/curryrs](https://github.com/mgattozzi/curryrs) — Bridge the gap between Haskell and Rust
*   Java
    *   [bennettanderson/rjni](https://github.com/benanders/rjni) — use Java from Rust
    *   [drrb/java-rust-example](https://github.com/drrb/java-rust-example) — use Rust from Java [![build badge](https://camo.githubusercontent.com/5ec6594c1e995846d835fc0afc2c064f69e8901ed399804795ee44f29b74870c/68747470733a2f2f6170692e7472617669732d63692e6f72672f647272622f6a6176612d727573742d6578616d706c652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/drrb/java-rust-example)
    *   [j4rs](https://crates.io/crates/j4rs) — use Java from Rust [![build badge](https://camo.githubusercontent.com/349fc7656f1a635301efc959cdee9a71b3b75033d69ea7d08f84d141853a0a8c/68747470733a2f2f6170692e7472617669732d63692e6f72672f6173746f6e62697465636f64652f6a3472732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/astonbitecode/j4rs)
    *   [jni](https://crates.io/crates/jni) — use Rust from Java [![build badge](https://camo.githubusercontent.com/47876641045bf4f176284f277e8057f0d8866df806e69a472b9a0bbd96857865/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a6e692d72732f6a6e692d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jni-rs/jni-rs)
    *   [jni-sys](https://crates.io/crates/jni-sys) — Rust definitions corresponding to jni.h [![build badge](https://camo.githubusercontent.com/9337f83fcc2eb266b3119b304ad4829c6e825126646b09993531447a8d1c0371/68747470733a2f2f6170692e7472617669732d63692e6f72672f736661636b6c65722f727573742d6a6e692d7379732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sfackler/rust-jni-sys)
    *   [rucaja](https://crates.io/crates/rucaja) — use Java from Rust [![build badge](https://camo.githubusercontent.com/c9f1542a2170b09de5bb65e455aa6d7a94b994a0e75dc1c544c6c4e060a03b44/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b756431696e672f727563616a612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kud1ing/rucaja)
*   Lua
    *   [jcmoyer/rust-lua53](https://github.com/jcmoyer/rust-lua53) — Lua 5.3 bindings for Rust [![build badge](https://camo.githubusercontent.com/541b2fd6c63d54d9c271c28593dd05bf8e5fb4ddd37ecf53a1273fcd5dc96247/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a636d6f7965722f727573742d6c756135332e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jcmoyer/rust-lua53)
    *   [lilyball/rust-lua](https://github.com/lilyball/rust-lua) — Safe Rust bindings to Lua 5.1 [![build badge](https://camo.githubusercontent.com/f1c5456a3aa803b3a6853615afba9a973c2bb7c2b7d667689f251f7be949927c/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c696c7962616c6c2f727573742d6c75612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lilyball/rust-lua)
    *   [tickbh/td\_rlua](https://github.com/tickbh/td_rlua) \[[td\_rlua](https://crates.io/crates/td_rlua)\] — Zero-cost high-level lua 5.3 wrapper for Rust [![build badge](https://camo.githubusercontent.com/6d5a2133874ec1ceb96dc37dec14dd2f1d21d5371ed1369518d552a25f6c219b/68747470733a2f2f6170692e7472617669732d63692e6f72672f7469636b62682f74645f726c75612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tickbh/td_rlua)
    *   [tomaka/hlua](https://github.com/tomaka/hlua) — Rust library to interface with Lua [![build badge](https://camo.githubusercontent.com/1f278e6dceb03ce9cda2016cf91190b7f759b844d0ddf328cded6c50566c653a/68747470733a2f2f6170692e7472617669732d63692e6f72672f746f6d616b612f686c75612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tomaka/hlua)
*   mruby
    *   [anima-engine/mrusty](https://github.com/anima-engine/mrusty) — mruby safe bindings for Rust [![build badge](https://camo.githubusercontent.com/e111748c93f5c3b7fcbd0d4ee55ad69c9583c3b6cbecd0c6f9cfe8f8859e18cc/68747470733a2f2f6170692e7472617669732d63692e6f72672f616e696d612d656e67696e652f6d72757374792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/anima-engine/mrusty)
*   Node.js
    *   [infinyon/node-bindgen](https://github.com/infinyon/node-bindgen) - Easy way to generate nodejs module using Rust
    *   [neon-bindings/neon](https://github.com/neon-bindings/neon) — Rust bindings for writing safe and fast native Node.js modules [![build badge](https://camo.githubusercontent.com/1802e98cd7eb98d09b11145462064f9080c9ec1512396042148a1c17c18cec04/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e656f6e2d62696e64696e67732f6e656f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/neon-bindings/neon)
*   Objective-C
    *   [SSheldon/rust-objc](https://github.com/SSheldon/rust-objc) — Objective-C Runtime bindings and wrapper for Rust
*   Perl
    *   [vickenty/perl-xs](https://github.com/vickenty/perl-xs) — Create Perl XS modules using Rust [![build badge](https://camo.githubusercontent.com/6f1c84c2ba4f9ce982c3eb796a50829931bc0ccac9cd9d4d675525fb5c1fdaf4/68747470733a2f2f6170692e7472617669732d63692e6f72672f7669636b656e74792f7065726c2d78732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vickenty/perl-xs)
*   Python
    *   [dgrunwald/rust-cpython](https://github.com/dgrunwald/rust-cpython) — Python bindings [![build badge](https://camo.githubusercontent.com/7b70314f1f55176a671f516a139d1eb507f7c4a72c031b15d1b0e9bc57c3ae2b/68747470733a2f2f6170692e7472617669732d63692e6f72672f646772756e77616c642f727573742d63707974686f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/dgrunwald/rust-cpython)
    *   [getsentry/milksnake](https://github.com/getsentry/milksnake) — extension for python setuptools that allows you to distribute dynamic linked libraries in Python wheels in the most portable way imaginable.
    *   [PyO3/PyO3](https://github.com/PyO3/PyO3) — Rust bindings for the Python interpreter [![build badge](https://camo.githubusercontent.com/f3a561a33263c7547dd7ac11ecb52595f520852110ee299f7d3d492f3f16c3d4/68747470733a2f2f6170692e7472617669732d63692e6f72672f50794f332f70796f332e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/PyO3/pyo3)
*   Ruby
    *   [d-unseductable/ruru](https://github.com/d-unseductable/ruru) — native Ruby extensions written in Rust [![build badge](https://camo.githubusercontent.com/353cf49d0c93373aa19dd688e0766b511e5afddd8aba52bb9509a4fbe7f3440f/68747470733a2f2f6170692e7472617669732d63692e6f72672f642d756e73656475637461626c652f727572752e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/d-unseductable/ruru)
    *   [danielpclark/rutie](https://github.com/danielpclark/rutie) — native Ruby extensions written in Rust and vice versa [![Build Status](https://camo.githubusercontent.com/64badf81c52cc17ecdc2f5a8f3117d9f52376c38769ea81182e73fb7ab73b866/68747470733a2f2f6170692e7472617669732d63692e6f72672f64616e69656c70636c61726b2f72757469652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/danielpclark/rutie)
    *   [tildeio/helix](https://github.com/tildeio/helix) — write Ruby classes in Rust [![build badge](https://camo.githubusercontent.com/4e875d2f2fb3c25224aa5ec0a213f0e4cbbad9c685b3288da77dc6106db127b6/68747470733a2f2f6170692e7472617669732d63692e6f72672f74696c6465696f2f68656c69782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tildeio/helix)
*   Web Assembly
    *   [rhysd/wain](https://github.com/rhysd/wain) - wain: WebAssembly INterpreter from scratch in Safe Rust with zero dependency [![build badge](https://github.com/rhysd/wain/workflows/CI/badge.svg?branch=master&event=push)](https://github.com/rhysd/wain/actions?query=workflow%3ACI+branch%3Amaster+event%3Apush)
    *   [rustwasm/wasm-bindgen](https://github.com/rustwasm/wasm-bindgen) — A project for facilitating high-level interactions between wasm modules and JS. [![build badge](https://camo.githubusercontent.com/2f96e685fe3af86fc2926cb07ad57b797d745653cfa073887da26c0c70c1acdc/68747470733a2f2f6170692e7472617669732d63692e636f6d2f727573747761736d2f7761736d2d62696e6467656e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rustwasm/wasm-bindgen)
    *   [rustwasm/wasm-pack](https://github.com/rustwasm/wasm-pack) — ![package](https://github.githubassets.com/images/icons/emoji/unicode/1f4e6.png) ![sparkles](https://github.githubassets.com/images/icons/emoji/unicode/2728.png) pack up the wasm and publish it to npm! [![build badge](https://camo.githubusercontent.com/a22c7c6d9e797d07aa68dd4a6cfb5a04c1969b18a264ba70f325021327f9b897/68747470733a2f2f6170692e7472617669732d63692e636f6d2f727573747761736d2f7761736d2d7061636b2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rustwasm/wasm-pack)

### [](#ides)IDEs

See also [Are we (I)DE yet?](https://areweideyet.com/) and [Rust Tools](https://www.rust-lang.org/tools).

*   [Atom](https://atom.io/)
    *   [rust-lang/atom-ide-rust](https://github.com/rust-lang/atom-ide-rust) — Rust IDE support for Atom, powered by the Rust Language Server (RLS) [![Build Status](https://camo.githubusercontent.com/d1a240c6219c7b2a1bb95a3bb1f3b03b372a59b9c75456023dddfc11e60b1e9d/68747470733a2f2f6170692e7472617669732d63692e636f6d2f727573742d6c616e672f61746f6d2d6964652d727573742e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/grust-lang/atom-ide-rust)
    *   [zargony/atom-language-rust](https://github.com/zargony/atom-language-rust)
*   [Eclipse](https://www.eclipse.org/)
    *   [Eclipse Corrosion](https://github.com/eclipse/corrosion)
    *   [RustDT](https://github.com/RustDT/RustDT) — [![build badge](https://camo.githubusercontent.com/fd9f642db5efdbb864f7f4621a79a9108190959629740b3d12e2477fbebaafe9/68747470733a2f2f6170692e7472617669732d63692e6f72672f5275737444542f5275737444542e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/RustDT/RustDT)
*   [Emacs](https://www.gnu.org/software/emacs/)
    *   [emacs-racer](https://github.com/racer-rust/emacs-racer) — Autocompletion (see also [company](https://company-mode.github.io) and [auto-complete](https://github.com/auto-complete/auto-complete))
    *   [flycheck-rust](https://github.com/flycheck/flycheck-rust) — Rust support for [Flycheck](https://github.com/flycheck/flycheck)
    *   [rust-mode](https://github.com/rust-lang/rust-mode) — Rust Major Mode
    *   [rustic](https://github.com/brotzeit/rustic) - Rust development environment for Emacs [![build badge](https://github.com/brotzeit/rustic/workflows/CI/badge.svg)](https://github.com/brotzeit/rustic/actions?query=workflow%3ACI)
*   [gitpod.io](https://gitpod.io) — Online IDE with full Rust support based on Rust Language Server
*   [gnome-builder](https://wiki.gnome.org/Apps/Builder) native support for rust and cargo since Version 3.22.2
*   [IntelliJ](https://www.jetbrains.com/idea/)
    *   [intellij-rust/intellij-rust](https://github.com/intellij-rust/intellij-rust) — [![build badge](https://camo.githubusercontent.com/f4fdb9431acd58fc554833690fc2fae88c21d98321f24e459111129c68c959b2/68747470733a2f2f6170692e7472617669732d63692e6f72672f696e74656c6c696a2d727573742f696e74656c6c696a2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/intellij-rust/intellij-rust)
*   [Kakoune](http://kakoune.org/)
    *   [kak-lsp/kak-lsp](https://github.com/kak-lsp/kak-lsp/) — [LSP](https://microsoft.github.io/language-server-protocol/) client. Implemented in Rust and supports rls out of the box.
*   [Ride](https://github.com/madeso/ride) — [![build badge](https://camo.githubusercontent.com/9b9ec4156e7519497d1f9c3639db7b78cadc196c4b1f3407f1c3692d8f994dec/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d616465736f2f726964652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/madeso/ride)
*   [SolidOak](https://github.com/oakes/SolidOak) — A simple IDE for Rust, based on GTK+ and [Neovim](https://github.com/neovim/neovim)
*   [Sublime Text](https://www.sublimetext.com/)
    *   [rust-lang/rust-enhanced](https://github.com/rust-lang/rust-enhanced) — official Rust package
*   [Vim](https://vim.sourceforge.io/) — the ubiquitous text editor
    *   [autozimu/LanguageClient-neovim](https://github.com/autozimu/LanguageClient-neovim) — [LSP](https://microsoft.github.io/language-server-protocol/) client. Implemented in Rust and supports rls out of the box.
    *   [rust.vim](https://github.com/rust-lang/rust.vim) — provides file detection, syntax highlighting, formatting, Syntastic integration, and more.
    *   [vim-racer](https://github.com/racer-rust/vim-racer) — allows vim to use [Racer](https://github.com/racer-rust/racer) for Rust code completion and navigation.
*   Visual Studio
    *   [dgriffen/rls-vs2017](https://github.com/ZoeyR/rls-vs2017) — Rust support for Visual Studio 2017 Preview [![build badge](https://camo.githubusercontent.com/5398e1eb0d1d7c6f889e9e9f8680706430ee829ff26370e6f0f0c422a3b3c3a3/68747470733a2f2f63692e6170707665796f722e636f6d2f6170692f70726f6a656374732f7374617475732f64326c786c696e63776e696e68736e673f7376673d74727565)](https://ci.appveyor.com/project/dgriffen/rls-vs2017)
    *   [PistonDevelopers/VisualRust](https://github.com/PistonDevelopers/VisualRust) — A Visual Studio extension for Rust [![Build status](https://camo.githubusercontent.com/947dc0757468a91b113b6afbb21482d6a7221386630a8e5a2fcce49df538d6ec/68747470733a2f2f63692e6170707665796f722e636f6d2f6170692f70726f6a656374732f7374617475732f356e77356e6f31306a6a3079347033663f7376673d74727565)](https://ci.appveyor.com/project/vosen/visualrust)
*   [Visual Studio Code](https://code.visualstudio.com/)
    *   [CodeLLDB](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb) — A LLDB extension
    *   [crates](https://github.com/serayuzgur/crates) — crates is an extension for crates.io dependencies. [![build badge](https://camo.githubusercontent.com/36ac8243897a4ce09029c11417be8d47fc408397ee9f8ece005df29e3b157caf/68747470733a2f2f696d672e736869656c64732e696f2f7673636f64652d6d61726b6574706c6163652f762f7365726179757a6775722e6372617465732e737667)](https://github.com/serayuzgur/crates) [![build badge](https://camo.githubusercontent.com/5d196fef106a72fffe450eb00bfed9fe8ec76ac3f45aa02754811bd937591346/68747470733a2f2f6170692e7472617669732d63692e6f72672f7365726179757a6775722f6372617465732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/serayuzgur/crates)
    *   [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=matklad.rust-analyzer) — An alternative rust language server to the RLS
    *   [rust-lang/rls-vscode](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust) — Rust support for Visual Studio Code

### [](#profiling)Profiling

*   [bheisler/criterion.rs](https://github.com/bheisler/criterion.rs) — Statistics-driven benchmarking library for Rust [![Build Status](https://camo.githubusercontent.com/0e49ef038b5e1c9bdaacc4ec836083f7c4422950d9f2ce2188382547a9ae0040/68747470733a2f2f6170692e7472617669732d63692e6f72672f62686569736c65722f637269746572696f6e2e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/bheisler/criterion.rs)
*   [Bytehound](https://github.com/koute/bytehound) — A memory profiler for Linux
*   [ellisonch/rust-stopwatch](https://github.com/ellisonch/rust-stopwatch) — A stopwatch library [![build badge](https://camo.githubusercontent.com/381f0ed8e2fb49752304b14bc07eac4388e4d5fb010ee764f0d266b91c055e35/68747470733a2f2f6170692e7472617669732d63692e6f72672f656c6c69736f6e63682f727573742d73746f7077617463682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ellisonch/rust-stopwatch)
*   FlameGraphs
    *   [llogiq/flame](https://github.com/llogiq/flame) — [![build badge](https://camo.githubusercontent.com/ceb77565497a678d911578ce07ff835c83c25c10999f93ea736237d6f8b69329/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c6c6f6769712f666c616d652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/llogiq/flame)
    *   [mrhooray/torch](https://github.com/mrhooray/torch) — generates FlameGraphs based on DWARF Debug Info
*   [sharkdp/hyperfine](https://github.com/sharkdp/hyperfine) — A command-line benchmarking tool [![Version info](https://camo.githubusercontent.com/a78a364a825fa3618f3bf4327efb6d7c77f1b7057ece62e1ab55229e0e816dc2/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f687970657266696e652e737667)](https://crates.io/crates/hyperfine) [![Build Status](https://camo.githubusercontent.com/7a48159cb9e70f1941009b2fb602c36b03dfe05d13658ad30d19fb78a38072dc/68747470733a2f2f6170692e7472617669732d63692e6f72672f736861726b64702f687970657266696e652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sharkdp/hyperfine)

### [](#services)Services

*   [deps.rs](https://github.com/deps-rs/deps.rs) — Detect outdated or insecure dependencies
*   [docs.rs](https://docs.rs) — Automatic documentation generation of crates

### [](#static-analysis)Static analysis

\[[assert](https://crates.io/keywords/assert), [static](https://crates.io/keywords/static)\]

*   [facebookexperimental/MIRAI](https://github.com/facebookexperimental/mirai) — an abstract interpreter operating on Rust's mid-level intermediate representation (MIR) [![Continuous Integration](https://github.com/facebookexperimental/MIRAI/actions/workflows/rust.yml/badge.svg)](https://github.com/facebookexperimental/MIRAI/actions/workflows/rust.yml)
*   [static\_assertions](https://crates.io/crates/static_assertions) — Compile-time assertions to ensure that invariants are met [![Build Status](https://camo.githubusercontent.com/2a19d6c170b5f3f394fb9e6e47eae6b2de9a6b4ec4744631e53a3d765499b05b/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e767a717a2f7374617469632d617373657274696f6e732d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/nvzqz/static-assertions-rs/)

### [](#testing)Testing

\[[test](https://crates.io/keywords/test), [testing](https://crates.io/keywords/testing)\]

*   Code Coverage
    *   [tarpaulin](https://crates.io/crates/cargo-tarpaulin) — A code coverage tool designed for Rust [![build badge](https://camo.githubusercontent.com/e78fd416adb7b4a644ad07b0509a805a51f270e502c57bd88f6641daf101654d/68747470733a2f2f6170692e7472617669732d63692e6f72672f7265706f7369746f726965732f78643030393634322f7461727061756c696e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/xd009642/tarpaulin)
*   Continuous Integration
    *   [trust](https://github.com/japaric/trust) — A Travis CI and AppVeyor template to test your Rust crate on 5 architectures and publish binary releases of it for Linux, macOS and Windows
*   Frameworks and Runners
    *   [AlKass/polish](https://github.com/AlKass/polish) — Mini Testing/Test-Driven Framework [![Build Status](https://camo.githubusercontent.com/fe20575193f8626925c084a590c29b66da7a7174015ec84ae778f6d0affe35a2/68747470733a2f2f6170692e7472617669732d63692e6f72672f416c4b6173732f706f6c6973682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/AlKass/polish) [![Crates Package Status](https://camo.githubusercontent.com/c175114e571f6830ac368ad8ad2314ee8ea6fa654c7b25f9ffd22c1eb7372c7a/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f706f6c6973682e737667)](https://crates.io/crates/polish)
    *   [cargo-dinghy](https://crates.io/crates/cargo-dinghy/) - A cargo extension to simplify running library tests and benches on smartphones and other small processor devices.
    *   [cucumber](https://crates.io/crates/cucumber) [![Latest Version](https://camo.githubusercontent.com/a2ff852bfa3d7a889b3694b653da29c89f0d055907f2ebb30e51f77db7d42ab4/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f637563756d6265722e737667)](https://crates.io/crates/cucumber) — An implementation of the Cucumber testing framework for Rust. Fully native, no external test runners or dependencies. [![Build Status](https://github.com/cucumber-rs/cucumber/workflows/CI/badge.svg?branch=master)](https://github.com/cucumber-rs/cucumber)
    *   [demonstrate](https://crates.io/crates/demonstrate) — Declarative Testing Framework [![Build Status](https://github.com/austinsheep/demonstrate/workflows/Continuous%20Integration/badge.svg?branch=master)](https://github.com/austinsheep/demonstrate)
    *   [rstest](https://crates.io/crates/rstest) — Fixture-based test framework for Rust [![Build Status](https://github.com/la10736/rstest/workflows/Test/badge.svg?branch=master)](https://github.com/la10736/rstest/actions)
    *   [speculate](https://crates.io/crates/speculate) — An RSpec inspired minimal testing framework for Rust
*   Mocking and Test Data
    *   [asomers/mockall](https://github.com/asomers/mockall) \[[mockall](https://crates.io/crates/mockall)\] — A powerful mock object library for Rust. [![Cirrus Build Status](https://camo.githubusercontent.com/e973e042f1480a36e909c31baeef3bafda1a2d1dfe0ad4de32a5852a05550971/68747470733a2f2f6170692e6369727275732d63692e636f6d2f6769746875622f61736f6d6572732f6d6f636b616c6c2e737667)](https://cirrus-ci.com/github/asomers/mockall)
    *   [fake-rs](https://github.com/cksac/fake-rs) — A library for generating fake data [![build badge](https://camo.githubusercontent.com/e4fd3d5872a991471cabeb9851edf7173f1ebf740495c2aaf1f9b974c7c46904/68747470733a2f2f6170692e7472617669732d63692e6f72672f7265706f7369746f726965732f636b7361632f66616b652d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cksac/fake-rs)
    *   [goldenfile](https://github.com/calder/rust-goldenfile) \[[goldenfile](https://crates.io/crates/goldenfile)\] - A library providing a simple API for goldenfile testing. [![build badge](https://camo.githubusercontent.com/7bc90b31a262b437a56547adbc9b7192b7c561eab4be56c6f11b016fabe9e23e/68747470733a2f2f6170692e7472617669732d63692e6f72672f63616c6465722f727573742d676f6c64656e66696c652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/calder/rust-goldenfile)
    *   [httpmock](https://github.com/alexliesenfeld/httpmock) — HTTP mocking [![build badge](https://camo.githubusercontent.com/59c305f8a1fbcb05815ac15858d5a19dfce2a1dcb40e034b04f01a2e4a230deb/68747470733a2f2f6465762e617a7572652e636f6d2f616c65786c696573656e66656c642f687474706d6f636b2f5f617069732f6275696c642f7374617475732f616c65786c696573656e66656c642e687474706d6f636b3f6272616e63684e616d653d6d6173746572)](https://dev.azure.com/alexliesenfeld/httpmock/_build/latest?definitionId=2&branchName=master)
    *   [mockiato](https://crates.io/crates/mockiato) — A strict, yet friendly mocking library for Rust 2018 [![build badge](https://camo.githubusercontent.com/5dca9a125b46b4ffa4e9f6a7f458595ba87b9a3dbcd00acb75e870ff2e05b1c3/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6d6f636b6961746f2f6d6f636b6961746f2e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/mockiato/mockiato)
    *   [mockito](https://crates.io/crates/mockito) — HTTP mocking [![build badge](https://camo.githubusercontent.com/61a12d6472bae797ef81bd4684d01bde008a16138b2b85a90fe79f31f8ac6617/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c6970616e736b692f6d6f636b69746f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lipanski/mockito)
    *   [nrxus/faux](https://github.com/nrxus/faux/) [![Latest Version](https://camo.githubusercontent.com/0d6b67c9b21d89e2d3a6c293c7399ae7bf84c867862db9ceefe7392693354602/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f666175782e737667)](https://crates.io/crates/faux) — A library to create mocks out of structs. [![build](https://github.com/nrxus/faux/workflows/test/badge.svg?branch=master)](https://github.com/nrxus/faux/workflows/test/badge.svg?branch=master)
*   Property Testing and Fuzzing
    *   [mutagen](https://github.com/llogiq/mutagen) \[[mutagen](https://crates.io/crates/mutagen)) — A source-level mutation testing framework (nightly only) [![build badge](https://camo.githubusercontent.com/12d2f836bb65739f9e170fd33d2af1ec987bec85ade4bf4f26b8fbcbe0b73a0d/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c6c6f6769712f6d75746167656e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/llogiq/mutagen)
    *   [proptest](https://crates.io/crates/proptest) — property testing framework inspired by the [Hypothesis](https://hypothesis.works/) framework for Python [![build badge](https://camo.githubusercontent.com/d102435f114aac92cfad73de69a2c451814dba5224b2046c68b5bcd1810bbddb/68747470733a2f2f6170692e7472617669732d63692e6f72672f616c7473797372712f70726f70746573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/altsysrq/proptest)
    *   [quickcheck](https://crates.io/crates/quickcheck) — A Rust implementation of [QuickCheck](https://wiki.haskell.org/Introduction_to_QuickCheck1) [![build badge](https://camo.githubusercontent.com/ecdd59235a39af8ad988e8a2aa83ba484654ccf897c05670aa2024bd77c1476f/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f717569636b636865636b2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/quickcheck)
    *   [rust-fuzz/afl.rs](https://github.com/rust-fuzz/afl.rs) — A Rust fuzzer, using [AFL](https://lcamtuf.coredump.cx/afl/) [![build badge](https://camo.githubusercontent.com/505c55a5aadf4b67ddf5e163b6a0efad6509d3f7083adce9d40e424301619dd5/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d66757a7a2f61666c2e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-fuzz/afl.rs)

### [](#transpiling)Transpiling

*   [BayesWitnesses/m2cgen](https://github.com/BayesWitnesses/m2cgen) — A CLI tool to transpile trained classic machine learning models into a native Rust code with zero dependencies. [![GitHub Actions Status](https://github.com/BayesWitnesses/m2cgen/workflows/GitHub%20Actions/badge.svg?branch=master)](https://github.com/BayesWitnesses/m2cgen/actions)
*   [immunant/c2rust](https://github.com/immunant/c2rust) — C to Rust translator and cross checker built atop Clang/LLVM. [![Build Status](https://camo.githubusercontent.com/c87c2eac3ebcdb2e8b1f92dd22c03bf72a5531f83824f7805636151266c5559a/68747470733a2f2f6170692e7472617669732d63692e6f72672f696d6d756e616e742f6332727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/immunant/c2rust)
*   [jameysharp/corrode](https://github.com/jameysharp/corrode) — A C to Rust translator written in Haskell.

[](#libraries)Libraries
-----------------------

*   [perf-monitor-rs](https://github.com/larksuite/perf-monitor-rs) — A toolkit designed to be a foundation for applications to monitor their performance. [![crates.io](https://camo.githubusercontent.com/316ba35db234698fcc0a9405441b889c30423127f87e8642df150ef4f42b8e16/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f706572665f6d6f6e69746f722e737667)](https://crates.io/crates/perf_monitor)
*   [Phate6660/nixinfo](https://github.com/Phate6660/nixinfo) \[[crate](https://crates.io/crates/nixinfo)\] — A lib crate for gathering system info such as cpu, distro, environment, kernel, etc.

### [](#artificial-intelligence)Artificial Intelligence

#### [](#genetic-algorithms)Genetic algorithms

*   [innoave/genevo](https://github.com/innoave/genevo) — Execute genetic algorithm (GA) simulations in a customizable and extensible way.
*   [m-decoster/RsGenetic](https://github.com/m-decoster/RsGenetic) — Genetic Algorithm library in Rust. In maintenance mode.
*   [Martin1887/oxigen](https://github.com/Martin1887/oxigen) — Fast, parallel, extensible and adaptable genetic algorithm library. A example using this library solves the N Queens problem for N = 255 in only few seconds and using less than 1 MB of RAM.
*   [pkalivas/radiate](https://github.com/pkalivas/radiate) — A customizable parallel genetic programming engine capable of evolving solutions for supervised, unsupervised, and reinforcement learning problems. Comes with complete and customizable implementation of NEAT and Evtree. [![Build Status](https://camo.githubusercontent.com/a58ffd66448e3b3010d9ffb63b4f9a657cca9fcb074b0a426f4e3a771514ca46/68747470733a2f2f6170692e7472617669732d63692e636f6d2f706b616c697661732f726164696174652e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/pkalivas/radiate)[![Crates.io](https://camo.githubusercontent.com/e499fe8fbd874858dcec4813d4ede64f34fe1768231c760a4086aac397a2df6c/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f72616469617465)](https://camo.githubusercontent.com/e499fe8fbd874858dcec4813d4ede64f34fe1768231c760a4086aac397a2df6c/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f72616469617465)
*   [willi-kappler/darwin-rs](https://github.com/willi-kappler/darwin-rs) — Evolutionary algorithms with Rust [![Build Status](https://camo.githubusercontent.com/c1bd9a141825a17f00c2cf8e0f25a27cbd0e16f322e4f5636c17d9e49293d461/68747470733a2f2f6170692e7472617669732d63692e6f72672f77696c6c692d6b6170706c65722f64617277696e2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/willi-kappler/darwin-rs)

#### [](#machine-learning)Machine learning

See \[[Machine learning](https://crates.io/keywords/machine-learning)\]

See also [About Rust’s Machine Learning Community](https://medium.com/@autumn_eng/about-rust-s-machine-learning-community-4cda5ec8a790#.hvkp56j3f) and [Are we learning yet?](https://www.arewelearningyet.com).

*   [AtheMathmo/rusty-machine](https://github.com/AtheMathmo/rusty-machine) — Machine learning library for Rust [![Build Status](https://camo.githubusercontent.com/f701f9dedcab72df5083a9fa0a8918c9ae303b7dad6b8db4a97cf903aa0f4fc8/68747470733a2f2f6170692e7472617669732d63692e6f72672f417468654d6174686d6f2f72757374792d6d616368696e652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/AtheMathmo/rusty-machine)
*   [autumnai/leaf](https://github.com/autumnai/leaf) — Open Machine Intelligence framework. [![Build Status](https://camo.githubusercontent.com/53f03d0c2c15925a79e478ab89d41abf8deab0de3afe4edf64643d512579eb1b/68747470733a2f2f6170692e7472617669732d63692e6f72672f617574756d6e61692f6c6561662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/autumnai/leaf). Abandoned project. The most updated fork is [spearow/juice](https://github.com/spearow/juice).
*   [huggingface/tokenizers](https://github.com/huggingface/tokenizers) - Hugging Face's tokenizers for modern NLP pipelines written in Rust (original implementation) with bindings for Python. [![Build Status](https://github.com/huggingface/tokenizers/workflows/Rust/badge.svg?branch=master)](https://github.com/huggingface/tokenizers/actions)
*   [LaurentMazare/tch-rs](https://github.com/LaurentMazare/tch-rs) — Rust language bindings for PyTorch. [![Build Status](https://camo.githubusercontent.com/95325bef93d0fad4f718044cb01f6b26250153f357c7b111a238d39adcb48b31/68747470733a2f2f6170692e7472617669732d63692e6f72672f4c617572656e744d617a6172652f7463682d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/LaurentMazare/tch-rs)
*   [maciejkula/rustlearn](https://github.com/maciejkula/rustlearn) — Machine learning crate for Rust. [![Circle CI](https://camo.githubusercontent.com/6ac50db599f482155df4c3fe8ba3fe5f9655c60bde581a9d327b1c7239bd8298/68747470733a2f2f636972636c6563692e636f6d2f67682f6d616369656a6b756c612f727573746c6561726e2e7376673f7374796c653d737667)](https://app.circleci.com/pipelines/github/maciejkula/rustlearn)
*   [rust-ml/linfa](https://github.com/rust-ml/linfa) — Machine learning framework.
*   [smartcorelib/smartcore](https://github.com/smartcorelib/smartcore) — Machine Learning Library In Rust [![Build Status](https://camo.githubusercontent.com/ecfeaa56a7ef7903478c85db42a856f428d1d9ae2efe431209fe98c24f2f7665/68747470733a2f2f696d672e736869656c64732e696f2f636972636c6563692f6275696c642f6769746875622f736d617274636f72656c69622f736d617274636f7265)](https://smartcorelib.org/)
*   [tensorflow/rust](https://github.com/tensorflow/rust) — Rust language bindings for TensorFlow. [![Build Status](https://camo.githubusercontent.com/fe26543530e36f259a01bd985de095572136999d6107d9aa270b50e198f4567f/68747470733a2f2f6170692e7472617669732d63692e6f72672f74656e736f72666c6f772f727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tensorflow/rust)

### [](#astronomy)Astronomy

\[[astronomy](https://crates.io/keywords/astronomy)\]

*   [fitsio](https://crates.io/crates/fitsio) — fits interface library wrapping cfitsio [![build badge](https://camo.githubusercontent.com/7dc8a1e7ef801b157731b04006c16d8e149bcda40bc67cd7cbbfb84c083b2ece/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d696e6472696f743130312f727573742d66697473696f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mindriot101/rust-fitsio)
*   [flosse/rust-sun](https://github.com/flosse/rust-sun) \[[sun](https://crates.io/crates/sun)\] — A rust port of the JS library suncalc [![build badge](https://camo.githubusercontent.com/e6a1ab7655c8b51edccae1e1171ee29d0866761647871833c2140cd12a458bd2/68747470733a2f2f6170692e7472617669732d63692e6f72672f666c6f7373652f727573742d73756e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/flosse/rust-sun)
*   [saurvs/astro-rust](https://github.com/saurvs/astro-rust) — astronomy for Rust [![build badge](https://camo.githubusercontent.com/6aa44762a00fbb7464df09d1b871cc8c603eb656b511fa2063babd09ce4c37e3/68747470733a2f2f6170692e7472617669732d63692e6f72672f7361757276732f617374726f2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/saurvs/astro-rust)

### [](#asynchronous)Asynchronous

*   [async-std](https://async.rs/) [\[async-std\]](https://crates.io/crates/async-std) - Async version of the Rust standard library [![CI](https://github.com/async-rs/async-std/actions/workflows/ci.yml/badge.svg?branch=master)](https://github.com/async-rs/async-std/actions/workflows/ci.yml)
*   [dpc/mioco](https://github.com/dpc/mioco) — Scalable, coroutine-based, asynchronous IO handling library [![build badge](https://camo.githubusercontent.com/0f22dde75d27dec5913e732a570496db32257f5e9ea42d4afd2c0671f0ed6de9/68747470733a2f2f6170692e7472617669732d63692e6f72672f6470632f6d696f636f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/dpc/mioco)
*   [mio](https://github.com/tokio-rs/mio) — MIO is a lightweight IO library for Rust with a focus on adding as little overhead as possible over the OS abstractions [![build badge](https://camo.githubusercontent.com/2cfcfc2698cdc595eb6d0456f79210b4dc886e09ec548d80d408184898dc22fa/68747470733a2f2f6170692e7472617669732d63692e6f72672f746f6b696f2d72732f6d696f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tokio-rs/mio)
*   [rust-lang/futures-rs](https://github.com/rust-lang/futures-rs) — Zero-cost futures in Rust [![build badge](https://camo.githubusercontent.com/b1cc4a9ed4c23baadb6ea4bc776541f5fc21969600d42e0b2a2ad573c06a24b4/68747470733a2f2f6170692e7472617669732d63692e636f6d2f727573742d6c616e672f667574757265732d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-lang/futures-rs)
*   [TeaEntityLab/fpRust](https://github.com/TeaEntityLab/fpRust) — Monad/MonadIO, Handler, Coroutine/doNotation, Functional Programming features for Rust [![build badge](https://camo.githubusercontent.com/031cc50d04db67f12b9324a1cf72ed1b721ae491f0faa85f27871df7a019de9e/68747470733a2f2f6170692e7472617669732d63692e6f72672f546561456e746974794c61622f6670527573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/TeaEntityLab/fpRust)
*   [Xudong-Huang/may](https://github.com/Xudong-Huang/may) — rust stackful coroutine library [![build badge](https://camo.githubusercontent.com/750c3f474c73b5e8fed749b7c3a16987bc78156cda509f6c50f5233659c8b3ba/68747470733a2f2f6170692e7472617669732d63692e6f72672f5875646f6e672d4875616e672f6d61792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Xudong-Huang/may)
*   [zonyitoo/coio-rs](https://github.com/zonyitoo/coio-rs) — A coroutine I/O library with a working-stealing scheduler [![build badge](https://camo.githubusercontent.com/d6d128e57e79b5c547de9de0433fbdaba73821a0726c4113d70c44b7eeb40fd7/68747470733a2f2f6170692e7472617669732d63692e6f72672f7a6f6e7969746f6f2f636f696f2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/zonyitoo/coio-rs)

### [](#audio-and-music-1)Audio and Music

\[[audio](https://crates.io/keywords/audio)\]

*   [hound](https://crates.io/crates/hound) — A WAV encoding and decoding library [![build badge](https://camo.githubusercontent.com/6f2c02ec19d57973d9b107714fa91384f102277a7e0ea765a367b92082b26652/68747470733a2f2f6170692e7472617669732d63692e6f72672f72757564612f686f756e642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ruuda/hound)
*   [jhasse/ears](https://github.com/jhasse/ears) — A simple library to play Sounds and Musics, on top of OpenAL and libsndfile [![build badge](https://camo.githubusercontent.com/01774606690590925595e74b6e8ca6aa06e555f3378c25cf6bad9bcaef94bedd/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a68617373652f656172732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jhasse/ears)
*   [jpernst/alto](https://github.com/jpernst/alto) — OpenAL 1.1 bindings [![build badge](https://camo.githubusercontent.com/bdd7d66c6c65f3c99bcd0f23bf224057bf152f37c2b494d4649c5be237be1141/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a7065726e73742f616c746f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jpernst/alto)
*   [musitdev/portmidi-rs](https://github.com/musitdev/portmidi-rs) — [PortMidi](http://portmedia.sourceforge.net/portmidi/) bindings [![build badge](https://camo.githubusercontent.com/d0faf89734ca9dfcd8882c9b59b58f828aba8d7e8004e1b6292ce4b8662b4ab0/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d757369746465762f706f72746d6964692d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/musitdev/portmidi-rs)
*   [ozankasikci/rust-music-theory](https://github.com/ozankasikci/rust-music-theory) — A Rust music theory library [![Build Status](https://camo.githubusercontent.com/83b818e0d860d76806d55043dc3f6706f020c83e15994c85c0d722eafe7a6b10/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6f7a616e6b6173696b63692f727573742d6d757369632d7468656f72792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ozankasikci/rust-music-theory)
*   [pdeljanov/Symphonia](https://github.com/pdeljanov/Symphonia) — A pure Rust audio decoding and media demuxing library supporting AAC, FLAC, MP3, MP4, OGG, Vorbis, and WAV.
*   [RustAudio](https://github.com/RustAudio)
    *   [RustAudio/cpal](https://github.com/RustAudio/cpal) - Low-level cross-platform audio I/O library in pure Rust. [![Actions Status](https://github.com/RustAudio/cpal/workflows/cpal/badge.svg?branch=master)](https://github.com/RustAudio/cpal/actions)
    *   [RustAudio/rodio](https://github.com/RustAudio/rodio) — A Rust audio playback library [![Build Status](https://camo.githubusercontent.com/ae7ba7bb8e522b26681b24b7079b5c7949db19c453fb62bbdf5ee1b08b69b904/68747470733a2f2f6170692e7472617669732d63692e6f72672f52757374417564696f2f726f64696f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/RustAudio/rodio)
    *   [RustAudio/rust-portaudio](https://github.com/RustAudio/rust-portaudio) — [PortAudio](http://www.portaudio.com/) bindings [![build badge](https://camo.githubusercontent.com/f2836571e7287de5c3b1e9966760335c3fe0e8fd46374fcb245b867ea7347c3a/68747470733a2f2f6170692e7472617669732d63692e6f72672f52757374417564696f2f727573742d706f7274617564696f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/RustAudio/rust-portaudio)

### [](#authentication)Authentication

*   [Keats/jsonwebtoken](https://github.com/Keats/jsonwebtoken) — [JSON Web Token](https://en.wikipedia.org/wiki/JSON_Web_Token) lib in rust [![Build Status](https://camo.githubusercontent.com/e38846d0efe48206614a971785ade27c931cea3552c0870444945d0616a9bee5/68747470733a2f2f6170692e7472617669732d63692e6f72672f4b656174732f6a736f6e776562746f6b656e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Keats/jsonwebtoken)
*   [oauth2](https://github.com/ramosbugs/oauth2-rs) — Extensible, strongly-typed Rust OAuth2 client library [![Build Status](https://camo.githubusercontent.com/39bf72552ca5955fb9a5f98e58f328f5870d7252dd71024f3b2a1ddf842509db/68747470733a2f2f6170692e7472617669732d63692e6f72672f72616d6f73627567732f6f61757468322d72732e7376673f6272616e63683d6d61696e)](https://travis-ci.org/ramosbugs/oauth2-rs)
*   [oxide-auth](https://github.com/HeroicKatora/oxide-auth) — A OAuth2 server library, for use in combination with actix or other frontends, featuring a set of configurable and pluggable backends [![Build Status](https://camo.githubusercontent.com/277515d6f94613a5c858720366f44afca2a91af9c36ec83b55d15b7eaaba272b/68747470733a2f2f6170692e6369727275732d63692e636f6d2f6769746875622f4865726f69634b61746f72612f6f786964652d617574682e7376673f6272616e63683d6d6173746572)](https://cirrus-ci.com/github/HeroicKatora/oxide-auth)
*   [sgrust01/jwtvault](https://github.com/sgrust01/jwtvault) — Async library to manage and orchestrate JWT workflow [![Build Status](https://camo.githubusercontent.com/80826c5b60e15bcef23adfa5afb27ca3d28358ed46ce805c0e2ee9059557fc3f/68747470733a2f2f6170692e7472617669732d63692e6f72672f73677275737430312f6a77747661756c742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sgrust01/jwtvault)
*   [yup-oauth2](https://github.com/dermesser/yup-oauth2) — An oauth2 client implementation providing the Device, Installed and Service Account flows [![Build Status](https://camo.githubusercontent.com/9ce3df91f54f0661b9d6e582ea707fcec4cebd5404a6be9d1bd6bc3ac8da45d9/68747470733a2f2f6170692e7472617669732d63692e6f72672f6465726d65737365722f7975702d6f61757468322e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/dermesser/yup-oauth2)

### [](#automotive)Automotive

*   [marcelbuesing/can-dbc](https://github.com/marcelbuesing/can-dbc) \[[can-dbc](https://crates.io/crates/can-dbc)\] — A parser for the DBC format [![build badge](https://camo.githubusercontent.com/73fd5fb927777ed2412caaad5c99e01a6183a5c857faf80134f238942335b601/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d617263656c62756573696e672f63616e2d6462632e7376673f6272616e63683d646576)](https://travis-ci.org/marcelbuesing/can-dbc)
*   [marcelbuesing/tokio-socketcan-bcm](https://github.com/marcelbuesing/tokio-socketcan-bcm) \[[tokio-socketcan-bcm](https://crates.io/crates/tokio-socketcan-bcm)\] — Linux SocketCAN BCM support for tokio [![build badge](https://camo.githubusercontent.com/430e1de579d3dd18fc1e3c3f8deed1895383892b18cd603c697c06fd9bac7a5c/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d617263656c62756573696e672f746f6b696f2d736f636b657463616e2d62636d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/marcelbuesing/tokio-socketcan-bcm)
*   [mbr/socketcan](https://github.com/mbr/socketcan-rs) \[[socketcan](https://crates.io/crates/socketcan)\] — Linux SocketCAN library [![build badge](https://camo.githubusercontent.com/02516fead19728679fe1779665f7c10d20cd7a5bb4c3c492a1fb46eafeb33f27/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d62722f736f636b657463616e2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mbr/socketcan-rs)
*   [oefd/tokio-socketcan](https://github.com/oefd/tokio-socketcan) [\[tokio-socketcan\]](https://crates.io/crates/tokio-socketcan)\] — Linux SocketCAN support for tokio based on the socketcan crate
*   [Sensirion/lin-bus](https://github.com/Sensirion/lin-bus-rs) \[[lin-bus](https://crates.io/crates/lin-bus)\] — LIN bus driver traits and protocol implementation [![build badge](https://camo.githubusercontent.com/753d2a0494bedeffeaf75ab01068692e00167fbe3ac51a41db2fbaaf80c8a756/68747470733a2f2f636972636c6563692e636f6d2f67682f53656e736972696f6e2f6c696e2d6275732d72732e7376673f7374796c653d737667)](https://app.circleci.com/pipelines/github/Sensirion/lin-bus-rs)

### [](#bioinformatics)Bioinformatics

*   [Rust-Bio](https://github.com/rust-bio) — bioinformatics libraries in Rust.

### [](#caching)Caching

*   [aisk/rust-memcache](https://github.com/aisk/rust-memcache) — Memcached client library [![build badge](https://camo.githubusercontent.com/d88350b98d00027d9e339a261a4db2bdf98c19f734c9bbf5b8e9becd46b76a33/68747470733a2f2f6170692e7472617669732d63692e6f72672f6169736b2f727573742d6d656d63616368652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/aisk/rust-memcache)
*   [al8n/stretto](https://github.com/al8n/stretto) - A high performance thread-safe memory-bound Rust cache [![build badge](https://github.com/al8n/stretto/actions/workflows/ci.yml/badge.svg)](https://github.com/al8n/stretto/actions/workflows/ci.yml)
*   [jaemk/cached](https://github.com/jaemk/cached) — Simple function caching/memoization
*   [jaysonsantos/bmemcached-rs](https://github.com/jaysonsantos/bmemcached-rs) \[[bmemcached](https://crates.io/crates/bmemcached)\] — Memcached library written in pure rust [![build badge](https://camo.githubusercontent.com/5ab6f78b5a96f9ff04532eafae2f8705cc6da0df4b52326c5a13eca693be42de/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a6179736f6e73616e746f732f626d656d6361636865642d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jaysonsantos/bmemcached-rs)
*   [mozilla/sccache](https://github.com/mozilla/sccache/) - Shared Compilation Cache, great for Rust compilation [![build badge](https://camo.githubusercontent.com/c4ad93635ed662a926a69ff91c5eba16735a7f5f5b55758a1d45927ee89c5e7b/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6f7a696c6c612f736363616368652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mozilla/sccache)

### [](#concurrency)Concurrency

*   [crossbeam-rs/crossbeam](https://github.com/crossbeam-rs/crossbeam) – Support for parallelism and low-level concurrency in Rust [![build badge](https://camo.githubusercontent.com/08dab90a9aa7f23c431ef07f6ceb7d8d7d7f592d9f56ec0d0c699728141c3393/68747470733a2f2f6170692e7472617669732d63692e6f72672f63726f73736265616d2d72732f63726f73736265616d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/crossbeam-rs/crossbeam)
*   [orium/archery](https://github.com/orium/archery) \[[archery](https://crates.io/crates/archery)\] — Library to abstract from `Rc`/`Arc` pointer types. [![build badge](https://camo.githubusercontent.com/2f756237c4285ec2b2d2e8661cbc66e6a2f18edddc482d529b98d6d9d925103d/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f7269756d2f617263686572792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/orium/archery)
*   [Rayon](https://github.com/rayon-rs/rayon) – A data parallelism library for Rust [![build badge](https://camo.githubusercontent.com/483e73c2a6471a0ba8f1f9af93b2b9fa48622c5a303852d38cab998a069fe4bd/68747470733a2f2f6170692e7472617669732d63692e6f72672f7261796f6e2d72732f7261796f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rayon-rs/rayon)
*   [rustcc/coroutine-rs](https://github.com/rustcc/coroutine-rs) – Coroutine Library in Rust [![build badge](https://camo.githubusercontent.com/271017c80453a81a95a4600e7106b74fa0ed91141974dfe226aa3048bbf636ee/68747470733a2f2f6170692e7472617669732d63692e6f72672f7275737463632f636f726f7574696e652d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rustcc/coroutine-rs)
*   [zonyitoo/coio-rs](https://github.com/zonyitoo/coio-rs) – Coroutine I/O for Rust [![build badge](https://camo.githubusercontent.com/d6d128e57e79b5c547de9de0433fbdaba73821a0726c4113d70c44b7eeb40fd7/68747470733a2f2f6170692e7472617669732d63692e6f72672f7a6f6e7969746f6f2f636f696f2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/zonyitoo/coio-rs)

### [](#cloud)Cloud

*   AWS \[[aws](https://crates.io/keywords/aws)\]
    *   [awslabs/aws-lambda-rust-runtime](https://github.com/awslabs/aws-lambda-rust-runtime) \[[lambda\_runtime](https://crates.io/crates/lambda_runtime)\] — A Rust runtime for AWS Lambda [![build badge](https://github.com/awslabs/aws-lambda-rust-runtime/workflows/Rust/badge.svg)](https://github.com/awslabs/aws-lambda-rust-runtime/actions)
    *   [rusoto/rusoto](https://github.com/rusoto/rusoto) — [![build badge](https://camo.githubusercontent.com/b0abf45a3f6a7bc75337dc059bfedb99c352ec1d543199e18ca27fb50c1db905/68747470733a2f2f6170692e7472617669732d63692e6f72672f7275736f746f2f7275736f746f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rusoto/rusoto)
*   Load Balancer
    *   [Convey](https://github.com/bparli/convey) - Layer 4 Load Balancer with dynamic configuration loading.

### [](#command-line)Command-line

*   Argument parsing
    *   [clap-rs](https://github.com/clap-rs/clap) \[[clap](https://crates.io/crates/clap)\] — A simple to use, full featured command-line argument parser [![build badge](https://camo.githubusercontent.com/38700b50e0d9ef4aff5b91e8ee7873d4655e5499b6f96b7f16978e6d448d7def/68747470733a2f2f6170692e7472617669732d63692e6f72672f636c61702d72732f636c61702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/clap-rs/clap)
    *   [docopt/docopt.rs](https://github.com/docopt/docopt.rs) \[[docopt](https://crates.io/crates/docopt)\] — A Rust implementation of [DocOpt](http://docopt.org) [![build badge](https://camo.githubusercontent.com/5138b0312f82fef5ed890e15282bcaa2f321b4f3d7aa337df6e805c8857dc58c/68747470733a2f2f6170692e7472617669732d63692e6f72672f646f636f70742f646f636f70742e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/docopt/docopt.rs)
    *   [google/argh](https://github.com/google/argh) \[[argh](https://crates.io/crates/argh)\] — An opinionated Derive-based argument parser optimized for code size [![build badge](https://github.com/google/argh/workflows/Argh/badge.svg?branch=master)](https://github.com/google/argh/actions)
    *   [killercup/quicli](https://github.com/killercup/quicli) \[[quicli](https://crates.io/crates/quicli)\] — quickly build cool CLI apps in Rust [![build badge](https://camo.githubusercontent.com/3f940135adaaed45c96ad27bc41e3c0e57664c66b040b5344085d9bfeaf4e1c2/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b696c6c65726375702f717569636c692e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/killercup/quicli)
    *   [ksk001100/seahorse](https://github.com/ksk001100/seahorse) \[[seahorse](https://crates.io/crates/seahorse)\] — A minimal CLI framework written in Rust [![Build status](https://github.com/ksk001100/seahorse/workflows/CI/badge.svg?branch=master)](https://github.com/ksk001100/seahorse/actions)
    *   [TeXitoi/structopt](https://github.com/TeXitoi/structopt) \[[structopt](https://crates.io/crates/structopt)\] — parse command line argument by defining a struct [![build badge](https://camo.githubusercontent.com/75e2601942408a88ed54da48bf760197c68b69d61acb8992e2ccebc52f00a9bc/68747470733a2f2f6170692e7472617669732d63692e6f72672f54655869746f692f7374727563746f70742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/TeXitoi/structopt)
*   Data visualization
    *   [nukesor/comfy-table](https://github.com/nukesor/comfy-table) \[[comfy-table](https://crates.io/crates/comfy-table)\] — Beautiful dynamic tables for your cli tools. [![Build status](https://github.com/Nukesor/comfy-table/workflows/Tests/badge.svg?branch=master)](https://github.com/nukesor/comfy-table/actions)
    *   [zhiburt/tabled](https://github.com/zhiburt/tabled) \[[tabled](https://crates.io/crates/tabled)\] — An easy to use library for pretty print tables of Rust structs and enums. [![Build Status](https://github.com/zhiburt/tabled/actions/workflows/ci.yml/badge.svg)](https://github.com/zhiburt/tabled/actions)
*   Human-centered design
    *   [rust-cli/human-panic](https://github.com/rust-cli/human-panic) \[[human-panic](https://crates.io/crates/human-panic)\] — panic messages for humans [![build badge](https://camo.githubusercontent.com/69742ec39bdbcf8b4b0358278e953f35a5c5b00a81acfa36d3fd0dc2f12c01ac/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d636c692f68756d616e2d70616e69632e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-cli/human-panic)
*   Line editor
    *   [kkawakam/rustyline](https://github.com/kkawakam/rustyline) \[[rustyline](https://crates.io/crates/rustyline)\] — readline implementation in Rust [![build badge](https://camo.githubusercontent.com/35bd9dac59f94e89d5af8c9e0769dc11ff0ace3040ee833d060dcc8609c22dac/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b6b6177616b616d2f72757374796c696e652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kkawakam/rustyline)
    *   [MovingtoMars/liner](https://github.com/MovingtoMars/liner) \[[liner](https://crates.io/crates/liner)\] — A library offering readline-like functionality [![build badge](https://camo.githubusercontent.com/d0d50d0c0313b8c3b30405860ea2ec3234f19b8c26e5204585ea455aed111df4/68747470733a2f2f6170692e7472617669732d63692e6f72672f4d6f76696e67746f4d6172732f6c696e65722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/MovingtoMars/liner)
    *   [murarth/linefeed](https://github.com/murarth/linefeed) \[[linefeed](https://crates.io/crates/linefeed)\] — Configurable, extensible, interactive line reader [![build badge](https://camo.githubusercontent.com/19836fae33fdf83ce5556cf5b3863f33e15e5f99e6731c0a30377027aeaef82a/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d7572617274682f6c696e65666565642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/murarth/linefeed)
    *   [srijs/rust-copperline](https://github.com/srijs/rust-copperline) \[[copperline](https://crates.io/crates/copperline)\] — pure-Rust command line editing library
*   Pipeline
    *   [hniksic/rust-subprocess](https://github.com/hniksic/rust-subprocess) \[[subprocess](https://crates.io/crates/subprocess)\] — facilities for interaction with external pipelines [![build badge](https://camo.githubusercontent.com/7c45d8970a70e803b277d1a6a569f7eb3ae5fabf7821a1b147abf6c8dd057425/68747470733a2f2f6170692e7472617669732d63692e6f72672f686e696b7369632f727573742d73756270726f636573732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/hniksic/rust-subprocess)
    *   [imp/pager-rs](https://gitlab.com/imp/pager-rs) \[[pager](https://crates.io/crates/pager)\] — pipe your output through an external pager
    *   [oconnor663/duct.rs](https://github.com/oconnor663/duct.rs) \[[duct](https://crates.io/crates/duct)\] — A builder for subprocess pipelines and IO redirection [![build badge](https://camo.githubusercontent.com/7e968e7ef6d333df89ce9f02d563f60dc271051823fbb89694df5cd7184a3d0d/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f636f6e6e6f723636332f647563742e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/oconnor663/duct.rs)
    *   [philippkeller/rexpect](https://github.com/philippkeller/rexpect) \[[rexpect](https://crates.io/crates/rexpect)\] — automate interactive applications such as ssh, ftp, passwd, etc [![build badge](https://camo.githubusercontent.com/83719123dfaed2062bd76a9fe870fffebe6d344fd2279a61c87b3f1f689039b1/68747470733a2f2f6170692e7472617669732d63692e6f72672f7068696c6970706b656c6c65722f726578706563742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/philippkeller/rexpect)
*   Progress
    *   [a8m/pb](https://github.com/a8m/pb) \[[pbr](https://crates.io/crates/pbr)\] — console progress bar for Rust
    *   [console-rs/indicatif](https://github.com/console-rs/indicatif) \[[indicatif](https://crates.io/crates/indicatif)\] — indicate progress to users
    *   [FGRibreau/spinners](https://github.com/FGRibreau/spinners) \[[spinners](https://crates.io/crates/spinners)\] — 60+ elegant terminal spinners
*   Prompt
    *   [hashmismatch/terminal\_cli.rs](https://github.com/hashmismatch/terminal_cli.rs) \[[terminal\_cli](https://crates.io/crates/terminal_cli)\] — build an interactive command prompt [![build badge](https://camo.githubusercontent.com/7f9304336cd76e466776492671d2222022973593be91adb76c34dea364555b09/68747470733a2f2f6170692e7472617669732d63692e6f72672f686173686d69736d617463682f7465726d696e616c5f636c692e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/hashmismatch/terminal_cli.rs)
    *   [starship/starship](https://starship.rs/) \[[starship](https://crates.io/crates/starship)\] — A minimal, blazing fast, and extremely customizable prompt for any shell [![Build status](https://github.com/starship/starship/workflows/Main%20workflow/badge.svg?branch=master)](https://github.com/starship/starship/actions)
*   Style
    *   [LukasKalbertodt/bunt](https://github.com/LukasKalbertodt/bunt) \[[bunt](https://crates.io/crates/bunt)\] — cross-platform terminal colors and styling with macros [![Build status](https://github.com/LukasKalbertodt/bunt/actions/workflows/ci.yml/badge.svg)](https://github.com/LukasKalbertodt/bunt/actions?query=workflow%3ACI+branch%3Amaster)
    *   [LukasKalbertodt/term-painter](https://github.com/LukasKalbertodt/term-painter) \[[term-painter](https://crates.io/crates/term-painter)\] — cross-platform styled terminal output [![build badge](https://camo.githubusercontent.com/1901fe42f6d1aa561dd979598e7633985d614d2e3f279be462f0bf58a0c23ffd/68747470733a2f2f6170692e7472617669732d63692e6f72672f4c756b61734b616c626572746f64742f7465726d2d7061696e7465722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/LukasKalbertodt/term-painter)
    *   [mackwic/colored](https://github.com/mackwic/colored) \[[colored](https://crates.io/crates/colored)\] — Coloring terminal so simple, you already know how to do it!
    *   [ogham/rust-ansi-term](https://github.com/ogham/rust-ansi-term) \[[ansi\_term](https://crates.io/crates/ansi_term)\] — control colours and formatting on ANSI terminals [![build badge](https://camo.githubusercontent.com/b5479b2efcf09fdc4b487435edf8ab8e3de412b3cb6e9489c17895ab4353f49b/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f6768616d2f727573742d616e73692d7465726d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ogham/rust-ansi-term)
    *   [SergioBenitez/yansi](https://github.com/SergioBenitez/yansi) \[[yansi](https://crates.io/crates/yansi)\] — A dead simple ANSI terminal color painting library
*   TUI
    *   BearLibTerminal
        *   [cfyzium/bearlibterminal](https://github.com/nabijaczleweli/BearLibTerminal.rs) \[[bear-lib-terminal](https://crates.io/crates/bear-lib-terminal)\] — [BearLibTerminal](https://github.com/tommyettinger/BearLibTerminal) bindings [![build badge](https://camo.githubusercontent.com/338153a7c9db22c027852b846e5b94d89d0e43363c9566d0bcdce116ed3534fa/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e6162696a61637a6c6577656c692f426561724c69625465726d696e616c2e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/nabijaczleweli/BearLibTerminal.rs)
    *   [fdehau/tui-rs](https://github.com/fdehau/tui-rs) \[[tui](https://crates.io/crates/tui)\] — A TUI library inspired by [blessed-contrib](https://github.com/yaronn/blessed-contrib) and [termui](https://github.com/gizak/termui) [![build badge](https://camo.githubusercontent.com/2ac798638715bc7623d63e14d94b49687c2c9762e792535feed312d888561dc8/68747470733a2f2f6170692e7472617669732d63692e6f72672f6664656861752f7475692d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/fdehau/tui-rs)
    *   [gyscos/Cursive](https://github.com/gyscos/Cursive) \[[cursive](https://crates.io/crates/cursive)\] — build rich TUI applications [![build badge](https://camo.githubusercontent.com/caee0b5e61e8d132d860683eb96439f09d5cd286f10637aaa1b1af0af9f6b689/68747470733a2f2f6170692e7472617669732d63692e6f72672f677973636f732f437572736976652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/gyscos/Cursive)
    *   [ivanceras/titik](https://github.com/ivanceras/titik) - a crossplatform TUI widget library with the goal of providing interactive widgets [![Build Status](https://camo.githubusercontent.com/11519a90bdff5a812832a0d95d0ef63499eab8a9690a663705ac4f1835f562f7/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6976616e63657261732f746974696b2e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/ivanceras/titik)
    *   ncurses
        *   [ihalila/pancurses](https://github.com/ihalila/pancurses) \[[pancurses](https://crates.io/crates/pancurses)\] — curses library, supports linux and windows [![build badge](https://camo.githubusercontent.com/05ef8c72b7497eb4d9ce4c9c73d4b11dc2763038f659f843a069e58394916466/68747470733a2f2f6170692e7472617669732d63692e6f72672f6968616c696c612f70616e6375727365732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ihalila/pancurses)
        *   [jeaye/ncurses-rs](https://github.com/jeaye/ncurses-rs) \[[ncurses](https://crates.io/crates/ncurses)\] — [ncurses](https://www.gnu.org/software/ncurses/) bindings [![build badge](https://camo.githubusercontent.com/f5166075f58d1f3b8224c7b4ba9004474b2741a7adbb355e4ecf8d2c4d0c2226/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a656179652f6e6375727365732d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jeaye/ncurses-rs)
    *   [ogham/rust-term-grid](https://github.com/ogham/rust-term-grid) \[[term\_grid](https://crates.io/crates/term_grid)\] — Rust library for putting things in a grid [![build badge](https://camo.githubusercontent.com/017604f5be2bf9314855731b691d0518795ea7c5d5b645bcc63bc7b8f8caae7e/68747470733a2f2f6170692e7472617669732d63692e6f72672f6f6768616d2f727573742d7465726d2d677269642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ogham/rust-term-grid)
    *   [redox-os/termion](https://github.com/redox-os/termion) \[[termion](https://crates.io/crates/termion)\] — bindless library for controlling terminals/TTY [![build badge](https://camo.githubusercontent.com/b8cd5ba85dcb7384db940a123d76e0beb09c28c6995eeb434697f5e4907c0755/68747470733a2f2f6170692e7472617669732d63692e6f72672f7265646f782d6f732f7465726d696f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/redox-os/termion)
    *   Termbox
        *   [gchp/rustbox](https://github.com/gchp/rustbox) \[[rustbox](https://crates.io/crates/rustbox)\] — bindings to [Termbox](https://github.com/nsf/termbox) [![build badge](https://camo.githubusercontent.com/c4207583793eabecd8dc9c40d912c993eceeb4e9bc3bba7d76a404f442de9fb9/68747470733a2f2f6170692e7472617669732d63692e6f72672f676368702f72757374626f782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/gchp/rustbox)
    *   [TimonPost/crossterm](https://github.com/crossterm-rs/crossterm) \[[crossterm](https://crates.io/crates/crossterm)\] — crossplatform terminal library

### [](#compression)Compression

*   [Brotli](https://opensource.googleblog.com/2015/09/introducing-brotli-new-compression.html)
    *   [dropbox/rust-brotli](https://github.com/dropbox/rust-brotli) — Brotli decompressor in Rust that optionally avoids the stdlib
    *   [ende76/brotli-rs](https://github.com/ende76/brotli-rs) — implementation of Brotli compression
*   bzip2
    *   [alexcrichton/bzip2-rs](https://github.com/alexcrichton/bzip2-rs) — [libbz2](https://www.sourceware.org/bzip2/) bindings [![build badge](https://camo.githubusercontent.com/8f4233b3cf938308119f8095f4d091dc74df142b8cf7ce31d6a0a308a586f70a/68747470733a2f2f6170692e7472617669732d63692e636f6d2f616c65786372696368746f6e2f627a6970322d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/alexcrichton/bzip2-rs)
*   gzip
    *   [carols10cents/zopfli](https://github.com/carols10cents/zopfli) — implementation of the [Zopfli](https://github.com/google/zopfli) compression algorithm for higher quality deflate or zlib compression
*   gzp
    *   [sstadick/gzp](https://github.com/sstadick/gzp/) - multi-threaded encoding and decoding of deflate formats and snappy
*   miniz
    *   [rust-lang/flate2-rs](https://github.com/rust-lang/flate2-rs) — [miniz](https://code.google.com/archive/p/miniz) bindings [![build badge](https://github.com/rust-lang/flate2-rs/workflows/CI/badge.svg?branch=master)](https://github.com/rust-lang/flate2-rs/actions)
*   snappy
    *   [JeffBelgum/rust-snappy](https://github.com/JeffBelgum/rust-snappy) — [snappy](https://github.com/google/snappy) bindings [![build badge](https://camo.githubusercontent.com/fc0171dd32aee9ca7354f9172f0d95bee0269356c1fbcac2eb6c62e21bbca0b8/68747470733a2f2f6170692e7472617669732d63692e6f72672f4a65666642656c67756d2f727573742d736e617070792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/JeffBelgum/rust-snappy)
*   tar
    *   [alexcrichton/tar-rs](https://github.com/alexcrichton/tar-rs) — tar archive reading/writing in Rust [![build badge](https://camo.githubusercontent.com/52b435d83463bdb952a13d9f46e8c624cdfc4c03e314bc4a2fcf92f70054d9e0/68747470733a2f2f6170692e7472617669732d63692e636f6d2f616c65786372696368746f6e2f7461722d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/alexcrichton/tar-rs)
*   zip
    *   [zip-rs/zip](https://github.com/zip-rs/zip) — read and write ZIP archives [![Build Status](https://camo.githubusercontent.com/9814e59d9f411f9d9f728d31c7ae70a257326717a0e41c007a4eedaf59e3ac05/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d76646e65732f7a69702d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mvdnes/zip-rs)

### [](#computation)Computation

*   [argmin-rs/argmin](https://github.com/argmin-rs/argmin) \[[argmin](https://crates.io/crates/argmin)\] — A pure Rust optimization library [![build badge](https://camo.githubusercontent.com/a04e46b895a84d1c7308bf8c01aea85f788a7540c59be9aa1a93cf8c4c007e68/68747470733a2f2f6170692e7472617669732d63692e6f72672f6172676d696e2d72732f6172676d696e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/argmin-rs/argmin)
*   [BLAS](https://en.wikipedia.org/wiki/Basic_Linear_Algebra_Subprograms) \[[blas](https://crates.io/keywords/blas)\]
    *   [mikkyang/rust-blas](https://github.com/mikkyang/rust-blas) — BLAS bindings
*   [calebwin/emu](https://github.com/calebwin/emu) — A language for GPGPU numerical computing from a Rust macro
*   [dimforge/nalgebra](https://github.com/dimforge/nalgebra) — low-dimensional linear algebra library [![build badge](https://camo.githubusercontent.com/5c92cb666bf1bfc511c12664e1766cfa729b4d08d955c18b0036c49fcce55438/68747470733a2f2f6170692e7472617669732d63692e6f72672f64696d666f7267652f6e616c67656272612e7376673f6272616e63683d646576)](https://travis-ci.org/dimforge/nalgebra)
*   [GSL](http://www.gnu.org/software/gsl/)
    *   [GuillaumeGomez/rust-GSL](https://github.com/GuillaumeGomez/rust-GSL) — GSL bindings [![build badge](https://camo.githubusercontent.com/05b80732c3828aeb4ce0fd8bf88da3975aede0ea2461244f12a4ed9ec35c175e/68747470733a2f2f6170692e7472617669732d63692e6f72672f4775696c6c61756d65476f6d657a2f727573742d47534c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/GuillaumeGomez/rust-GSL)
*   [LAPACK](https://en.wikipedia.org/wiki/LAPACK)
    *   [stainless-steel/lapack](https://github.com/blas-lapack-rs/lapack) — LAPACK bindings [![build badge](https://camo.githubusercontent.com/5a3de077151555ebb80da421c8828de613d8a88e4ec9905a3496bec93d2d1629/68747470733a2f2f6170692e7472617669732d63692e6f72672f626c61732d6c617061636b2d72732f6c617061636b2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/blas-lapack-rs/lapack)
*   Parallel
    *   [arrayfire/arrayfire-rust](https://github.com/arrayfire/arrayfire-rust) — [Arrayfire](https://github.com/arrayfire) bindings
    *   [autumnai/collenchyma](https://github.com/autumnai/collenchyma) — An extensible, pluggable, backend-agnostic framework for parallel, high-performance computations on CUDA, OpenCL and common host CPU. [![build badge](https://camo.githubusercontent.com/051b9e8726107c3c9da28d564b2c436ba07a7008ed0af9de03c4781665c62ed1/68747470733a2f2f6170692e7472617669732d63692e6f72672f617574756d6e61692f636f6c6c656e6368796d612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/autumnai/collenchyma)
    *   [luqmana/rust-opencl](https://github.com/luqmana/rust-opencl) — [OpenCL](https://www.khronos.org/opencl/) bindings
*   Scirust
    *   [indigits/scirust](https://github.com/indigits/scirust) — scientific computing library in Rust [![Build Status](https://camo.githubusercontent.com/57a0eeb02ff75c2e1455609b28cdee7ecc1973aeeae7f976befbe06e634d6f01/68747470733a2f2f6170692e7472617669732d63692e6f72672f696e6469676974732f736369727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/indigits/scirust)
*   Statrs
    *   [statrs-dev/statrs](https://github.com/statrs-dev/statrs) — Robust statistical computation library in Rust [![Build Status](https://camo.githubusercontent.com/1b12c8bfa847e1e06d2180690f868943ed7be4ecdf9b9b280934b687e7144027/68747470733a2f2f6170692e7472617669732d63692e6f72672f626f78746f776e2f7374617472732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/boxtown/statrs)

### [](#configuration)Configuration

*   [andoriyu/uclicious](https://github.com/andoriyu/uclicious) \[[uclicious](https://crates.io/crates/uclicious)\] — [libUCL](https://github.com/vstakhov/libucl) based feature-rich configuration library. [![CircleCI](https://camo.githubusercontent.com/4ce877339cadf403bdc601d78579315f5cbb1323c3bd45054fb9aada9b243c1d/68747470733a2f2f636972636c6563692e636f6d2f67682f767374616b686f762f6c696275636c2e7376673f7374796c653d737667)](https://app.circleci.com/pipelines/github/vstakhov/libucl)
*   [Kixunil/configure\_me](https://github.com/Kixunil/configure_me) \[[configure\_me](https://crates.io/crates/configure_me)\] — library for processing application configuration easily
*   [mehcode/config-rs](https://github.com/mehcode/config-rs) \[[config](https://crates.io/crates/config)\] — Layered configuration system for Rust applications (with strong support for 12-factor applications). [![build badge](https://camo.githubusercontent.com/67833235c4727e254e251d2e468af0492628d20bcb7383c004f39c9eb3481e0c/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6568636f64652f636f6e6669672d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mehcode/config-rs)

### [](#cryptography)Cryptography

\[[crypto](https://crates.io/keywords/crypto), [cryptography](https://crates.io/keywords/cryptography)\]

*   [briansmith/ring](https://github.com/briansmith/ring) — Safe, fast, small crypto using Rust and BoringSSL's cryptography primitives. [![build badge](https://camo.githubusercontent.com/36d688fbaccf26fec69d5ceb50cf59019fe3465fcb8e4085106e16af679013ff/68747470733a2f2f6170692e7472617669732d63692e6f72672f627269616e736d6974682f72696e672e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/briansmith/ring)
*   [briansmith/webpki](https://github.com/briansmith/webpki) — Web PKI TLS X.509 certificate validation in Rust. [![build badge](https://camo.githubusercontent.com/7d49bf96144bf8b9fac4c4015623451d91ae8f2753dca1da67c7811d92293a98/68747470733a2f2f6170692e7472617669732d63692e6f72672f627269616e736d6974682f776562706b692e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/briansmith/webpki)
*   [conradkleinespel/rooster](https://github.com/conradkleinespel/rooster) \[[rooster](https://crates.io/crates/rooster)\] — Simple password manager to use in your terminal
*   [cossacklabs/themis](https://github.com/cossacklabs/themis) \[[themis](https://crates.io/crates/themis)\] — a high-level cryptographic library for solving typical data security tasks, best fit for multi-platform apps. [![build badge](https://camo.githubusercontent.com/dc6db50c30d20ff93a531ea46681d8d6dc0851d5a5b59763e9c4e74ae7c150b5/68747470733a2f2f636972636c6563692e636f6d2f67682f636f737361636b6c6162732f7468656d69732f747265652f6d61737465722e7376673f7374796c653d736869656c64)](https://app.circleci.com/pipelines/github/cossacklabs/themis)
*   [DaGenix/rust-crypto](https://github.com/DaGenix/rust-crypto) — cryptographic algorithms in Rust [![build badge](https://camo.githubusercontent.com/008ce617f1ea92a99db0a4e5e909d4e985caf0d3fc77aae4d45c4ffe3caa7dfd/68747470733a2f2f6170692e7472617669732d63692e6f72672f446147656e69782f727573742d63727970746f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/DaGenix/rust-crypto)
*   [dalek-cryptography/curve25519-dalek](https://github.com/dalek-cryptography/curve25519-dalek) — Pure Rust implementation of Curve25519 operations
*   [dalek-cryptography/ed25519-dalek](https://github.com/dalek-cryptography/ed25519-dalek) — Pure Rust implementation of Ed25519 digital signatures
*   [dalek-cryptography/x25519-dalek](https://github.com/dalek-cryptography/x25519-dalek) — Pure Rust implementation of X25519 key exchange
*   [debris/tiny-keccak](https://github.com/debris/tiny-keccak) — Pure Rust implementation of the Keccak family (SHA3)
*   [exonum/exonum](https://github.com/exonum/exonum) \[[exonum](https://crates.io/crates/exonum)\] — extensible framework for blockchain projects [![build badge](https://camo.githubusercontent.com/44c52e5bf44827a198c4df54052d92bd4e751111e1110576e0201567fbb8099a/68747470733a2f2f6170692e7472617669732d63692e636f6d2f65786f6e756d2f65786f6e756d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/exonum/exonum)
*   [klutzy/suruga](https://github.com/klutzy/suruga) — A Rust implementation of [TLS 1.2](https://datatracker.ietf.org/doc/html/rfc5246)
*   [kornelski/rust-security-framework](https://github.com/kornelski/rust-security-framework) — Bindings for Security Framework (OSX native)
*   [libOctavo/octavo](https://github.com/libOctavo/octavo) — Modular hash and crypto library in Rust [![build badge](https://camo.githubusercontent.com/c50b034e5bd734396821a031c7b6adff6a8671d8d8d29ff6267c835bddd44d35/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c69624f637461766f2f6f637461766f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/libOctavo/octavo)
*   [novifinancial/opaque-ke](https://github.com/novifinancial/opaque-ke) — Pure Rust implementation of the recent [OPAQUE](https://datatracker.ietf.org/doc/draft-krawczyk-cfrg-opaque/) password-authenticated key exchange. [![build badge](https://github.com/novifinancial/opaque-ke/workflows/Rust%20CI/badge.svg?branch=master)](https://github.com/novifinancial/opaque-ke)
*   [orion-rs/orion](https://github.com/orion-rs/orion) — This library aims to provide easy and usable crypto. 'Usable' meaning exposing high-level API's that are easy to use and hard to misuse. [![Tests](https://github.com/orion-rs/orion/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/orion-rs/orion/actions/workflows/test.yml)
*   [racum/rust-djangohashers](https://github.com/racum/rust-djangohashers) — A Rust port of the password primitives used in the Django Project. It doesn't require Django, only hashes and validates passwords according to its style. [![build badge](https://camo.githubusercontent.com/7d2ebe5c8300aef3a63ada915870bb09b6b6833139cd05a9fb7af50e62b658d3/68747470733a2f2f6170692e7472617669732d63692e6f72672f526163756d2f727573742d646a616e676f686173686572732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Racum/rust-djangohashers)
*   [RustCrypto/hashes](https://github.com/RustCrypto/hashes) — Collection of cryptographic hash functions written in pure Rust [![build badge](https://camo.githubusercontent.com/4adc87010ba2a0a799f48c18b8d0d4969ac72a6aab382a9c9e9ea333607dc1db/68747470733a2f2f6170692e7472617669732d63692e6f72672f5275737443727970746f2f6861736865732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/RustCrypto/hashes)
*   [rustls/rustls](https://github.com/rustls/rustls) — A Rust implementation of TLS
*   [sfackler/rust-native-tls](https://github.com/sfackler/rust-native-tls) — Bindings for native TLS libraries
*   [sfackler/rust-openssl](https://github.com/sfackler/rust-openssl) — [OpenSSL](https://www.openssl.org/) bindings [![build badge](https://camo.githubusercontent.com/c6c29b7af47e68040e8e5aef93de2559b1558f102fab26970f593820f8ef7337/68747470733a2f2f6170692e7472617669732d63692e6f72672f736661636b6c65722f727573742d6f70656e73736c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sfackler/rust-openssl)
*   [sodiumoxide/sodiumoxide](https://github.com/sodiumoxide/sodiumoxide) — [libsodium](https://github.com/jedisct1/libsodium) bindings [![build badge](https://camo.githubusercontent.com/bcb0ad2f593dc3104e2fb4cd858c115915f8215a3c87d69b61906b4e376d419f/68747470733a2f2f6170692e7472617669732d63692e6f72672f736f6469756d6f786964652f736f6469756d6f786964652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sodiumoxide/sodiumoxide)
*   [vityafx/randomorg](https://github.com/vityafx/randomorg) - A [https://www.random.org/](https://www.random.org/) client library. [![Crates badge](https://camo.githubusercontent.com/d6f2e522213aa52bf85a8387841489327b311cb51c8479ea1d5defb411f29f82/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f72616e646f6d6f72672e737667)](https://crates.io/crates/randomorg)
*   [w3f/schnorrkel](https://github.com/w3f/schnorrkel) - Schnorr VRFs and signatures on the Ristretto group

### [](#database-1)Database

\[[database](https://crates.io/keywords/database)\]

*   NoSQL \[[nosql](https://crates.io/keywords/nosql)\]
    
    *   [ArangoDB](https://www.arangodb.com)
        *   [Aragog](https://gitlab.com/qonfucius/aragog) \[[aragog](https://crates.io/crates/aragog)\] - A Lightweight ArangoDB Object document, relational and graph mapper [![pipeline status](https://camo.githubusercontent.com/d70e51ecdfc4be70c5fd6207194c2c9377281f83776c7d0070b0c86cc9c674bd/68747470733a2f2f6769746c61622e636f6d2f716f6e6675636975732f617261676f672f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/qonfucius/aragog/-/commits/master)
        *   [Arangors](https://github.com/fMeow/arangors) \[[arangors](https://crates.io/crates/arangors)\] - An ArangoDB driver for Rust
    *   [Cassandra](https://cassandra.apache.org/_/index.html) \[[cassandra](https://crates.io/keywords/cassandra), [cql](https://crates.io/keywords/cql)\]
        *   [AlexPikalov/cdrs](https://github.com/AlexPikalov/cdrs) \[[cdrs](https://crates.io/crates/cdrs)\] — native client written in Rust [![build badge](https://camo.githubusercontent.com/98b3be98b660ac7c83f24eed450b31747b92d4af8f429cadc6a103fec1fc330a/68747470733a2f2f6170692e7472617669732d63692e6f72672f416c657850696b616c6f762f636472732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/AlexPikalov/cdrs)
        *   [krojew/cdrs-tokio](https://github.com/krojew/cdrs-tokio) \[[cdrs-tokio](https://crates.io/crates/cdrs-tokio)\] - production-ready async Apache Cassandra driver written in pure Rust [![build badge](https://github.com/krojew/cdrs-tokio/actions/workflows/rust.yml/badge.svg)](https://github.com/krojew/cdrs-tokio/actions)
        *   [Metaswitch/cassandra-rs](https://github.com/Metaswitch/cassandra-rs) — bindings to the DataStax C/C++ client [![build badge](https://camo.githubusercontent.com/0a990b11143f5cca8d0964e2d8e2140c31b7fa75faa3f64a1fcb7a84679c7885/68747470733a2f2f6170692e7472617669732d63692e6f72672f4d6574617377697463682f63617373616e6472612d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Metaswitch/cassandra-rs)
    *   CouchDB \[[couchdb](https://crates.io/keywords/couchdb)\]
        *   [chill-rs/chill](https://github.com/chill-rs/chill) \[[couchdb](https://crates.io/crates/chill)\] — A Rust client for the CouchDB REST API [![build badge](https://camo.githubusercontent.com/20511f74efcef005c542afe5e4da005a1fe0dff39d3a5615dd3e3e204b63adf2/68747470733a2f2f6170692e7472617669732d63692e6f72672f6368696c6c2d72732f6368696c6c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/chill-rs/chill)
    *   [DynamoDB](https://aws.amazon.com/dynamodb/) \[[dynamodb](https://crates.io/keywords/dynamodb)\]
        *   [softprops/dynomite](https://github.com/softprops/dynomite) - A library for strongly-typed and convenient interaction with `rusoto_dynamodb` [![build badge](https://github.com/softprops/dynomite/workflows/Main/badge.svg?branch=master)](https://github.com/softprops/dynomite/actions)
    *   Elasticsearch \[[elasticsearch](https://crates.io/keywords/elasticsearch)\]
        *   [benashford/rs-es](https://github.com/benashford/rs-es) \[[rs-es](https://crates.io/crates/rs-es)\] — A Rust client for the [Elastic](https://www.elastic.co/) REST API [![build badge](https://camo.githubusercontent.com/87fa1bac7eed367041a8f486ccfa7de74ac14a85ff4d8fe08a998c99936b7f9e/68747470733a2f2f6170692e7472617669732d63692e6f72672f62656e617368666f72642f72732d65732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/benashford/rs-es)
        *   [elastic-rs/elastic](https://github.com/elastic-rs/elastic) \[[elastic](https://crates.io/crates/elastic)\] — elastic is an efficient, modular API client for Elasticsearch written in Rust [![build badge](https://camo.githubusercontent.com/f1108a96a43b94f87bf6f60f85a50728ad0fbfa42d3067fa7012e68c36f194af/68747470733a2f2f63692e6170707665796f722e636f6d2f6170692f70726f6a656374732f7374617475732f63736137387463756d64706e627572323f7376673d74727565)](https://ci.appveyor.com/project/KodrAus/elastic)
    *   etcd
        *   [jimmycuadra/rust-etcd](https://github.com/jimmycuadra/rust-etcd) \[[etcd](https://crates.io/crates/etcd)\] — A client library for CoreOS's etcd. [![build badge](https://camo.githubusercontent.com/56e3ed7fed51b69175a86b486b16bd62dee6e40851c5c032d845f18262f1b4ff/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a696d6d796375616472612f727573742d657463642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jimmycuadra/rust-etcd)
        *   [luncj/etcd-rs](https://github.com/luncj/etcd-rs) — An asynchronous etcd client for rust [![build badge](https://camo.githubusercontent.com/0224362341071cd21fc6fc786b6138116aecc405cefe334c1c5c7d5a0b546ffa/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c756e636a2f657463642d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/luncj/etcd-rs)
    *   ForestDB
        *   [vhbit/sherwood](https://github.com/vhbit/sherwood) — [ForestDB](https://github.com/couchbase/forestdb) bindings [![build badge](https://camo.githubusercontent.com/23ca25fc26320d83d3a0d950d0fc4036a7a7fc1dba773de916796b5cadc9ae0b/68747470733a2f2f6170692e7472617669732d63692e6f72672f76686269742f73686572776f6f642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vhbit/sherwood)
    *   [InfluxDB](https://www.influxdata.com/)
        *   [driftluo/InfluxDBClient-rs](https://github.com/driftluo/InfluxDBClient-rs) — Synchronization interface [![build badge](https://camo.githubusercontent.com/514365ca57f6441f51381f83cf8b0032043fbcb55f940ecbc853c0dd50583ec7/68747470733a2f2f6170692e7472617669732d63692e6f72672f64726966746c756f2f496e666c75784442436c69656e742d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/driftluo/InfluxDBClient-rs)
    *   LevelDB
        *   [skade/leveldb](https://github.com/skade/leveldb) — [LevelDB](https://github.com/google/leveldb) bindings [![build badge](https://camo.githubusercontent.com/0c8c31e78dad40cbe8d6a7ef53377f78523b7baf731b7ae3a31b933695040de7/68747470733a2f2f6170692e7472617669732d63692e6f72672f736b6164652f6c6576656c64622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/skade/leveldb)
    *   LMDB \[[lmdb](https://crates.io/keywords/lmdb)\]
        *   [vhbit/lmdb-rs](https://github.com/vhbit/lmdb-rs) \[[lmdb-rs](https://crates.io/crates/lmdb-rs)\] — [LMDB](https://www.symas.com/symas-embedded-database-lmdb) bindings [![build badge](https://camo.githubusercontent.com/4aaca22911abefd0bdba66c2f84448b43c2ea993212ac754469b9b0e26cb72f1/68747470733a2f2f6170692e7472617669732d63692e6f72672f76686269742f6c6d64622d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vhbit/lmdb-rs)
    *   MongoDB \[[mongodb](https://crates.io/keywords/mongodb)\]
        *   [mongodb/mongo-rust-driver](https://github.com/mongodb/mongo-rust-driver) \[[mongodb](https://crates.io/crates/mongodb)\] — [MongoDB](https://www.mongodb.com/) bindings
    *   [PickleDB](https://pythonhosted.org/pickleDB/)
        *   [seladb/pickledb-rs](https://github.com/seladb/pickledb-rs) — a lightweight and simple key-value store, heavily inspired by Python's PickleDB. [![build badge](https://camo.githubusercontent.com/844b9167350039cc13b5b0dc0a35be197d4f5d3b20204d672eb86ce796200d62/68747470733a2f2f6170692e7472617669732d63692e6f72672f73656c6164622f7069636b6c6564622d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/seladb/pickledb-rs)
    *   Redis \[[redis](https://crates.io/keywords/redis)\]
        *   [mitsuhiko/redis-rs](https://github.com/mitsuhiko/redis-rs) — [Redis](https://redis.io/) library in Rust [![build badge](https://camo.githubusercontent.com/96d09375a7ae37388a0629a49a1d1ae26df80532a824fd06c00f5c61e7e2f560/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6974737568696b6f2f72656469732d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mitsuhiko/redis-rs)
    *   [RocksDB](https://rocksdb.org/)
        *   [rust-rocksdb/rust-rocksdb](https://github.com/rust-rocksdb/rust-rocksdb) — RocksDB bindings [![RocksDB CI](https://github.com/rust-rocksdb/rust-rocksdb/actions/workflows/rust.yml/badge.svg?branch=master)](https://github.com/rust-rocksdb/rust-rocksdb/actions/workflows/rust.yml)
    *   [UnQLite](https://unqlite.org/)
        *   [zitsen/unqlite.rs](https://github.com/zitsen/unqlite.rs) — UnQLite bindings [![build badge](https://camo.githubusercontent.com/8221a0184b1d45711ea65c06837bc2738cc8d4b3650916db129ee61527a9dc52/68747470733a2f2f6170692e7472617669732d63692e6f72672f7a697473656e2f756e716c6974652e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/zitsen/unqlite.rs)
    *   [ZooKeeper](https://zookeeper.apache.org/)
        *   [bonifaido/rust-zookeeper](https://github.com/bonifaido/rust-zookeeper) \[[zookeeper](https://crates.io/crates/zookeeper)\] — A client library for Apache ZooKeeper. [![build badge](https://camo.githubusercontent.com/27d1e69fde715bac507f2bcf617d01f5878fd58e4f3676ae1cbfae9c4b116379/68747470733a2f2f6170692e7472617669732d63692e6f72672f626f6e69666169646f2f727573742d7a6f6f6b65657065722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/bonifaido/rust-zookeeper)
        *   [krojew/rust-zookeeper](https://github.com/krojew/rust-zookeeper) \[[zookeeper-async](https://crates.io/crates/zookeeper-async)\] - Async Zookeeper client written 100% in Rust, based on tokio. [![build status](https://github.com/krojew/rust-zookeeper/actions/workflows/rust.yml/badge.svg)](https://github.com/krojew/rust-zookeeper/actions/workflows/rust.yml/badge.svg)
*   OGM \[[ogm](https://crates.io/keywords/ogm)\]
    
    *   [Aragog](https://gitlab.com/qonfucius/aragog) \[[aragog](https://crates.io/crates/aragog)\] - A Lightweight ArangoDB Object document, relational and graph mapper [![pipeline status](https://camo.githubusercontent.com/d70e51ecdfc4be70c5fd6207194c2c9377281f83776c7d0070b0c86cc9c674bd/68747470733a2f2f6769746c61622e636f6d2f716f6e6675636975732f617261676f672f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/qonfucius/aragog/-/commits/master)
*   ORM \[[orm](https://crates.io/keywords/orm)\]
    
    *   [diesel-rs/diesel](https://github.com/diesel-rs/diesel) — an ORM and Query builder for Rust [![Build Status](https://camo.githubusercontent.com/1ee15d8eee59f587d123c361a3868bab817f6f9e4951fbe04d601aa9c39d648b/68747470733a2f2f6170692e7472617669732d63692e6f72672f64696573656c2d72732f64696573656c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/diesel-rs/diesel)
    *   [ivanceras/rustorm](https://github.com/ivanceras/rustorm) — an ORM for Rust [![Build Status](https://camo.githubusercontent.com/eb53570069688bac15e607b8eaed6369f48dd847e66f2e0e97262b7b636ab590/68747470733a2f2f6170692e7472617669732d63692e6f72672f6976616e63657261732f727573746f726d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ivanceras/rustorm)
    *   [rbatis/rbatis](https://github.com/rbatis/rbatis) — Rust ORM Framework High Performance(JSON based) [![Build Status](https://camo.githubusercontent.com/68b2952ea42e8648474abc3d79e1e597548437fd8b3f1c681d0bb58b89aeca66/68747470733a2f2f6170692e7472617669732d63692e6f72672f7a68757869756a69612f7262617469732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/zhuxiujia/rbatis)
    *   [SeaQL/sea-orm](https://github.com/SeaQL/sea-orm) — an async & dynamic ORM for Rust [![Build Status](https://github.com/SeaQL/sea-orm/actions/workflows/rust.yml/badge.svg)](https://github.com/SeaQL/sea-orm/actions/workflows/rust.yml)
*   [sfackler/r2d2](https://github.com/sfackler/r2d2) — generic connection pool [![build badge](https://camo.githubusercontent.com/0eba95a9c5049eff96b28682e4908a7d1f189d1f5bdbe6d4f5947c473f0fa80a/68747470733a2f2f6170692e7472617669732d63692e6f72672f736661636b6c65722f723264322e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sfackler/r2d2)
    
*   SQL \[[sql](https://crates.io/keywords/sql)\]
    
    *   Generic
        *   [launchbadge/sqlx](https://github.com/launchbadge/sqlx) - async PostgreSQL/MySQL/SQLite connection pool with strong typing support [![build badge](https://camo.githubusercontent.com/fd5efda4fc09b4e474ecc9e2fb9cb6485e01a33b44e0c0dbf4cedac08fe9f87d/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f6c61756e636862616467652f73716c782f527573742f6d61737465723f7374796c653d666c61742d737175617265)](https://github.com/launchbadge/sqlx)
    *   Microsoft SQL
        *   [prisma/tiberius](https://github.com/prisma/tiberius) — [![Cargo tests](https://github.com/prisma/tiberius/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/prisma/tiberius/actions/workflows/test.yml)
    *   MySql \[[mysql](https://crates.io/keywords/mysql)\]
        *   [AgilData/mysql-proxy-rs](https://github.com/AgilData/mysql-proxy-rs) — A MySQL Proxy [![CircleCI](https://camo.githubusercontent.com/6cb821bd2d8c9beda8413a068b72343b78873ff532565144409aed9cc197b63c/68747470733a2f2f636972636c6563692e636f6d2f67682f4167696c446174612f6d7973716c2d70726f78792d72732f747265652f6d61737465722e7376673f7374796c653d737667)](https://app.circleci.com/pipelines/github/AgilData/mysql-proxy-rs?branch=master)
        *   [blackbeam/mysql\_async](https://github.com/blackbeam/mysql_async) \[[mysql\_async](https://crates.io/crates/mysql_async)\] — asyncronous Rust Mysql driver based on Tokio. [![CircleCI](https://camo.githubusercontent.com/2ada19d14d9cef985f2e3294aa1debf0cbdcd675dbc19f4127eb76ee312760c7/68747470733a2f2f636972636c6563692e636f6d2f67682f626c61636b6265616d2f6d7973716c5f6173796e632f747265652f6d61737465722e7376673f7374796c653d736869656c64)](https://app.circleci.com/pipelines/github/blackbeam/mysql_async?branch=master)
        *   [blackbeam/rust-mysql-simple](https://github.com/blackbeam/rust-mysql-simple) \[[mysql](https://crates.io/crates/mysql)\] — A native MySql client [![build badge](https://camo.githubusercontent.com/04a53e3b4c9b630b4071cc5e22cd8d920c8701fb8627bb6d28d5f665c99c700f/68747470733a2f2f6170692e7472617669732d63692e6f72672f626c61636b6265616d2f727573742d6d7973716c2d73696d706c652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/blackbeam/rust-mysql-simple)
    *   PostgreSql \[[postgres](https://crates.io/keywords/postgres), [postgresql](https://crates.io/keywords/postgresql)\]
        *   [sfackler/rust-postgres](https://github.com/sfackler/rust-postgres) \[[postgres](https://crates.io/crates/postgres)\] — A native [PostgreSQL](https://www.postgresql.org/) client [![build badge](https://camo.githubusercontent.com/9b43c9f74c641b56af1d296d06a3639511291778778ac2cc51ea8511e9ef4484/68747470733a2f2f6170692e7472617669732d63692e6f72672f736661636b6c65722f727573742d706f7374677265732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sfackler/rust-postgres)
    *   Sqlite \[[sqlite](https://crates.io/keywords/sqlite)\]
        *   [rusqlite](https://github.com/rusqlite/rusqlite) — [Sqlite3](https://www.sqlite.org/index.html) bindings [![build badge](https://camo.githubusercontent.com/471cb16bd8e1545f811d7a8e5a0a2a501ef00dee3cbd75124db6b391c126f604/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573716c6974652f727573716c6974652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rusqlite/rusqlite)

### [](#data-processing)Data processing

*   [amv-dev/yata](https://github.com/amv-dev/yata) — high perfomance technical analysis library [![Build Status](https://camo.githubusercontent.com/374ecc988383fbccdb6d710959c28c7ea8f1d69f6549bdacbc37de85e828ed0e/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f616d762d6465762f796174612f527573743f6272616e63683d6d6173746572)](https://github.com/amv-dev/yata/actions?query=workflow%3ARust)
*   [bluss/ndarray](https://github.com/rust-ndarray/ndarray) — N-dimensional array with array views, multidimensional slicing, and efficient operations
*   [kernelmachine/utah](https://github.com/kernelmachine/utah) — Dataframe structure and operations in Rust
*   [pola-rs/polars](https://github.com/pola-rs/polars) - Fast feature complete DataFrame library [![Build and test](https://github.com/pola-rs/polars/workflows/Build%20and%20test/badge.svg?branch=master)](https://github.com/pola-rs/polars/workflows/Build%20and%20test/badge.svg?branch=master)
*   [weld-project/weld](https://github.com/weld-project/weld) — High-performance runtime for data analytics applications

### [](#data-streaming)Data streaming

*   [infinyon/fluvio](https://github.com/infinyon/fluvio) - Programmable data streaming platform [![CI](https://github.com/infinyon/fluvio/workflows/CI/badge.svg?branch=stable)](https://github.com/infinyon/fluvio/actions)

### [](#data-structures)Data structures

*   [billyevans/tst](https://github.com/billyevans/tst) \[[tst](https://crates.io/crates/tst)\] — Ternary search tree collection [![build badge](https://camo.githubusercontent.com/10ad26f3105d0d0c8254fc39c55532b15cb0e8c1ba64b32a690c139e995d9ce1/68747470733a2f2f6170692e7472617669732d63692e6f72672f62696c6c796576616e732f7473742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/billyevans/tst)
*   [contain-rs](https://github.com/contain-rs) — Extension of Rust's std::collections
*   [danielpclark/array\_tool](https://github.com/danielpclark/array_tool) — Array helpers for Rust. Some of the most common methods you would use on Arrays made available on Vectors. Polymorphic implementations for handling most of your use cases. [![build badge](https://camo.githubusercontent.com/34bed373d1233c0a0e27899056a40fd3cf9b1b75070ff354212d9f8e8da40ec6/68747470733a2f2f6170692e7472617669732d63692e6f72672f64616e69656c70636c61726b2f61727261795f746f6f6c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/danielpclark/array_tool)
*   [fizyk20/generic-array](https://github.com/fizyk20/generic-array) – a hack to allow for arrays sized by typenums [![build badge](https://camo.githubusercontent.com/5cdf9baacedbe3967c67bb38ba2db8327fde3f521380aa889d1bafe7b848720d/68747470733a2f2f6170692e7472617669732d63692e6f72672f66697a796b32302f67656e657269632d61727261792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/fizyk20/generic-array)
*   [garro95/priority-queue](https://github.com/garro95/priority-queue)\[[priority-queue](https://crates.io/crates/priority-queue)\] — A priority queue that implements priority changes. [![build badge](https://camo.githubusercontent.com/53f307c3c724a522c6d70a757aa7642d616762333e423af353ec304803e5b20b/68747470733a2f2f6170692e7472617669732d63692e6f72672f676172726f39352f7072696f726974792d71756575652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/garro95/priority-queue)
*   [mrhooray/kdtree-rs](https://github.com/mrhooray/kdtree-rs) — K-dimensional tree in Rust for fast geospatial indexing and nearest neighbors lookup
*   [orium/rpds](https://github.com/orium/rpds) \[[rpds](https://crates.io/crates/rpds)\] — Persistent data structures in Rust. [![build badge](https://github.com/orium/rpds/workflows/CI/badge.svg)](https://github.com/orium/rpds/actions?query=workflow%3ACI)
*   [RoaringBitmap/roaring-rs](https://github.com/RoaringBitmap/roaring-rs) – Roaring Bitmaps in Rust
*   [rust-itertools/itertools](https://github.com/rust-itertools/itertools) — [![build badge](https://camo.githubusercontent.com/4416362f6a28148d18323ae8ea0b5384c9fcaee44bfd7a5553b308e67db5847c/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d69746572746f6f6c732f69746572746f6f6c732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-itertools/itertools)
*   [tnballo/scapegoat](https://github.com/tnballo/scapegoat) \[[scapegoat](https://crates.io/crates/scapegoat)\] — Safe, fallible, stack-only alternative to `BTreeSet` and `BTreeMap`. [![GitHub Actions](https://github.com/tnballo/scapegoat/workflows/test/badge.svg?branch=master)](https://github.com/tnballo/scapegoat/actions)
*   [xfix/enum-map](https://github.com/xfix/enum-map) \[[enum-map](https://crates.io/crates/enum-map)\] — An optimized map implementation for enums using an array to store values. [![build badge](https://camo.githubusercontent.com/f77661b394b3b9ed62a3e5ee59a7b2b40c0702b5bf87d8c190ea8eea0c69983d/68747470733a2f2f6170692e7472617669732d63692e6f72672f786669782f656e756d2d6d61702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/xfix/enum-map)

### [](#data-visualization)Data visualization

*   [38/plotters](https://github.com/38/plotters) — [![build badge](https://camo.githubusercontent.com/0f80e46e31ef01e9364a7f21ea77dbd927e4ff84cc98fed4f146462b78cd00fd/68747470733a2f2f6170692e7472617669732d63692e6f72672f33382f706c6f74746572732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/38/plotters)
*   [igiagkiozis/plotly](https://github.com/igiagkiozis/plotly) — Plotly for Rust.
*   [milliams/plotlib](https://github.com/milliams/plotlib) — [![build badge](https://camo.githubusercontent.com/5a0e6bd0cf532c6a0ddb25f92718631c841318bc8aff449411a6cd3fb3a5fb88/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d696c6c69616d732f706c6f746c69622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/milliams/plotlib)
*   [saresend/gust](https://github.com/saresend/Gust) — [![build badge](https://camo.githubusercontent.com/be4ed89b0c26f509beacfa8c90b9c99876dae96a89c81e7788c0c570da676341/68747470733a2f2f6170692e7472617669732d63692e6f72672f7361726573656e642f477573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/saresend/Gust)

### [](#date-and-time)Date and time

\[[date](https://crates.io/keywords/date), [time](https://crates.io/keywords/time)\]

*   [chronotope/chrono](https://github.com/chronotope/chrono) — [![build badge](https://camo.githubusercontent.com/eb5e2e3eab775cca6db90df781e05f53a1d19622c60ec5ceb58b4eca43eaad12/68747470733a2f2f6170692e7472617669732d63692e6f72672f6368726f6e6f746f70652f6368726f6e6f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/chronotope/chrono)
*   [Mnwa/ms](https://github.com/Mnwa/ms) \[[ms-converter](https://crates.io/crates/ms-converter)\] — it's a library for converting human-like times to milliseconds [![build badge](https://github.com/Mnwa/ms/workflows/build/badge.svg?branch=master)](https://github.com/Mnwa/ms/actions?query=workflow%3Abuild)
*   [time-rs/time](https://github.com/time-rs/time) — [![build badge](https://github.com/time-rs/time/workflows/Build/badge.svg)](https://github.com/time-rs/time/actions)

### [](#distributed-systems)Distributed systems

*   Antimony
    *   [antimonyproject/antimony](https://github.com/antimonyproject/antimony) \[[antimony](https://crates.io/crates/antimony)\] — stream processing / distributed computation platform [![build badge](https://camo.githubusercontent.com/33f1e96f5e0e959ecbb4fe92124d4a4a2938467015ea16077da058dba31b6ff4/68747470733a2f2f6170692e7472617669732d63692e6f72672f616e74696d6f6e7970726f6a6563742f616e74696d6f6e792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/antimonyproject/antimony)
*   Apache Kafka
    *   [fede1024/rust-rdkafka](https://github.com/fede1024/rust-rdkafka) \[[rdkafka](https://crates.io/crates/rdkafka)\] — [librdkafka](https://github.com/edenhill/librdkafka) bindings [![build badge](https://camo.githubusercontent.com/337bf77a8405577b210186c9f1dc1f3e3007984f4bc23814a4546c7ddb2ebedd/68747470733a2f2f6170692e7472617669732d63692e6f72672f66656465313032342f727573742d72646b61666b612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/fede1024/rust-rdkafka)
    *   [gklijs/schema\_registry\_converter](https://github.com/gklijs/schema_registry_converter) \[[schema\_registry\_converter](https://crates.io/crates/schema_registry_converter)\] — to integrate with [confluent schema registry](https://www.confluent.io/product/confluent-platform/data-compatibility/) [![build badge](https://camo.githubusercontent.com/9d5ee53cf1def5bff625c06dabcad8a3491c9fed785c000ba972e5e2325922c0/68747470733a2f2f6170692e7472617669732d63692e6f72672f676b6c696a732f736368656d615f72656769737472795f636f6e7665727465722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/gklijs/schema_registry_converter)
    *   [kafka-rust/kafka-rust](https://github.com/kafka-rust/kafka-rust) — [![build badge](https://camo.githubusercontent.com/c8b254aa4ce2ca903f18bff94e79aa82b526e696bd835bc96812640672ffcbdc/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b61666b612d727573742f6b61666b612d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kafka-rust/kafka-rust)
*   Beanstalkd
    *   [schickling/rust-beanstalkd](https://github.com/schickling/rust-beanstalkd) — [Beanstalkd](https://github.com/beanstalkd/beanstalkd) bindings [![build badge](https://camo.githubusercontent.com/d835bbb16be916544955151c06676179bc6999ed245e00ad5d3ebe574114447c/68747470733a2f2f6170692e7472617669732d63692e6f72672f73636869636b6c696e672f727573742d6265616e7374616c6b642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/schickling/rust-beanstalkd)
*   HDFS
    *   [hyunsik/hdfs-rs](https://github.com/hyunsik/hdfs-rs) \[[hdfs](https://crates.io/crates/hdfs)\] — libhdfs bindings

### [](#domain-driven-design)Domain driven design

*   [serverlesstechnology/cqrs](https://github.com/serverlesstechnology/cqrs) \[[cqrs-es](https://crates.io/crates/cqrs-es)\] — A framework for CQRS and event sourcing with [user guide](https://doc.rust-cqrs.org/)

### [](#email)Email

\[[email](https://crates.io/keywords/email), [imap](https://crates.io/keywords/imap), [smtp](https://crates.io/keywords/smtp)\]

*   [gsquire/sendgrid-rs](https://github.com/gsquire/sendgrid-rs) — unofficial Rust library for SendGrid API [![build badge](https://camo.githubusercontent.com/ff9ccf5e9e5eacf2b4bfcc6f43c0bf86b98bb98119f0e81505b4dcd08c0a27a0/68747470733a2f2f6170692e7472617669732d63692e6f72672f677371756972652f73656e64677269642d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/gsquire/sendgrid-rs)
*   [jdrouet/catapulte](https://github.com/jdrouet/catapulte) [![build badge](https://camo.githubusercontent.com/5d01a835c70f3b5e191f7d457d6108465cd1c78cba35d9c0a7bb3f882aee2483/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6a64726f7565742f6361746170756c74652e7376673f6272616e63683d6d61696e)](https://travis-ci.org/jdrouet/catapulte) - A microservice to send emails using [MRML](https://github.com/jdrouet/mrml) templates.
*   [jdrouet/jolimail](https://github.com/jdrouet/jolimail) [![pipeline status](https://camo.githubusercontent.com/67323c42aa97efd83e3c0fe3f01aabbbd9a37ff69dde6646f1d2a973f2160ff1/68747470733a2f2f6769746c61622e636f6d2f6a6572656d69652e64726f7565742f6a6f6c696d61696c2f6261646765732f6d61696e2f706970656c696e652e737667)](https://gitlab.com/jeremie.drouet/jolimail/-/commits/main) - A web application to build [MRML](https://github.com/jdrouet/mrml) templates.
*   [jdrouet/mrml](https://github.com/jdrouet/mrml) [![build badge](https://camo.githubusercontent.com/3052f950ad1542f53fa76b744ec992b6bf217432857abbb28b3430f161aea5c0/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6a64726f7565742f6d726d6c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jdrouet/mrml) - A library to generate nice email templates working on any mail client.
*   [lettre/lettre](https://github.com/lettre/lettre) — an SMTP-library for Rust [![CI](https://github.com/lettre/lettre/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/lettre/lettre/actions/workflows/test.yml)
*   [staktrace/mailparse](https://github.com/staktrace/mailparse) \[[mailparse](https://crates.io/crates/mailparse)\] — A library for parsing real-world email files [![build badge](https://camo.githubusercontent.com/7b77cd1022fd913291b148ba1c1ef9ef11bd0c4d871576ad013579dd589434d6/68747470733a2f2f6170692e7472617669732d63692e6f72672f7374616b74726163652f6d61696c70617273652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/staktrace/mailparse)
*   [stalwartlabs/mail-parser](https://github.com/stalwartlabs/mail-parser) \[[mail-parser](https://crates.io/crates/mail-parser)\] - A fast and robust e-mail parsing library with full MIME support [![build badge](https://github.com/stalwartlabs/mail-parser/actions/workflows/rust.yml/badge.svg)](https://github.com/stalwartlabs/mail-parser/actions/workflows/rust.yml)

### [](#encoding)Encoding

\[[encoding](https://crates.io/keywords/encoding)\]

*   ASN.1
    *   [alex/rust-asn1](https://github.com/alex/rust-asn1) — A Rust ASN.1 (DER) serializer [![build badge](https://camo.githubusercontent.com/315eaa2da34325abf5eeaf5aac985835d2c7410d8eb3d13607e0f9774857d1fb/68747470733a2f2f6170692e7472617669732d63692e6f72672f616c65782f727573742d61736e312e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/alex/rust-asn1)
*   Binary
    *   [bincode-org/bincode](https://github.com/bincode-org/bincode) — A binary encoder/decoder in Rust [![CI](https://github.com/bincode-org/bincode/actions/workflows/rust.yml/badge.svg?branch=trunk)](https://github.com/bincode-org/bincode/actions/workflows/rust.yml)
    *   [m4b/goblin](https://github.com/m4b/goblin) \[[goblin](https://crates.io/crates/goblin)\] — cross-platform, zero-copy, and endian-aware binary parsing [![build badge](https://camo.githubusercontent.com/d88c951a686b42e689d8753ea9dec4139697eed24e898589fc4a500813cf97c9/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d34622f676f626c696e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/m4b/goblin)
*   BSON
    *   [mongodb/bson-rust](https://github.com/mongodb/bson-rust) — Encoding and decoding support for BSON in Rust
*   Byte swapping
    *   [BurntSushi/byteorder](https://github.com/BurntSushi/byteorder) — Supports big-endian, little-endian and native byte orders [![build badge](https://camo.githubusercontent.com/f15280880e7634f92cac7565ca0bfb38c81df91634f8171a5208bf2ca73beb23/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f627974656f726465722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/byteorder)
*   Cap'n Proto
    *   [capnproto/capnproto-rust](https://github.com/capnproto/capnproto-rust) — [![build badge](https://camo.githubusercontent.com/bf156aa9d073afa8eb3ac4a370027392d27fb8c9e1363afa450468b31946c585/68747470733a2f2f6170692e7472617669732d63692e6f72672f6361706e70726f746f2f6361706e70726f746f2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/capnproto/capnproto-rust)
*   CBOR
    *   [serde\_cbor](https://crates.io/crates/serde_cbor) — CBOR support for serde [![build badge](https://camo.githubusercontent.com/16046515a230be8b25840ae9c6e28711d5e5ede9878aec8a799e0e88ee1b72af/68747470733a2f2f6170692e7472617669732d63692e6f72672f707966697363682f63626f722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/pyfisch/cbor)
*   Character Encoding
    *   [hsivonen/encoding\_rs](https://github.com/hsivonen/encoding_rs) \[[encoding\_rs](https://crates.io/crates/encoding_rs)\] — A Gecko-oriented implementation of the Encoding Standard in Rust [![build badge](https://camo.githubusercontent.com/4eb20dd175ad69174b5e4a16e4f01672212a34c576bc2193351fd54ecb75440d/68747470733a2f2f6170692e7472617669732d63692e6f72672f687369766f6e656e2f656e636f64696e675f72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/hsivonen/encoding_rs)
    *   [lifthrasiir/rust-encoding](https://github.com/lifthrasiir/rust-encoding) — [![build badge](https://camo.githubusercontent.com/92805967d7ea2092cfa49ea23abf7ed9d2fea3ade626318d4b86fce1a192a699/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c696674687261736969722f727573742d656e636f64696e672e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lifthrasiir/rust-encoding)
*   CRC
    *   [mrhooray/crc-rs](https://github.com/mrhooray/crc-rs) — [![build badge](https://camo.githubusercontent.com/b8a630b620496b0052f93efed03b51f711dea98280c6331b6c5af8ad046a8f54/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d72686f6f7261792f6372632d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mrhooray/crc-rs)
*   CSV
    *   [BurntSushi/rust-csv](https://github.com/BurntSushi/rust-csv) — A fast and flexible CSV reader and writer, with support for Serde [![build badge](https://camo.githubusercontent.com/e907cbdb9d5fa034fa22335b3d17e7820c6343c25940589f9425da7e5121b48d/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f727573742d6373762e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/rust-csv)
*   EDN
    *   [naomijub/edn-rs](https://github.com/naomijub/edn-rs) \[[edn-rs](https://crates.io/crates/edn-rs)\] — crate to parse and emit EDN format into Rust types. [![Build Status](https://camo.githubusercontent.com/44bbed86ed4b5c8aa832534cc16452f397d9e54acc0d0f0c40e56e9aed94c33a/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e616f6d696a75622f65646e2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/naomijub/edn-rs)
*   [FlatBuffers](https://google.github.io/flatbuffers/)
    *   [frol/flatc-rust](https://github.com/frol/flatc-rust) — FlatBuffers compiler (flatc) integration for Cargo build scripts [![build badge](https://camo.githubusercontent.com/38180acb070be3e938f446275cec7b651c0cecd2d58ec4489092b13b33720204/68747470733a2f2f6170692e7472617669732d63692e6f72672f66726f6c2f666c6174632d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/frol/flatc-rust)
*   HAR
    *   [mandrean/har-rs](https://github.com/mandrean/har-rs) \[[har](https://crates.io/crates/har)\] — A HTTP Archive Format (HAR) serialization & deserialization library [![Build Status](https://camo.githubusercontent.com/282c6c261eea08b8b0cd9c5b58b4fd7eeb08f1de456e43b635ceb8db638c63ca/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d616e647265616e2f6861722d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mandrean/har-rs)
*   HTML
    *   [servo/html5ever](https://github.com/servo/html5ever) — High-performance browser-grade HTML5 parser [![build badge](https://camo.githubusercontent.com/d84ffa9d4299c9a28eb05d56b9a9cc9fc4f49e35c4cfb09a86f5c9cdd093db26/68747470733a2f2f6170692e7472617669732d63692e636f6d2f736572766f2f68746d6c35657665722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/servo/html5ever)
*   JSON
    *   [importcjj/rust-ajson](https://github.com/importcjj/rust-ajson) [\[ajson\]](https://crates.io/crates/ajson) — Get JSON values quickly [![build badge](https://camo.githubusercontent.com/112fc02a6f9b04bcf0abe9ac53c1d394ca5d91f14d3d16fe66d157fe0d8935b7/68747470733a2f2f6170692e7472617669732d63692e636f6d2f696d706f7274636a6a2f727573742d616a736f6e2e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/importcjj/rust-ajson)
    *   [maciejhirsz/json-rust](https://github.com/maciejhirsz/json-rust) \[[json](https://crates.io/crates/json)\] — JSON implementation in Rust [![build badge](https://camo.githubusercontent.com/3b00187cd2b513ed3dead46fd2c293b203b7def28e71c8c35e6cbb38ccebacf3/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d616369656a686972737a2f6a736f6e2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/maciejhirsz/json-rust)
    *   [pikkr/pikkr](https://github.com/pikkr/pikkr) \[[pikkr](https://crates.io/crates/pikkr)\] — JSON parser which picks up values directly without performing tokenization in Rust
    *   [serde-rs/json](https://github.com/serde-rs/json) \[[serde\_json](https://crates.io/crates/serde_json)\] — JSON support for [Serde](https://github.com/serde-rs/serde) framework [![build badge](https://camo.githubusercontent.com/07668c727e81ad9faf63f226f4f426fbcd80b6b71e17012b6642b4900b8f90f7/68747470733a2f2f6170692e7472617669732d63692e6f72672f73657264652d72732f6a736f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/serde-rs/json)
    *   [simd-lite/simd-json](https://github.com/simd-lite/simd-json) \[[simd-json](https://crates.io/crates/simd-json)\] — High performance JSON parser based on a port of simdjson
*   MsgPack
    *   [3Hren/msgpack-rust](https://github.com/3Hren/msgpack-rust) — A pure Rust low/high level MessagePack implementation [![build badge](https://camo.githubusercontent.com/269a589150e76f53ed96f3f439de463addc6265b76a3a62e97fa55c561b3e6b7/68747470733a2f2f6170692e7472617669732d63692e6f72672f334872656e2f6d73677061636b2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/3Hren/msgpack-rust)
*   PEM
    *   [jcreekmore/pem-rs](https://github.com/jcreekmore/pem-rs) \[[pem](https://crates.io/crates/pem)\] — A Rust based way to parse and encode PEM-encoded data [![build badge](https://camo.githubusercontent.com/dc0127da5bd093b4f5a34f74fc13c20681433a7fc96ad29aee4cba09a86d7498/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a637265656b6d6f72652f70656d2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jcreekmore/pem-rs)
*   ProtocolBuffers
    *   [stepancheg/rust-protobuf](https://github.com/stepancheg/rust-protobuf) — [![build badge](https://camo.githubusercontent.com/480f06194fe3cf20d7150e0e2034ef594a7bf9cf58549caf9fe6f86ea5840114/68747470733a2f2f6170692e7472617669732d63692e6f72672f73746570616e636865672f727573742d70726f746f6275662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/stepancheg/rust-protobuf)
    *   [tokio-rs/prost](https://github.com/tokio-rs/prost) — [![continuous integration](https://github.com/tokio-rs/prost/workflows/continuous%20integration/badge.svg?branch=master)](https://github.com/tokio-rs/prost/actions)
*   RON (Rusty Object Notation)
    *   [https://github.com/ron-rs/ron](https://github.com/ron-rs/ron) — [![build badge](https://camo.githubusercontent.com/cc4c12f4077c742242c7005372f95d878fba416fdd980ebb896886afa24edb61/68747470733a2f2f6170692e7472617669732d63692e6f72672f726f6e2d72732f726f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/https://github.com/ron-rs/ron)
*   Serde
    *   [vityafx/serde-aux](https://github.com/vityafx/serde-aux/) - additional tools for using with the serde library. [![CI](https://github.com/vityafx/serde-aux/actions/workflows/ci.yml/badge.svg)](https://github.com/vityafx/serde-aux/actions/workflows/ci.yml) [![Crates badge](https://camo.githubusercontent.com/107255d793507a6e968121a6c99241eda9d8fc636be9b645a6d7a1b3f54e2ffb/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f73657264652d6175782e737667)](https://crates.io/crates/serde-aux)
*   TOML
    *   [alexcrichton/toml-rs](https://github.com/alexcrichton/toml-rs) — [![build badge](https://camo.githubusercontent.com/0bbf1479dcf7c8115df29a7a41de76ff1c9ae68da40ae51d41fb34d0a33844ca/68747470733a2f2f6170692e7472617669732d63692e636f6d2f616c65786372696368746f6e2f746f6d6c2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/alexcrichton/toml-rs)
*   XML
    *   [Florob/RustyXML](https://github.com/Florob/RustyXML) — an XML parser written in Rust [![build badge](https://camo.githubusercontent.com/69554118f5f686ad03e17485caa5564d1b40db884428b87bf3deaada20aaea89/68747470733a2f2f6170692e7472617669732d63692e6f72672f466c6f726f622f5275737479584d4c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Florob/RustyXML)
    *   [media-io/yaserde](https://github.com/media-io/yaserde) — Yet Another Serializer/Deserializer specialized for XML [![build badge](https://camo.githubusercontent.com/fc19e7d43913ca6b2c5f55a9ffbffc353e39f4a74ee73d27e349b1dc846490bc/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d656469612d696f2f796173657264652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/media-io/yaserde)
    *   [netvl/xml-rs](https://github.com/netvl/xml-rs) — A streaming XML library [![build badge](https://camo.githubusercontent.com/c449c0db3e4ee0e087951f3931c54ff1e7bbf6f4451a18ddf231bcaf5399b947/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e6574766c2f786d6c2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/netvl/xml-rs)
    *   [shepmaster/sxd-document](https://github.com/shepmaster/sxd-document) — An XML library in Rust [![build badge](https://camo.githubusercontent.com/94f260832b96c46c18d84b15c9d0aa0fa31d48009c687f3a11ea0fa143f2ef59/68747470733a2f2f6170692e7472617669732d63692e6f72672f736865706d61737465722f7378642d646f63756d656e742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/shepmaster/sxd-document)
    *   [shepmaster/sxd-xpath](https://github.com/shepmaster/sxd-xpath) — An XPath library in Rust [![build badge](https://camo.githubusercontent.com/b52f8b93b83f55b9a50f5a6dd343798e38318ae8731163e36f588ecc36730746/68747470733a2f2f6170692e7472617669732d63692e6f72672f736865706d61737465722f7378642d78706174682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/shepmaster/sxd-xpath)
    *   [tafia/quick-xml](https://github.com/tafia/quick-xml) — High performance XML pull reader/writer [![build badge](https://camo.githubusercontent.com/61814ebeb5a461fe04440531324a15f1d997038cda5d075f51c36b67fc62b2c3/68747470733a2f2f6170692e7472617669732d63692e6f72672f74616669612f717569636b2d786d6c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tafia/quick-xml)
*   YAML
    *   [chyh1990/yaml-rust](https://github.com/chyh1990/yaml-rust) — The missing YAML 1.2 implementation for Rust. [![build badge](https://camo.githubusercontent.com/34bfb2b1240279038f441053ac23f914e69adecd206dd226221271c6f681990d/68747470733a2f2f6170692e7472617669732d63692e6f72672f63687968313939302f79616d6c2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/chyh1990/yaml-rust)
    *   [dtolnay/serde-yaml](https://github.com/dtolnay/serde-yaml) \[[serde\_yaml](https://crates.io/crates/serde_yaml)\] — YAML support for [Serde](https://github.com/serde-rs/serde) framework [![build](https://camo.githubusercontent.com/3ebf5062b2878a29ef6266e3f5ad8d113c82da0c694a04968218682ee57f9834/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f64746f6c6e61792f73657264652d79616d6c2f43492f6d6173746572)](https://github.com/dtolnay/serde-yaml/actions?query=branch%3Amaster)
    *   [vitiral/stfu8](https://github.com/vitiral/stfu8) \[[stfu8](https://crates.io/crates/stfu8)\] — Sorta Text Format in UTF-8 [![build badge](https://camo.githubusercontent.com/471ba361c0252bf8ce59c4fb0d79884e12f0c30800ba81fe319a0af31ec80646/68747470733a2f2f6170692e7472617669732d63692e6f72672f7669746972616c2f73746675382e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vitiral/stfu8)

### [](#filesystem)Filesystem

\[[filesystem](https://crates.io/keywords/filesystem)\]

*   Operations
    *   [pop-os/dbus-udisks2](https://github.com/pop-os/dbus-udisks2) \[[dbus-udisks2](https://crates.io/crates/dbus-udisks2)\] - UDisks2 DBus API
    *   [pop-os/sys-mount](https://github.com/pop-os/sys-mount) \[[sys-mount](https://crates.io/crates/sys-mount)\] — High level abstraction for the `mount` / `umount2` system calls.
    *   [vitiral/path\_abs](https://github.com/vitiral/path_abs) \[[path\_abs](https://crates.io/crates/path_abs)\] — Absolute serializable path types and associated methods. [![build badge](https://camo.githubusercontent.com/21d5bb2f548859bd7873f19d93c41200b813111f1ed8d5812606b292b8084bc2/68747470733a2f2f6170692e7472617669732d63692e6f72672f7669746972616c2f706174685f6162732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/webdesus/fs_extr://travis-ci.org/vitiral/path_abs)
    *   [webdesus/fs\_extra](https://github.com/webdesus/fs_extra) — expanding opportunities standard library std::fs and std::io [![build badge](https://camo.githubusercontent.com/07b3e232ed305ba22378f2ad3f9d879fc588dd6d9aeab16a643fdb5c9d6b8334/68747470733a2f2f6170692e7472617669732d63692e6f72672f77656264657375732f66735f65787472612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/webdesus/fs_extra)
*   Temporary Files
    *   [rust-lang-deprecated/tempdir](https://github.com/rust-lang-deprecated/tempdir) — temporary directory library [![build badge](https://camo.githubusercontent.com/bf488a9f8b523c421b9741b641ac99ac7637ff0e63fd42bb8507b18591fb9b56/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d6c616e672d646570726563617465642f74656d706469722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-lang-deprecated/tempdir)
    *   [Stebalien/tempfile](https://github.com/Stebalien/tempfile) — temporary file library [![build badge](https://camo.githubusercontent.com/304e59309d1a4e645b2f126ada69006eded5dfd169a0de9264efbd1578ca071c/68747470733a2f2f6170692e7472617669732d63692e6f72672f53746562616c69656e2f74656d7066696c652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Stebalien/tempfile)
    *   [Stebalien/xattr](https://github.com/Stebalien/xattr) \[[xattr](https://crates.io/crates/xattr)\] — list and manipulate unix extended file attributes [![build badge](https://camo.githubusercontent.com/35e234f415d61380400ee4115cbdd2f80a608dc38321c647742d6767e53fd7fb/68747470733a2f2f6170692e7472617669732d63692e6f72672f53746562616c69656e2f78617474722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Stebalien/xattr)
    *   [zboxfs/zbox](https://github.com/zboxfs/zbox) \[[zbox](https://crates.io/crates/zbox)\] — Zero-details, privacy-focused embeddable file system. [![build badge](https://camo.githubusercontent.com/75d7cee5b8b0794f8c6818403fc3e702928c48dcadb79d48aba1190ae766332a/68747470733a2f2f6170692e7472617669732d63692e6f72672f7a626f7866732f7a626f782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/zboxfs/zbox)

### [](#functional-programming)Functional Programming

\[[functional programming](https://crates.io/keywords/fp)\]

*   Prelude
    *   [JasonShin/fp-core.rs](https://github.com/JasonShin/fp-core.rs) — A library for functional programming in Rust
    *   [myrrlyn/tap](https://github.com/myrrlyn/tap) - Suffix-Position Pipeline Behavior

### [](#game-development)Game development

See also [Are we game yet?](https://arewegameyet.rs)

*   Allegro
    *   [SiegeLord/RustAllegro](https://github.com/SiegeLord/RustAllegro) — [Allegro 5](https://liballeg.org/) bindings [![build badge](https://camo.githubusercontent.com/b7f81af2745eefa891f96792faa90e11ec97ec00b8b420609642066019657be6/68747470733a2f2f6170692e7472617669732d63692e6f72672f53696567654c6f72642f52757374416c6c6567726f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/SiegeLord/RustAllegro)
*   [Awesome Quads](https://github.com/ozkriff/awesome-quads) — A curated list of links to miniquad/macroquad-related code & resources
*   [Awesome wgpu](https://github.com/rofrol/awesome-wgpu) — A curated list of wgpu code and resources
*   bracket-lib (previously RLTK)
    *   [bracket-lib](https://github.com/amethyst/bracket-lib) \[[bracket-lib](https://crates.io/crates/bracket-lib)\] - The Roguelike Toolkit (RLTK), implemented for Rust. [![Rust](https://github.com/amethyst/bracket-lib/actions/workflows/rust.yml/badge.svg)](https://github.com/amethyst/bracket-lib/actions/workflows/rust.yml)
*   Challonge
    *   [vityafx/challonge-rs](https://github.com/vityafx/challonge-rs) \[[challonge](https://crates.io/crates/challonge)\] — Client library for the Challonge REST API. Helps to organize tournaments. [![CI](https://github.com/vityafx/challonge-rs/actions/workflows/ci.yml/badge.svg)](https://github.com/vityafx/challonge-rs/actions/workflows/ci.yml)
*   Corange
    *   [lucidscape/corange-rs](https://github.com/lucidscape/corange-rs) — [Corange](https://github.com/orangeduck/Corange) bindings
*   Entity-Component Systems (ECS)
    *   [amethyst/specs](https://github.com/amethyst/specs) — Specs Parallel ECS [![build badge](https://camo.githubusercontent.com/3f487a1fe745a5e6affdcb47ee04e61c7c6cb1e65effab620c020d6634903550/68747470733a2f2f6170692e7472617669732d63692e6f72672f616d6574687973742f73706563732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/amethyst/specs)
    *   [legion](https://github.com/amethyst/legion) — A feature rich high performance ECS library with minimal boilerplate [![build badge](https://github.com/amethyst/legion/workflows/CI/badge.svg?branch=master)](https://github.com/amethyst/legion/actions)
*   Game Engines
    *   [Amethyst](https://amethyst.rs) — Data-oriented game engine - [![Crates.io](https://camo.githubusercontent.com/3fbd375d13286134eaa7426efb69787530b66c8455c93325e3a325a427f5d98b/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f616d657468797374)](https://crates.io/crates/amethyst) [![license](https://camo.githubusercontent.com/83d3746e5881c1867665223424263d8e604df233d0a11aae0813e0414d433943/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6c6963656e73652d4d49542d626c75652e737667)](https://github.com/amethyst/amethyst/blob/main/COPYING) [![Crates.io](https://camo.githubusercontent.com/80fba3ee843608bb559385e4338abdcd3e3cf956a6b8f0dbd66b0fb1cce02cce/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f616d6574687973742e737667)](https://crates.io/crates/amethyst)
    *   [Bevy](https://github.com/bevyengine/bevy) is a refreshingly simple data-driven game engine built in Rust. - [![Crates.io](https://camo.githubusercontent.com/fe403c1f013640f6a78617b79155ed3df66042f74918ef4305d7154b7c4d424b/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f626576792e737667)](https://crates.io/crates/bevy) [![license](https://camo.githubusercontent.com/83d3746e5881c1867665223424263d8e604df233d0a11aae0813e0414d433943/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6c6963656e73652d4d49542d626c75652e737667)](https://github.com/bevyengine/bevy/blob/main/LICENSE) [![Crates.io](https://camo.githubusercontent.com/c394677215ba5d5b4291703a798a74f3211789e83e6fcffce11c1ef4150f3c19/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f626576792e737667)](https://crates.io/crates/bevy)
    *   [ggez](https://github.com/ggez/ggez) — A lightweight game framework for making 2D games with minimum friction - [![Crates.io](https://camo.githubusercontent.com/56cdec065ea9084bfc9eb3383c4a7b949a0b588b4139a839ccadbe3457cc4018/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f6767657a2e737667)](https://crates.io/crates/ggez) [![license](https://camo.githubusercontent.com/83d3746e5881c1867665223424263d8e604df233d0a11aae0813e0414d433943/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6c6963656e73652d4d49542d626c75652e737667)](https://github.com/ggez/ggez/blob/master/LICENSE) [![Crates.io](https://camo.githubusercontent.com/1f5afe5f43a4f22a326a92369e2ea44ff6704aac5a2971eb924a328f60df2860/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f6767657a2e737667)](https://crates.io/crates/ggez)
    *   [harmony](https://github.com/StarArawn/harmony) — A modern 3D/2D game engine that uses wgpu
    *   [Kiss3d](http://kiss3d.org) — A Keep It Simple, Stupid 3d graphics engine written with Rust [![Crates.io](https://camo.githubusercontent.com/3405c7d3e4311b673fc5302e84ddff78a7a23941865ad3e0a078be0ac2c08b59/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f6b69737333642e737667)](https://crates.io/crates/kiss3d)
    *   [oxidator](https://github.com/Ruddle/oxidator) — A real time strategy game/engine written with Rust and WebGPU
    *   [Piston](https://www.piston.rs/) — [![Crates.io](https://camo.githubusercontent.com/a9829302928ceca4fec3587229b6aa7bba8e6f753d684ef01fd5a22a0829e049/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f706973746f6e2e7376673f7374796c653d666c61742d737175617265)](https://crates.io/crates/piston) [![Crates.io](https://camo.githubusercontent.com/6e1636bd2abb48d1a4ff356355cb35123d20ea712a1064c042fa073560d18a52/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f6c2f706973746f6e2e737667)](https://github.com/PistonDevelopers/piston/blob/master/LICENSE) [![Crates.io](https://camo.githubusercontent.com/88c7ec5746a14da0cfefbc1f560942aaaaa7e29bcd8e85408e10c6bffc6a7547/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f706973746f6e2e737667)](https://crates.io/crates/piston)
    *   [RG3D](https://rg3d.rs) — Rust Game engine 3D [![Crates.io](https://camo.githubusercontent.com/c00735c5cb6a962ea456dc826fd2a513f1f534c8c51fc0b56b1d235f518db6ee/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f726733642e737667)](https://crates.io/crates/rg3d) [![license](https://camo.githubusercontent.com/b41452d4a3f97ae0f3919cb4e8f0427735070e124d9950dde8482ca20e285ea3/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f6c2f726733642e737667)](https://github.com/FyroxEngine/Fyrox/blob/master/LICENSE.md) [![Crates.io](https://camo.githubusercontent.com/007952d5c9787bd6f9b6644d64a233498b96f301108b9054766c3d49ce892edd/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f726733642e737667)](https://crates.io/crates/rg3d)
    *   [Unrust](https://github.com/unrust/unrust) — unrust — A pure rust based (webgl 2.0 / native) game engine
*   [Godot](https://godotengine.org/)
    *   [godot-rust/godot-rust](https://github.com/godot-rust/godot-rust) \[[gdnative](https://crates.io/crates/gdnative)\] - Rust bindings to the Godot game engine [![CI](https://github.com/godot-rust/godot-rust/actions/workflows/full-ci.yml/badge.svg)](https://github.com/godot-rust/godot-rust/actions/workflows/full-ci.yml)
*   [SDL](http://www.libsdl.org/) \[[sdl](https://crates.io/keywords/sdl)\]
    *   [brson/rust-sdl](https://github.com/brson/rust-sdl) — SDL1 bindings [![build badge](https://camo.githubusercontent.com/aa2ceaf109484c1567694cdf17406e522d3cfb393a1db505e80ca231cb034829/68747470733a2f2f6170692e7472617669732d63692e6f72672f6272736f6e2f727573742d73646c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/brson/rust-sdl)
    *   [Rust-SDL2/rust-sdl2](https://github.com/Rust-SDL2/rust-sdl2) — SDL2 bindings [![build badge](https://camo.githubusercontent.com/8eae772c0495444decf529c09eafc1c6fd4fa165ea6422d9ae8cd09b80acf149/68747470733a2f2f6170692e7472617669732d63692e6f72672f527573742d53444c322f727573742d73646c322e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Rust-SDL2/rust-sdl2)
*   SFML
    *   [jeremyletang/rust-sfml](https://github.com/jeremyletang/rust-sfml) — [SFML](https://www.sfml-dev.org/) bindings
*   Tcod-rs
    *   [tomassedovic/tcod-rs](https://github.com/tomassedovic/tcod-rs) — Libtcod bindings for Rust.
    *   Warning: Not maintained anymore
*   Toornament-rs
    *   [vityafx/toornament-rs](https://github.com/vityafx/toornament-rs) - Toornament.com API bindings for Rust. [![CI](https://github.com/vityafx/toornament-rs/actions/workflows/ci.yml/badge.svg)](https://github.com/vityafx/toornament-rs/actions/workflows/ci.yml) [![Crates badge](https://camo.githubusercontent.com/32f013380906fe6044f05efe8ae9b1f1c03d8ec38104858a886bd277aa68dc3a/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f746f6f726e616d656e742e737667)](https://crates.io/crates/toornament)
*   Victorem
    *   [VictoremWinbringer/Victorem](https://github.com/VictoremWinbringer/Victorem) \[[Victorem](https://crates.io/crates/Victorem)\] — Easy UDP Game Server and UDP Client framework for creating simple 2D and 3D online game prototype [![build badge](https://camo.githubusercontent.com/69cbc7c24c15f014a943300cef80be9870375899e83ba897994b9651cab02bf0/68747470733a2f2f6170692e7472617669732d63692e6f72672f566963746f72656d57696e6272696e6765722f566963746f72656d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/VictoremWinbringer/Victorem)

### [](#geospatial)Geospatial

\[[geo](https://crates.io/keywords/geo), [gis](https://crates.io/keywords/gis)\]

*   [DaveKram/coord\_transforms](https://github.com/DaveKram/coord_transforms) \[[coord\_transforms](https://crates.io/crates/coord_transforms)\] — coordinate transformations (2-d, 3-d, and geospatial) [![build badge](https://camo.githubusercontent.com/e173cd0997d75f0c452cc0dc4dffcd40599481e136bc315c0f1ae2ed0c3fa3e0/68747470733a2f2f6170692e7472617669732d63692e6f72672f446176654b72616d2f636f6f72645f7472616e73666f726d732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/DaveKram/coord_transforms)
*   [Georust](https://github.com/georust) — geospatial tools and libraries written in Rust
*   [rust-reverse-geocoder](https://github.com/gx0r/rrgeo) — A fast, offline reverse geocoder in Rust, inspired by [thampiman/reverse-geocoder](https://github.com/thampiman/reverse-geocoder)
*   [vlopes11/geomorph](https://github.com/vlopes11/geomorph) \[[geomorph](https://crates.io/crates/geomorph)\] — conversion between UTM, LatLon and MGRS coordinates [![build badge](https://camo.githubusercontent.com/2a5e867f147259f467a37bacc97b038123f1d777f6261173d7c50da984464a32/68747470733a2f2f6170692e7472617669732d63692e6f72672f766c6f70657331312f67656f6d6f7270682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vlopes11/geomorph)

### [](#graphics-1)Graphics

\[[graphics](https://crates.io/keywords/graphics)\]

*   Font
    *   [RazrFalcon/rustybuzz](https://github.com/RazrFalcon/rustybuzz) - An incremental harfbuzz port to Rust [![build badge](https://camo.githubusercontent.com/09483d6145a9efa015e646da5c761ae4c77a0777c5c293e86c6dc75d11ba4c44/68747470733a2f2f6170692e7472617669732d63692e6f72672f52617a7246616c636f6e2f727573747962757a7a2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/RazrFalcon/rustybuzz)
    *   [redox-os/rusttype](https://github.com/redox-os/rusttype) — A pure Rust alternative to libraries like FreeType [![build badge](https://camo.githubusercontent.com/5cbc83a1f43e6f18b6431929511529ebd4925b2023a08b20c52391eeaae80508/68747470733a2f2f6170692e7472617669732d63692e6f72672f7265646f782d6f732f72757374747970652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/redox-os/rusttype)
*   [gfx-rs/gfx](https://github.com/gfx-rs/gfx) — A high-performance, bindless graphics API for Rust. [![build badge](https://camo.githubusercontent.com/fe4b94469538833bbd9c3a7045d196eeca87839a0865e1fdc1c66bbab97e77fc/68747470733a2f2f6170692e7472617669732d63692e6f72672f6766782d72732f6766782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/gfx-rs/gfx)
*   [gfx-rs/wgpu](https://github.com/gfx-rs/wgpu) - Native WebGPU implementation based on gfx-hal. [![build badge](https://github.com/gfx-rs/wgpu/workflows/CI/badge.svg?branch=master)](https://github.com/gfx-rs/wgpu/actions)
*   OpenGL \[[opengl](https://crates.io/keywords/opengl)\]
    *   [brendanzab/gl-rs](https://github.com/brendanzab/gl-rs) — [![build badge](https://camo.githubusercontent.com/cee8a0daf9f498fe5a450289eb8a3f85da1b2a9f2ebce12f867c202b94ec9cfa/68747470733a2f2f6170692e7472617669732d63692e6f72672f6272656e64616e7a61622f676c2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/brendanzab/gl-rs)
    *   [glium/glium](https://github.com/glium/glium) — safe OpenGL wrapper for the Rust language. [![build badge](https://camo.githubusercontent.com/aaf83f79a70f2ed9980e006194769d9a052d403ed0d7de068ebb255df4a66458/68747470733a2f2f6170692e7472617669732d63692e6f72672f676c69756d2f676c69756d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/glium/glium)
    *   [glutin](https://crates.io/crates/glutin) — Rust alternative to [GLFW](https://www.glfw.org/) [![build badge](https://camo.githubusercontent.com/fb36c5d3b8ca42bc0d60e9e2d9acbdbdbdfbd104bd6c3b15dbe7d0c14e037d3c/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d77696e646f77696e672f676c7574696e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-windowing/glutin)
    *   [Kiss3d](http://kiss3d.org) — draw simple geometric figures and play with them with one-liners [![build badge](https://camo.githubusercontent.com/f96689ca775c0b286b18af97c397c71b1b980bc74fdba381efb2cbbe4462ef58/68747470733a2f2f6170692e7472617669732d63692e6f72672f73656263726f7a65742f6b69737333642e7376673f6272616e63683d6d6173746572)](https://api.travis-ci.org/repositories/sebcrozet/kiss3d)
    *   [PistonDevelopers/glfw-rs](https://github.com/PistonDevelopers/glfw-rs) — [![build badge](https://camo.githubusercontent.com/4730f48cecbdbe0adc9cd21c5e21826cab0d32208ac49e8e8314d4d6a14f601e/68747470733a2f2f6170692e7472617669732d63692e6f72672f506973746f6e446576656c6f706572732f676c66772d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/PistonDevelopers/glfw-rs)
*   PDF
    *   [fschutt/printpdf](https://github.com/fschutt/printpdf) — PDF writing library [![build badge](https://camo.githubusercontent.com/bd1ea4ccd0628bb8c8d529330e0134fabdd344053edd89d7016c5462d27bd746/68747470733a2f2f6170692e7472617669732d63692e6f72672f667363687574742f7072696e747064662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/fschutt/printpdf)
    *   [J-F-Liu/lopdf](https://github.com/J-F-Liu/lopdf) — PDF document manipulation [![build badge](https://camo.githubusercontent.com/7cb8baf2e67002d49249541597241879280dcb60d91d781675ddb2d0945741ea/68747470733a2f2f6170692e7472617669732d63692e6f72672f4a2d462d4c69752f6c6f7064662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/J-F-Liu/lopdf)
    *   [kaj/rust-pdf](https://github.com/kaj/rust-pdf) — [![build badge](https://camo.githubusercontent.com/94a0dea66b29025f9236e2f8379cf152146dce878be305a06754333149ccaeb6/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b616a2f727573742d7064662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kaj/rust-pdf)
    *   [WASM-PDF](https://github.com/jussiniinikoski/wasm-pdf) – Generates PDF files with JavaScript and WASM (WebAssembly) [![build badge](https://camo.githubusercontent.com/c614161f43d38df44724573dc7dc2ad6596a834460a84e911eea36d6facf763f/68747470733a2f2f6170692e7472617669732d63692e6f72672f6a757373696e69696e696b6f736b692f7761736d2d7064662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/jussiniinikoski/wasm-pdf)
*   [Vulkan](https://www.vulkan.org/) \[[vulkan](https://crates.io/keywords/vulkan)\]
    *   [vulkano](https://github.com/vulkano-rs/vulkano) \[[vulkano](https://crates.io/crates/vulkano)\] — [![build badge](https://camo.githubusercontent.com/e33a5b74c17d1e655de5f567cea63dfbf8e696fe7c6a9ce882f37a8158b1d3f2/68747470733a2f2f6170692e7472617669732d63692e6f72672f76756c6b616e6f2d72732f76756c6b616e6f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vulkano-rs/vulkano)

### [](#gui)GUI

\[[gui](https://crates.io/keywords/gui)\]

*   [autopilot-rs/autopilot-rs](https://github.com/autopilot-rs/autopilot-rs) — A simple, cross-platform GUI automation library for Rust.
*   Cocoa
    *   [servo/core-foundation-rs](https://github.com/servo/core-foundation-rs) — [![build badge](https://camo.githubusercontent.com/b1579a0e7410da634c32ee29fb68df5c256efe9c778da86e7bae5b7e686b0fbc/68747470733a2f2f6170692e7472617669732d63692e636f6d2f736572766f2f636f72652d666f756e646174696f6e2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/servo/core-foundation-rs)
*   [Druid](https://github.com/linebender/druid) \[[druid](https://crates.io/crates/druid)\] — [Druid](https://linebender.org/druid/), a data-first Rust-native UI design toolkit. [![build badge](https://github.com/linebender/druid/workflows/.github/workflows/ci.yml/badge.svg)](https://github.com/linebender/druid/actions)
*   [emilk/egui](https://github.com/emilk/egui) - Simple, fast, and highly portable immediate mode GUI library for Rust. egui runs on the web, natively, and in your favorite game engine. [![Build Status](https://github.com/emilk/egui/workflows/CI/badge.svg)](https://github.com/emilk/egui/actions?workflow=CI)
*   [emoon/rust\_minifb](https://github.com/emoon/rust_minifb) — minifb is a cross-platform window setup with optional bitmap rendering. It also comes with easy mouse and keyboard input. Primarily designed for prototyping
*   [FLTK](https://www.fltk.org/)
    *   [fltk-rs](https://github.com/fltk-rs/fltk-rs) — FLTK Rust bindings [![Build](https://github.com/fltk-rs/fltk-rs/workflows/Build/badge.svg?branch=master)](https://github.com/fltk-rs/fltk-rs/actions)
*   [Flutter](https://flutter.dev/)
    *   [flutter-rs](https://github.com/flutter-rs/flutter-rs) — Build flutter desktop app in dart & rust.
*   [fschutt/azul](https://github.com/fschutt/azul) — A free, functional, IMGUI-oriented GUI framework for rapid development of desktop applications written in Rust, supported by the Mozilla WebRender rendering engine. [![build badge](https://camo.githubusercontent.com/2449fefa43073796990e1b5f51b202d13f6b94200085438429d29169722aec5a/68747470733a2f2f6170692e7472617669732d63692e6f72672f667363687574742f617a756c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/fschutt/azul)
*   [GTK+](https://www.gtk.org/) \[[gtk](https://crates.io/keywords/gtk)\]
    *   [gtk-rs/gtk3-rs](https://github.com/gtk-rs/gtk3-rs) - GTK3 binding for rust [![CI](https://github.com/gtk-rs/gtk3-rs/workflows/CI/badge.svg)](https://github.com/gtk-rs/gtk3-rs/workflows/CI/badge.svg)
    *   [relm](https://github.com/antoyo/relm) — Asynchronous, GTK+-based, GUI library, inspired by Elm [![build badge](https://camo.githubusercontent.com/700af10e981efe1535ad627c5e336f18090ef9dd65142ef8a9aa86c6591024c1/68747470733a2f2f6170692e7472617669732d63692e6f72672f616e746f796f2f72656c6d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/antoyo/relm)
*   [iced-rs/iced](https://github.com/iced-rs/iced) — A cross-platform GUI library for Rust focused on simplicity and type-safety. Inspired by Elm.
*   [ImGui](https://github.com/ocornut/imgui)
    *   [imgui-rs](https://github.com/imgui-rs/imgui-rs) — Rust bindings for ImGui [![Build Status](https://github.com/imgui-rs/imgui-rs/workflows/ci/badge.svg?branch=master)](https://github.com/imgui-rs/imgui-rs/actions)
*   [IUP](http://webserver2.tecgraf.puc-rio.br/iup/)
    *   [Kiss-ui](https://github.com/KISS-UI/kiss-ui) — A simple UI framework built on IUP [![Build Status](https://camo.githubusercontent.com/f21f69b711459ea0cef2fc5393751e66636c9df6d43596fa7d248af8a4049491/68747470733a2f2f6170692e7472617669732d63692e6f72672f63796265726765656b39342f6b6973732d75692e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cybergeek94/kiss-ui)
*   [ivanceras/sauron-native](https://github.com/ivanceras/sauron-native) - A truly native and cross platform GUI library. One unified code can be run as native GUI, Html Web and TUI. [![Build Status](https://camo.githubusercontent.com/a0498d93bb52b1154d311f3f33b5d3ed9cd3010b8b0ac736d68ae55d02a4fbbd/68747470733a2f2f6170692e7472617669732d63692e636f6d2f6976616e63657261732f736175726f6e2d6e61746976652e7376673f6272616e63683d6d6173746572)](https://app.travis-ci.com/github/ivanceras/sauron-native)
*   [libui](https://github.com/andlabs/libui)
    *   [rust-native-ui/libui-rs](https://github.com/rust-native-ui/libui-rs) — libui bindings [![build badge](https://camo.githubusercontent.com/10a05343c2c384b2c2c2d84f2cef17bbf953d843532c76923ed05954d587d1a8/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d6e61746976652d75692f6c696275692d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-native-ui/libui-rs).
*   [Nuklear](https://github.com/Immediate-Mode-UI/Nuklear)
    *   [nuklear-rust](https://github.com/snuk182/nuklear-rust) — Rust bindings for Nuklear
*   [OrbTk](https://github.com/redox-os/orbtk) — The Orbital Widget Toolkit is a multi platform (G)UI toolkit using SDL2 [![Build and test](https://github.com/redox-os/orbtk/workflows/build/badge.svg?branch=develop)](https://github.com/redox-os/orbtk/actions)
*   [PistonDevelopers/conrod](https://github.com/PistonDevelopers/conrod/) — An easy-to-use, immediate-mode, 2D GUI library written entirely in Rust [![build badge](https://camo.githubusercontent.com/c9e9ffe808a2e2acfd5dcc31586270f180d78c877831023f3ab168e5e0025383/68747470733a2f2f6170692e7472617669732d63692e6f72672f506973746f6e446576656c6f706572732f636f6e726f642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/PistonDevelopers/conrod)
*   [Qt](https://doc.qt.io)
    *   [cyndis/qmlrs](https://github.com/cyndis/qmlrs) — QtQuick bindings [![build badge](https://camo.githubusercontent.com/46c8af5751b59c21def2b16c70b8062c89de911c1a6a02bc3ca8580a728b2633/68747470733a2f2f6170692e7472617669732d63692e6f72672f63796e6469732f716d6c72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/cyndis/qmlrs)
    *   [rust-qt](https://github.com/rust-qt)
    *   [White-Oak/qml-rust](https://github.com/White-Oak/qml-rust) — QML bindings. [![build badge](https://camo.githubusercontent.com/77aad515c59bf23815f815bc2a55825f1c67b468a02e3b340544166e367b877d/68747470733a2f2f6170692e7472617669732d63692e6f72672f57686974652d4f616b2f716d6c2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/White-Oak/qml-rust)
    *   [woboq/qmetaobject-rs](https://github.com/woboq/qmetaobject-rs) — Integrate Qml and Rust by building the QMetaObject at compile time. [![build badge](https://camo.githubusercontent.com/fe50db53c8627acdc711192d295d292d8ff0d27e1d2a114e077fe8c626e3d36a/68747470733a2f2f6170692e7472617669732d63692e6f72672f776f626f712f716d6574616f626a6563742d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/woboq/qmetaobject-rs)
*   [rise-ui](https://github.com/rise-ui/rise) — Simple component-based cross-Platform GUI Toolkit for developing beautiful and user-friendly interfaces.
*   [saurvs/nfd-rs](https://github.com/saurvs/nfd-rs) — [nativefiledialog](https://github.com/mlabbe/nativefiledialog) bindings
*   [Sciter](https://sciter.com/)
    *   [sciter-sdk/rust-sciter](https://github.com/sciter-sdk/rust-sciter) — Sciter bindings [![build badge](https://camo.githubusercontent.com/76667f43751b6bfa7a5e8b97193f1e6bc33cd7af7bb6de4310e84cd02da4bfac/68747470733a2f2f63692e6170707665796f722e636f6d2f6170692f70726f6a656374732f7374617475732f6769746875622f7363697465722d73646b2f727573742d7363697465723f7376673d74727565)](https://ci.appveyor.com/project/sciter-sdk/rust-sciter)
*   [tauri-apps/tauri](https://github.com/tauri-apps/tauri) — Build smaller, faster, and more secure desktop applications with a web frontend, powered by [WRY](https://github.com/tauri-apps/wry). [![test library](https://camo.githubusercontent.com/541bf51b5a65e3abeab91c5e8e6106af28143983f10b7144b09921542a76ac78/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f74617572692d617070732f74617572692f746573742532306c6962726172793f6c6162656c3d746573742532306c696272617279)](https://github.com/tauri-apps/tauri/actions?query=workflow%3A%22test+library%22)
*   [tauri-apps/wry](https://github.com/tauri-apps/wry) - Webview Rendering librarY.

### [](#image-processing-2)Image processing

*   [abonander/img\_hash](https://github.com/abonander/img_hash) — Perceptual image hashing and comparison for equality and similarity. [![Build Status](https://camo.githubusercontent.com/874e4ce791740f8c5b79b55c3a33297be51235a7333aa783ff5a343d08577500/68747470733a2f2f6170692e7472617669732d63692e6f72672f61626f6e616e6465722f696d675f686173682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/abonander/img_hash)
*   [image-rs/image](https://github.com/image-rs/image) — Basic imaging processing functions and methods for converting to and from image formats [![build badge](https://camo.githubusercontent.com/50c75e0a703ac046bac14fcb354cf8f8a6d095ff797f6560c626a4a461d993ee/68747470733a2f2f6170692e7472617669732d63692e6f72672f696d6167652d72732f696d6167652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/image-rs/image)
*   [image-rs/imageproc](https://github.com/image-rs/imageproc) — An image processing library, based on the `image` library. [![Build Status](https://camo.githubusercontent.com/697a38edb09be86a0e71eab962bc93750c7f29143ce1eb10b47ca19a83bd2976/68747470733a2f2f6170692e7472617669732d63692e6f72672f696d6167652d72732f696d61676570726f632e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/image-rs/imageproc)
*   [rust-cv/cv](https://github.com/rust-cv/cv) — Rust CV is a project to implement computer vision algorithms, abstractions, and systems in Rust. #\[no\_std\] is supported where possible. [![build badge](https://github.com/rust-cv/cv/workflows/tests/badge.svg)](https://github.com/rust-cv/cv/workflows/tests/badge.svg)
*   [teovoinea/steganography](https://github.com/teovoinea/steganography) \[[steganography](https://crates.io/crates/steganography)\] — A simple steganography library [![build badge](https://camo.githubusercontent.com/da8471d67d2a2ef2df5b96659b064c4f79c91b71dec0fcbb2d6fd32e20d5f317/68747470733a2f2f6170692e7472617669732d63692e6f72672f74656f766f696e65612f73746567616e6f6772617068792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/teovoinea/steganography)
*   [twistedfall/opencv-rust](https://github.com/twistedfall/opencv-rust) — Rust bindings for OpenCV [![build badge](https://camo.githubusercontent.com/f7e2a5ef2c5843eecf7a817dcc3cfc3ae5ddf27e1f82e3acc86d63e6cd32070f/68747470733a2f2f6170692e7472617669732d63692e6f72672f7477697374656466616c6c2f6f70656e63762d727573742e7376673f6272616e63683d637632)](https://travis-ci.org/twistedfall/opencv-rust)

### [](#language-specification)Language specification

*   [shnewto/bnf](https://github.com/shnewto/bnf) — A library for parsing Backus–Naur form context-free grammars. [![build badge](https://camo.githubusercontent.com/a76d0be22bc3204441461d5b8225023c33f6480814965ced117444a41acc09a5/68747470733a2f2f6170692e7472617669732d63692e6f72672f73686e6577746f2f626e662e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/shnewto/bnf)

### [](#logging)Logging

\[[log](https://crates.io/keywords/log)\]

*   [estk/log4rs](https://github.com/estk/log4rs) — highly configurable logging framework modeled after Java's Logback and log4j libraries [![CircleCI](https://camo.githubusercontent.com/9156c3276f5aac0f26da09f2b510811f6429f0f67e481a16a4642ad7a07566dd/68747470733a2f2f636972636c6563692e636f6d2f67682f6573746b2f6c6f673472732e7376673f7374796c653d736869656c64)](https://app.circleci.com/pipelines/github/estk/log4rs)
*   [jesusprubio/leg](https://github.com/jesusprubio/leg) — Elegant print for lazy devs. Make your CLIs nicer with minimal effort. [![Build Status](https://github.com/jesusprubio/leg/workflows/CI/badge.svg)](https://github.com/jesusprubio/leg/actions/workflows/ci.yml)
*   [rust-lang/log](https://github.com/rust-lang/log) — Logging implementation for Rust [![Build Status](https://camo.githubusercontent.com/bb813333bbea3703b505e4e8b17b4af29ef29ae77dc9d77ccca73487cca69b3f/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d6c616e672f6c6f672e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-lang/log)
*   [seanmonstar/pretty-env-logger](https://github.com/seanmonstar/pretty-env-logger) — A pretty, easy-to-use logger for Rust. [![Build Status](https://camo.githubusercontent.com/ae49cbb57fe19e7daa9be50cd1730b12d45e2dbf89491ad91f37e27fed94a946/68747470733a2f2f6170692e7472617669732d63692e6f72672f7365616e6d6f6e737461722f7072657474792d656e762d6c6f676765722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/seanmonstar/pretty-env-logger)
*   [slog-rs/slog](https://github.com/slog-rs/slog) — Structured, composable logging for Rust [![Build Status](https://camo.githubusercontent.com/bcec7a085e02775e7d6d34fcded03c34f8a5dfd0de64d20101b11bfe3393df4f/68747470733a2f2f6170692e7472617669732d63692e6f72672f736c6f672d72732f736c6f672e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/slog-rs/slog)
*   [tokio-rs/tracing](https://github.com/tokio-rs/tracing) — An application level tracing framework for async-aware structured logging, error handling, metrics, and more [![Build Status](https://github.com/tokio-rs/tracing/workflows/CI/badge.svg?branch=master)](https://github.com/tokio-rs/tracing/actions?query=workflow%3ACI)

### [](#macro)Macro

*   cute
    *   [mattgathu/cute](https://github.com/mattgathu/cute) — Macro for Python-esque list comprehensions in Rust. [![Build Status](https://camo.githubusercontent.com/0f3bb5c0bd67a5a46951d9725d13b646b1d25f01d2fb28510ff8f187aa620c7f/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d61747467617468752f637574652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tensorflow/rust)
*   [Linq-in-Rust](https://github.com/StardustDL/Linq-in-Rust) - Macro and methods for C#-LINQ-like expressions. [![CI](https://github.com/StardustDL/Linq-in-Rust/workflows/CI/badge.svg?branch=master)](https://github.com/StardustDL/Linq-in-Rust/actions?query=workflow%3ACI)

### [](#markup-language)Markup language

*   CommonMark
    *   [raphlinus/pulldown-cmark](https://github.com/raphlinus/pulldown-cmark) — [CommonMark](https://commonmark.org/) parser in Rust

### [](#mobile)Mobile

[Geal/rust\_on\_mobile](https://github.com/Geal/rust_on_mobile)

*   Android
    *   [rust-windowing/android-rs-glue](https://github.com/rust-windowing/android-rs-glue) — glue between Rust and Android [![build badge](https://camo.githubusercontent.com/cd89bc40678540a5b194fafb864a5e20c104455f3355627facbd9961a6d2f709/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573742d77696e646f77696e672f616e64726f69642d72732d676c75652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-windowing/android-rs-glue)
*   Android / iOS
    *   [ivanschuetz/rust\_android\_ios](https://github.com/ivanschuetz/rust_android_ios) — An example of using a shared Rust lib for Android and iOS using rust-swig and cbindgen respectively.
*   iOS
    *   [TimNN/cargo-lipo](https://github.com/TimNN/cargo-lipo) — A cargo lipo subcommand which automatically creates a universal library for use with your iOS application. [![build badge](https://camo.githubusercontent.com/a67912c4faf7b509f1c2d8d0a1b5682bd10f8da1135c385ba372bb591edfb3a3/68747470733a2f2f6170692e7472617669732d63692e6f72672f54696d4e4e2f636172676f2d6c69706f2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/TimNN/cargo-lipo)

### [](#network-programming)Network programming

*   CoAP
    *   [Covertness/coap-rs](https://github.com/Covertness/coap-rs) — A [Constrained Application Protocol(CoAP)](https://datatracker.ietf.org/doc/html/rfc7252) library for Rust. [![build badge](https://camo.githubusercontent.com/bc11bfd5e9a6b217a3b05cd3f49b3625ab0d43ed2b8d49710372f015820c0756/68747470733a2f2f6170692e7472617669732d63692e6f72672f436f766572746e6573732f636f61702d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Covertness/coap-rs)
*   Docker
    *   [fussybeaver/bollard](https://github.com/fussybeaver/bollard) — Docker daemon API in Rust
*   FTP
    *   [mattnenterprise/rust-ftp](https://github.com/mattnenterprise/rust-ftp) — an [FTP](https://en.wikipedia.org/wiki/File_Transfer_Protocol) client for Rust [![build badge](https://camo.githubusercontent.com/4b01faf425e40be08d3db281427b46d24b57c5ef45f280d3f8a4708959e7b643/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6174746e656e74657270726973652f727573742d6674702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mattnenterprise/rust-ftp)
*   gRPC
    *   [tikv/grpc-rs](https://github.com/tikv/grpc-rs) — The gRPC library for Rust built on C Core library and futures [![Build Status](https://camo.githubusercontent.com/7c55e4f9f66a70e0d2269aab2c3ef384841685136444a6840865b4d5040c41d3/68747470733a2f2f6170692e7472617669732d63692e6f72672f74696b762f677270632d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tikv/grpc-rs)
*   IPNetwork
    *   [achanda/ipnetwork](https://github.com/achanda/ipnetwork) — A library to work with IP networks in pure Rust [![build badge](https://camo.githubusercontent.com/682b7315cef1c997032a94ac3f087a44d7c00cc6ca40ebd7a6ef6285f27c11da/68747470733a2f2f6170692e7472617669732d63692e6f72672f616368616e64612f69706e6574776f726b2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/achanda/ipnetwork)
    *   [candrew/netsim](https://github.com/canndrew/netsim) — A Rust library for network simulation and testing [![build badge](https://camo.githubusercontent.com/45efa91fb25efaf4ae048251c65d40372c2b4be682db8a99dba37d4147720236/68747470733a2f2f6170692e7472617669732d63692e6f72672f63616e6e647265772f6e657473696d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/canndrew/netsim)
*   Low level
    *   [actix/actix](https://github.com/actix/actix) — Actor library for Rust [![build badge](https://camo.githubusercontent.com/06917ab751bc253678ca24443a6994638071bf364515f57d10c21586ea4eea74/68747470733a2f2f6170692e7472617669732d63692e6f72672f61637469782f61637469782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/actix/actix)
    *   [dylanmckay/protocol](https://github.com/dylanmckay/protocol) — Custom TCP/UDP protocol definitions
    *   [libpnet/libpnet](https://github.com/libpnet/libpnet) — A cross-platform, low level networking [![build badge](https://camo.githubusercontent.com/ec3839acd33b25a11ae0924e65afea8ee91d74943dd64836878b2d6d0fdad025/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c6962706e65742f6c6962706e65742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/libpnet/libpnet)
    *   [smoltcp-rs/smoltcp](https://github.com/smoltcp-rs/smoltcp) — A standalone, event-driven TCP/IP stack that is designed for bare-metal, real-time systems [![build badge](https://camo.githubusercontent.com/bb5b32522edc6c8ba43501d0ee4ee59dc6d66882e91754717112282279f857d3/68747470733a2f2f6170692e7472617669732d63692e6f72672f736d6f6c7463702d72732f736d6f6c7463702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/smoltcp-rs/smoltcp)
    *   [tokio-rs/tokio](https://github.com/tokio-rs/tokio) — A network application framework for rapid development and highly scalable production deployments of clients and servers.
*   message-io
    *   [lemunozm/message-io](https://github.com/lemunozm/message-io) — Event-driven message library to build network applications easy and fast. Supports TCP, UDP and WebSockets. [![build badge](https://camo.githubusercontent.com/a5ea3ee2b5c80418381c3f8c7b1ad9f951e52f07bfe01f5add421f3722e89a88/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f6c656d756e6f7a6d2f6d6573736167652d696f2f6d6573736167652d696f2532306369)](https://github.com/lemunozm/message-io/actions?query=workflow%3A%22message-io+ci%22)
*   NanoMsg
    *   [thehydroimpulse/nanomsg.rs](https://github.com/thehydroimpulse/nanomsg.rs) — [nanomsg](https://nanomsg.org/) bindings [![build badge](https://camo.githubusercontent.com/01a12285d49578fd81d93c9dea0226420bca52f800d2af73e497fb91c60db0cb/68747470733a2f2f6170692e7472617669732d63692e6f72672f746865687964726f696d70756c73652f6e616e6f6d73672e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/thehydroimpulse/nanomsg.rs)
*   NATS
    *   [nats-io/nats.rs](https://github.com/nats-io/nats.rs) — Rust client for NATS, the cloud native messaging system. [![Build Status](https://github.com/nats-io/nats.rs/workflows/Rust/badge.svg?branch=master)](https://github.com/nats-io/nats.rs/actions)
*   Nng
    *   [neachdainn/nng-rs](https://gitlab.com/neachdainn/nng-rs) \[[Nng](https://crates.io/crates/nng)\] — [Nng (nanomsg v2)](https://nng.nanomsg.org/index.html) bindings [![build badge](https://camo.githubusercontent.com/9955dc586a91b520028de1f499dd44236fcb3fd2f88c2181a10dc67ae9c97a92/68747470733a2f2f6769746c61622e636f6d2f6e656163686461696e6e2f6e6e672d72732f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/neachdainn/nng-rs/-/pipelines)
*   NNTP
    *   [mattnenterprise/rust-nntp](https://github.com/mattnenterprise/rust-nntp) \[[nntp](https://crates.io/crates/nntp)\] — an [NNTP](https://en.wikipedia.org/wiki/Network_News_Transfer_Protocol) client for Rust [![build badge](https://camo.githubusercontent.com/cee4c5f3777027305034c2ae0effeb4062204e1b43a345a006f7b45739b51197/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6174746e656e74657270726973652f727573742d6e6e74702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mattnenterprise/rust-nntp)
*   P2P
    *   [libp2p/rust-libp2p](https://github.com/libp2p/rust-libp2p) — The Rust Implementation of libp2p networking stack. [![Circle CI](https://camo.githubusercontent.com/857798baf9b4c77b29a076c48893d041e19077f84aaf5df9864adcadc9370d14/68747470733a2f2f636972636c6563692e636f6d2f67682f6c69627032702f727573742d6c69627032702e7376673f7374796c653d737667)](https://app.circleci.com/pipelines/github/libp2p/rust-libp2p)
*   POP3
    *   [mattnenterprise/rust-pop3](https://github.com/mattnenterprise/rust-pop3) \[[pop3](https://crates.io/crates/pop3)\] — A [POP3](https://en.wikipedia.org/wiki/Post_Office_Protocol) client for Rust [![build badge](https://camo.githubusercontent.com/6de723edb5bdf570ad1a6db8dfe7426116e7bda746b290a792864a7831a570bb/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d6174746e656e74657270726973652f727573742d706f70332e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mattnenterprise/rust-pop3)
*   QUIC
    *   [cloudflare/quiche](https://github.com/cloudflare/quiche) — cloudflare implementation of the QUIC transport protocol and HTTP/3 [![build](https://camo.githubusercontent.com/d36de17f9d16c3917484170f6836d210c9398ed5d7ee726939c11d5c605e510e/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f636c6f7564666c6172652f7175696368652f537461626c65)](https://camo.githubusercontent.com/d36de17f9d16c3917484170f6836d210c9398ed5d7ee726939c11d5c605e510e/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f776f726b666c6f772f7374617475732f636c6f7564666c6172652f7175696368652f537461626c65)
    *   [mozilla/neqo](https://github.com/mozilla/neqo) — an Implementation of QUIC written in Rust
    *   [quinn-rs/quinn](https://github.com/quinn-rs/quinn) — Futures-based QUIC implementation in Rust [![build badge](https://camo.githubusercontent.com/e58807af295718d16b3a54f0b7ec753e0df4afdd4869b12b3994a2feb586695b/68747470733a2f2f6465762e617a7572652e636f6d2f646f6368746d616e2f50726f6a656374732f5f617069732f6275696c642f7374617475732f5175696e6e3f6272616e63684e616d653d6d6173746572)](https://dev.azure.com/dochtman/Projects/_build)
*   RPC
    *   [ENQT-GmbH/remoc](https://github.com/ENQT-GmbH/remoc) \[[remoc](https://crates.io/crates/remoc)\] - Remoc provides channels (broadcast, mpsc, oneshot, watch) similar to Tokio's and trait calling over any remote transport. [![build badge](https://github.com/ENQT-GmbH/remoc/actions/workflows/rust.yml/badge.svg?branch=master)](https://github.com/ENQT-GmbH/remoc/actions/workflows/rust.yml)
    *   [smallnest/rpcx-rs](https://github.com/smallnest/rpcx-rs) — A RPC library for Rust for developing microservices in easy and simple way. [![build badge](https://camo.githubusercontent.com/fe1fafb95335d792597cab8faaf5217a7abc2ba42c0313be84ff54df099769a4/68747470733a2f2f6170692e7472617669732d63692e6f72672f736d616c6c6e6573742f727063782d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/smallnest/rpcx-rs)
*   SSH
    *   [alexcrichton/ssh2-rs](https://github.com/alexcrichton/ssh2-rs) — [libssh2](https://www.libssh2.org/) bindings [![build badge](https://camo.githubusercontent.com/037a8856fb5d186056c944bec96d6e73cdca520d73a4c0d256f2ad69b4429eff/68747470733a2f2f6170692e7472617669732d63692e636f6d2f616c65786372696368746f6e2f737368322d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/alexcrichton/ssh2-rs)
    *   [Thrussh](https://pijul.org/thrussh) \[[thrussh](https://crates.io/crates/thrussh)\] — an SSH library written from scratch in Rust, backed by [libsodium](https://doc.libsodium.org/)
*   Stomp
    *   [zslayton/stomp-rs](https://github.com/zslayton/stomp-rs) — A [STOMP 1.2](http://stomp.github.io/stomp-specification-1.2.html) client implementation in Rust [![build badge](https://camo.githubusercontent.com/4913c386350e90cda5f1b661034529801473fd6888e64307713cdc284eed4d64/68747470733a2f2f6170692e7472617669732d63692e6f72672f7a736c6179746f6e2f73746f6d702d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/zslayton/stomp-rs)
*   uTP
    *   [meqif/rust-utp](https://github.com/meqif/rust-utp) — A [uTP](http://www.bittorrent.org/beps/bep_0029.html) (Micro Transport Protocol) library for Rust. [![build badge](https://camo.githubusercontent.com/e998656812226050021ff56ab774c2d9fe98da80eab424c708d7162578298936/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d657169662f727573742d7574702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/meqif/rust-utp)
*   ZeroMQ
    *   [erickt/rust-zmq](https://github.com/erickt/rust-zmq) — [ZeroMQ](https://zeromq.org/) bindings [![build badge](https://camo.githubusercontent.com/5416df8f07f14d5be2ec5af4e9fd2a932960331e894a60331b1676526a86551a/68747470733a2f2f6170692e7472617669732d63692e6f72672f657269636b742f727573742d7a6d712e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/erickt/rust-zmq)

### [](#parsing)Parsing

*   [Folyd/robotstxt](https://github.com/Folyd/robotstxt) - A native Rust port of Google's robots.txt parser and matcher C++ library
*   [freestrings/jsonpath](https://github.com/freestrings/jsonpath) — [JsonPath](https://goessner.net/articles/JsonPath/) engine written in Rust. Webassembly and Javascript support too [![Build Status](https://camo.githubusercontent.com/a85a78acfc9a606ae04b70dd5ff5a175e0fa112fda7ee12bdec02f76c9849d7a/68747470733a2f2f6170692e7472617669732d63692e6f72672f66726565737472696e67732f6a736f6e706174682e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/freestrings/jsonpath)
*   [Geal/nom](https://github.com/Geal/nom) — parser combinator library [![build badge](https://camo.githubusercontent.com/b0ca7a00249e596528b05d0782a65fb4d04cc9363cc3d29fb0aa9c03187c0f8b/68747470733a2f2f6170692e7472617669732d63692e6f72672f4765616c2f6e6f6d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Geal/nom)
*   [kevinmehall/rust-peg](https://github.com/kevinmehall/rust-peg) — Parsing Expression Grammar (PEG) parser generator
*   [lalrpop/lalrpop](https://github.com/lalrpop/lalrpop) — LR(1) parser generator for Rust [![Build status](https://camo.githubusercontent.com/e4f18bf3120a56820ca72d7e1aa43539924ebf93ff003cf2e13f198abe71f72e/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c616c72706f702f6c616c72706f702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lalrpop/lalrpop)
*   [m4rw3r/chomp](https://github.com/m4rw3r/chomp) – A fast monadic-style parser combinator [![build badge](https://camo.githubusercontent.com/3f984bcc23d2ff58a9d614d76c38b1d80372ba11c0e50550b65970f91741bfbb/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d34727733722f63686f6d702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/m4rw3r/chomp)
*   [Marwes/combine](https://github.com/Marwes/combine) — parser combinator library [![build badge](https://camo.githubusercontent.com/c7a50bf66067fe48cfb9c471e2a7e62eaf00fe59f0d47f6a3b3c074bda088146/68747470733a2f2f6170692e7472617669732d63692e6f72672f4d61727765732f636f6d62696e652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Marwes/combine)
*   [nrc/zero](https://github.com/nrc/zero) \[[zero](https://crates.io/crates/zero/)\] — zero-allocation parsing of binary data
*   [pest-parser/pest](https://github.com/pest-parser/pest) — The Elegant Parser [![Build Status](https://camo.githubusercontent.com/b9a93eb8d43308917538214653aafcc305914c73431fbac4314307905923e17c/68747470733a2f2f6170692e7472617669732d63692e6f72672f706573742d7061727365722f706573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/pest-parser/pest)
*   [ptal/oak](https://github.com/ptal/oak) — A typed PEG parser generator (compiler plugin)
*   [replicadse/wavefront\_rs](https://github.com/replicadse/wavefront_rs) — A parser for the Wavefront OBJ format. [![crates.io](https://camo.githubusercontent.com/f071bbeaf41a42e2c3933d46ff0d159f045adc82f900dacf23409a460766d2d4/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f7761766566726f6e745f72732e737667)](https://crates.io/crates/wavefront_rs) [![crates.io](https://camo.githubusercontent.com/aa469ced46ef9b15356af8698dbbe72b6c02f7eb5add36ee9b96577658ca5c2c/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f642f7761766566726f6e745f72733f6c6162656c3d6372617465732e696f253230646f776e6c6f616473)](https://crates.io/crates/wavefront_rs) [![build badge](https://github.com/replicadse/wavefront_rs/workflows/pipeline/badge.svg?branch=master)](https://github.com/replicadse/wavefront_rs/actions)
*   [s-panferov/queryst](https://github.com/s-panferov/queryst) — A query string parsing library for Rust inspired by [gs](https://github.com/ljharb/qs#readme)
*   [softdevteam/grmtools](https://github.com/softdevteam/grmtools/) - A LR parser with better error correction

### [](#peripherals)Peripherals

*   Serial Port
    *   [Susurrus/serialport-rs](https://gitlab.com/susurrus/serialport-rs) \[[serialport](https://crates.io/crates/serialport)\] — A cross-platform library that provides access to a serial port

### [](#platform-specific)Platform specific

*   Cross-platform
    *   [svartalf/rust-battery](https://crates.io/crates/battery) — Cross-platform information about the notebook batteries [![build badge](https://camo.githubusercontent.com/dd824c3169308614b037f387747e005faaa635c84d4f419c473948f36c33cbcd/68747470733a2f2f6170692e7472617669732d63692e6f72672f7376617274616c662f727573742d626174746572792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/svartalf/rust-battery)
    *   [vityafx/thread-priority](https://github.com/vityafx/thread-priority/) - Simple, crossplatform thread priority management. [![CI](https://github.com/vityafx/thread-priority/actions/workflows/ci.yml/badge.svg)](https://github.com/vityafx/thread-priority/actions/workflows/ci.yml) [![Crates badge](https://camo.githubusercontent.com/5dcfc670f750d7c5aef50bc500f1bb91ada9747aa3e6aad6ab362320df34031c/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f7468726561642d7072696f726974792e737667)](https://crates.io/crates/thread-priority)
*   FreeBSD
    *   [fubarnetes/libjail-rs](https://github.com/fubarnetes/libjail-rs/) \[[jail](https://crates.io/crates/jail)\] — Rust implementation of a FreeBSD jail library
*   Linux
    *   [arvancloud/nginx-rs](https://github.com/arvancloud/nginx-rs) — [Nginx](https://www.nginx.com) bindings [![build badge](https://camo.githubusercontent.com/5ee1687a5465d504b753b4ab6dc02b734d70a3563520677a48e58296ade93026/68747470733a2f2f6170692e7472617669732d63692e6f72672f617276616e636c6f75642f6e67696e782d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/arvancloud/nginx-rs)
    *   [hannobraun/inotify-rs](https://github.com/hannobraun/inotify-rs) — [inotify](https://en.wikipedia.org/wiki/Inotify) bindings [![Rust](https://github.com/hannobraun/inotify-rs/actions/workflows/rust.yml/badge.svg)](https://github.com/hannobraun/inotify-rs/actions/workflows/rust.yml)
    *   [pop-os/distinst](https://github.com/pop-os/distinst/) — Linux distribution installer
    *   [yaa110/rust-iptables](https://github.com/yaa110/rust-iptables) \[[iptables](https://crates.io/crates/iptables)\] — [iptables](https://www.netfilter.org/projects/iptables/index.html) bindings [![build badge](https://camo.githubusercontent.com/a593eb1b24e532c8e43d25a00ae777e721d4ab8cd626febe72eaf4c9b0c0479a/68747470733a2f2f6170692e7472617669732d63692e6f72672f7961613131302f727573742d69707461626c65732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/yaa110/rust-iptables)
*   Unix-like
    *   [nix-rust/nix](https://github.com/nix-rust/nix) — Unix-like API bindings [![Cirrus Build Status](https://camo.githubusercontent.com/4e9307fc8c48ac73b688e1f49b11542f14bdb0b588a5a8060d950aba19ce2749/68747470733a2f2f6170692e6369727275732d63692e636f6d2f6769746875622f6e69782d727573742f6e69782e737667)](https://cirrus-ci.com/github/nix-rust/nix)
    *   [zargony/fuse-rs](https://github.com/zargony/fuse-rs) — [FUSE](https://github.com/libfuse/libfuse) bindings
*   Windows
    *   [retep998/winapi-rs](https://github.com/retep998/winapi-rs) — Windows API bindings [![Rust](https://github.com/retep998/winapi-rs/actions/workflows/rust.yml/badge.svg?branch=dev)](https://github.com/retep998/winapi-rs/actions/workflows/rust.yml)

### [](#scripting)Scripting

\[[scripting](https://crates.io/keywords/scripting)\]

*   [duckscript](https://crates.io/crates/duckscript) — [Simple, extendable and embeddable scripting language.](https://github.com/sagiegurari/duckscript) [![build badge](https://camo.githubusercontent.com/9a038ecfb6006c898f74efe8d1b3cdab3713f9b42a69d894734339900274df7d/68747470733a2f2f6170692e7472617669732d63692e6f72672f73616769656775726172692f6475636b7363726970742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sagiegurari/duckscript)
*   [fleabitdev/gamelisp](https://github.com/fleabitdev/glsp) — A LISP-lisk scripting language for Rust game development
*   [gluon-lang/gluon](https://github.com/gluon-lang/gluon) — A small, statically-typed, functional programming language
*   [metacall/core](https://github.com/metacall/core) \[[metacall](https://crates.io/crates/metacall)\] — Cross-platform Polyglot Runtime which supports NodeJS, JavaScript, TypeScript, Python, Ruby, C#, Wasm, Java, Cobol and more. [![build badge](https://camo.githubusercontent.com/30479092e6f06337e8b2cdf642626036a07b95c604a7b094dc93f5f573861c2c/68747470733a2f2f6769746c61622e636f6d2f6d65746163616c6c2f636f72652f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/metacall/core)
*   [mun](https://github.com/mun-lang/mun) — A compiled, statically-typed scripting language with first class hot reloading support [![build badge](https://camo.githubusercontent.com/20319cefdcf79d016d9fcdf565b3db0ab8a3bcef65d34f09c68a2ba13181c7d7/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d756e2d6c616e672f6d756e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mun-lang/mun)
*   [murarth/ketos](https://github.com/murarth/ketos) — A Lisp dialect functional programming language serving as a scripting and extension language for rust
*   [PistonDevelopers/dyon](https://github.com/PistonDevelopers/dyon) — A rusty dynamically typed scripting language
*   [rhaiscript/rhai](https://github.com/rhaiscript/rhai) — A tiny and fast embedded scripting language resembling a combination of JavaScript and Rust [![build badge](https://github.com/rhaiscript/rhai/workflows/Build/badge.svg)](https://github.com/rhaiscript/rhai/actions)
*   [rune-rs/rune](https://github.com/rune-rs/rune) — An embeddable dynamic programming language for Rust

### [](#simulation)Simulation

\[[simulation](https://crates.io/keywords/simulation)\]

*   [nyx-space](https://crates.io/crates/nyx-space) - High fidelity, fast, reliable and validated astrodynamical toolkit library, used for spacecraft mission design and orbit determination [![Build Status](https://camo.githubusercontent.com/764690474d992fe0ed298806d41a10c3d32ff9e583d642270bba98abf7ccd6bc/68747470733a2f2f6769746c61622e636f6d2f6e79782d73706163652f6e79782f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/nyx-space/nyx/-/pipelines)

### [](#task-scheduling-1)Task scheduling

*   [delay-timer](https://github.com/BinChengZhao/delay-timer) — Time-manager of delayed tasks. Like crontab, but asynchronous tasks are possible. [![Build](https://github.com/BinChengZhao/delay-timer/actions/workflows/rust.yml/badge.svg)](https://github.com/BinChengZhao/delay-timer/actions)

### [](#template-engine)Template engine

*   Handlebars
    *   [botika/yarte](https://github.com/botika/yarte) — Yarte stands for **Y**et **A**nother **R**ust **T**emplate **E**ngine, is the fastest template engine. [![Build Status](https://camo.githubusercontent.com/bd8a24e48ee29e78f992afc1327e25e6292b5929901f2c54ba5bc30ae5f07d8b/68747470733a2f2f6170692e7472617669732d63692e6f72672f626f74696b612f79617274652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/botika/yarte)
    *   [sunng87/handlebars-rust](https://github.com/sunng87/handlebars-rust) — Handlebars template engine with inheritance, custom helper support. [![build badge](https://camo.githubusercontent.com/9bf13e1559268051264c0b956c1a913f0edffe376a2a2e4ea6b6e0a0f55d4356/68747470733a2f2f6170692e7472617669732d63692e6f72672f73756e6e6738372f68616e646c65626172732d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sunng87/handlebars-rust)
*   HTML
    *   [djc/askama](https://github.com/djc/askama) — template rendering engine based on Jinja [![build badge](https://camo.githubusercontent.com/f25194bbce1030c764a8e5bc08290f5b4f472116d1ca60e995132f690dca15d3/68747470733a2f2f6170692e7472617669732d63692e6f72672f646a632f61736b616d612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/djc/askama)
    *   [kaj/ructe](https://github.com/kaj/ructe) — HTML template system for Rust [![build badge](https://camo.githubusercontent.com/de56f347f3d4866b48c0ae2234c5c3c4d2cea702c272f2127404527becddf7aa/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b616a2f72756374652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/kaj/ructe)
    *   [Keats/tera](https://github.com/Keats/tera) — template engine based on Jinja2 and the Django template language. [![Actions Status](https://github.com/Keats/tera/workflows/ci/badge.svg?branch=master)](https://github.com/Keats/tera/actions)
    *   [lambda-fairy/maud](https://github.com/lambda-fairy/maud) — compile-time HTML templates [![build badge](https://camo.githubusercontent.com/7e04107c5e92406183b60648f90c0bec1f9dfc832081c8baa7be6a35acfe52a0/68747470733a2f2f6170692e7472617669732d63692e6f72672f6c616d6264612d66616972792f6d6175642e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/lambda-fairy/maud)
    *   [Stebalien/horrorshow-rs](https://github.com/Stebalien/horrorshow-rs) — compile-time HTML templates [![build badge](https://camo.githubusercontent.com/45d17c343e9f4e6f55bf445bd9138b402e693f9dc83c6dc002fe220a1e1863b6/68747470733a2f2f6170692e7472617669732d63692e6f72672f53746562616c69656e2f686f72726f7273686f772d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Stebalien/horrorshow-rs)
*   Mustache
    *   [rustache/rustache](https://github.com/rustache/rustache) — [![build badge](https://camo.githubusercontent.com/383a2adc1659ebe46d4f7ffdc174ab1012f4fc53151f3d9f090060a8cf7dde7a/68747470733a2f2f6170692e7472617669732d63692e6f72672f72757374616368652f72757374616368652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rustache/rustache)

### [](#text-processing-1)Text processing

*   [becheran/wildmatch](https://github.com/becheran/wildmatch) \[[wildmatch](https://crates.io/crates/wildmatch)\] — Simple string matching with questionmark- and star-wildcard operator [![Actions Status](https://github.com/becheran/wildmatch/workflows/Build/badge.svg?branch=master)](https://github.com/becheran/wildmatch/actions)
*   [BurntSushi/suffix](https://github.com/BurntSushi/suffix) — Linear time suffix array construction (with Unicode support) [![build badge](https://camo.githubusercontent.com/4bba8d1392e9375e458ca648fe0900887e67f82aab0bc2fa4202d5e65b870232/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f7375666669782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/suffix)
*   [BurntSushi/tabwriter](https://github.com/BurntSushi/tabwriter) — Elastic tab stops (i.e., text column alignment) [![build badge](https://camo.githubusercontent.com/ea69ca8cc13447f24a562f6e6045cd8b1d1a4f45b7bb2afcb31fb6989d2d5bf5/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f7461627772697465722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/tabwriter)
*   [Daniel-Liu-c0deb0t/triple\_accel](https://github.com/Daniel-Liu-c0deb0t/triple_accel) \[[triple\_accel](https://crates.io/crates/triple_accel)\] - Rust edit distance routines accelerated using SIMD; supports fast Hamming, Levenshtein, restricted Damerau-Levenshtein, etc. distance calculations and string search [![build badge](https://github.com/Daniel-Liu-c0deb0t/triple_accel/workflows/Test/badge.svg?branch=master)](https://github.com/Daniel-Liu-c0deb0t/triple_accel/actions)
*   [fancy-regex/fancy-regex](https://github.com/fancy-regex/fancy-regex) \[[fancy-regex](https://crates.io/crates/fancy-regex)\] - Regular expressions implementation designed to support a relatively rich set of features such as look-around and backtracking. [![crates](https://camo.githubusercontent.com/2d3a66df714e2cbb98b87ce0be0e699d321b3051eed8b99209295a95ab16e82d/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f66616e63792d72656765782e737667)](https://crates.io/crates/fancy-regex) [![build badge](https://github.com/fancy-regex/fancy-regex/workflows/ci/badge.svg)](https://github.com/fancy-regex/fancy-regex/actions/workflows/ci.yml)
*   [greyblake/whatlang-rs](https://github.com/greyblake/whatlang-rs) — Natural language detection library based on trigrams [![build badge](https://camo.githubusercontent.com/0626e1980d2f879bbdedb35595975fcb892b2936ab2bc060b6ab06dbc303bb3c/68747470733a2f2f6170692e7472617669732d63692e6f72672f67726579626c616b652f776861746c616e672d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/greyblake/whatlang-rs)
*   [Lucretiel/joinery](https://github.com/Lucretiel/joinery) \[[joinery](https://crates.io/crates/joinery)\] – Generic string + iterable joining [![build badge](https://camo.githubusercontent.com/e0f02d06f4c32adf030c2cb17c39d6ba2231acacac11b8ed36d4b6de08007183/68747470733a2f2f6170692e7472617669732d63692e6f72672f4c756372657469656c2f6a6f696e6572792e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Lucretiel/joinery)
*   [mgeisler/textwrap](https://github.com/mgeisler/textwrap) \[[textwrap](https://crates.io/crates/textwrap)\] — Word wrap text (with support for hyphenation) [![build badge](https://camo.githubusercontent.com/bdc1369cda013726f8c87853ef22bb1a896a778d719ccf5d5c1d2ef22ac50ca5/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d676569736c65722f74657874777261702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/mgeisler/textwrap)
*   [ps1dr3x/easy\_reader](https://github.com/ps1dr3x/easy_reader) — A reader that allows forwards, backwards and random navigations through the lines of huge files without consuming iterators [![build badge](https://camo.githubusercontent.com/b93b0f60c114e9750ef32460f4f3a4ea50af6354ef8f0eb390488dafcc8dd80c/68747470733a2f2f6170692e7472617669732d63692e6f72672f707331647233782f656173795f7265616465722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ps1dr3x/easy_reader)
*   [pwoolcoc/ngrams](https://github.com/pwoolcoc/ngrams) \[[ngrams](https://crates.io/crates/ngrams)\] — Construct [n-grams](https://en.wikipedia.org/wiki/N-gram) from arbitrary iterators [![build badge](https://camo.githubusercontent.com/c28cf56acd9ec7503eb451b96c4a29ea71084b93d32b472879e8aa7c0a09d5ea/68747470733a2f2f6170692e7472617669732d63692e6f72672f70776f6f6c636f632f6e6772616d732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/pwoolcoc/ngrams)
*   [rust-lang/regex](https://github.com/rust-lang/regex) — Regular expressions (RE2 style) [![build badge](https://camo.githubusercontent.com/a24e265a1ca3aeefec12cc03b8e3f945812e1920df944fa6f1d44ceefd2f01f3/68747470733a2f2f6170692e7472617669732d63692e636f6d2f727573742d6c616e672f72656765782e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rust-lang/regex)
*   [strsim-rs](https://crates.io/crates/strsim) — String similarity metrics [![build badge](https://camo.githubusercontent.com/7f6fb2ad55e53008e331bbbeb557b0ae17001a3b8932c62d50573a0d7143f00f/68747470733a2f2f6170692e7472617669732d63692e6f72672f6467756f2f73747273696d2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/dguo/strsim-rs)
*   [yaa110/rake-rs](https://github.com/yaa110/rake-rs) \[[rake](https://crates.io/crates/rake)\] — Multilingual implementation of RAKE algorithm for Rust [![build badge](https://camo.githubusercontent.com/951ed968d7248bb98ea763d05b5aab805647c8e1792b078081bcf4d84638ff30/68747470733a2f2f6170692e7472617669732d63692e6f72672f7961613131302f72616b652d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/yaa110/rake-rs)

### [](#text-search)Text search

*   [andylokandy/simsearch-rs](https://github.com/andylokandy/simsearch-rs) \[[simsearch](https://crates.io/crates/simsearch)\] — A simple and lightweight fuzzy search engine that works in memory, searching for similar strings
*   [BurntSushi/fst](https://github.com/BurntSushi/fst) \[[fst](https://crates.io/crates/fst)\] — [![build badge](https://camo.githubusercontent.com/82827c87ce8405bd0f0f6ded7205dff28a5e1b2881171308ccc8fe2620bbd416/68747470733a2f2f6170692e7472617669732d63692e6f72672f4275726e7453757368692f6673742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/BurntSushi/fst)
*   [CurrySoftware/perlin](https://github.com/CurrySoftware/perlin) \[[perlin](https://crates.io/crates/perlin)\]
*   [meilisearch/MeiliSearch](https://github.com/meilisearch/MeiliSearch) — Ultra relevant, instant and typo-tolerant full-text search API. [![Build Status](https://github.com/meilisearch/MeiliSearch/workflows/Cargo%20test/badge.svg?branch=master)](https://github.com/meilisearch/MeiliSearch/actions)
*   [minio/minsql](https://github.com/minio/minsql) — High-performance log search engine. [![build badge](https://camo.githubusercontent.com/053bdff057cf48e5d9709022fd352bc38d0e80dd01478806c4f0b2efacab9051/68747470733a2f2f6170692e7472617669732d63692e6f72672f6d696e696f2f6d696e73716c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/minio/minsql)
*   [tantivy](https://github.com/quickwit-inc/tantivy) \[[tantivy](https://crates.io/crates/tantivy)\] — [![Build Status](https://github.com/quickwit-inc/tantivy/actions/workflows/test.yml/badge.svg)](https://github.com/quickwit-inc/tantivy/actions/workflows/test.yml)

### [](#unsafe)Unsafe

*   [zerocopy](https://crates.io/crates/zerocopy) — Utilities for safely reinterpreting arbitrary byte sequences as native Rust types

### [](#virtualization-1)Virtualization

*   [beneills/quantum](https://github.com/beneills/quantum) — Advanced Rust quantum computer simulator [![build badge](https://camo.githubusercontent.com/55ba90d44abd55cd1044fc7eb5da3ff1c5120450665056b3dcc79ae320b1f669/68747470733a2f2f6170692e7472617669732d63692e6f72672f62656e65696c6c732f7175616e74756d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/beneills/quantum)
*   [chromium/chromiumos/platform/crosvm](https://chromium.googlesource.com/chromiumos/platform/crosvm/) CrOSVM — Enables Chrome OS to run Linux apps inside a fast, secure virtualized environment
*   [saurvs/hypervisor-rs](https://github.com/saurvs/hypervisor-rs) — Hardware-accelerated virtualization on OS X
*   [unicorn-rs/unicorn-rs](https://github.com/unicorn-rs/unicorn-rs) — Rust bindings for the unicorn CPU emulator [![Build Status](https://camo.githubusercontent.com/111d6708a0b47e2aa204f256506d5f26a714b0e7444b066aba1fc01e02d345a1/68747470733a2f2f6170692e7472617669732d63692e6f72672f656b73652f756e69636f726e2d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ekse/unicorn-rs)

### [](#web-programming)Web programming

See also [Are we web yet?](https://www.arewewebyet.org) and [Rust web framework comparison](https://github.com/flosse/rust-web-framework-comparison).

*   Client-side / WASM
    *   [cargo-web](https://crates.io/crates/cargo-web) — A Cargo subcommand for the client-side Web [![Build Status](https://camo.githubusercontent.com/9714c026395dfc471004653c39d8c95096937aee3841e8ca15d5c01b8ed856d3/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b6f7574652f636172676f2d7765622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/koute/cargo-web)
    *   [sauron](https://github.com/ivanceras/sauron) - Client side web framework which closely adheres to The Elm Architecture. [![Build Status](https://camo.githubusercontent.com/a21c62a575f5f5eb4489a0dc0833a950afddaf274f9080194da9e90db4bbd7b6/68747470733a2f2f6170692e7472617669732d63692e6f72672f6976616e63657261732f736175726f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/ivanceras/sauron)
    *   [seed](https://seed-rs.org/) — A Rust framework for creating web apps
    *   [stdweb](https://crates.io/crates/stdweb) — A standard library for the client-side Web [![Build Status](https://camo.githubusercontent.com/83cc1d4c3a68db12e9a441fc6aaf7fc66b6ce5f4497bf688e5f9878eb970033b/68747470733a2f2f6170692e7472617669732d63692e6f72672f6b6f7574652f7374647765622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/koute/stdweb)
    *   [yew](https://crates.io/crates/yew) — Rust framework for making client web apps
*   HTTP Client
    *   [alexcrichton/curl-rust](https://github.com/alexcrichton/curl-rust) — [libcurl](https://curl.se/libcurl/) bindings [![build badge](https://camo.githubusercontent.com/98b41bc5dfa225fa82be7919e234d73ac3a322baf6b90a79665289b183933d09/68747470733a2f2f6170692e7472617669732d63692e636f6d2f616c65786372696368746f6e2f6375726c2d727573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/alexcrichton/curl-rust)
    *   [async-graphql](https://github.com/async-graphql/async-graphql) - A GraphQL server library implemented in Rust [![Build Status](https://camo.githubusercontent.com/d693aa87bf1b74ff3e2d90eb8db5c7b12af6a7507d4a14cdb45850c060302052/68747470733a2f2f6465762e617a7572652e636f6d2f6772617068716c2d727573742f4772617068514c253230527573742f5f617069732f6275696c642f7374617475732f6772617068716c2d727573742e6a756e69706572)](https://dev.azure.com/graphql-rust/GraphQL%20Rust/_build/latest?definitionId=1)
    *   [DoumanAsh/yukikaze](https://gitlab.com/Douman/yukikaze) \[[yukikaze](https://crates.io/crates/yukikaze)\] — Beautiful and elegant Yukikaze is little HTTP client library based on hyper. [![build badge](https://camo.githubusercontent.com/f5195e8b01f91ab664ffc94023447a85b5f4b5ca4ca6812f8d13e8a694f5035f/68747470733a2f2f6769746c61622e636f6d2f446f756d616e2f79756b696b617a652f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/Douman/yukikaze)
    *   [graphql-client](https://github.com/graphql-rust/graphql-client) — Typed, correct GraphQL requests and responses in Rust. [![Github actions Status](https://github.com/graphql-rust/graphql-client/workflows/CI/badge.svg?branch=master)](https://github.com/graphql-rust/graphql-client/actions)
    *   [hyperium/hyper](https://github.com/hyperium/hyper) — an HTTP implementation [![CI](https://github.com/hyperium/hyper/workflows/CI/badge.svg?branch=master)](https://github.com/hyperium/hyper/actions?query=workflow%3ACI)
    *   [seanmonstar/reqwest](https://github.com/seanmonstar/reqwest) — an ergonomic HTTP Client for Rust. [![build badge](https://camo.githubusercontent.com/1f939d8a49a6554a874d911710e7aaf3002d095d564a3de9df8119ac123a32b2/68747470733a2f2f6170692e7472617669732d63692e6f72672f7365616e6d6f6e737461722f726571776573742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/seanmonstar/reqwest)
*   HTTP Server
    *   [actix/actix-web](https://github.com/actix/actix-web) — A lightweight async web framework for Rust with websocket support [![build badge](https://camo.githubusercontent.com/10835b98e1dc0656c2dd2b8a35d12f10d7438449c398556096d0d71f0ade66ed/68747470733a2f2f6170692e7472617669732d63692e6f72672f61637469782f61637469782d7765622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/actix/actix-web)
    *   [branca](https://crates.io/crates/branca) — A Pure Rust implementation of Branca for Authenticated and Encrypted API tokens. [![build badge](https://camo.githubusercontent.com/e79a4b6699594059b6a734909fe1e2174a0b403f668857b745c2e0f8d6c48dbe/68747470733a2f2f6170692e7472617669732d63692e6f72672f72657475726e2f6272616e63612e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/return/branca)
    *   [carllerche/tower-web](https://github.com/carllerche/tower-web) \[[tower-web](https://crates.io/crates/tower-web)\] — A fast, boilerplate free, web framework for Rust [![build badge](https://camo.githubusercontent.com/ba734c027c53e97f0063edfd163c8d5fd40e6232b27c507dfef276f52c3bbc63/68747470733a2f2f6170692e7472617669732d63692e6f72672f6361726c6c65726368652f746f7765722d7765622e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/carllerche/tower-web)
    *   [danclive/sincere](https://github.com/danclive/sincere) — A micro web framework for Rust(stable) based on hyper and multithreading. [![build badge](https://camo.githubusercontent.com/00170fed02129bde3969c339766460b3dedd3f776c0d3964a77a000e8703d656/68747470733a2f2f6170692e7472617669732d63692e6f72672f64616e636c6976652f73696e636572652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/danclive/sincere)
    *   [daogangtang/sapper](https://github.com/daogangtang/sapper) — A lightweight web framework built on async hyper, implemented in Rust language. [![build badge](https://camo.githubusercontent.com/d22664798f240572e5781eed29932ef3242fea85e824c3610a9a1ed7514c4275/68747470733a2f2f6170692e7472617669732d63692e6f72672f64616f67616e6774616e672f7361707065722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/daogangtang/sapper)
    *   [GildedHonour/frank\_jwt](https://github.com/GildedHonour/frank_jwt) — JSON Web Token implementation in Rust. [![build badge](https://camo.githubusercontent.com/e884c380554930b00dffa108c2dbde6427d005d2f67d01dd147333bbba203c39/68747470733a2f2f6170692e7472617669732d63692e6f72672f47696c646564486f6e6f75722f6672616e6b5f6a77742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/GildedHonour/frank_jwt)
    *   [Gotham](https://github.com/gotham-rs/gotham) — A flexible web framework that does not sacrifice safety, security or speed. [![build badge](https://camo.githubusercontent.com/4f7a1ffb45d47f8b15c72fc8b3cdf6a43bdd255b1e314cd438641d5f78da32e8/68747470733a2f2f6170692e7472617669732d63692e6f72672f676f7468616d2d72732f676f7468616d2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/gotham-rs/gotham)
    *   [handlebars-rust](https://github.com/sunng87/handlebars-rust) — an Iron web framework middleware. [![build badge](https://camo.githubusercontent.com/99a04aadbe6f7011fed6de30f7179f73714960f0950c3dc53345c8edec470540/68747470733a2f2f6170692e7472617669732d63692e6f72672f73756e6e6738372f68616e646c65626172732d69726f6e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/sunng87/handlebars-iron)
    *   [hyperium/hyper](https://github.com/hyperium/hyper) — an HTTP implementation [![CI](https://github.com/hyperium/hyper/workflows/CI/badge.svg?branch=master)](https://github.com/hyperium/hyper/actions?query=workflow%3ACI)
    *   [Iron](https://github.com/iron/iron) — A middleware-based server framework [![build badge](https://camo.githubusercontent.com/e884c380554930b00dffa108c2dbde6427d005d2f67d01dd147333bbba203c39/68747470733a2f2f6170692e7472617669732d63692e6f72672f47696c646564486f6e6f75722f6672616e6b5f6a77742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/GildedHonour/frank_jwt)
    *   [Juniper](https://github.com/graphql-rust/juniper) — GraphQL server library for Rust [![build badge](https://camo.githubusercontent.com/fc6d9901595a88f5d52853b849214ae503b671ec4336c92ad3c0910e6b5d17b8/68747470733a2f2f6170692e7472617669732d63692e6f72672f6772617068716c2d727573742f6a756e697065722e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/graphql-rust/juniper)
    *   [Nickel](https://github.com/nickel-org/nickel.rs/) — inspired by [Express](http://expressjs.com/) [![build badge](https://camo.githubusercontent.com/5321ced8764490fd6ab108a11be3376bef57b67c42f1ab304499673a19c6bf3f/68747470733a2f2f6170692e7472617669732d63692e6f72672f6e69636b656c2d6f72672f6e69636b656c2e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/nickel-org/nickel.rs)
    *   [Ogeon/rustful](https://github.com/Ogeon/rustful) — A RESTful web framework for Rust [![build badge](https://camo.githubusercontent.com/23c19b563c42c20b997f05a9ec2ea8fb82d1094a12faf019da122dd4585f25e0/68747470733a2f2f6170692e7472617669732d63692e6f72672f4f67656f6e2f7275737466756c2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/Ogeon/rustful)
    *   [oltdaniel/zap](https://github.com/oltdaniel/zap) — A lightning fast http framework for Rust
    *   [Rocket](https://github.com/SergioBenitez/Rocket) — Rocket is web framework for Rust (nightly) with a focus on ease-of-use, expressability, and speed [![build badge](https://camo.githubusercontent.com/444fe5c4eb9e4fd0f9ccbbde4d74ab6ada2363fedffc4a9f5fad6c7b01b17dd3/68747470733a2f2f6170692e7472617669732d63692e6f72672f53657267696f42656e6974657a2f526f636b65742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/SergioBenitez/Rocket)
    *   [Rustless](https://github.com/rustless/rustless) — A REST-like API micro-framework inspired by [Grape](https://github.com/ruby-grape/grape) and [Hyper](https://github.com/hyperium/hyper) [![build badge](https://camo.githubusercontent.com/8bc41b47fb98d119793ab601ffc3b3aa452094284da9eed7b4c8dcd03ae92f18/68747470733a2f2f6170692e7472617669732d63692e6f72672f727573746c6573732f727573746c6573732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/rustless/rustless)
    *   [Salvo](https://github.com/salvo-rs/salvo) — an easy to use webframework base on hyper and tokio. [![build build](https://github.com/salvo-rs/salvo/workflows/CI%20(Linux)/badge.svg?branch=master&event=push)](https://github.com/salvo-rs/salvo/actions)
    *   [Saphir](https://github.com/richerarc/saphir) — A progressive web framework with low-level control, without the pain.
    *   [tiny-http](https://github.com/tiny-http/tiny-http) — Low level HTTP server library [![build badge](https://camo.githubusercontent.com/a2e2d81f79f21dbd7fb8cef760becdc6925de32239995a39260b638593be6398/68747470733a2f2f6170692e7472617669732d63692e6f72672f74696e792d687474702f74696e792d687474702e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tiny-http/tiny-http)
    *   [tokio/axum](https://github.com/tokio-rs/axum) - Ergonomic and modular web framework built with Tokio, Tower, and Hyper [![Build badge](https://github.com/tokio-rs/axum/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/tokio-rs/axum/actions/workflows/CI.yml)
    *   [tomaka/rouille](https://github.com/tomaka/rouille) — Web framework in Rust [![build badge](https://camo.githubusercontent.com/77750dc58fba14e28990111f30f193fc58f5c08ba9d13efd2e6a7b76709ecc50/68747470733a2f2f6170692e7472617669732d63692e6f72672f746f6d616b612f726f75696c6c652e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/tomaka/rouille)
*   Miscellaneous
    *   [cargonauts](https://github.com/cargonauts-rs/cargonauts) — A web framework intended for building maintainable, well-factored web apps.
    *   [causal-agent/scraper](https://github.com/causal-agent/scraper) \[[scraper](https://crates.io/crates/scraper)\] - HTML parsing and querying with CSS selectors. [![Build Status](https://github.com/causal-agent/scraper/actions/workflows/test.yml/badge.svg?branch=master)](https://github.com/causal-agent/scraper/actions)
    *   [osohq/oso](https://github.com/osohq/oso) \[[oso](https://crates.io/crates/oso)\] - A policy engine for authorization that's embedded in your application. [![Build Status](https://github.com/osohq/oso/workflows/Development/badge.svg?branch=main)](https://github.com/osohq/oso/actions?query=branch%3Amain+workflow%3ADevelopment)
    *   [pwoolcoc/soup](https://gitlab.com/pwoolcoc/soup) \[[soup](https://crates.io/crates/soup)\] — A library similar to Python's BeautifulSoup, designed to enable quick and easy manipulation and querying of HTML documents. [![Build Status](https://camo.githubusercontent.com/fb2f394c0ac0cd25ae916a6dc93ed8a238e456a22e75648b38b901c1ef2da351/68747470733a2f2f6769746c61622e636f6d2f70776f6f6c636f632f736f75702f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/pwoolcoc/soup/badges/master/pipeline.svg)
    *   [pyros2097/rust-embed](https://github.com/pyros2097/rust-embed) — A macro to embed static assets into the rust binary
    *   [softprops/openapi](https://github.com/softprops/openapi) — A library for processing openapi spec files
    *   [tbot](https://gitlab.com/SnejUgal/tbot) \[[tbot](https://crates.io/crates/tbot)\] - Make cool Telegram bots with Rust easily [![pipeline status](https://camo.githubusercontent.com/43633ead0e47ee54071eabc9a1017d04cd587568877f93887a3dd50f300a9ed5/68747470733a2f2f6769746c61622e636f6d2f536e656a5567616c2f74626f742f6261646765732f6d61737465722f706970656c696e652e737667)](https://gitlab.com/SnejUgal/tbot/-/commits/master)
    *   [teloxide/teloxide](https://github.com/teloxide/teloxide/) - An elegant Telegram bots framework for Rust [![Build Status](https://github.com/teloxide/teloxide/workflows/Continuous%20integration/badge.svg?branch=master)](https://github.com/teloxide/teloxide/actions)
    *   [utkarshkukreti/select.rs](https://github.com/utkarshkukreti/select.rs) \[[select](https://crates.io/crates/select)\] — A library to extract useful data from HTML documents, suitable for web scraping. [![Build Status](https://camo.githubusercontent.com/132f0dc7f3f6910d7d43997c0eb2bd258df16a8850fcaa78e4a358eae594348d/68747470733a2f2f6170692e7472617669732d63692e6f72672f75746b617273686b756b726574692f73656c6563742e72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/utkarshkukreti/select.rs)
*   Reverse Proxy
    *   [sozu-proxy/sozu](https://github.com/sozu-proxy/sozu) \[[sozu](https://crates.io/crates/sozu)\] — A HTTP reverse proxy. [![CI](https://github.com/sozu-proxy/sozu/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/sozu-proxy/sozu/actions/workflows/ci.yml)
*   Static Site Generators
    *   [cobalt-org/cobalt.rs](https://github.com/cobalt-org/cobalt.rs) — Static site generator written in Rust [![Build Status](https://camo.githubusercontent.com/cf7b25e16e17eb4e34141173b63efa23731f4f6cff641148f939ff32806c22b4/68747470733a2f2f6465762e617a7572652e636f6d2f636f62616c742d6f72672f636f62616c742d6f72672f5f617069732f6275696c642f7374617475732f636f62616c742e72733f6272616e63684e616d653d6d6173746572)](https://dev.azure.com/cobalt-org/cobalt-org/_build?definitionId=2)
    *   [FuGangqiang/mdblog.rs](https://github.com/FuGangqiang/mdblog.rs) \[[mdblog](https://crates.io/crates/mdblog)\] — Static site generator from markdown files.
    *   [getzola/zola](https://github.com/getzola/zola) \[[zola](https://www.getzola.org/)\] — An opinionated static site generator with everything built-in. [![Build Status](https://camo.githubusercontent.com/49066c213c78770fb679aa5b982f79bb399f17a310f66d63e6012ba080dde2f2/68747470733a2f2f6465762e617a7572652e636f6d2f6765747a6f6c612f7a6f6c612f5f617069732f6275696c642f7374617475732f6765747a6f6c612e7a6f6c613f6272616e63684e616d653d6d6173746572)](https://dev.azure.com/getzola/zola/_build)
    *   [leven-the-blog/leven](https://github.com/leven-the-blog/leven) \[[leven](https://crates.io/crates/leven)\] — A simple, parallelized blog generator. [![build badge](https://camo.githubusercontent.com/9a6e838ad6f9cd00b89c73054ba0e46f6dabab0606dd99401eea883ec3870b87/68747470733a2f2f6170692e7472617669732d63692e6f72672f717561647275706c65736c61702f6c6576656e2e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/quadrupleslap/leven)
*   [WebSocket](https://datatracker.ietf.org/doc/rfc6455/)
    *   [actix/sockjs](https://github.com/actix/sockjs) — A [SockJS](https://github.com/sockjs) server for Rust [![build badge](https://camo.githubusercontent.com/4dfba35d62373f5d8f5bb56d39575ae7c20d4e8b22342137f5013c05c3a3d38d/68747470733a2f2f6170692e7472617669732d63692e6f72672f61637469782f736f636b6a732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/actix/sockjs)
    *   [housleyjk/ws-rs](https://github.com/housleyjk/ws-rs) — lightweight, event-driven WebSockets for Rust [![build badge](https://camo.githubusercontent.com/5aa9e7c357d4d4a87cbbef76677b2356fdffd0802da88bb084e8233422c24f61/68747470733a2f2f6170692e7472617669732d63692e6f72672f686f75736c65796a6b2f77732d72732e7376673f6272616e63683d737461626c65)](https://travis-ci.org/housleyjk/ws-rs)
    *   [rust-websocket](https://github.com/websockets-rs/rust-websocket) — A framework for dealing with WebSocket connections (both clients and servers) [![build badge](https://camo.githubusercontent.com/5f7d67b309d7cde476152411f887cb369108e51d9c109ae3e49a437ba4ff0dbd/68747470733a2f2f6170692e7472617669732d63692e6f72672f776562736f636b6574732d72732f727573742d776562736f636b65742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/websockets-rs/rust-websocket)
    *   [snapview/tungstenite-rs](https://github.com/snapview/tungstenite-rs) — Lightweight stream-based WebSocket implementation for Rust.
    *   [vi/websocat](https://github.com/vi/websocat) — CLI for interacting with WebSockets, with functionality of Netcat, Curl and Socat. [![build badge](https://camo.githubusercontent.com/fd8061503442ec1f3049f63c0bc8d6d57c1c696564832497190bde5084e9cee1/68747470733a2f2f6170692e7472617669732d63692e6f72672f76692f776562736f6361742e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/vi/websocat)
    *   [vityafx/urlshortener-rs](https://github.com/vityafx/urlshortener-rs) — A very simple urlshortener library for Rust. [![CI](https://github.com/vityafx/urlshortener-rs/actions/workflows/ci.yml/badge.svg)](https://github.com/vityafx/urlshortener-rs/actions/workflows/ci.yml) [![Crates badge](https://camo.githubusercontent.com/e236566202f1b56a31216a3b291339612990a95693ade6135a57a5e6e53c0b99/68747470733a2f2f696d672e736869656c64732e696f2f6372617465732f762f75726c73686f7274656e65722e737667)](https://crates.io/crates/urlshortener)

[](#registries)Registries
-------------------------

A registry allows you to publish your Rust libraries as crate packages, to share them with others publicly and privately.

*   [Cloudsmith ![heavy_dollar_sign](https://github.githubassets.com/images/icons/emoji/unicode/1f4b2.png)](https://cloudsmith.com/cargo-registry/) — A fully managed package management SaaS, with first-class support for public and private Cargo/Rust registries (plus many others). Has a generous free-tier and is also completely free for open-source.
*   [Crates](https://crates.io) — The official public registry for Rust/Cargo.
*   [w4/chartered](https://github.com/w4/chartered) - A private, authenticated, permissioned Cargo registry [![CI](https://github.com/w4/chartered/actions/workflows/ci.yml/badge.svg)](https://github.com/w4/chartered/actions/workflows/ci.yml)

[](#resources)Resources
-----------------------

*   Benchmarks
    *   [TeXitoi/benchmarksgame-rs](https://github.com/TeXitoi/benchmarksgame-rs) — Rust implementations for the [The Computer Language Benchmarks Game](https://benchmarksgame-team.pages.debian.net/benchmarksgame/) [![build badge](https://camo.githubusercontent.com/2ee06c32e9a861e09c521a69c1fa3707a44efe30aece3651d9883e95d0c5490e/68747470733a2f2f6170692e7472617669732d63692e6f72672f54655869746f692f62656e63686d61726b7367616d652d72732e7376673f6272616e63683d6d6173746572)](https://travis-ci.org/TeXitoi/benchmarksgame-rs)
*   Decks & Presentations
    *   [Learning systems programming with Rust](https://speakerdeck.com/jvns/learning-systems-programming-with-rust) — Presented by [Julia Evans](https://twitter.com/@b0rk) @ Rustconf 2016.
    *   [Rust: Hack Without Fear!](https://www.youtube.com/watch?v=lO1z-7cuRYI) — Presented by [Nicholas Matsakis](https://github.com/nikomatsakis) @ C++Now 2018
    *   [Shipping a Solid Rust Crate](https://www.youtube.com/watch?v=t4CyEKb-ywA) — Presented by [Michael Gattozzi](https://github.com/mgattozzi) @ RustConf 2017
*   Learning
    *   [Awesome Rust Streaming](https://github.com/jamesmunns/awesome-rust-streaming) - A community curated list of livestreams about Rust.
    *   [awesome-rust-mentors](https://rustbeginners.github.io/awesome-rust-mentors/) — A list of helpful Rust mentors willing to take mentees and eductate them about Rust and programming.
    *   [Build a language VM](https://blog.subnetzero.io/post/building-language-vm-part-00/)
    *   [Easy Rust](https://github.com/Dhghomon/easy_rust) - Learn Rust in easy English.
    *   [exercism.org](https://exercism.org/tracks/rust) — programming exercises that help you learn new concepts in Rust.
    *   [Hands-on Rust](https://pragprog.com/titles/hwrust/hands-on-rust/) - A hands-on guide to learning Rust by making games - by [Herbert Wolverson](https://github.com/thebracket/) (paid)
    *   [Idiomatic Rust](https://github.com/mre/idiomatic-rust) — A peer-reviewed collection of articles/talks/repos which teach idiomatic Rust.
    *   [Learning Rust With Entirely Too Many Linked Lists](https://rust-unofficial.github.io/too-many-lists/) — in-depth exploration of Rust's memory management rules, through implementing a few different types of list structures.
    *   [Programming Community Curated Resources for Learning Rust](https://hackr.io/tutorials/learn-rust) — A list of recommended resources voted by the programming community.
    *   [Refactoring to Rust](https://www.manning.com/books/refactoring-to-rust) - A book that introduces to Rust language.
    *   [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
    *   [Rust Cookbook](https://rust-lang-nursery.github.io/rust-cookbook/) — A collection of simple examples that demonstrate good practices to accomplish common programming tasks, using the crates of the Rust ecosystem.
    *   [Rust for professionals](https://overexact.com/rust-for-professionals/) — A quick introduction to Rust for experienced software developers.
    *   [Rust Gym](https://github.com/warycat/rustgym) - A big collection of coding interview problems solved in Rust.
    *   [Rust in Action](https://www.manning.com/books/rust-in-action) — A hands-on guide to systems programming with Rust by [Tim McNamara](https://github.com/timClicks) (paid)
    *   [Rust in Motion](https://www.manning.com/livevideo/rust-in-motion?a_aid=cnichols&a_bid=6a993c2e) — A video series by [Carol Nichols](https://github.com/carols10cents) and [Jake Goulding](https://github.com/shepmaster) (paid)
    *   [Rust Online Courses at Classpert](https://classpert.com/search/rust) — A list of Rust online courses (paid) from Classpert Online Course Search
    *   [rust-learning](https://github.com/ctjhoa/rust-learning) — A collection of useful resources to learn Rust
    *   [Rustlings](https://github.com/rust-lang/rustlings) — small exercises to get you used to reading and writing Rust code
    *   [stdx](https://github.com/brson/stdx) — Learn these crates first as an extension to std
    *   [University of Pennsylvania's Comp Sci Rust Programming Course](http://cis198-2016s.github.io/schedule/)
*   Podcasts
    *   [New Rustacean](https://newrustacean.com) — A podcast about learning Rust
    *   [Rustacean Station](https://rustacean-station.org/) — A community project for creating podcast content for Rust
*   [Rust Design Patterns](https://github.com/rust-unofficial/patterns)
*   [Rust Guidelines](http://aturon.github.io/)
*   [Rust Servers, Services and Apps - MEAP](https://www.manning.com/books/rust-servers-services-and-apps) - Build backend servers, services, and front-ends in Rust to get fast, reliable, and maintainable applications.
*   [Rust Subreddit](https://www.reddit.com/r/rust/) — A subreddit(forum) where rust related questions, articles and resources are posted and discussed
*   [RustBooks](https://github.com/sger/RustBooks) — list of RustBooks
*   [RustCamp 2015 Talks](https://www.youtube.com/playlist?list=PLE7tQUdRKcybdIw61JpCoo89i4pWU5f_t)
*   [RustViz](https://github.com/rustviz/rustviz) — generates visualizations from simple Rust programs to assist users in better understanding the Rust Lifetime and Borrowing mechanism.

[](#license)License
-------------------

[![CC0](https://camo.githubusercontent.com/9e918e1e7cd28a73246cf1c8d2c9903da3e487a65931c823a2391afe4b4a0d04/68747470733a2f2f6c6963656e7365627574746f6e732e6e65742f702f7a65726f2f312e302f38387833312e706e67)](https://creativecommons.org/publicdomain/zero/1.0/)