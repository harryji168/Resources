 
## Database 

 In computing, a database is an organized collection of data stored and accessed electronically. Small databases can be stored on a file system, while large databases are hosted on computer clusters or cloud storage. The design of databases spans formal techniques and practical considerations including data modeling, efficient data representation and storage, query languages, security and privacy of sensitive data, and distributed computing issues including supporting concurrent access and fault tolerance.

A database management system (DBMS) is the software that interacts with end users, applications, and the database itself to capture and analyze the data. The DBMS software additionally encompasses the core facilities provided to administer the database. The sum total of the database, the DBMS and the associated applications can be referred to as a database system. Often the term "database" is also used loosely to refer to any of the DBMS, the database system or an application associated with the database.

Computer scientists may classify database management systems according to the database models that they support. Relational databases became dominant in the 1980s. These model data as rows and columns in a series of tables, and the vast majority use SQL for writing and querying data. In the 2000s, non-relational databases became popular, collectively referred to as NoSQL because they use different query languages.


A categorized community-driven collection of amazingly awesome database resources.  
  
Free assets and resources are prioritized over paid when possible.  
  
Suggestions and contributions are always welcome!  
Make sure to read the [contribution guidelines](https://github.com/agarcialeon/awesome-database/blob/master/CONTRIBUTING.md) for more information before submitting a pull request.

[![forthebadge](https://camo.githubusercontent.com/6d42385cf53224da8a8cebb37354c4a93ab981640456cb770ca9ed0e489e0331/68747470733a2f2f666f7274686562616467652e636f6d2f696d616765732f6261646765732f63632d302e737667)](https://forthebadge.com)

[](#bookmark_tabs-contents)![bookmark_tabs](https://github.githubassets.com/images/icons/emoji/unicode/1f4d1.png) Contents
==========================================================================================================================

*   [Motivation](#motivation)
*   [Considerations](#considerations)
*   [Legend](#legend)
    *   [Icons](#icons)
    *   [Tags](#tags)
*   [Categories](#categories)
    *   [Databases](#databases)
    *   [Scripting](#scripting)
        *   [SQL Languages](#sql-languages)
        *   [Algorithms](#algorithms)
        *   [Patterns](#patterns)
        *   [Libraries](#libraries)
        *   [Utilities](#utilities)
        *   [Tools](#tools)
        *   [Plugins](#plugins)
        *   [Snippets & Gists](#snippets-&-gists)
        *   [Dynamic SQL](#dynamic-sql)
    *   [Integrated Development Environment (IDE)](#ide)
    *   [VCS (Version Control Systems)](#vcs)
    *   [Continuous Integration (CI)](#continuous-integration)
    *   [Testing](#testing)
    *   [Documentation](#documentation)
    *   [Database Development](#db-development)
    *   [Benchmarks](#benchmarks)
    *   [Customization](#customization)
    *   [Extensibility](#extensibility)
    *   [Miscellaneuous](#miscellaneous)
*   [Learning Resources](#learning-resources)
    *   [Tips and Tricks](#tips-tricks)
    *   [Books](#books)
    *   [Research Papers](#research-papers)
    *   [Blogs](#blogs)
    *   [Videos](#videos)
        *   [Youtube Channels](#youtube-channels)
    *   [Tutorials](#tutorials)
    *   [Best Practices](#best-practices)
    *   [Shortcuts](#shortcuts)
    *   [Other References](#other-references)
*   [Recommended](#recommended)
*   [Projects](#projects)
*   [Communities](#communities)
    *   [Chat Servers](#chat-servers)
    *   [Forums](#forums)
    *   [Groups](#groups)
    *   [People to Follow](#people-to-follow)
*   [Frequently Asked Questions (FAQ)](#faq)
*   [Contributors to this repository](#contributors)
*   [Contributing](#contributing)
*   [Code of Conduct](#code-of-conduct)
*   [To be done](#to-do)

[](#motivation-)Motivation
==========================

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#considerations-)Considerations
==================================

[](#legend-)Legend
==================

[](#icons-)Icons
----------------

Free resource: ![free](https://github.githubassets.com/images/icons/emoji/unicode/1f193.png)

Paid resource: ![moneybag](https://github.githubassets.com/images/icons/emoji/unicode/1f4b0.png)

Interesting resource: ![cool](https://github.githubassets.com/images/icons/emoji/unicode/1f192.png)

[](#tags-)Tags
--------------

(UNMAINTAINED) - The repository hasn't been updated for a long time.

(DEPRECATED) - Another solution or package has been released that does the same and it's more recent.

(ARCHIVED) - The repository is read only for learning purposes.

#\[CATEGORY\] - Where \[CATEGORY\] represents a category of the document. Means that the resource is related with another category too.

[](#bookmark-categories-)![bookmark](https://github.githubassets.com/images/icons/emoji/unicode/1f516.png) Categories
=====================================================================================================================

[](#databases-)Databases
------------------------

Search [more](https://dbdb.io/) databases.

### [](#relational-databases-)Relational Databases

#### [](#oracle-)Oracle

*   [SQL Developer](http://www.oracle.com/technetwork/developer-tools/sql-developer/overview/index.html) - Oracle's Free IDE for PL/SQL development and administration of Oracle databases.
*   [SQL Tools for Oracle](http://sourceforge.net/projects/sqlt/) - Lightweight frontend for Oracle DB development.
*   [Oracle Database 11g Express Edition](http://www.oracle.com/technetwork/database/database-technologies/express-edition/overview/index.html) - Free entry level database to develop and deploy applications.
*   [Alexandria PL/SQL Utility Library](https://github.com/mortenbra/alexandria-plsql-utils) - Collection of utility packages for PL/SQL
*   [PLSQL-JSON](https://github.com/doberkofler/PLSQL-JSON) - PL/SQL library to encode/decode JSON
*   [utPLSQL](https://utplsql.github.io/) - Unit testing framework for PL/SQL.

#### [](#sql-server-)SQL Server

*   [SQL Server Express Edition](http://www.microsoft.com/en-us/server-cloud/products/sql-server-editions/sql-server-express.aspx) - Free SQL Server Database to develop and deploy applications.
*   [SQL Server Data Tools](http://msdn.microsoft.com/en-us/data/tools.aspx) - Integrated environment for developers to design and build database and other business intelligence solutions for MS SQL Server stack.
*   [tSQLt](http://tsqlt.org/) - Unit testing framework for SQL Server.

##### [](#monitoring)Monitoring

*   [Monitor CPU Usage](https://github.com/SqlAdmin/AwesomeSQLServer/blob/master/T-SQL%20Scripts/CPU%20Monitoring.sql)
*   [Monitor Memory Usage](https://github.com/SqlAdmin/AwesomeSQLServer/blob/master/T-SQL%20Scripts/Memory%20Monitoring.sql)
*   [Monitor Disk Usage](https://github.com/SqlAdmin/AwesomeSQLServer/blob/master/T-SQL%20Scripts/Disk%20Space%20Monitoring.sql)
*   [Session Monitoring](https://github.com/SqlAdmin/AwesomeSQLServer/blob/master/T-SQL%20Scripts/Session%20Monitoring.sql)
*   [Blocking, Deadlock Monitoring](https://github.com/SqlAdmin/AwesomeSQLServer/blob/master/T-SQL%20Scripts/Blocking%20Monitoring.sql)
*   [IO Monitoring](https://github.com/SqlAdmin/AwesomeSQLServer/blob/master/T-SQL%20Scripts/IO%20Monitoring.sql)
*   [Wait stat Monitoring](https://github.com/SqlAdmin/AwesomeSQLServer/blob/master/T-SQL%20Scripts/Wait%20stat%20Monitoring.sql)

#### [](#mariadb-)[MariaDB](https://mariadb.org/)

_An enhanced, drop-in replacement for MySQL._

#### [](#mysql-)[MySQL](http://mysql.com)

_MySQL is the world's most popular open source database._

*   [Facebook/MySQL-5.6](https://github.com/facebook/mysql-5.6) - Facebook's branch of the Oracle MySQL v5.6 database. (#C/C++)
*   [Twitter/MySQL](https://github.com/twitter/mysql) - MySQL fork maintained and used at Twitter. See its [wiki](https://github.com/twitter/mysql/wiki). (#C/C++)
*   [Percona Server](http://www.percona.com/software) - Enhanced, drop-in MySQL replacement.
*   [TokuDB Engine](https://github.com/Tokutek/tokudb-engine) - TokuDB is a high-performance, write optimized, compressing, transactional storage engine for MySQL and MariaDB. (#C/C++) (#MARIADB)
*   [Galera](http://galeracluster.com/) - Galera Cluster for MySQL is an easy-to-use high-availability solution with high system up-time, no data loss, and scalability for future growth.

#### [](#sqlite-)[SQLite](http://www.sqlite.org/)

_A completely embedded, full-featured relational database in a few 100k that you can include right into your project._

*   [Awesome SQLite](https://github.com/mindreframer/awesome-sqlite) - All things around SQLite.

#### [](#db2-)[DB2](https://www.ibm.com/es-es/analytics/db2/tools)

_Database management products developed by IBM_

*   [Awesome DB2](https://github.com/angoca/awesome-db2) - A curated list of awesome Db2 resources, tools and documentation to develop in that database.

#### [](#other-databases-)Other Databases

*   [Firebird](http://www.firebirdsql.org/) - True universal open source database.
*   [VoltDB](https://github.com/VoltDB/voltdb/) - VoltDB is a horizontally-scalable, in-memory SQL RDBMS designed for applications that have extremely high read and write throughput requirements.
*   [YugabyteDB](https://github.com/yugabyte/yugabyte-db) - PostgreSQL-compatible, Cassandra-compatible, horizontally scalable, fault tolerant database server.

### [](#object-relational-databases)Object-Relational Databases

#### [](#postgresql-)[PostgreSQL](http://www.postgresql.org/)

_A powerful, open source object-relational database system._

*   [PostgreSQL](https://github.com/postgres/postgres) - Mirror of the official PostgreSQL Git repository. (#C/C++)
*   [PostgreSQL-XL](http://www.postgres-xl.org/) - Scalable Open Source PostgreSQL-based database cluster.
*   [Cstore FDW](https://github.com/citusdata/cstore_fdw) - Fast columnar store for analytics with PostgreSQL. [Website](http://citusdata.github.io/cstore_fdw/). (#C/C++)
*   [Barman](http://www.pgbarman.org) - Backup and Recovery Manager for disaster recovery of PostgreSQL servers.

### [](#nosql-databases-)NoSQL Databases

See [list](http://nosql-database.org/) of databases.

#### [](#key-value-cache-)Key-Value Cache

*   Coherence
*   eXtreme Scale
*   GigaSpaces
*   GemFire
*   Hazelcast
*   Infinispan
*   JBoss Cache
*   **Memcached**
*   Repcached
*   Terracotta
*   Velocity
*   [Go Cache](https://github.com/pmylund/go-cache) - An in-memory key:value store/cache (similar to Memcached) library for Go, suitable for single-machine applications. (#GO-LANG)

#### [](#key-value-store-)Key-Value Store

*   Flare
*   Keyspace
*   RAMCloud
*   SchemaFree
*   Hyperdex
*   [Aerospike](https://github.com/aerospike/aerospike-server) - Flash-optimized, in-memory, noSQL database. Previously [AlchemyDB](https://github.com/JakSprats/Alchemy-Database). See [more](http://www.aerospike.com).
*   [Bolt](https://github.com/boltdb/bolt) - A low-level key/value database for Go. (#GO-LANG)
*   [Diskv](https://github.com/peterbourgon/diskv) - A home-grown disk-backed key-value store. (#GO-LANG)
*   [LevelDB](https://github.com/google/leveldb) - High performance key-value storage library written at Google. See [more](https://code.google.com/p/leveldb/).
*   [Go LevelDB](https://github.com/syndtr/goleveldb) - An implementation of the [LevelDB](https://code.google.com/p/leveldb/) key/value database in the Go. (#GO-LANG)

#### [](#key-value-store-eventually-consistent-)Key-Value Store (Eventually-Consistent)

*   DovetailDB
*   **Oracle NoSQL Database**
*   Dynamo
*   [Voldemort](https://github.com/voldemort/voldemort) - An open source clone of Amazon's Dynamo. [Website](http://project-voldemort.com) (#JAVA)
*   [Riak](http://basho.com/riak/) - Another fault-tolerant key-value NoSQL database.
*   Dynomite
*   MotionDb
*   Voldemort
*   SubRecord

#### [](#key-value-store-ordered-)Key-Value Store (Ordered)

*   Actord
*   FoundationDB
*   Lightcloud
*   [LMDB](http://symas.com/mdb/) - Very fast embedded key/value store with full ACID semantics. (#C/C++)
*   Luxio
*   [Memcached](https://github.com/memcached/memcached) - Free & open source, high-performance, distributed memory object caching system. (#C/C++)
*   [Groupcache](https://github.com/golang/groupcache) - Groupcache is a caching and cache-filling library, intended as a replacement for memcached in many cases. (#GO-LANG)
*   **MemcacheDB**
*   NMDB
*   Scalaris
*   TokyoTyrant

#### [](#data-structures-server-)Data-Structures server

*   [Redis](https://github.com/antirez/redis) - Redis is an in-memory database that persists on disk. The data model is key-value, but many different kind of values are supported: Strings, Lists, Sets, Sorted Sets, Hashes.[Website](http://redis.io). (#C/C++)
*   [Redis NDS](https://github.com/mpalmer/redis/tree/nds-2.6) - This is a version of Redis patched to implement NDS (the Naive Disk Store). (#C/C++)
*   [SSDB](https://github.com/ideawu/ssdb) - A fast NoSQL database, an alternative to Redis. [Website](http://ssdb.io). (#C/C++)
*   [LedisDB](https://github.com/siddontang/ledisdb) - Ledisdb is a high performance NoSQL like Redis based on LevelDB. (#GO-LANG)

#### [](#tuple-store-)Tuple Store

*   Apache River
*   Coord
*   GigaSpaces

#### [](#object-database-)Object Database

*   DB4O
*   Objectivity/DB
*   Perst
*   Shoal
*   ZopeDB

#### [](#document-store-)Document Store

*   Clusterpoint
*   [Couchbase](http://www.couchbase.com/) - In-memory, replicated, peristent key/value datastore.
*   [MongoDB](https://github.com/mongodb/mongo) - MongoDB is a document database that provides high performance, high availability, and easy scalability. Documents (objects) map nicely to programming language data types. Embedded documents and arrays reduce need for joins. Dynamic schema makes polymorphism easier. \[Website\] ([https://www.mongodb.org/](https://www.mongodb.org/)). (#JAVASCRIPT)
*   [TokuMX](https://github.com/Tokutek/mongo) - TokuMX is a high-performance, concurrent, compressing, drop-in replacement engine for MongoDB. (#C/C++)
*   [Apache CouchDB](https://github.com/apache/couchdb) - A database that uses JSON for documents, JavaScript for MapReduce indexes, and regular HTTP for its API \[Website\] ([http://couchdb.apache.org/](http://couchdb.apache.org/)). (#JAVASCRIPT)
*   [PouchDB](https://github.com/pouchdb/pouchdb) - PouchDB is a pocket-sized database. (#JAVASCRIPT). Inspired by CouchDB.
*   [RethinkDB](https://github.com/rethinkdb/rethinkdb) - An open-source distributed JSON document database with a pleasant and powerful query language. For building realtime web applications. [Website](http://www.rethinkdb.com). (#C/C++)
*   [ElasticSearch](http://www.elasticsearch.org/) - Popular with log aggregation, and email archiving projects. (#JAVA)
*   DocumentDB
*   [RavenDB](https://github.com/ravendb/ravendb) - Document based database with ACID/Transactional features. [Website](http://ravendb.net/) (#.NET)
*   Lotus Notes
*   MarkLogic
*   Qizx
*   XML-databases

#### [](#wide-columnar-store-)Wide Columnar Store

*   **BigTable**
*   [Cassandra](https://github.com/apache/cassandra) - A partitioned row store. Rows are organized into tables with a required primary key. [Website](http://cassandra.apache.org/) (#JAVA)
*   Druid
*   [Apache HBase](http://hbase.apache.org/) - Hadoop database, a distributed, big data store.
*   [Hypertable](http://hypertable.org/) - C++ based BigTable-like DBMS, communicates through Thrift and runs either as stand-alone or on distributed FS such as Hadoop.
*   KAI
*   KDI
*   OpenNeptune
*   Qbase

#### [](#graph-databases-)Graph Databases

*   [Neo4j](https://github.com/neo4j/neo4j) - The world’s leading Graph Database. [Website](http://neo4j.org). (#JAVA)
*   [FlockDB](https://github.com/twitter/flockdb) - Twitter's distributed, fault-tolerant graph database.
*   [Titan](https://github.com/thinkaurelius/titan) - Distributed Graph Database [Website](http://titandb.io). (#JAVA)
*   [OrientDB](https://github.com/orientechnologies/orientdb) - OrientDB is an Open Source NoSQL DBMS with the features of both Document and Graph DBMSs. (#JAVA) (#DOCUMENT-STORE)
*   [ArangoDB](https://github.com/triAGENS/ArangoDB) - ArangoDB is a multi-purpose, open-source database with flexible data models for documents, graphs, and key-values. Build high performance applications using a convenient SQL-like query language or JavaScript/Ruby extensions. Use ACID transaction if you require them. Scale horizontally and vertically with a few mouse clicks.

#### [](#others)Others

*   [Memstate](https://github.com/devrexlabs/memstate) - Previously named OrigoDB. An in-memory embedded database engine for NET/Mono. See [more](https://origodb.com/). (#.NET)
*   [MonetDB](https://github.com/snaga/monetdb) - A high-performance database kernel for query-intensive applications. The MonetDB kernel works together with an SQL frontend that is in a separate CVS module. [Website](https://www.monetdb.org/). (#C/C++)
*   [Tiedot](https://github.com/HouzuoGuo/tiedot) - Your NoSQL database powered by Golang. (#GO-LANG)
*   [InfluxDB](https://github.com/influxdb/influxdb) - Scalable datastore for metrics, events, and real-time analytics. (#GO-LANG)
*   [Roshi](https://github.com/soundcloud/roshi/) - Roshi is a large-scale CRDT set implementation for timestamped events. (#GO-LANG)
*   [SkyDB.io](https://github.com/skydb/sky) - Sky is an open source database used for flexible, high performance analysis of behavioral data. (#GO-LANG)

### [](#embeddable-engines-)Embeddable engines

*   [Derby](https://db.apache.org/derby/) - Open source relational database implemented entirely in Java.
*   [H2](https://github.com/h2database/h2database) - An embeddable RDBMS written in Java.
*   [PalDB](https://github.com/linkedin/PalDB) - Embeddable write-once key-value store written in Java.
*   [RocksDB](https://github.com/facebook/rocksdb) - Embedded key-value store for fast storage. [Website](http://rocksdb.org). (#C/C++)
*   [MapDB](https://github.com/jankotek/mapdb/) - MapDB provides concurrent Maps, Sets and Queues backed by disk storage or off-heap-memory. It is a fast and easy to use embedded Java database engine. [Website](http://www.mapdb.org). (#JAVA)
*   [Xodus](https://github.com/JetBrains/xodus/) - JetBrains Xodus is a Java transactional schema-less embedded database.

[](#clojure)Clojure
-------------------

*   [Datomic](http://www.datomic.com/)
*   [Clojure.jdbc](https://github.com/niwibe/clojure.jdbc)
*   [CravenDB](https://github.com/robashton/cravendb)

[](#erlang)Erlang
-----------------

*   [Riak](https://github.com/basho/riak) - Riak is a decentralized datastore from Basho Technologies.
*   [PulseDB](http://pulsedb.io) - PulseDB is a time series database server and library.

[](#java)Java
-------------

*   [Elasticsearch](https://github.com/elasticsearch/elasticsearch) - Open Source, Distributed, RESTful Search Engine [Website](http://elasticsearch.org). (#JAVA)
*   [Lmdbjni](https://github.com/deephacks/lmdbjni) - LMDB for Java, which is a very fast embedded key/value store with full ACID semantics. (#JAVA)

[](#scala)Scala
---------------

*   [BlinkDB](https://github.com/sameeragarwal/blinkdb) - BlinkDB: Sub-Second Approximate Queries on Very Large Data \[Website\] ([http://blinkdb.cs.berkeley.edu/](http://blinkdb.cs.berkeley.edu/)). (#SCALA)
*   [VerdictDB](https://github.com/mozafari/verdictdb) - Interactive-Speed Analytics: 200x Faster, 200x Fewer Cluster Resources, Approximate Query Processing.

[](#frameworks-)Frameworks
--------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#services-)Services
----------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#pencil2-scripting-)![pencil2](https://github.githubassets.com/images/icons/emoji/unicode/270f.png) Scripting
----------------------------------------------------------------------------------------------------------------

### [](#sql-languages-)SQL Languages

*   SQL (Structured Query Language)
*   T-SQL (Transact SQL)

#### [](#sublanguages-)Sublanguages

Take picture from [here](https://www.quora.com/What-are-different-sub-languages-in-SQL)

*   Data Definition Language (DDL)
*   Data Manipulation Language (DML)
*   Data Control Language (DCL)
*   Transaction Control Language(TCL)
*   DQL (Data Query Language)

#### [](#versions)Versions

Take table from [here](https://es.wikipedia.org/wiki/SQL)

#### [](#dialects)Dialects

### [](#chart_with_upwards_trend-algorithms-)![chart_with_upwards_trend](https://github.githubassets.com/images/icons/emoji/unicode/1f4c8.png) Algorithms

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

### [](#straight_ruler-patterns-)![straight_ruler](https://github.githubassets.com/images/icons/emoji/unicode/1f4cf.png) Patterns

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

### [](#orange_book-libraries-)![orange_book](https://github.githubassets.com/images/icons/emoji/unicode/1f4d9.png) Libraries

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

### [](#nut_and_bolt-utilities-)![nut_and_bolt](https://github.githubassets.com/images/icons/emoji/unicode/1f529.png) Utilities

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

### [](#wrench-tools-)![wrench](https://github.githubassets.com/images/icons/emoji/unicode/1f527.png) Tools

*   [PixQL](https://github.com/Phildo/pixQL) - Command-line image processing tool in SQL.
*   [SQL Fiddle](http://sqlfiddle.com/) - Easly test and share database problems and their solutions. Can use different backend DBMS's (MySQL, PostgreSQL, MS SQL Server, Oracle, and SQLite).
*   [SqlPad](http://rickbergfalk.github.io/sqlpad/) - A web app for running SQL queries and visualizing the results.
*   [ERAlchemy](https://github.com/Alexis-benoist/eralchemy) - ERAlchemy generates Entity Relation (ER) diagram from databases.
*   [BigBash](https://github.com/zalando/bigbash) - Open-source converter that generates a bash one-liner from an SQL Select query, no database necessary.
*   [Flyway](https://flywaydb.org/) - Database migration tool.
*   [Liquibase](http://www.liquibase.org/) - Source Control for your database.
*   [Awesome DB Tools](https://github.com/mgramin/awesome-db-tools) - a community driven list of database tools (ide, cli, managing, monitoring, migrations, modelers, visualization etc)
*   [10 Database tools for sys admins](https://techtalk.gfi.com/top-10-free-database-tools-for-sys-admins/)
*   [Wikipedia Database Tools Comparison](https://en.wikipedia.org/wiki/Comparison_of_database_tools)

[](#formatters-)Formatters
--------------------------

*   [SQL Format](http://www.dpriver.com/pp/sqlformat.htm) - Instant SQL Formatter.
*   [Poor SQL](http://poorsql.com/) - A small free .Net and JS library (with demo UI, command-line bulk formatter, SSMS/VS add-in, notepad++ plugin, winmerge plugin, and demo webpage) for reformatting and coloring T-SQL code to the user's preferences. See more on [Github](https://github.com/TaoK/PoorMansTSqlFormatter).
*   [T-SQL Tidy](http://www.tsqltidy.com/Default.aspx) - Online T-SQL formatting with Webservice and Plugins for SSMS.

[](#electric_plug-plugins-)![electric_plug](https://github.githubassets.com/images/icons/emoji/unicode/1f50c.png) Plugins
-------------------------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#snippets--gists-)Snippets & Gists
-------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#dynamic-sql-)Dynamic SQL
----------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#integrated-development-environment-ide-)Integrated Development Environment (IDE)
------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#vcs-version-control-systems-)VCS (Version Control Systems)
--------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#continuous-integration-)Continuous Integration
--------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#testing-)Testing
--------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#documentation-)Documentation
--------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#database-development-)Database Development
----------------------------------------------

*   [Awesome DB Dev](https://github.com/huachaohuang/awesome-dbdev) - Awesome materials about database development.

[](#benchmarks-)Benchmarks
--------------------------

*   [Awesome DB Benchmarks](https://github.com/benstopford/awesome-db-benchmarks) - Community driven list of database benchmarks.

[](#sunglasses-customization-)![sunglasses](https://github.githubassets.com/images/icons/emoji/unicode/1f60e.png) Customization
-------------------------------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#extensibility-)Extensibility
--------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#misc-)Misc.
---------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#mortar_board-learning-resources-)![mortar_board](https://github.githubassets.com/images/icons/emoji/unicode/1f393.png) Learning Resources
=============================================================================================================================================

[](#rocket-tips-and-tricks-)![rocket](https://github.githubassets.com/images/icons/emoji/unicode/1f680.png) Tips and Tricks
---------------------------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#books-books-)![books](https://github.githubassets.com/images/icons/emoji/unicode/1f4da.png) Books
-----------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#research-papers)Research Papers
-----------------------------------

*   [db-readings](https://github.com/rxin/db-readings) - A list of papers essential to understanding databases and building new data systems.

[](#newspaper-blogs-)![newspaper](https://github.githubassets.com/images/icons/emoji/unicode/1f4f0.png) Blogs
-------------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#tv--videos-)![tv](https://github.githubassets.com/images/icons/emoji/unicode/1f4fa.png) Videos
--------------------------------------------------------------------------------------------------

### [](#vhs-youtube-channels-)![vhs](https://github.githubassets.com/images/icons/emoji/unicode/1f4fc.png) Youtube Channels

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#beginner-tutorials-)![beginner](https://github.githubassets.com/images/icons/emoji/unicode/1f530.png) Tutorials
-------------------------------------------------------------------------------------------------------------------

*   [Curated SQL Learning Resources on Hackr.io](https://hackr.io/tutorials/learn-sql) - Programming Community Curated Resources for learning SQL.

[](#star-best-practices-)![star](https://github.githubassets.com/images/icons/emoji/unicode/2b50.png) Best Practices
--------------------------------------------------------------------------------------------------------------------

### [](#abcd-coding-practices-)![abcd](https://github.githubassets.com/images/icons/emoji/unicode/1f521.png) Coding Practices

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

### [](#capital_abcd-organizational-practices-)![capital_abcd](https://github.githubassets.com/images/icons/emoji/unicode/1f520.png) Organizational Practices

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#triangular_ruler-style-guide-)![triangular_ruler](https://github.githubassets.com/images/icons/emoji/unicode/1f4d0.png) Style Guide
---------------------------------------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#key-shortcuts-)![key](https://github.githubassets.com/images/icons/emoji/unicode/1f511.png) Shortcuts
---------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#paperclip-other-references-)![paperclip](https://github.githubassets.com/images/icons/emoji/unicode/1f4ce.png) Other references
-----------------------------------------------------------------------------------------------------------------------------------

*   [Awesome DB Tools](https://github.com/mgramin/awesome-db-tools) - A community driven list of database tools (ide, cli, managing, monitoring, migrations, modelers, visualization, etc...).
*   [Awesome SQL](https://github.com/danhuss/awesome-sql) - List of tools and techniques for working with relational databases.
*   [Awesome Databases](https://github.com/dhamaniasad/awesome-databases) - A curated list of awesome databases.
*   [Awesome DB](https://github.com/pditommaso/awesome-db) - A curated list of awesome DBs.
*   [Awesome SQL Server](https://github.com/SqlAdmin/AwesomeSQLServer) - A big collection of SQL Server Queries and documeantations to fix your SQL Server's bottle neck.
*   [Awesome MySQL](https://github.com/shlomi-noach/awesome-mysql) - A curated list of awesome MySQL software, libraries, tools and resources.
*   [Awesome SQLite](https://github.com/planetopendata/awesome-sqlite) - A collection of awesome sqlite tools, scripts, books, etc.
*   [Awesome PostgresSQL](https://github.com/dhamaniasad/awesome-postgres) - A curated list of awesome PostgreSQL software, libraries, tools and resources, inspired by awesome-mysql.
*   [Awesome DB2](https://github.com/angoca/awesome-db2) - A curated list of awesome Db2 resources, libraries, tools and applications.
*   [Awesome BigData](https://github.com/onurakpolat/awesome-bigdata) - A curated list of awesome big data frameworks, resources and other awesomeness.

[](#trophy-recommended-)![trophy](https://github.githubassets.com/images/icons/emoji/unicode/1f3c6.png) Recommended
===================================================================================================================

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#projects-)Projects
======================

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#busts_in_silhouette-communities-)![busts_in_silhouette](https://github.githubassets.com/images/icons/emoji/unicode/1f465.png) Communities
=============================================================================================================================================

[](#speech_balloon-chat-servers-)![speech_balloon](https://github.githubassets.com/images/icons/emoji/unicode/1f4ac.png) Chat Servers
-------------------------------------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#forums-)Forums
------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#groups-)Groups
------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#name_badge-people-to-follow-)![name_badge](https://github.githubassets.com/images/icons/emoji/unicode/1f4db.png) People to follow
-------------------------------------------------------------------------------------------------------------------------------------

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#question-frequently-asked-questions-faq-)![question](https://github.githubassets.com/images/icons/emoji/unicode/2753.png) Frequently Asked Questions (FAQ)
==============================================================================================================================================================

![construction](https://github.githubassets.com/images/icons/emoji/unicode/1f6a7.png)

[](#clap-tada-contributors-to-this-repository-)![clap](https://github.githubassets.com/images/icons/emoji/unicode/1f44f.png) ![tada](https://github.githubassets.com/images/icons/emoji/unicode/1f389.png) Contributors to this repository
==========================================================================================================================================================================================================================================

![guardsman](https://github.githubassets.com/images/icons/emoji/unicode/1f482-2642.png) [@agarcialeon](https://github.com/agarcialeon) - Owner of the repository

[](#contributing-)Contributing
==============================

Please see [CONTRIBUTING](https://github.com/agarcialeon/awesome-unity/blob/master/CONTRIBUTING.md) for details.

Thanks to all the [contributors](https://github.com/agarcialeon/awesome-unity/graphs/contributors), this wouldn't be possible without you!

[](#code-of-conduct-)Code of Conduct
====================================

See [Code of Conduct](https://github.com/agarcialeon/awesome-unity/blob/master/CODE-OF-CONDUCT.md).

[](#memo-to-be-done-)![memo](https://github.githubassets.com/images/icons/emoji/unicode/1f4dd.png) To be done
=============================================================================================================

![warning](https://github.githubassets.com/images/icons/emoji/unicode/26a0.png) NOTE: Following list of tasks is written without any order of preference.

*   Fill Open Issue template file to help providing new resources.
*   Add license file.
*   Add awesome sqlite repository resources. (not commercial ones)
*   Add awesome postgres repository resources.
*   Add repository logo.
*   Add contributing file.
*   Move language-related resources to its category and add language tags to filter them.
*   The logo image should be high-DPI. Set it to maximum half the width of the original image.
*   Wait 30 days from first commit to make the pull request to awesome lists topic.
*   Add tags for free and paid resources.
*   Add better icons for sections.
*   Use tags to classify a resource instead of using a category.
*   Reorder category resources by most well known resources if possible.
*   Starter kit section with all the things needed or recommended for beginners.
*   Include resources for recommended packages section (well tested, most voted and so on).
*   Fill up continuous integration section.
*   Fill up people to follow.
*   Fill up communities section.
*   Fill snippets and gists under scripting section.
*   Create more categories for specific resources that don't combine well.
*   Add category for error reporting, logging and debugging.
*   Mark deprecated packages (![x](https://github.githubassets.com/images/icons/emoji/unicode/274c.png)).
*   Change introduction at the beginning ot the readme file to indicate better the visitors how its organized.
*   Do shortcut png image with IDE shortcuts.
*   Create open collective to show the image with the contributors if necessary.
*   Review items by category to select one between similar ones in order to select the most complete. Reference the others in another section or repository.

And many more...

 [![top](https://github.githubassets.com/images/icons/emoji/unicode/1f51d.png) Back to Top](#awesome-database)