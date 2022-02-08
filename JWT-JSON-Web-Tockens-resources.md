JSON Web Tokens

JSON Web Tokens are an open, industry standard RFC 7519 method for representing claims securely between two parties.

JWT.IO allows you to decode, verify and generate JWT.

What is JSON Web Token?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

Although JWTs can be encrypted to also provide secrecy between parties, we will focus on signed tokens. Signed tokens can verify the integrity of the claims contained within it, while encrypted tokens hide those claims from other parties. When tokens are signed using public/private key pairs, the signature also certifies that only the party holding the private key is the one that signed it.


[](#awesome-jwt-json-web-tokens-)Awesome JWT (JSON Web Tokens) [![Awesome](https://camo.githubusercontent.com/abb97269de2982c379cbc128bba93ba724d8822bfbe082737772bd4feb59cb54/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f643733303566333864323966656437386661383536353265336136336531353464643865383832392f6d656469612f62616467652e737667)](https://github.com/sindresorhus/awesome)
==================================================================================================================================================================================================================================================================================================================================================================================================================================

[![](https://camo.githubusercontent.com/dd51cf3dbd56f3c69f73f26255f377384d4dec4665d884a56ae1fd6a7bda319c/687474703a2f2f6a77742e696f2f696d672f6c6f676f2d61737365742e737667)](https://jwt.io)

> A collection of awesome things regarding JSON Web Tokens.

_Please read the [contribution guidelines](/iamchathu/awesome-jwt/blob/master/contributing.md) before contributing._

[](#json-web-tokens)JSON Web Tokens
-----------------------------------

[JSON Web Tokens](https://en.wikipedia.org/wiki/JSON_Web_Token) are an open, industry standard [RFC 7519](https://tools.ietf.org/html/rfc7519) method for representing claims securely between two parties.

[](#contents)Contents
---------------------

*   [JSON Web Tokens](#json-web-tokens)
*   [Libraries](#libraries)
    *   [C](#c)
    *   [Clojure](#clojure)
    *   [Delphi](#delphi)
    *   [Elixir](#elixir)
    *   [Go](#go)
    *   [Java](#java)
    *   [JavaScript](#javascript)
    *   [Lua](#lua)
    *   [.Net](#net)
    *   [Node.js](#nodejs)
    *   [Objective-C](#objective-c)
    *   [Perl](#perl)
    *   [PHP](#php)
    *   [Python](#python)
    *   [Ruby](#ruby)
    *   [Rust](#rust)
    *   [Scala](#scala)
    *   [Swift](#swift)
*   [Tools](#tools)
*   [Tutorials](#tutorials)
*   [Articles](#articles)
*   [Videos](#videos)
*   [Presentations](#presentations)
*   [Podcasts](#podcasts)
*   [Books](#books)
*   [Blogs](#blogs)
*   [Courses](#courses)

* * *

[](#libraries)Libraries
-----------------------

### [](#c)C

*   [libjwt](https://github.com/benmcollins/libjwt) - C Library.

### [](#clojure)Clojure

*   [buddy](https://github.com/funcool/buddy/) - Security library for Clojure.

### [](#delphi)Delphi

*   [delphi-jose-jwt](https://github.com/paolo-rossi/delphi-jose-jwt) - Delphi implementation of JOSE and JWT.

### [](#elixir)Elixir

*   [json\_web\_token\_ex](https://github.com/garyf/json_web_token_ex) - Elixir implementation of the JSON Web Token (JWT) standard RFC 7519.
*   [joken](https://github.com/bryanjos/joken) - This library provides a convenient way to create, sign, verify, and validate JWTs while allowing the flexibility to customize each step along the way.
*   [jwtex](https://github.com/mschae/jwtex) - Library to encode and decode JWT tokens.
*   [plug\_jwt](https://github.com/bryanjos/plug_jwt) - Plug for JWT authentication.
*   [guardian](https://github.com/ueberauth/guardian) - Elixir Authentication.

### [](#go)Go

*   [jwt-go](https://github.com/dgrijalva/jwt-go) - Golang implementation of JSON Web Tokens (JWT).
*   [jose2go](https://github.com/dvsekhvalnov/jose2go) - Golang (GO) implementation of Javascript Object Signing and Encryption specification.
*   [jose](https://github.com/SermoDigital/jose) - Comprehensive set of JWT, JWS, and JWE libraries.
*   [jwt](https://github.com/robbert229/jwt) - This is an implementation of JWT in golang.
*   [go-jose](https://github.com/square/go-jose) - Implementation of JOSE standards (JWE, JWS, JWT) in Go.

### [](#java)Java

*   [java-jwt](https://github.com/auth0/java-jwt) - Java implementation of JSON Web Token (JWT).
*   [jose4j](https://bitbucket.org/b_c/jose4j/wiki/Home) - Implementation of JWT and the JOSE specification suite.
*   [Nimbus-JOSE-JWT](https://bitbucket.org/connect2id/nimbus-jose-jwt/wiki/Home) - Java library that implements the Javascript Object Signing and Encryption (JOSE) spec suite and the closely related JSON Web Token (JWT) spec.
*   [jJWT](https://github.com/jwtk/jjwt) - Java JWT: JSON Web Token for Java and Android.

### [](#javascript)JavaScript

*   [jsrsasign](https://github.com/kjur/jsrsasign) - The 'jsrsasign' (RSA-Sign JavaScript Library) is an opensource free cryptography library supporting RSA/RSAPSS/ECDSA/DSA signing/validation, ASN.1, PKCS#1/5/8 private/public key, X.509 certificate, CRL, OCSP, CMS SignedData, TimeStamp, CAdES JSON Web Signature/Token in pure JavaScript.
*   [angular2-jwt](https://github.com/auth0/angular2-jwt) - Helper library for handling JWTs in Angular 2 apps.
*   [jwt-decode](https://github.com/auth0/jwt-decode) - Decode JWT tokens, useful for browser applications.

### [](#lua)Lua

*   [lua-reasty-jwt](https://github.com/SkyLothar/lua-resty-jwt) - The Great Openresty's JWT.

### [](#net).Net

*   [jose-jwt](https://github.com/dvsekhvalnov/jose-jwt) - Ultimate Javascript Object Signing and Encryption (JOSE) and JSON Web Token (JWT) Implementation for .NET and .NET Core.
*   [jose-rt](https://github.com/dvsekhvalnov/jose-rt) - WinRT (Windows 8.1 and Windows Phone 8.1) implementation of Javascript Object Signing and Encryption (JOSE) and JSON Web Token (JWT).
*   [azure-activedirectory-identitymodel-extensions-for-dotnet](https://github.com/AzureAD/azure-activedirectory-identitymodel-extensions-for-dotnet) - IdentityModel extensions for .Net.
*   [Jwt.Net](https://github.com/jwt-dotnet/jwt) - Implementation for .NET.

### [](#nodejs)Node.js

*   [Node-jsonwebtoken](https://github.com/auth0/node-jsonwebtoken) - Implementation for Node.js.
*   [nJWT](https://github.com/jwtk/njwt) - Node.js JWT support.
*   [express-jwt](https://github.com/auth0/express-jwt) - Connect/express middleware that validates a JsonWebToken (JWT) and set the req.user with the attributes.
*   [express-jwt-authz](https://github.com/auth0/express-jwt-authz) - Validate the JWT scope to authorize access to an endpoint.
*   [express-jwt-permissions](https://github.com/MichielDeMey/express-jwt-permissions) - Express middleware for JWT permissions.
*   [socketio-jwt](https://github.com/auth0/socketio-jwt) - Authenticate socket.io incoming connections with JWTs.

### [](#objective-c)Objective-C

*   [JWT](https://github.com/yourkarma/JWT) - JSON Web Token implementation in Objective-C.

### [](#perl)Perl

*   [perl-Crypt-JWT](https://github.com/DCIT/perl-Crypt-JWT) - Implements JSON Web Token (JWT, JWS, JWE).

### [](#php)PHP

*   [php-jwt](https://github.com/firebase/php-jwt) - Simple library to encode and decode JSON Web Tokens (JWT) in PHP.

### [](#python)Python

*   [pyjwt](https://github.com/jpadilla/pyjwt/) - Implementation in Python.
*   [python-jose](https://github.com/mpdavis/python-jose/) - JOSE implementation in Python.

### [](#ruby)Ruby

*   [ruby-jwt](https://github.com/jwt/ruby-jwt) - Pure ruby implementation of the RFC 7519 OAuth JSON Web Token (JWT) standard.
*   [json-jwt](https://github.com/nov/json-jwt) - JSON Web Signature, JSON Web Encryption and JSON Web Key and JWT in Ruby.
*   [json\_web\_token](https://github.com/garyf/json_web_token) - Ruby implementation of the JSON Web Token (JWT) standard, RFC 7519.

### [](#rust)Rust

*   [frank\_jwt](https://github.com/GildedHonour/frank_jwt) - Implementation in Rust.

### [](#scala)Scala

*   [authentikat-jwt](https://github.com/jasongoodwin/authentikat-jwt) - JWT Scala Implementation, Claims based auth for Scala.
*   [jwt-scala](https://github.com/pauldijou/jwt-scala) - Support for Scala.
*   [jwt](https://github.com/iain-logan/jwt) - Scala implementation of the JWT specification.

### [](#swift)Swift

*   [JSONWebToken](https://github.com/kylef/JSONWebToken.swift) - Swift implementation of JSON Web Token (JWT).
*   [jwt](https://github.com/vapor/jwt) - Implementation in Swift.

[](#tools)Tools
---------------

*   [JWT.io](https://jwt.io) - Decode, verify and generate JWT online.
*   [JWT Debugger](https://chrome.google.com/webstore/detail/jwt-debugger/ppmmlchacdbknfphdeafcbmklcghghmd) - Chrome Extenstion for debugging JWT.
*   [JSONWebToken.io](https://www.jsonwebtoken.io/) - Encode or Decode JWTs online.
*   [JWT Inspector](https://www.jwtinspector.io/) - Chrome Extension to inspect JWT.

[](#tutorials)Tutorials
-----------------------

[](#articles)Articles
---------------------

*   [JWT Introduction](https://chathu.me/2017/08/28/jwt-introduction/) - Introduction to JSON Web Tokens.
*   [The Anatomy of a JSON Web Token](https://scotch.io/tutorials/the-anatomy-of-a-json-web-token) - Getting to know JSON Web Tokens.

[](#videos)Videos
-----------------

*   [JSON Web Token (JWT) Introduction by EggHead.io](https://egghead.io/lessons/angularjs-json-web-token-jwt-introduction) - Basic introduction to the mechanics of JWTs and the application we will be building in an AngularJS lesson series.

[](#presentations)Presentations
-------------------------------

*   [JSON Web Tokens](https://speakerdeck.com/thameera/json-web-tokens) - Presentation done at Colombo JS Meetup by Thameera Senanayaka.

[](#podcasts)Podcasts
---------------------

[](#books)Books
---------------

*   [JWT Handbook](https://auth0.com/e-books/jwt-handbook) - Learn everything you wanted to know about JSON Web Tokens.

[](#blogs)Blogs
---------------

[](#courses)Courses
-------------------

*   [Creating Apps With AngularJS, Node, and Token Authentication by Pluralsight](https://www.pluralsight.com/courses/creating-apps-angular-node-token-authentication) - Learn about Authentication, Authorization, and OAuth2 with Node Express and Angular.
*   [AngularJS Authentication with JWT by EggHead.io](https://egghead.io/courses/angularjs-authentication-with-jwt) - In this series, Kent will be building a simple application to get random user information from a node server with an Angular client.

* * *

**License**

[![CC0](https://camo.githubusercontent.com/80163f7b2e90d10162f1b595c71e432e245537c055de2dcf49846b5af8ab786a/687474703a2f2f6d6972726f72732e6372656174697665636f6d6d6f6e732e6f72672f70726573736b69742f627574746f6e732f38387833312f7376672f63632d7a65726f2e737667)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Chathu Vishwajith](https://chathu.me) has waived all copyright and related or neighboring rights to this work.