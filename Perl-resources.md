## Perl 

Perl is a family of two high-level, general-purpose, interpreted, dynamic programming languages. "Perl" refers to Perl 5, but from 2000 to 2019 it also referred to its redesigned "sister language", Perl 6, before the latter's name was officially changed to Raku in October 2019.[9][10]

Though Perl is not officially an acronym,[11] there are various backronyms in use, including "Practical Extraction and Reporting Language".[12] Perl was developed by Larry Wall in 1987 as a general-purpose Unix scripting language to make report processing easier.[13] Since then, it has undergone many changes and revisions. Raku, which began as a redesign of Perl 5 in 2000, eventually evolved into a separate language. Both languages continue to be developed independently by different development teams and liberally borrow ideas from each other.

The Perl languages borrow features from other programming languages including C, shell script (sh), AWK, and sed;[14] They provide text processing facilities without the arbitrary data-length limits of many contemporary Unix command line tools.[15] Perl 5 gained widespread popularity in the late 1990s as a CGI scripting language, in part due to its powerful regular expression and string parsing abilities.[16][17][18][19]

In addition to CGI, Perl 5 is used for system administration, network programming, finance, bioinformatics, and other applications, such as for GUIs. It has been nicknamed "the Swiss Army chainsaw of scripting languages" because of its flexibility and power,[20] and also its ugliness.[21] In 1998, it was also referred to as the "duct tape that holds the Internet together," in reference to both its ubiquitous use as a glue language and its perceived inelegance.[22]

Perl is a highly expressive programming language: source code for a given algorithm can be short and highly compressible.[23][24]

### [](#another-module-list)Another module list

We also recommend these lists.

*   [Task::Kensho](https://github.com/EnlightenedPerlOrganisation/task-kensho "Task::Kensho")
*   [Perlres - A list of resources about Perl](https://github.com/thibaultduponchelle/perlres)
*   [PerlMaven.com list of Perl Software](http://perlmaven.com/perl-based-open-source-products)
*   [Slaven's CPAN in a nutshell](https://github.com/eserte/srezic-misc/blob/master/cpan_in_a_nutshell/cpan_in_a_nutshell.pod)
*   Many Task::\*\* Modules. (ex. Task::Plack, Task::BeLike::...)

### [](#contents)Contents

*   [Awesome Perl](#awesome-perl)
    *   [Args](#args)
    *   [Audio](#audio)
        *   [Digital Signal Processing](#DSP)
    *   [Benchmarks](#benchmarks)
    *   [Caches](#caches)
    *   [Class Builder](#class-builder)
    *   [CLI](#cli)
    *   [Cloud](#cloud)
    *   [Cryptography](#cryptography)
    *   [Commercial WebServices](#commercial-webservices)
    *   [Container](#container)
    *   [Data Format](#data-format)
    *   [Database](#database)
    *   [Database Drivers](#database-drivers)
        *   [Relational Databases](#relational-databases)
        *   [NoSQL Databases](#nosql-databases)
    *   [Date & Time](#date--time)
    *   [Devices](#devices)
    *   [DevOps](#devops-tools)
    *   [Email](#email)
    *   [Event Loops](#event-loops)
    *   [Exception Handling](#exception-handling)
    *   [DOM Manipulation](#dom-manipulation)
    *   [File Manipulation](#file-manipulation)
    *   [Form Frameworks](#form-frameworks)
    *   [Images](#images)
    *   [List Manipulation](#list-manipulation)
    *   [Logging](#logging)
    *   [Module Development](#module-development)
    *   [Network](#network)
    *   [ORM](#orm)
    *   [Package Management](#package-management)
    *   [Processes and Threads](#processes-and-threads)
    *   [Profiling](#profiling)
    *   [Protocol](#protocol)
    *   [Queueing](#queueing)
    *   [REST Frameworks](#rest-frameworks)
    *   [Science/Numerics](#sciencenumerics)
    *   [Stream Manipulation](#stream-manipulation)
    *   [Template Engines](#template-engines)
    *   [Testing](#testing)
        *   [Testing Frameworks](#testing-frameworks)
        *   [Test Double](#test-double)
        *   [Coverage](#coverage)
    *   [Tools](#tools)
    *   [Type Checking](#type-checking)
    *   [Video](#video)
    *   [Web Frameworks](#web-frameworks)
        *   [Middlewares](#middlewares)
    *   [Web Frameworks-Like](#web-frameworks-like)
    *   [Web Scraping](#web-scraping)
    *   [Network Security](#Network-Security)
    *   [Digital Forensics](#Metadata-Forensics)
    *   [Reverse Engineering](#Reverse-Engineering)

[](#args)Args
-------------

_Libraries for argument manifestation and validation._

*   [Data::Validator](https://metacpan.org/pod/Data::Validator) - Rule based validator on type constraint system.
*   [Params::Util](https://metacpan.org/pod/Params::Util) - Simple, compact and correct param-checking functions.
*   [Params::ValidationCompiler](https://metacpan.org/pod/Params::ValidationCompiler) - Validate method/function parameters.
*   [Smart::Args](https://metacpan.org/pod/Smart::Args)

[](#audio)Audio
---------------

*   [Audio::CD](https://metacpan.org/pod/Audio::CD) - Interface to libcdaudio (cd + cddb)
*   [Audio::Wav](https://metacpan.org/pod/Audio::Wav) - Modules for reading & writing Microsoft WAV files.
*   [Audio::SndFile](https://metacpan.org/pod/Audio::SndFile) - Perl library for reading and writing sound files
*   [Audio::Ao](https://metacpan.org/pod/Audio::Ao) - A Perl wrapper for the Ao audio library
*   [MIDI::ALSA](https://metacpan.org/pod/MIDI::ALSA) - the perl ALSA library, plus some interface functions

### [](#dsp)DSP

*   [Audio::Analyzer](https://metacpan.org/pod/Audio::Analyzer) - Demodulate Audio through FFT and perl!
*   [Audio::Analyzer::ToneDetect](https://metacpan.org/pod/Audio::Analyzer::ToneDetect) - Detect freq of tones in an audio file or stream

[](#benchmarks)Benchmarks
-------------------------

_Libraries for benchmarking_

*   [Benchmark](https://metacpan.org/pod/Benchmark)
*   [Dumbbench](https://metacpan.org/pod/Dumbbench)
*   [Parallel::Benchmark](https://metacpan.org/pod/Parallel::Benchmark) - Benchmark in multiprocesses

[](#caches)Caches
-----------------

_Libraries to talk to Cache Softwares_

*   [CHI](https://metacpan.org/pod/CHI) - Unified cache handling interface, think DBI for caches
*   [CHI::Driver::DBI](https://metacpan.org/pod/CHI::Driver::DBI) - DBI driver for CHI
*   [CHI::Driver::DBIC](https://metacpan.org/pod/CHI::Driver::DBIC) - DBIx::Class driver for CHI
*   [CHI::Driver::Memcached](https://metacpan.org/pod/CHI::Driver::Memcached) - Memcached driver for CHI
*   [CHI::Driver::MongoDB](https://metacpan.org/pod/CHI::Driver::MongoDB) - MongoDB driver for CHI
*   [CHI::Driver::Redis](https://metacpan.org/pod/CHI::Driver::Redis) - Redis driver for CHI
*   [Catalyst::Plugin::Session::Store::CHI](https://metacpan.org/pod/Catalyst::Plugin::Session::Store::CHI) - Use CHI module to handle storage backend for session data
*   [CGI::Application::Plugin::CHI](https://metacpan.org/pod/CGI::Application::Plugin::CHI) - CGI-App plugin for CHI caching interface
*   [Mojolicious::Plugin::CHI](https://metacpan.org/pod/Mojolicious::Plugin::CHI) - Interact with CHI caches

[](#class-builder)Class Builder
-------------------------------

_Libraries to support writing classes and meta programming_

*   [Class::Accessor::Lite](https://metacpan.org/pod/Class::Accessor::Lite) - Simple accessor generator.
*   [Class::Accessor::Lite::Lazy](https://metacpan.org/pod/Class::Accessor::Lite::Lazy) - Generate lazy accessors.
*   [Homer](https://metacpan.org/pod/Homer) - Simple Prototype-based object system.
*   [Mo](https://metacpan.org/pod/Mo) - Micro Objects. Mo is less.
*   [Moo](https://metacpan.org/pod/Moo) - Class builder supporting meta programming.
*   [Moose](https://metacpan.org/pod/Moose) - The one and only, Moose.
*   [Mouse](https://metacpan.org/pod/Mouse) - Yet another class builder like Moo/Moose.
*   [Object::Pad](https://metacpan.org/pod/Object::Pad) - `class Example { has $x; method reader { return $x } }`, experimental proving-ground for [Cor](https://gist.github.com/Ovid/68b33259cb81c01f9a51612c7a294ede)
*   [Object::Tiny](https://metacpan.org/pod/Object::Tiny) - A class builder that is terse, fast, and tiny.

[](#cli)CLI
-----------

_Libraries for developing CLI applications_

*   [App::Cmd](https://metacpan.org/pod/App::Cmd) - Write command line apps with less suffering.
*   [Getopt::Long](https://metacpan.org/pod/Getopt::Long) - Extended processing of command line options.

[](#cloud)Cloud
---------------

*   [AWS::CloudFront](https://metacpan.org/pod/AWS::CloudFront) - Lightweight interface to Amazon CloudFront CDN
*   [AWS::S3](https://metacpan.org/pod/AWS::S3) - Lightweight interface to Amazon S3 (Simple Storage Service)
*   [Net::Amazon::EC2](https://metacpan.org/pod/Net::Amazon::EC2) - Interface to the Amazon Elastic Compute Cloud (EC2) environment.
*   [Net::AWS::SES](https://metacpan.org/pod/Net::AWS::SES) - Perl extension that implements Amazon Simple Email Service (SES) client
*   [WebService::DigitalOcean](https://metacpan.org/pod/WebService::DigitalOcean) - Access the DigitalOcean RESTful API (v2)
*   [WebService::Dropbox](https://metacpan.org/pod/WebService::Dropbox) - Interface to Dropbox API

[](#cryptography)Cryptography
-----------------------------

*   [Bitcoin::Crypto](https://metacpan.org/pod/Bitcoin::Crypto) - Bitcoin cryptography in Perl
*   [CryptX](https://metacpan.org/pod/CryptX) - Cryptographic toolkit

[](#commercial-webservices)Commercial WebServices
-------------------------------------------------

*   [Net::Xero](https://metacpan.org/pod/Net::Xero) - Interface to Xero accounting
*   [PagerDuty::Agent](https://metacpan.org/pod/PagerDuty::Agent) - A perl PagerDuty client
*   [WebService::Spotify](https://metacpan.org/pod/WebService::Spotify) - A simple interface to the Spotify Web API
*   [WebService::Xero](https://metacpan.org/pod/WebService::Xero) - Access Xero Accounting Package Public and Private Application API
*   [WWW::Shopify](https://metacpan.org/pod/WWW::Shopify) - object representing acess to a particular Shopify store
*   [WWW::Spotify](https://metacpan.org/pod/WWW::Spotify) - Spotify Web API Wrapper

[](#container)Container
-----------------------

_Libraries for Singleton Pattern implementation._

*   [Object::Container](https://metacpan.org/pod/Object::Container)

[](#data-format)Data Format
---------------------------

_Libraries for serializing, formatting and parsing_

*   [BSON](https://metacpan.org/pod/BSON) - Binary JSON format
*   [CBOR::Free](https://metacpan.org/pod/CBOR::Free) - Support for (CBOR)\[[https://tools.ietf.org/html/rfc7049](https://tools.ietf.org/html/rfc7049)\], IETF’s “binary JSON”
*   [Data::Dumper::Simple](https://metacpan.org/pod/Data::Dumper::Simple) - Reduce and faster Data::Dumper and eval() equivalent
*   [Data::MessagePack](https://metacpan.org/pod/Data::MessagePack)
*   [JSON::PP](https://metacpan.org/pod/JSON::PP)
*   [JSON::XS](https://metacpan.org/pod/JSON::XS)
*   [Sereal](https://metacpan.org/pod/Sereal)
*   [Storable](https://metacpan.org/pod/Storable)
*   [Text::CSV](https://metacpan.org/pod/Text::CSV)
*   [Text::CSV\_XS](https://metacpan.org/pod/Text::CSV_XS)
*   [Text::Markdown](https://metacpan.org/pod/Text::Markdown)
*   [TOML](https://metacpan.org/pod/TOML)
*   [XML::LibXML](https://metacpan.org/pod/XML::LibXML)
*   [XML::Compile::Schema](https://metacpan.org/pod/XML::Compile::Schema) - Interpret schema elements and types: create processors for XML messages.
*   [XML::Compile::SOAP](https://metacpan.org/pod/XML::Compile::SOAP) - Implements the SOAP 1.1 protocol, client side.
*   [XML::Compile::WSDL](https://metacpan.org/pod/XML::Compile::WSDL) - Use SOAP with a WSDL version 1.1 communication specification file.
*   [YAML](https://metacpan.org/pod/YAML)

[](#database)Database
---------------------

_Libraries for dealing with relational databases_

*   [DBI](https://metacpan.org/pod/DBI)
*   [DBIx::Connector](https://metacpan.org/pod/DBIx::Connector) - Fast, safe DBI connection and transaction management
*   [DBIx::Handler](https://metacpan.org/pod/DBIx::Handler) - Fork-safe DBI handler
*   [DBIx::Inspector](https://metacpan.org/pod/DBIx::Inspector)
*   [DBIx::QueryLog](https://metacpan.org/pod/DBIx::QueryLog)
*   [DBIx::Sunny](https://metacpan.org/pod/DBIx::Sunny) - Useful DBI Wrapper
*   [DBIx::TransactionManager](https://metacpan.org/pod/DBIx::TransactionManager)

[](#database-drivers)Database Drivers
-------------------------------------

_Libraries for using specific database products_

### [](#relational-databases)Relational Databases

*   [DBD::CSV](https://metacpan.org/pod/DBD::CSV)
*   [DBD::Firebird](https://metacpan.org/pod/DBD::Firebird)
*   [DBD::mysql](https://metacpan.org/pod/DBD::mysql)
*   [DBD::ODBC](https://metacpan.org/pod/DBD::ODBC) - Any ODBC Driver. MS-SQL w/ placeholders
*   [DBD::Oracle](https://metacpan.org/pod/DBD::Oracle) - Oracle database driver for the DBI module
*   [DBD::Pg](https://metacpan.org/pod/DBD::Pg) - PostgreSQL driver for DBI.
*   [DBD::SQLite](https://metacpan.org/pod/DBD::SQLite)
*   [DBD::Sybase](https://metacpan.org/pod/DBD::Sybase) - Sybase and MS-SQL. No placeholders w/ MS-SQL though

### [](#nosql-databases)NoSQL Databases

*   [Cache::Memcached::Fast](https://metacpan.org/pod/Cache::Memcached::Fast)
*   [Mango](https://metacpan.org/pod/Mango) - Pure-Perl non-blocking I/O MongoDB driver
*   [Redis](https://metacpan.org/pod/Redis)
*   [Redis::Fast](https://metacpan.org/pod/Redis::Fast) - Perl wrapper around hiredis driver
*   [Search::Elasticsearch](https://metacpan.org/pod/Search::Elasticsearch) - Offical Elasticsearch client library
*   [UnQLite](https://metacpan.org/pod/UnQLite)

[](#date--time)Date & Time
--------------------------

_Libraries for working with dates and times_

*   [DateTime](https://metacpan.org/pod/DateTime)
*   [Time::Moment](https://metacpan.org/pod/Time::Moment)
*   [Time::Piece](https://metacpan.org/pod/Time::Piece)

[](#devices)Devices
-------------------

_Libraries to talk to physical devices_

*   [Device::SerialPort](https://metacpan.org/pod/Device::SerialPort) - Generic Serial Port library for serial line communication
*   [Device::Modem](https://metacpan.org/pod/Device::Modem) - Talk to modem devices conneted via serial port
*   [Device::Onkyo](https://metacpan.org/pod/Device::Onkyo) - Control Onkyo/Integra AV equipment via LAN or Serial
*   [Chipcard::PCSC::Card](https://metacpan.org/pod/distribution/pcsc-perl/Card/Card.pod) - Control Smart card using perl and PCSC
*   [Device::XBee::API](https://metacpan.org/pod/Device::XBee::API) - Control XBee Device using pure perl code
*   [Device::Firmata](https://metacpan.org/pod/Device::Firmata) - module for controlling Firmata devices like Arduino

[](#devops-tools)DevOps Tools
-----------------------------

_Libraries that help when you want to deploy software across networks on several hosts/are working across computer networks_

*   [Rex](https://metacpan.org/pod/Rex) - Remote Execution

[](#email)Email
---------------

_Libraries that implement email creation and sending_

*   [Email::Sender](https://metacpan.org/pod/Email::Sender)
*   [Email::Reply](https://metacpan.org/pod/Email::Reply)
*   [Email::Stuffer](https://metacpan.org/pod/Email::Stuffer)

[](#event-loops)Event Loops
---------------------------

_Libraries for various event loops. Asynchronous programming if you like_

*   [AE](https://metacpan.org/pod/AE) - Simpler, faster, newer AnyEvent API
*   [AnyEvent](https://metacpan.org/pod/AnyEvent) - the DBI of event loop programming
*   [EV](https://metacpan.org/pod/EV) - Uses libev, very fast and popular. Default for AnyEvent if present
*   [Event](https://metacpan.org/pod/Event) - Works well, but older
*   [IO::Async](https://metacpan.org/pod/IO::Async) - Asynchronous event-driven programming
*   [POE](https://metacpan.org/pod/POE) - Common interface for several event loops
*   [Promise::XS](https://metacpan.org/pod/Promise::XS) - Promises in Perl

[](#exception-handling)Exception Handling
-----------------------------------------

_Libraries that assist with and/or provide alternatives to eval{ die() }_

*   [autodie](https://metacpan.org/pod/autodie) - Replace functions with ones that succeed or die with lexical scope
*   [Exception::Class](https://metacpan.org/pod/Exception::Class) - A module that allows you to declare real exception classes in Perl
*   [Syntax::Keyword::Try](https://metacpan.org/pod/Syntax::Keyword::Try) - a try/catch/finally syntax for perl
*   [Throwable](https://metacpan.org/pod/Throwable) - a role for classes that can be thrown
*   [Try::Tiny](https://metacpan.org/pod/Try::Tiny) - minimal try/catch with proper preservation of $@
*   [TryCatch](https://metacpan.org/pod/TryCatch) - first class try catch semantics for Perl, without source filters

[](#dom-manipulation)DOM Manipulation
-------------------------------------

*   [HTML5::DOM](https://metacpan.org/pod/HTML5::DOM) - Super fast html5 DOM library with css selectors (based on Modest/MyHTML).

[](#file-manipulation)File Manipulation
---------------------------------------

*   [File::Util](https://metacpan.org/pod/File::Util) - Easy, versatile, portable file handling.
*   [Path::Tiny](https://metacpan.org/pod/Path::Tiny) - Simple object-oriented file manipulation.

[](#form-frameworks)Form Frameworks
-----------------------------------

_Libraries that take the boredom & repetition out of (web and UI) forms_

*   [Catalyst::Controller::HTML::FormFu](https://metacpan.org/pod/Catalyst::Controller::HTML::FormFu) - Use HTML::FormFu in Catalyst.
*   [CGI::FormBuilder](https://metacpan.org/pod/CGI::FormBuilder) - Easily generate and process stateful forms.
*   [Form::Sensible](https://metacpan.org/pod/Form::Sensible) - A sensible way to handle form based user interface.
*   [Form::Tiny](https://metacpan.org/pod/Form::Tiny) - Forms reusing Type::Tiny type constraints.
*   [Form::Toolkit](https://metacpan.org/pod/Form::Toolkit) - A toolkit to build Data centric Forms.
*   [HTML::FormFu](https://metacpan.org/pod/HTML::FormFu) - HTML Form Creation, Rendering and Validation Framework.
*   [HTML::FormFu::ExtJS](https://metacpan.org/pod/HTML::FormFu::ExtJS) - ExtJS form generation from HTML::FormFu config files.
*   [HTML::FormHandler](https://metacpan.org/pod/HTML::FormHandler) - HTML forms using Moose.
*   [Mojolicious::Plugin::FormFields](https://metacpan.org/pod/Mojolicious::Plugin::FormFields) - Lightweight, flexible form builder with validation and filtering.
*   [WWW::Form](https://metacpan.org/pod/WWW::Form) - Simple and extendable module that allows developers to handle HTML form input validation and display flexibly and consistently.

[](#images)Images
-----------------

_Libraries for manipulating images_

*   [Image::Magick](https://metacpan.org/pod/Image::Magick) - An object-oriented interface to ImageMagick's image composing libraries.
*   [Imager](https://metacpan.org/pod/Imager)
*   [GD](https://metacpan.org/pod/GD) - Interface to Gd Graphics Library
*   [Image::Info](https://metacpan.org/pod/Image::Info) - Get image informations
*   [Image::PNG::Libpng](https://metacpan.org/pod/release/BKB/Image-PNG-Libpng-0.52_03/lib/Image/PNG/Libpng.pm) - Perl interface for libpng
*   [Graphics::TIFF](https://metacpan.org/pod/Graphics::TIFF) - Perl wrapper for libtiff
*   [Image::BMP](https://metacpan.org/pod/Image::BMP) - Perl bitmap image parser and viewer

[](#list-manipulation)List Manipulation
---------------------------------------

_Libraries for manipulation lists (arrays)_

*   [Array::Unique](https://metacpan.org/pod/Array::Unique) - Tie-able array that allows only unique values
*   [List::AllUtils](https://metacpan.org/pod/List::AllUtils) - Combines List::Util, List::SomeUtils and List::UtilsBy in one bite-sized package
*   [List::Compare](https://metacpan.org/pod/List::Compare) - Compare elements of two or more lists
*   [List::Gen](https://metacpan.org/pod/List::Gen) - Provides functions for generating lists
*   [List::MoreUtils](https://metacpan.org/pod/List::MoreUtils) - Provide the stuff missing in List::Util
*   [List::SomeUtils](https://metacpan.org/pod/List::SomeUtils) - Provide the stuff missing in List::Util
*   [List::Util](https://metacpan.org/pod/List::Util) - A selection of general-utility list subroutines
*   [List::UtilsBy](https://metacpan.org/pod/List::UtilsBy) - higher-order list utility functions

[](#logging)Logging
-------------------

_Libraries for generating and working with log files_

*   [Log::Dispatch](https://metacpan.org/pod/Log::Dispatch)
*   [Log::Log4perl](https://metacpan.org/pod/Log::Log4perl)
*   [Log::Minimal](https://metacpan.org/pod/Log::Minimal)

[](#module-development)Module Development
-----------------------------------------

_Libraries that simplify and improve Perl module development_

*   [Dist::Zilla](https://metacpan.org/pod/Dist::Zilla) - [http://dzil.org/](http://dzil.org/)
*   [Minilla](https://metacpan.org/pod/Minilla) - CPAN module authoring tool

[](#network)Network
-------------------

_Libraries that help when you are dealing with computer networks_

*   [DOCSIS::ConfigFile](https://metacpan.org/pod/DOCSIS::ConfigFile) - Decodes and encodes DOCSIS config files
*   [NetAddr::MAC](https://metacpan.org/pod/NetAddr::MAC) - Handle MAC addresses

_Libraries that help when you are working across computer networks_

*   [Net::SSH::Perl](https://metacpan.org/pod/Net::SSH::Perl) - SSH client implemented in Perl.
*   [Net::SSH2](https://metacpan.org/pod/Net::SSH2) - Wrapper for [libssh2](https://libssh2.org/).
*   [Net::OpenSSH](https://metacpan.org/pod/Net::OpenSSH) - Run commands remotely using the [OpenSSH](http://www.openssh.com/) client.
*   [Net::OpenSSH::Parallel](https://metacpan.org/pod/Net::OpenSSH::Parallel) - Run remote commands in parallel using the OpenSSH client.
*   [Net::SSH::Any](https://metacpan.org/pod/Net::SSH::Any) - Run remote commands using any module or binary client available.
*   [Net::SFTP::Foreign](https://metacpan.org/pod/Net::SFTP::Foreign) - SFTP client for remote file access.
*   [Object::Remote](https://metacpan.org/pod/Object::Remote) - Run Perl code on remote machines.
*   [Net::CLI::Interact](https://metacpan.org/pod/Net::CLI::Interact) - Automates interactive programs.
*   [Net::Appliance::Session](https://metacpan.org/pod/Net::Appliance::Session) - Automates interaction with appliances.

[](#orm)ORM
-----------

_Libraries that implement Object-Relational Mapping or datamapping techniques_

*   [DBIx::Class](https://metacpan.org/pod/DBIx::Class)
*   [Rose::DB](https://metacpan.org/pod/Rose::DB)
*   [Teng](https://metacpan.org/pod/Teng)

[](#package-management)Package Management
-----------------------------------------

_Libraries for package and dependency management_

*   [App::cpanminus](https://metacpan.org/pod/App::cpanminus)
*   [Carton](https://metacpan.org/pod/Carton)
*   [Pinto](https://metacpan.org/pod/Pinto) - Powerful local CPAN repos

[](#processes-and-threads)Processes and Threads
-----------------------------------------------

_Libraries for managing processes and threads_

*   [Parallel::ForkManager](https://metacpan.org/pod/Parallel::ForkManager) - A simple parallel processing fork manager
*   [Parallel::Prefork](https://metacpan.org/pod/Parallel::Prefork) - A simple prefork server framework
*   [Proclet](https://metacpan.org/pod/Proclet) - Minimalistic supervisor, a Perl port of [foreman](https://github.com/ddollar/foreman)

[](#profiling)Profiling
-----------------------

_Libraries for examining run-time activity of your program_

*   [Devel::KYTProf](https://metacpan.org/pod/Devel::KYTProf) - Very light profiler for I/Os such as HTTP request-responses and SQL queries.
*   [Devel::NYTProf](https://metacpan.org/pod/Devel::NYTProf) - Code profiler.

[](#protocol)Protocol
---------------------

_Protocol clients and libraries_

*   [Furl](https://metacpan.org/pod/Furl) - Faster HTTP(S) Client
*   [HTTP::Tiny](https://metacpan.org/pod/HTTP::Tiny) - Minimal and fast client. Included in the standard packages.
*   [LWP::UserAgent](https://metacpan.org/pod/LWP::UserAgent) - Popular HTTP(S) Client
*   [Net::Curl](https://metacpan.org/pod/Net::Curl) - (libcurl)\[[https://curl.se/libcurl/](https://curl.se/libcurl/)\] integration
*   [Net::DHCP](https://metacpan.org/pod/Net::DHCP) - Send and receive DHCP packets
*   [Net::DNS](https://metacpan.org/pod/Net::DNS) - Resolve DNS host names
*   [Protocol::DBus](https://metacpan.org/pod/Protocol::DBus) - D-Bus in (pure) Perl

[](#queueing)Queueing
---------------------

_Message Queue, Job Queue System.._

*   [Gearman](https://metacpan.org/pod/Gearman)
*   [Minion](https://docs.mojolicious.org/Minion) - Pure-Perl job queue
*   [Net::RabbitMQ](https://metacpan.org/pod/Net::RabbitMQ)
*   [Net::Stomp](https://metacpan.org/pod/Net::Stomp)
*   [Qudo](https://metacpan.org/pod/Qudo)
*   [Resque](https://metacpan.org/pod/Resque)
*   [TheSchwartz](https://metacpan.org/pod/TheSchwartz)

[](#sciencenumerics)Science/Numerics
------------------------------------

_Hand-picked modules for research, science, numerics and hyper-computing_

*   [BioPerl](https://metacpan.org/pod/BioPerl)
*   [Chart::Clicker](https://metacpan.org/pod/Chart::Clicker) - Powerful, extensible charting
*   [PDL](http://pdl.perl.org/)
*   [PDL (CPAN)](https://metacpan.org/pod/PDL)
*   [PDL::Graphics::Gnuplot](https://metacpan.org/pod/PDL::Graphics::Gnuplot)
*   [PDL::IO::\*](https://metacpan.org/search?q=PDL%3A%3AIO&size=20)
*   [PDL::LinearAlgebra](https://metacpan.org/pod/PDL::LinearAlgebra)
*   [PDL::Stats](https://metacpan.org/pod/PDL::Stats)
*   [Physics::\*](https://metacpan.org/search?q=physics%3A%3A&size=20)

[](#stream-manipulation)Stream Manipulation
-------------------------------------------

_Libraries for manipulating event streams_

*   [RxPerl](https://metacpan.org/pod/RxPerl) - Perl implementation of [Reactive Extensions](http://reactivex.io) / rxjs

[](#rest-frameworks)REST Frameworks
-----------------------------------

_Libraries for developing REST applications_

*   [Catalyst::Action::REST](https://metacpan.org/pod/Catalyst::Action::REST) - Automated REST Method Dispatching
*   [Dancer2::Plugin::REST](https://metacpan.org/pod/Dancer2::Plugin::REST) - A plugin for writing RESTful apps with Dancer2
*   [Dancer::Plugin::REST](https://metacpan.org/pod/Dancer::Plugin::REST) - A plugin for writing RESTful apps with Dancer
*   [Raisin](https://metacpan.org/pod/Raisin) - a REST API micro framework for Perl
*   [Squatting](https://metacpan.org/pod/Squatting) - A Camping-inspired Web Microframework for Perl

[](#template-engines)Template Engines
-------------------------------------

_Libraries and tools for templating_

*   [HTML::Template](https://metacpan.org/pod/HTML::Template) - Templates for web pages
*   [Template::Alloy](https://metacpan.org/pod/Template::Alloy) - TT2/3, HT, HTE, Tmpl, and Velocity Engine
*   [Template::Toolkit](https://metacpan.org/pod/Template::Toolkit) - Very Popular Template Processing System
*   [Text::MicroTemplate](https://metacpan.org/pod/Text::MicroTemplate) - Fast, simple and safe template engine written in pure-Perl and core modules.
*   [Text::MicroTemplate::Extended](https://metacpan.org/pod/Text::MicroTemplate::Extended) - Extended Text::MicroTemplate.
*   [Text::Template](https://metacpan.org/pod/Text::Template) - Templates with embedded perl
*   [Text::Xslate](https://metacpan.org/pod/Text::Xslate) - Faster template engine with XS. Supports multiple syntaxes.
*   [Tiffany](https://metacpan.org/pod/Tiffany) - Generic interface for template engines. It makes it easy to use multiple template engines.
*   [Template::Magic](https://metacpan.org/pod/Template::Magic) - Magic merger of runtime values with templates.

[](#testing)Testing
-------------------

_Libraries for testing codebases and generating test data._

### [](#testing-frameworks)Testing Frameworks

*   [Test::Base](https://metacpan.org/pod/Test::Base) - A Data Driven Testing Framework
*   [Test::Base::Less](https://metacpan.org/pod/Test::Base::Less) - Limited version of Test::Base
*   [Test::BDD::Cucumber](https://metacpan.org/pod/Test::BDD::Cucumber) - Implementation of the popular Cucumber framework in Perl
*   [Test::Class](https://metacpan.org/pod/Test::Class) - Class-based testing. Support "setup" and "teardown".
*   [Test::Deep](https://metacpan.org/pod/Test::Deep) - Test deep and complex data structures with great flexibility.
*   [Test::Deep::Matcher](https://metacpan.org/pod/Test::Deep::Matcher)
*   [Test::Harness](https://metacpan.org/pod/Test::Harness) - Run Perl standard test scripts with statistics
*   [Test::Kantan](https://metacpan.org/pod/Test::Kantan) - simple, flexible, fun "Testing framework"
*   [Test::More](https://metacpan.org/pod/Test::More)

### [](#test-double)Test Double

*   [Test::Exception](https://metacpan.org/pod/Test::Exception)
*   [Test::Fatal](https://metacpan.org/pod/Test::Fatal) - Simple module for verifying exceptions.
*   [Test::Mock::Guard](https://metacpan.org/pod/Test::Mock::Guard) - Mocking package subroutines.
*   [Test::MockTime](https://metacpan.org/pod/Test::MockTime)
*   [Test::mysqld](https://metacpan.org/pod/Test::mysqld)
*   [Test::TCP](https://metacpan.org/pod/Test::TCP) - Launch temporary TCP Server
*   [Test::Time](https://metacpan.org/pod/Test::Time) - Simple module for faking system time.

### [](#coverage)Coverage

*   [Devel::Cover](https://metacpan.org/pod/Devel::Cover)
*   [Devel::Cover::Report::Coveralls](https://metacpan.org/pod/Devel::Cover::Report::Coveralls) Report to Coveralls

[](#tools)Tools
---------------

_Some useful tools_

*   [App::Ack](https://metacpan.org/pod/App::Ack) - ack is a tool like grep, optimized for programmers.
*   [App::Nopaste](https://metacpan.org/pod/App::Nopaste) - Post to various pastebins from the CLI
*   [Daiku](https://metacpan.org/pod/Daiku) - Make for Perl.
*   [Data::Printer](https://metacpan.org/pod/Data::Printer) - Colored pretty-print of Perl data structures and objects.
*   [Reply](https://metacpan.org/pod/Reply) - Read-eval-print-loop(REPL) command-line tool.
*   [Riji](https://metacpan.org/pod/Riji) - Static site generator using markdown and git mainly for blogging.
*   [Smart::Comments](https://metacpan.org/pod/Smart::Comments) - Comments that do more than just sit there.

_Libraries for developping command line applications_

*   [Toolbox::Simple](https://metacpan.org/pod/Toolbox::Simple) - Simplfy some common tasks in Perl.
*   [Script::Toolbox](https://metacpan.org/pod/Script::Toolbox) - Framework for the daily business scripts.
*   [Devel::Kit](https://metacpan.org/pod/Devel::Kit)\- Handy toolbox of things to ease development/debugging.

_Libraries for handling configuration files_

*   [Config::Tiny](https://metacpan.org/pod/Config::Tiny) - Read/Write .ini style files with as little code as possible

[](#type-checking)Type checking
-------------------------------

*   [MooseX::Types](https://metacpan.org/pod/MooseX::Types) - Moose types management tool
*   [Type::Tiny](https://metacpan.org/pod/Type::Tiny) - Tiny, yet comprehensive type library

[](#video)Video
---------------

*   [FFmpeg](https://metacpan.org/pod/FFmpeg) - Interface to FFmpeg, a video converter written in C
*   [Video::Info](https://metacpan.org/pod/Video::Info) - Retrieve video properties such as: height width codec fps
*   [Vlc::Engine](https://metacpan.org/pod/Vlc::Engine) - use Vlc media player with Perl
*   [VideoLAN::LibVLC](https://metacpan.org/pod/VideoLAN::LibVLC) - Perl bindings for libvlc.so
*   [Video::Generator](https://metacpan.org/pod/Video::Generator) - Perl class for video generation

[](#web-frameworks)Web Frameworks
---------------------------------

_Libraries for developing Web applications_

*   [Amon2](https://metacpan.org/pod/Amon2)
*   [Catalyst](https://metacpan.org/pod/Catalyst) - Overflowing with features. Very popular.
*   [Dancer](https://metacpan.org/pod/Dancer) ([Official site](http://perldancer.org/))
*   [Dancer2](https://metacpan.org/pod/Dancer2)
*   [Gantry](https://metacpan.org/pod/Gantry) - Web application framework for mod\_perl, cgi, etc.
*   [Kelp](https://metacpan.org/pod/Kelp) - Plack-focused Perl web framework
*   [Kossy](https://metacpan.org/pod/Kossy) - A Web framework with simple interface.
*   [Mojolicious](https://metacpan.org/pod/Mojolicious) - An all in one framework.
*   [Poet](https://metacpan.org/pod/Poet) - a modern Perl web framework for Mason developers

### [](#middlewares)Middlewares

_Libraries for creating HTTP middlewares_

*   [Gazelle](https://metacpan.org/pod/Gazelle) - Preforked Plack Handler for performance freaks
*   [Plack](https://metacpan.org/pod/Plack) - PSGI server implementation and utilities for Web applications.
*   [Server::Starter](https://metacpan.org/pod/Server::Starter) - Process manager with the "graceful restart" feature.
*   [Starlet](https://metacpan.org/pod/Starlet) - High-performance PSGI Server
*   [Starman](https://metacpan.org/pod/Starman) - High-performance preforking PSGI/Plack web server
*   [Twiggy](https://metacpan.org/pod/Twiggy) - Event-driven PSGI application server

[](#web-frameworks-like)Web Frameworks-Like
-------------------------------------------

_Somewhere between templates and full on frameworks_

*   [Embperl](https://metacpan.org/pod/Embperl) - Building dynamic Websites with Perl (sort of like Perl crossed with PHP)
*   [Mason](https://metacpan.org/pod/Mason) - Powerful, high-performance templating for the web and beyond

[](#web-scraping)Web Scraping
-----------------------------

_Libraries for extracting some information from websites_

*   [Web::Scraper](https://metacpan.org/pod/Web::Scraper)
*   [WWW::Mechanize](https://metacpan.org/pod/WWW::Mechanize)
*   [WWW::Mechanize::PhantomJS](https://metacpan.org/pod/WWW::Mechanize::PhantomJS) - automate the PhantomJS browser
*   [WWW::Scripter](https://metacpan.org/pod/distribution/WWW-Scripter/lib/WWW/Scripter.pod) - For scripting web sites that have scripts
*   [WWW::Selenium](https://metacpan.org/pod/WWW::Selenium)

[](#network-security)Network Security
-------------------------------------

_Some great libraries for starting the world of Network security with Perl_

*   [Net::Pcap](https://metacpan.org/pod/Net::Pcap) - Interface to the pcap LBL packet capture library
*   [Net::Ncap](https://metacpan.org/pod/Net::Ncap) - Perl binding to the ncap network data capture library
*   [Net::Frame](https://metacpan.org/pod/Net::Frame) - Perl framework for frame crafting
*   [NetPacket](https://metacpan.org/pod/NetPacket) - assemble/disassemble network packets at the protocol level
*   [Net::Write](https://metacpan.org/pod/Net::Write) - portable interface to open and send raw data to network
*   [Net::Analysis](https://metacpan.org/pod/Net::Analysis) - Perl library for analysing network traffic
*   [Net::Silk](https://metacpan.org/pod/Net::Silk) - Perl's Interface to the SiLK network flow library
*   [Net::Inspect](https://metacpan.org/pod/Net::Inspect) - Perl library for inspection of data on various network layers
*   [Net::Tshark](https://metacpan.org/pod/Net::Tshark) - Perl interface for Tshark network capture utility
*   [Net::Sharktools](https://metacpan.org/pod/Net::Sharktools) - Wireshark's packet inspection capabilities in Perl
*   [File::PCAP](https://metacpan.org/pod/File::PCAP) - Read, Write and manipulate PCAP file format through Perl
*   [Net::P0f](https://metacpan.org/pod/Net::P0f) - Perl interface to p0f utility, usefull for finger-printing os
*   [Net::Pcap::Reassemble](https://metacpan.org/pod/Net::Pcap::Reassemble) - Perl IP fragment reassembly for Net::Pcap
*   [Nagios::NRPE](https://metacpan.org/pod/Nagios::NRPE) - Pure perl Nagios NRPE implementation
*   [Monitoring::Plugin](https://metacpan.org/pod/Monitoring::Plugin) - A family of perl modules to streamline writing Naemon, Nagios, Icinga or Shinken (and compatible) plugins
*   [Net::Connection::Sniffer](https://metacpan.org/pod/Net::Connection::Sniffer) - practical Perl library for MiTM connections
*   [Net::ARP](https://metacpan.org/pod/Net::ARP) - Library for crafting ARP packets
*   [SNMPMonitor](https://metacpan.org/pod/SNMPMonitor) - Perl extension for writing SNMP Monitors
*   [Net::LibNIDS](https://metacpan.org/pod/Net::LibNIDS) - Perl interface for the Network Intrusion Detection System library
*   [Parse::Snort](https://metacpan.org/pod/Parse::Snort) - Perl Snort rules parser
*   [Net::Wireless::802\_11::WPA::CLI](https://metacpan.org/pod/Net::Wireless::802_11::WPA::CLI) - Perl WPA\_CLI interface
*   [IO::Socket::SSL::Intercept](https://metacpan.org/IO::Socket::SSL::Intercept) - library for intercepting SSL connections through Perl

[](#metadata-forensics)Metadata Forensics
-----------------------------------------

_General Metadata files parser, usefull during forensics investigations_

*   [Image::ExifTool](https://metacpan.org/pod/distribution/Image-ExifTool/exiftool) - General metadata parser and viewer framework

[](#reverse-engineering)Reverse Engineering
-------------------------------------------

_Libraries used for disassembly assembly operations, ELF files and bytecode_

*   [Disassembly](https://metacpan.org/pod/distribution/B-C/script/disassemble) - Decompiles binary bytecode to readable and recompilable bytecode assembler
*   [Python::Bytecode](https://metacpan.org/pod/Python::Bytecode) - Parse Python bytecode
*   [B::Bytecode](https://metacpan.org/pod/B::Bytecode) - Compiles a Perl script into a bytecode format that could be loaded later
*   [Perf::ARM](https://metacpan.org/pod/Perf::ARM) - Use ARM instructions in Perl
*   [Asm::Z80::Table](https://metacpan.org/pod/Asm::Z80::Table) - assemble / disassemble all Z80 CPU assembly instructions with Perl
*   [X86::Disasm](https://metacpan.org/pod/X86::Disasm) - Disassemble Intel x86 instructions with Perl
*   [Disassemble::X86](https://metacpan.org/pod/Disassemble::X86) - Another library for disassembe X86 instructions
*   [X86::Udis86](https://metacpan.org/pod/X86::Udis86) - Interface for the C Udis disassembler
*   [Asm::X86](https://metacpan.org/pod/Asm::X86) - List of instructions and registers of x86-compatible processors, validating and converting instructions and memory references
*   [ELF::Writer](https://metacpan.org/pod/ELF::Writer) - write and read executable ELF files

[](#other-awesome-lists)Other Awesome Lists
===========================================

Other amazingly awesome lists can be found in:

*   [bayandin/awesome-awesomeness](https://github.com/bayandin/awesome-awesomeness)
*   [emijrp/awesome-awesome](https://github.com/emijrp/awesome-awesome)
*   [fleveque/awesome-awesomes](https://github.com/fleveque/awesome-awesomes)
*   [sindresorhus/awesome](https://github.com/sindresorhus/awesome)
*   [t3chnoboy/awesome-awesome-awesome](https://github.com/t3chnoboy/awesome-awesome-awesome)

[](#how-to-contribute)How to contribute?
========================================

Please read [CONTRIBUTING.md](/hachiojipm/awesome-perl/blob/master/CONTRIBUTING.md)