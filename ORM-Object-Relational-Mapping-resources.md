# ORM Object–relational mapping

Object–relational mapping (ORM, O/RM, and O/R mapping tool) in computer science is a programming technique for converting data between incompatible type systems using object-oriented programming languages. This creates, in effect, a "virtual object database" that can be used from within the programming language. There are both free and commercial packages available that perform object–relational mapping, although some programmers opt to construct their own ORM tools.

In object-oriented programming, data-management tasks act on objects that are almost always non-scalar values. For example, consider an address book entry that represents a single person along with zero or more phone numbers and zero or more addresses. This could be modeled in an object-oriented implementation by a "Person object" with an attribute/field to hold each data item that the entry comprises: the person's name, a list of phone numbers, and a list of addresses. The list of phone numbers would itself contain "PhoneNumber objects" and so on. Each such address-book entry is treated as a single object by the programming language (it can be referenced by a single variable containing a pointer to the object, for instance). Various methods can be associated with the object, such as methods to return the preferred phone number, the home address, and so on.

By contrast, many popular database products such as SQL database management systems (DBMS) are not object-oriented and can only store and manipulate scalar values such as integers and strings organized within tables. The programmer must either convert the object values into groups of simpler values for storage in the database (and convert them back upon retrieval), or only use simple scalar values within the program. Object–relational mapping implements the first approach.[1]

The heart of the problem involves translating the logical representation of the objects into an atomized form that is capable of being stored in the database while preserving the properties of the objects and their relationships so that they can be reloaded as objects when needed. If this storage and retrieval functionality is implemented, the objects are said to be persistent.[1]

Overview
Implementation-specific details of storage drivers are generally wrapped in an API in the programming language in use, exposing methods to interact with the storage medium in a way which is simpler and more in line with the paradigms of surrounding code.

The following is a simple example, written in C# code, to execute a query written in SQL using a database engine.

var sql = "SELECT id, first_name, last_name, phone, birth_date, sex, age FROM persons WHERE id = 10";
var result = context.Persons.FromSqlRaw(sql).ToList();
var name = result[0]["first_name"];
In contrast, the following makes use of an ORM-job API, allowing the writing of code which naturally makes use of the features of the language.

var person = repository.GetPerson(10);
var firstName = person.GetFirstName();
The case above makes use of an object representing the storage repository and methods of that object. Other frameworks might provide code as static methods, as in the below, and yet other methods may not implement an object-oriented system at all. Often the choice of paradigm is made to fit the ORM best into the surrounding language's design principles.

var person = Person.Get(10);
Usually, the framework will expose some filtering and querying functionality, allowing subsets of the storage base to be accessed and modified. The code below queries for people in the database whose ID value is '10'.

var person = Person.Get(Person.Properties.Id == 10);
Comparison with traditional data access techniques
Compared to traditional techniques of exchange between an object-oriented language and a relational database, ORM often reduces the amount of code that needs to be written.[2]

Disadvantages of ORM tools generally stem from the high level of abstraction obscuring what is actually happening in the implementation code. Also, heavy reliance on ORM software has been cited as a major factor in producing poorly designed databases.[3]

Object-oriented databases
Another approach is to use an object-oriented database management system (OODBMS) or document-oriented databases such as native XML databases that provide more flexibility in data modeling. OODBMSs are databases designed specifically for working with object-oriented values. Using an OODBMS eliminates the need for converting data to and from its SQL form, as the data is stored in its original object representation and relationships are directly represented, rather than requiring join tables/operations. The equivalent of ORMs for document-oriented databases are called object-document mappers (ODMs).

Document-oriented databases also prevent the user from having to "shred" objects into table rows. Many of these systems also support the XQuery query language to retrieve datasets.

Object-oriented databases tend to be used in complex, niche applications. One of the arguments against using an OODBMS is that it may not be able to execute ad-hoc, application-independent queries.[citation needed] For this reason, many programmers find themselves more at home with an object-SQL mapping system, even though most object-oriented databases are able to process SQL queries to a limited extent. Other OODBMS provide replication to SQL databases, as a means of addressing the need for ad-hoc queries, while preserving well-known query patterns.[citation needed]

Challenges
A variety of difficulties arise when considering how to match an object system to a relational database. These difficulties are referred to as the object–relational impedance mismatch.[4]

An alternative to implementing ORM is use of the native procedural languages provided with every major database. These can be called from the client using SQL statements. The Data Access Object (DAO) design pattern is used to abstract these statements and offer a lightweight object-oriented interface to the rest of the application.[5]


**This article will briefly explain what object relational mapping (ORM) is, what an ORM _library_ is, and why you should consider using one with your next JavaScript project. We’ll also help you evaluate the best JavaScript and [TypeScript](https://www.sitepoint.com/typescript-tutorial-for-beginners/) ORM libraries based on your needs as a project developer and maintainer.**

We’ll look at each of the following tools:

*   [Knex.js: SQL Query Builder](#knexjssqlquerybuilder)
*   [Sequelize](#sequelize)
*   [Bookshelf](#bookshelf)
*   [Waterline](#waterline)
*   [Objection.js](#objectionjs)
*   [Mongoose](#mongoose)
*   [Typegoose](#typegoose)
*   [TypeORM](#typeorm)
*   [MikroORM](#mikroorm)
*   [Prisma](#prisma)

Object Relational Mapping
-------------------------

Object relational mapping might seem complex, but its purpose is to make your life as a programmer easier. To get data out of a database, you need to write a query. Does that mean you have to learn SQL? Well, no. Object relational mapping makes it possible for you to write queries in the language of your choice.

Object relational mapping is a technique for converting a database query result into entity class instances. An **entity** is simply an object wrapper for a database table. It contains attributes that are mapped to columns of a database table. Entity instances have ways of performing CRUD operations and have support for additional functions that contain custom logic such as validation and data encryption.

If you’re building a small project, installing an ORM library isn’t required. Using SQL statements to drive your application should be sufficient. An ORM is quite beneficial for medium- to large-scale projects that source data from hundreds of database tables. In such a situation, you need a framework that allows you to operate and maintain your application’s data layer in a consistent and predictable way.

Entity classes are the building blocks of business applications, as they’re designed to encapsulate logic for implementing business rules. A business rule is defined to ensure that an automated process only executes within the boundaries of a business policy. Examples of business rules include:

*   customer discounts
*   loan approvals
*   sales commissions
*   shipping and tax calculations

ORM Libraries
-------------

Object relational mapping is commonly undertaken with help of a **library**. The term ORM most commonly refers to an actual ORM library — an object relational _mapper_ — that carries out the work of object relational mapping for you.

Often business rules require the execution of multiple SQL statements that need to run in batches. If a single SQL statement fails, it can leave the database in an inconsistent state. Most ORM libraries support a feature known as **Transactions**, which prevents such an incidents from happening. If an SQL statement fails to run within the context of a transaction, all other SQL statements that had successfully executed within that batch are reversed through an operation known as **roll back**.

Hence, using an ORM library to build your data layer helps ensure that the database will always remain in a consistent state. ORM libraries often contain many more essential features, such as:

*   query builders
*   migration scripts
*   a CLI tool for generating boilerplate code
*   a seeding feature for pre-populating tables with test data

In this article, I’ll provide snippets on how each ORM library does:

*   initial setup and configuration
*   basic CRUD operations
*   advance query operations

I’ve also included important information such as the launch dates, number of users and links to documentation, and support channels if available. I’ll also be discussing important issues relating to query performance, library maintenance and architecture philosophy that you should weigh heavily when making your decision.

I’ve ordered the list based on launch date from the earliest to the newest. I’ve split the list into two sections based on the primary supported language: JavaScript and TypeScript.

Before we begin our evaluation, let’s first take a look at Knex.js, a popular SQL **Query Builder** that comes already integrated with a number of ORM libraries listed here. Knex.js is very flexible and often performs better than some of the ORM libraries that have their own built-in implementation of a Query Builder. Consider this an advantage when choosing an ORM library that uses Knex.js as its foundation.

### Knex.js: SQL Query Builder

*   **Launch**: Dec, 2012
*   [Website](http://knexjs.org/)
*   [GitHub](https://github.com/knex/knex): Used by 158.6k
*   **Databases:** Postgres, MSSQL, MySQL, MariaDB, SQLite3, Oracle, and Amazon Redshift

Knex.js is currently the most mature JavaScript SQL Query builder that can run in both Node.js and the browser (via webpack or Browserify). It’s capable of generating highly performant SQL queries that are on par with manually written SQL statements.

So what’s a Query Builder?

It’s simply an API that provides a set of functions that can be chained together to form a query. Here’s an example:

    knex({ a: 'table', b: 'table' })
      .select({
        aTitle: 'a.title',
        bTitle: 'b.title'
      })
      .whereRaw('?? = ??', ['a.column_1', 'b.column_2'])
    
    SQL Output:
    select `a`.`title` as `aTitle`, `b`.`title` as `bTitle` from `table`
    as `a`, `table` as `b` where `a`.`column_1` = `b`.`column_2`
    

This begs the question of why should one use a Query Builder instead of writing raw SQL statements. I’ll give you four reasons:

*   It helps you abstract your code from your database’s SQL dialect, making switching easier.
*   It eliminates, or greatly reduces, the chances of SQL injection attacks on your application.
*   It allows easy building of queries with dynamic conditions.
*   It comes with additional features and CLI tools for performing database development operations.

Those features include:

*   connection pooling
*   callback and Promise interfaces
*   stream interface
*   transaction support
*   schema support
*   migration
*   seeding

Installing it in your application requires you to install the Knex.js package, along with the driver of the database you’re using:

    $ npm install knex --save
    
    # Then add one of the following (adding a --save) flag:
    $ npm install pg
    $ npm install sqlite3
    $ npm install mysql
    $ npm install mysql2
    $ npm install oracledb
    $ npm install mssql
    

Here’s an example of setup code:

    const knex = require('knex')({
      client: 'mysql',
      connection: {
        host : '127.0.0.1',
        user : 'your_database_user',
        password : 'your_database_password',
        database : 'myapp_test'
      }
    });
    
    knex.schema.createTable('users', function (table) {
      table.increments();
      table.string('name');
      table.timestamps();
    })
    
    Outputs:
    create table `users` (`id` int unsigned not null auto_increment primary key, `name` varchar(255),
    `created_at` datetime, `updated_at` datetime)
    

Here’s an example of a basic query:

    knex('users').where({
      first_name: 'Test',
      last_name:  'User'
    }).select('id')
    
    Outputs:
    select `id` from `users` where `first_name` = 'Test' and `last_name` = 'User'
    

Raw SQL statements are also supported. Here’s an example of a complex query:

    const subcolumn = knex.raw('select avg(salary) from employee where dept_no = e.dept_no')
    .wrap('(', ') avg_sal_dept');
    
    knex.select('e.lastname', 'e.salary', subcolumn)
    .from('employee as e')
    .whereRaw('dept_no = e.dept_no')
    
    Outputs:
    select `e`.`lastname`, `e`.`salary`, (select avg(salary) from employee where dept_no = e.dept_no)
    avg_sal_dept from `employee` as `e` where dept_no = e.dept_no
    

Knex.js also supports TypeScript, which is great, as it allows you to write code like this:

    import { Knex, knex } from 'knex'
    
    interface User {
      id: number;
      age: number;
      name: string;
      active: boolean;
      departmentId: number;
    }
    
    const config: Knex.Config = {
      client: 'sqlite3',
      connection: {
        filename: './data.db',
      },
    });
    
    const knexInstance = knex(config);
    
    try {
      const users = await knex<User>('users').select('id', 'age');
    } catch (err) {
      // error handling
    }
    

In the above TypeScript example, Knex.js is almost acting like an ORM. However, entity object instances aren’t being created. Instead, the interface definition is being used to create JavaScript objects with type-safe properties.

Do note a number of ORM libraries listed in this article use Knex.js under the hood. These include:

*   Bookshelf
*   Objection.js
*   MikroORM

ORM libraries often provide additional features on top of Knex.js. Let’s have a look at them in the next section.

JavaScript ORM Libraries
------------------------

In this category, all libraries listed here are written in JavaScript and can run directly in Node.js. TypeScript support is provided either through built-in types or through [@types/node](https://www.npmjs.com/package/@types/node) definitions package. If you want first-class support for TypeScript projects, you should skip to the **[TypeScript ORM Libraries](#typescriptormlibraries)** section.

In the data access layer, there are two popular architectural patterns that are used:

*   [Data Mapper](https://en.wikipedia.org/wiki/Data_mapper_pattern)
*   [Active Record](https://en.wikipedia.org/wiki/Active_record_pattern)

With the **Data Mapper pattern**, entity classes are pure and only contain attributes. CRUD operations and business rules are implemented in containers known as **repositories**. Here’s an example:

    const repository = connection.getRepository(User);.
    
    const user = new User();
    user.firstName = "Timber";
    await repository.save(user);
    
    const allUsers = await repository.find();
    

With **Active record pattern**, logic for CRUD operations and business rules are implemented within entity classes. Here’s a similar example implementation of the above:

    const user = new User();
    user.firstName = "Timber";
    await user.save();
    
    const allUsers = await User.find();
    

There are pros and cons of using either pattern. These patterns were named by Martin Fowler in his 2003 book _Patterns of Enterprise Application Architecture_. You should check the book out if you want more detailed information on the subject. Most ORM libraries listed in this article support one or both patterns.

Let’s start looking at them now.

### Sequelize

*   **Launch**: July 2010
*   [Website](https://sequelize.org/)
*   [GitHub](https://sequelize.org/): used by 271k
*   [Slack](https://sequelize-slack.herokuapp.com/)
*   **Databases**: Postgres, MySQL, MariaDB, SQLite and Microsoft SQL Server

Sequelize is a very mature and popular Node.js ORM library with excellent documentation containing well explained code examples. It supports many of the data layer features that we’ve already mentioned before in previous libraries. Unlike Bookshelf, it has its own Query Builder which performs just as well as Knex.js

Installing the library is quite simple, and the database driver is quite straightforward:

    $ npm i sequelize # This will install v6
    
    # And one of the following:
    $ npm i pg pg-hstore # Postgres
    $ npm i mysql2
    $ npm i mariadb
    $ npm i sqlite3
    $ npm i tedious # Microsoft SQL Server
    

Below is an example of the setup code along with examples of CRUD and basic query statements:

    const { Sequelize } = require('sequelize');
    
    // Connect to database
    const sequelize = new Sequelize('database', 'username', 'password', {
      host: 'localhost',
      dialect: /* one of 'mysql' | 'mariadb' | 'postgres' | 'mssql' */
    });
    
    // Create Model
    const User = sequelize.define('User', {
      // Model attributes are defined here
      firstName: {
        type: DataTypes.STRING,
        allowNull: false
      },
      lastName: {
        type: DataTypes.STRING
        // allowNull defaults to true
      }
    }, {
      // Other model options go here
    });
    
    // Create instance
    const jane = User.build({ firstName: "Jane", lastName: "Doe" });
    await jane.save(); // save to database
    
    // Shortcut for creating instance and saving to database at once
    const jane = await User.create({ firstName: "Jane", lastName: "Doe" });
    
    // Find all users
    const users = await User.findAll();
    console.log(users.every(user => user instanceof User)); // true
    console.log("All users:", JSON.stringify(users, null, 2));
    

The following is an example of how a complex query is written:

    // What if you wanted to obtain something like WHERE char_length("content") = 7?
    Post.findAll({
      where: sequelize.where(sequelize.fn('char_length', sequelize.col('content')), 7)
    });
    // SELECT ... FROM "posts" AS "post" WHERE char_length("content") = 7
    
    // A more complex example
    Post.findAll({
      where: {
        [Op.or]: [
          sequelize.where(sequelize.fn('char_length', sequelize.col('content')), 7),
          {
            content: {
              [Op.like]: 'Hello%'
            }
          },
          {
            [Op.and]: [
              { status: 'draft' },
              sequelize.where(sequelize.fn('char_length', sequelize.col('content')), {
                [Op.gt]: 10
              })
            ]
          }
        ]
      }
    });
    

In the last complex query example, the SQL output was:

    SELECT
      ...
    FROM "posts" AS "post"
    WHERE (
      char_length("content") = 7
      OR
      "post"."content" LIKE 'Hello%'
      OR (
        "post"."status" = 'draft'
        AND
        char_length("content") > 10
      )
    )
    

Sequelize supports raw SQL statements, which gives developers the flexibility to write complex and highly performant SQL statements. The results can also be mapped to object entity instances. Here’s an example:

    // Callee is the model definition. This allows you to easily map a query to a predefined model
    const projects = await sequelize.query('SELECT * FROM projects', {
      model: Projects,
      mapToModel: true // pass true here if you have any mapped fields
    });
    // Each element of `projects` is now an instance of Project
    

The main downside of Sequelize is that development has slowed down and that [issues](https://github.com/sequelize/sequelize/issues/12956) have piled up without being resolved. Fortunately, one of the maintainers has [announced](https://github.com/sequelize/sequelize/issues/12956) that the library will get the attention it deserves from 2021. Do note that all ORM library projects in this article are open source and that they do need help from developers to make them better.

### Bookshelf

*   **Launch**: March, 2013
*   [Website](https://bookshelfjs.org/)
*   [GitHub](https://github.com/bookshelf/bookshelf): Used by 22.4k
*   [Plugins](https://bookshelfjs.org/#official-plugins)
*   **Databases** : PostgreSQL, MySQL, and SQLite3

Bookshelf is one of the oldest and most basic ORM JavaScript library we have available. It’s built on top of Knex.js SQL Query Builder, and it takes a lot of ideas from the Data Mapper pattern. It provides additional features, such as:

*   eager and nested-eager relation loading
*   polymorphic associations
*   support for one-to-one, one-to-many, and many-to-many relations.

It’s unfortunate there’s no built-in support for validation. However, it can be implemented in code via a third-party library such as [`checkit`](https://github.com/tgriesser/checkit).

Installing Bookshelf in your project is as follows:

    $ npm install knex
    $ npm install bookshelf
    
    # Then add one of the following:
    $ npm install pg
    $ npm install mysql
    $ npm install sqlite3
    

Setup code looks like this:

    // Setting up the database connection
    const knex = require('knex')({
      client: 'mysql',
      connection: {
        host     : '127.0.0.1',
        user     : 'your_database_user',
        password : 'your_database_password',
        database : 'myapp_test',
        charset  : 'utf8'
      }
    })
    const bookshelf = require('bookshelf')(knex)
    
    // Define User model
    const User = bookshelf.model('User', {
      tableName: 'users',
      posts() {
        return this.hasMany(Posts)
      }
    })
    
    // Define Post model
    const Post = bookshelf.model('Post', {
      tableName: 'posts',
      tags() {
        return this.belongsToMany(Tag)
      }
    })
    
    // Define Tag model
    const Tag = bookshelf.model('Tag', {
      tableName: 'tags'
    })
    
    // Unfortunate example of unreadable code
    new User({id: 1}).fetch({withRelated: ['posts.tags']}).then((user) => {
      console.log(user.related('posts').toJSON())
    }).catch((error) => {
      console.error(error)
    })
    

You’ll need to look up the Knex.js documentation to see how to perform queries and CRUD transactions. Bookshelf’s documentation doesn’t cover this.

Interestingly, [Strapi](https://strapi.io/), a headless CMS, uses [Bookshelf](https://www.npmjs.com/package/strapi-connector-bookshelf) as its default database connector. However, it’s worth noting the following issues:

*   the documentation is not particularly helpful
*   at the time of writing, the library hadn’t been updated for five months

### Waterline

*   **Launch**: May 2013
*   [Website](https://waterlinejs.org)
*   [GitHub](https://github.com/balderdashy/waterline): Used by 8.5k
*   [Documentation](https://sailsjs.com/documentation/concepts/models-and-orm)
*   **Databases** : Local disk/memory, MySQL, MongoDB, and Postgres(official adapters)
*   [Community Database Adapters](https://sailsjs.com/documentation/concepts/extending-sails/adapters/available-adapters): Oracle, SAP, Cassandra, IBM, Apache Derby, Redis, Solr and more

Waterline is the default ORM used by [Sails.js](https://sailsjs.com/), a Node.js framework. When using Sails.js to develop your project, the amount of code you need to write to build your own database API is greatly reduced. This is achieved using convention-over-configuration philosophy and the [Blueprints API](https://sailsjs.com/documentation/concepts/blueprints) that contains boilerplate code for accessing the database and performing CRUD functions. In addition, Sails.js provides a command-line interface that helps developers generate API routes, perform migrations and other data layer functions. Typescript support is available via the [Typed definitions](https://github.com/DefinitelyTyped/DefinitelyTyped) package.

In this article, we’re going to assume you’d want to use the Waterline ORM as a standalone, which is possible. Let’s look at how to install and set it up.

Installation requires you to install the Waterline library, then one of the database adapters:

    $ npm install --save waterline
    
    # Install database adapters
    $ npm install --save sails-mysql
    $ npm install --save-dev sails-disk
    

Here’s a partial sample of the setup code:

    const Waterline = require('waterline');
    const sailsDiskAdapter = require('sails-disk');
    const waterline = new Waterline();
    
    const userCollection = Waterline.Collection.extend({
      identity: 'user',
      datastore: 'default',
      primaryKey: 'id',
    
      attributes: {
        id: {
            type: 'number',
            autoMigrations: {autoIncrement: true}
        },
        firstName: {type:'string'},
        lastName: {type:'string'},
    
        // Add a reference to Pets
        pets: {
          collection: 'pet',
          via: 'owner'
        }
      }
    });
    
    waterline.registerModel(userCollection);
    

Here’s a partial sample of some CRUD code:

    (async ()=>{
        // First we create a user
        var user = await User.create({
          firstName: 'Neil',
          lastName: 'Armstrong'
        });
    
        // Then we create the pet
        var pet = await Pet.create({
          breed: 'beagle',
          type: 'dog',
          name: 'Astro',
          owner: user.id
        });
    
        // Then we grab all users and their pets
        var users = await User.find().populate('pets');
      })()
    

Here’s a sample of a basic query code:

    var thirdPageOfRecentPeopleNamedMary = await Model.find({
      where: { name: 'mary' },
      skip: 20,
      limit: 10,
      sort: 'createdAt DESC'
    });
    

When it comes to handling complex queries, the documentation seems to be missing that part. If you plan on using Sails.js, using Waterline ORM is a no brainer. But as a standalone, the ORM library faces the following issues:

*   Documentation is mixed in with Sails.js documentation.
*   At the time of writing, the library package hadn’t been updated in nine months.

### Objection.js

*   **Launch**: April 2015
*   [Website](https://vincit.GitHub.io/objection.js/)
*   [GitHub](https://github.com/vincit/objection.js): Used by 5.7k
*   [Plugins](https://vincit.github.io/objection.js/guide/plugins.html#_3rd-party-plugins)
*   **Databases** : SQLite3, Postgres and MySQL (including all Knex.js supported databases)

Objection.js is a minimal Node.js ORM library designed to stay out of your way and make is easy to access SQL databases. In this category, Objection.js is the youngest, and it appears to defeat many arguments that have been raised against the use of ORM libraries.

The Objection.js documentation is excellent. It’s well written, as you can easily find clear instructions for building your application’s data layer. The syntax is clean and easy to understand. It’s built on top of Knex.js, and has official built-in support for TypeScript. It has about everything you need in an ORM.

Looking at the numbers, it’s quite surprising Objection.js isn’t as popular at it should be. ORM libraries such as Sequelize and TypeORM do offer many more features, which may explain their popularity. However, I think the set of features the Objection.js team decided to go with is perfect for an open-source library. It means fewer bugs occur over time, and the small team are able to resolve them in good time. You can see evidence of this by looking at the [issues](https://github.com/Vincit/objection.js/issues) tab, which had about 50 unresolved issues at the time of writing.

In contrast, Sequelize and TypeORM, which are bigger in terms features, have unfortunately generated a massive backlog for their maintainers. Currently, each have 1,000+ issues that haven’t been resolved and there doesn’t seem to be an increase in the number of maintainers contributing to the project.

If you’re having any doubt about picking this library, check out this [testimonals](https://github.com/Vincit/objection.js/issues/1069) link.

Let’s take a look at the installation steps and some sample code. To get started, you’ll need to install Objection.js, Knex.js and one of the database adapters:

    npm install objection knex
    
    # Install database adapter
    npm install pg
    npm install sqlite3
    npm install mysql
    npm install mysql2
    

The setup code is so simple it hardly needs any explanation:

    const { Model } = require('objection');
    const Knex = require('knex');
    
    // Initialize knex.
    const knex = Knex({
      client: 'sqlite3',
      useNullAsDefault: true,
      connection: {
        filename: 'example.db'
      }
    });
    
    // Give the Knex instance to Objection.
    Model.knex(knex);
    
    // Person model.
    class Person extends Model {
      static get tableName() {
        return 'persons';
      }
    
      static get relationMappings() {
        return {
          children: {
            relation: Model.HasManyRelation,
            modelClass: Person,
            join: {
              from: 'persons.id',
              to: 'persons.parentId'
            }
          }
        };
      }
    }
    
    async function createSchema() {
      if (await knex.schema.hasTable('persons')) {
        return;
      }
    
      // Create database schema. You should use Knex migration files
      // to do this. We create it here for simplicity.
      await knex.schema.createTable('persons', table => {
        table.increments('id').primary();
        table.integer('parentId').references('persons.id');
        table.string('firstName');
      });
    }
    
    async function main() {
      // Create some people.
      const sylvester = await Person.query().insertGraph({
        firstName: 'Sylvester',
    
        children: [
          {
            firstName: 'Sage'
          },
          {
            firstName: 'Sophia'
          }
        ]
      });
    
      console.log('created:', sylvester);
    
      // Fetch all people named Sylvester and sort them by ID.
      // Load `children` relation eagerly.
      const sylvesters = await Person.query()
        .where('firstName', 'Sylvester')
        .withGraphFetched('children')
        .orderBy('id');
    
      console.log('sylvesters:', sylvesters);
    }
    
    createSchema()
      .then(() => main())
      .then(() => knex.destroy())
      .catch(err => {
        console.error(err);
        return knex.destroy();
      });
    

Here’s an example of basic query:

    // query 1
    const person = await Person.query().findById(1);
    
    //query 2
    const middleAgedJennifers = await Person.query()
      .select('age', 'firstName', 'lastName')
      .where('age', '>', 40)
      .where('age', '<', 60)
      .where('firstName', 'Jennifer')
      .orderBy('lastName');
    

The SQL output for the basic query:

    -- query 1
    select "persons".* from "persons" where "persons"."id" = 1
    
    -- query 2
    select "age", "firstName", "lastName"
    from "persons"
    where "age" > 40
    and "age" < 60
    and "firstName" = 'Jennifer'
    order by "lastName" asc
    

Here’s an example of a complex query:

    const people = await Person.query()
      .select('persons.*', 'parent.firstName as parentFirstName')
      .innerJoin('persons as parent', 'persons.parentId', 'parent.id')
      .where('persons.age', '<', Person.query().avg('persons.age'))
      .whereExists(
        Animal.query()
          .select(1)
          .whereColumn('persons.id', 'animals.ownerId')
      )
      .orderBy('persons.lastName');
    
    console.log(people[0].parentFirstName);
    

The SQL output for the complex query:

    select "persons".*, "parent"."firstName" as "parentFirstName"
    from "persons"
    inner join "persons"
      as "parent"
      on "persons"."parentId" = "parent"."id"
    where "persons"."age" < (
      select avg("persons"."age")
      from "persons"
    )
    and exists (
      select 1
      from "animals"
      where "persons"."id" = "animals"."ownerId"
    )
    order by "persons"."lastName" asc
    

In addition to the features Knex.js already provides, Objection.js has:

*   official TypeScript support
*   support for lifecycle hooks
*   built-in validation support using [JSON Schema](http://json-schema.org/) syntax
*   [plugins](https://vincit.github.io/objection.js/guide/plugins.html#_3rd-party-plugins)

The library is very well maintained. For SQL databases, Objection.js appears to be the best ORM library for your JavaScript application. Unfortunately, it doesn’t support NoSQL databases. But the next library we feature does support NoSQL databases.

### Mongoose

*   **Launch**: April 2010
*   [Website](https://mongoosejs.com)
*   [GitHub](https://github.com/Automattic/mongoose/): Used by 1.4m
*   [Slack](http://slack.mongoosejs.io/)
*   [Plugins](https://plugins.mongoosejs.io/)
*   **Databases** : MongoDB

If you plan on using MongoDB as your database, then Mongoose is likely going to be your ORM of choice. It’s currently the most popular ORM library in the Node.js world. Mongoose uses schema syntax to define models. Its feature list includes:

*   built-in type casting
*   validation
*   query building
*   hooks via middleware

Mongoose only supports MongoDB, so installation only requires one package:

    npm install mongoose
    

Below is an example of the setup code:

    const mongoose = require('mongoose');
    mongoose.connect('mongodb://localhost/test', {useNewUrlParser: true, useUnifiedTopology: true});
    
    // With Mongoose, everything is derived from a Schema.
    const kittySchema = new mongoose.Schema({
       name: {
        type: String,
        required: true
      }
    });
    const Kitten = mongoose.model('Kitten', kittySchema);
    
    const fluffy = new Kitten({ name: 'fluffy' });
    fluffy.save(function (err, fluffy) {
        if (err) return console.error(err);
        console.log(fluffy.name, 'saved!')
      });
    

There are two ways of defining queries in Mongoose. Below are both examples:

    // With a JSON doc
    Person.
      find({
        occupation: /host/,
        'name.last': 'Ghost',
        age: { $gt: 17, $lt: 66 },
        likes: { $in: ['vaporizing', 'talking'] }
      }).
      limit(10).
      sort({ occupation: -1 }).
      select({ name: 1, occupation: 1 }).
      exec(callback);
    
    // Using query builder
    Person.
      find({ occupation: /host/ }).
      where('name.last').equals('Ghost').
      where('age').gt(17).lt(66).
      where('likes').in(['vaporizing', 'talking']).
      limit(10).
      sort('-occupation').
      select('name occupation').
      exec(callback);
    

Of course, there’s no raw SQL option, since MongoDB is a NoSQL database. MongoDB also doesn’t support transactions. If that’s important for your project, you’ll need to stick with SQL databases.

One key advantage of Mongoose over all other open-source ORM libraries listed here is that it’s development is sponsored by the [Tidelift](https://tidelift.com/) platform. This means security issues are identified and patched early.

One downside is that Mongoose doesn’t officially support TypeScript. Unofficially, you can use TypeScript, but it will take a bit of extra work to maintain your models. Fortunately, the next ORM library we’ll look at addresses this issue.

TypeScript ORM Libraries
------------------------

In this category, all libraries listed here provide first-class support for TypeScript projects. You can use them in JavaScript projects, but documentation is mostly written for TypeScript code.

### Typegoose

*   **Launch**: March 2017
*   [Website](https://typegoose.GitHub.io/typegoose/)
*   [GitHub](https://github.com/typegoose/typegoose): Used by 2k
*   **Databases**: MongoDB

Typegoose is a “wrapper” for easily writing Mongoose models with TypeScript. This library solves the problem of having to maintain a separate Mongoose model and a TypeScript interface. With Typegoose, you only need to define your model schema using the Typegoose interface.

Under the hood, it uses the Reflect and reflect-metadata API to retrieve the types of the properties, so redundancy can be significantly reduced.

Installing Typegoose in your projects requires several packages:

    npm i -s @typegoose/typegoose # install typegoose itself
    npm i -s mongoose # install peer-dependency mongoose
    npm i -D @types/mongoose # install all types for mongoose
    

Below is an example of a Mongoose model written in JavaScript:

    const kittenSchema = new mongoose.Schema({
      name: String
    });
    
    const Kitten = mongoose.model('Kitten', kittenSchema);
    
    let document = await Kitten.create({ name: 'Kitty' });
    // "document" has no types
    

Below is the same model written in TypeScript using Typegoose library:

    class KittenClass {
      @prop()
      public name?: string;
    }
    
    const Kitten = getModelForClass(KittenClass);
    
    let document = await Kitten.create({ name: 'Kitty' });
    // "document" has proper types of KittenClass
    

The following code sample shows the setup process and how to execute CRUD commands:

    import { prop, getModelForClass } from '@typegoose/typegoose';
    import * as mongoose from 'mongoose';
    
    class User {
      @prop()
      public name?: string;
    
      @prop({ type: () => [String] })
      public jobs?: string[];
    }
    
    const UserModel = getModelForClass(User); // UserModel is a regular Mongoose Model with correct types
    
    (async () => {
      await mongoose.connect('mongodb://localhost:27017/', { useNewUrlParser: true, useUnifiedTopology: true, dbName: "test" });
    
      const { _id: id } = await UserModel.create({ name: 'JohnDoe', jobs: ['Cleaner'] } as User); // an "as" assertion, to have types for all properties
      const user = await UserModel.findById(id).exec();
    
      console.log(user); // prints { _id: 59218f686409d670a97e53e0, name: 'JohnDoe', __v: 0 }
    })();
    

Since Typegoose is simply a TypeScript wrapper for an ORM library, you’ll have to look at the Mongoose documentation to see how to perform CRUD tasks.

### TypeORM

*   **Launch** : Feb 21, 2016
*   [Website](https://typeorm.io)
*   [GitHub](https://github.com/typeorm/typeorm): Used by 71.8k
*   [Slack](https://typeorm.slack.com/join/shared_invite/zt-gej3gc00-hR~L~DqGUJ7qOpGy4SSq3g#/)
*   **Databases** : MySQL, MariaDB, Postgres, CockroachDB, SQLite, Microsoft SQL Server, Oracle, SAP Hana, sql.js and MongoDB

TypeORM is currently the most popular ORM library built for TypeScript projects. It can run on many platforms, including:

*   Node.js
*   the browser
*   on mobile — Cordova, PhoneGap, Ionic, React Native and NativeScript
*   Electron

The library also supports both Active Record and Data Mapper patterns, allowing developers to build high-quality, scalable and maintainable database-driven applications. It’s highly influenced by other ORMs such as Hibernate, Doctrine and Entity Framework. This means developers with Java and Ruby backgrounds will feel right at home.

TypeORM is an ORM that can run in Node.js, the browser, Cordova, PhoneGap, Ionic, React Native, NativeScript, Expo, and Electron platforms, and can be used with TypeScript and JavaScript. Its goal is to always support the latest JavaScript features and provide additional features that help you to develop any kind of application that uses databases — from small applications with a few tables to large-scale enterprise applications with multiple databases.

Installing TypeORM requires installing multiple packages, including database adapters and additional TypeScript packages:

    npm install typeorm --save
    
    # You need to install reflect-metadata shim:
    npm install reflect-metadata --save
    
    # and import it somewhere in the global place of your app (for example in app.ts):
    # import "reflect-metadata";
    
    # You may need to install node typings:
    npm install @types/node --save-dev
    
    # Install a database driver:
    npm install mysql --save (you can install mysql2 instead as well)
    npm install pg --save
    npm install sqlite3 --save
    npm install mssql --save
    npm install sql.js --save
    # To make the Oracle driver work, you need to follow the installation instructions from their site.
    npm install oracledb --save
    # for SAP Hana
    npm i @sap/hana-client
    npm i hdb-pool
    # for MongoDB (experimental)
    npm install mongodb --save
    

Next, you’ll need to enable the following settings in `tsconfig.json`:

    "emitDecoratorMetadata": true,
    "experimentalDecorators": true,
    

You may also need to enable `es6` in the `lib` section of compiler options, or install `es6-shim` from `@types`.

Alternatively, instead of manually setting up a TypeORM project, you can simply use the TypeORM CLI tool to scaffold the project for you:

    npm install typeorm -g
    typeorm init --name MyProject --database mysql
    

Models can be defined using the DataMapper implementation:

    // Define entity model first
    import {Entity, PrimaryGeneratedColumn, Column} from "typeorm";
    
    @Entity()
    export class User {
    
        @PrimaryGeneratedColumn()
        id: number;
    
        @Column()
        firstName: string;
    
        @Column()
        lastName: string;
    
        @Column()
        age: number;
    
    }
    
    // Perform CRUD tasks
    const repository = connection.getRepository(User);
    
    const user = new User();
    user.firstName = "Timber";
    user.lastName = "Saw";
    user.age = 25;
    await repository.save(user);
    
    const allUsers = await repository.find();
    const firstUser = await repository.findOne(1); // find by id
    const timber = await repository.findOne({ firstName: "Timber", lastName: "Saw" });
    
    await repository.remove(timber);
    

Alternatively, you can use an Active Record pattern to define your models:

    import {Entity, PrimaryGeneratedColumn, Column, BaseEntity} from "typeorm";
    
    @Entity()
    export class User extends BaseEntity {
    
        @PrimaryGeneratedColumn()
        id: number;
    
        @Column()
        firstName: string;
    
        @Column()
        lastName: string;
    
        @Column()
        age: number;
    
    }
    
    const user = new User();
    user.firstName = "Timber";
    user.lastName = "Saw";
    user.age = 25;
    await user.save();
    
    const allUsers = await User.find();
    const firstUser = await User.findOne(1);
    const timber = await User.findOne({ firstName: "Timber", lastName: "Saw" });
    
    await timber.remove();
    

TypeORM provides multiple ways of building queries using its own [Query Builder](https://typeorm.io/#/select-query-builder). Here’s one of its examples:

    const firstUser = await connection
        .getRepository(User)
        .createQueryBuilder("user")
        .where("user.id = :id", { id: 1 })
        .getOne();
    

Below is the SQL output:

    SELECT
        user.id as userId,
        user.firstName as userFirstName,
        user.lastName as userLastName
    FROM users user
    WHERE user.id = 1
    

Here’s an example of a complex query:

    const posts = await connection.getRepository(Post)
        .createQueryBuilder("post")
        .where(qb => {
            const subQuery = qb.subQuery()
                .select("user.name")
                .from(User, "user")
                .where("user.registered = :registered")
                .getQuery();
            return "post.title IN " + subQuery;
        })
        .setParameter("registered", true)
        .getMany();
    

While TypeORM seems to cover all the features required to build the data layer for your application, there are a few thorny issues you should be aware of. The most notable one is regarding performance, which has been reported and documented in this [unresolved issue](https://github.com/typeorm/typeorm/issues/3857).

Due to the vast number of features that the library supports, the backlog of unresolved issues has piled up to significant levels, placing a heavy burden on the core maintainers. This issue has been addressed by the maintainers [here](https://github.com/typeorm/typeorm/issues/3267), where they discuss the future of TypeORM.

Regardless, TypeORM is currently the most popular TypeScript ORM. This means finding developers familiar with the library will be easier when it comes to supporting your project in the long run. Hopefully, more contributors will join the core maintenance team and help stabilize the ORM.

### MikroORM

*   **Launch**: Mar 11, 2018
*   [Website](https://mikro-orm.io/)
*   [GitHub](https://github.com/mikro-orm/mikro-orm): Used by 206
*   [Slack](https://join.slack.com/t/mikroorm/shared_invite/enQtNTM1ODYzMzM4MDk3LWM4ZDExMjU5ZDhmNjA2MmM3MWMwZmExNjhhNDdiYTMwNWM0MGY5ZTE3ZjkyZTMzOWExNDgyYmMzNDE1NDI5NjA)
*   **Databases** : MongoDB, MySQL, MariaDB, PostgreSQL and SQLite

MikroORM is one of the youngest Node.js TypeScript ORM entrants in this list. It supports both SQL and NoSQL databases, which is an amazing feat that not many ORMs have accomplished. It’s heavily inspired by [Doctrine](https://www.doctrine-project.org/) and [Nextras ORM](https://nextras.org/orm/). Anyone familiar with these should feel right at home with MikroORM.

The library is optimized for transactions and performance through [Identity Map patterns](https://martinfowler.com/eaaCatalog/identityMap.html). It also supports the Data Mapper pattern. The [documentation](https://mikro-orm.io/docs/installation) is excellent, with easy navigation to specific topics. One of the key advantages with using newer ORM libraries is that they’re designed to overcome many of the architectural issues faced by older and larger libraries.

As you go through the code samples I’ve provided, you’ll notice the syntax is much simpler to understand. This is key for building large-scale projects that will remain maintainable in the long run. Let’s now go through the installation process:

    npm i -s @mikro-orm/core @mikro-orm/mongodb     # for mongo
    npm i -s @mikro-orm/core @mikro-orm/mysql       # for mysql
    npm i -s @mikro-orm/core @mikro-orm/mariadb     # for mariadb
    npm i -s @mikro-orm/core @mikro-orm/postgresql  # for postgresql
    npm i -s @mikro-orm/core @mikro-orm/sqlite      # for sqlite
    

Next, you need to enable support for [decorators](https://www.typescriptlang.org/docs/handbook/decorators.html) and [`esModuleInterop`](https://www.typescriptlang.org/tsconfig#esModuleInterop) in `tsconfig.json`:

    "experimentalDecorators": true,
    "emitDecoratorMetadata": true,
    "esModuleInterop": true,
    

Then call `MikroORM.init` as part of bootstrapping your app:

    const orm = await MikroORM.init({
      entities: [Author, Book, BookTag],
      dbName: 'my-db-name',
      type: 'mongo', // one of `mongo` | `mysql` | `mariadb` | `postgresql` | `sqlite`
      clientUrl: '...', // defaults to 'mongodb://localhost:27017' for mongodb driver
    });
    console.log(orm.em); // access EntityManager via `em` property
    

MikroORM provides a command-line tool, `@mikro-orm/cli`, which you access using `npx` or by installing locally and accessing it like this:

    # manually
    $ node node_modules/.bin/mikro-orm
    # via npx
    $ npx mikro-orm
    # or via yarn
    $ yarn mikro-orm
    

The command-line tool helps with the development process and can help you with performing tasks such as:

*   schema management
*   importing SQL file to database
*   generating entities
*   database migration

MikroORM provides three ways of defining entity classes. Here’s one example using the [reflect metadata](https://www.npmjs.com/package/reflect-metadata) syntax:

    @Entity()
    export class Book extends BaseEntity {
    
      @Property()
      title!: string;
    
      @ManyToOne(() => Author)
      author!: Author;
    
      @ManyToOne(() => Publisher, { wrappedReference: true, nullable: true })
      publisher?: IdentifiedReference<Publisher>;
    
      @ManyToMany({ entity: 'BookTag', fixedOrder: true })
      tags = new Collection<BookTag>(this);
    
    }
    

Once you’ve defined your entities, you can use the [entity manager](https://mikro-orm.io/docs/entity-manager) to persist and query your data:

    // use constructors in your entities for required parameters
    const author = new Author('Jon Snow', 'snow@wall.st');
    author.born = new Date();
    
    const publisher = new Publisher('7K publisher');
    
    const book1 = new Book('My Life on The Wall, part 1', author);
    book1.publisher = publisher;
    const book2 = new Book('My Life on The Wall, part 2', author);
    book2.publisher = publisher;
    const book3 = new Book('My Life on The Wall, part 3', author);
    book3.publisher = publisher;
    
    // just persist books, author and publisher will be automatically cascade persisted
    await orm.em.persistAndFlush([book1, book2, book3]);
    
    // or one by one
    orm.em.persist(book1);
    orm.em.persist(book2);
    orm.em.persist(book3);
    await orm.em.flush(); // flush everything to database at once
    
    // Update existing book
    const book = await orm.em.findOne(Book, 1);
    book.title = 'How to persist things...';
    
    // no need to persist `book` as its already managed by the EM
    await orm.em.flush();
    
    // Retrieve all books
    const books = await orm.em.find(Book, {});
    for (const book of books) {
      console.log(book.title);
    }
    

Querying of entities can be done via a conditions object known as `FilterQuery`. Here are different examples:

    // search by entity properties
    const users = await orm.em.find(User, { firstName: 'John' });
    
    // for searching by reference you can use primary key directly
    const id = 1;
    const users = await orm.em.find(User, { organization: id });
    
    // or pass unpopulated reference (including `Reference` wrapper)
    const ref = await orm.em.getReference(Organization, id);
    const users = await orm.em.find(User, { organization: ref });
    
    // fully populated entities as also supported
    const ent = await orm.em.findOne(Organization, id);
    const users = await orm.em.find(User, { organization: ent });
    
    // complex queries with operators
    const users = await orm.em.find(User, { $and: [{ id: { $nin: [3, 4] } }, { id: { $gt: 2 } }] });
    
    // you can also search for array of primary keys directly
    const users = await orm.em.find(User, [1, 2, 3, 4, 5]);
    
    // and in findOne all of this works, plus you can search by single primary key
    const user1 = await orm.em.findOne(User, 1);
    

The library also supports:

*   fetching partial entities
*   fetching paginated results
*   using custom SQL fragments

To perform even more complex queries, you can use the [Query Builder](https://mikro-orm.io/docs/query-builder). Here’s some example code:

    const qb = orm.em.createQueryBuilder(Author);
    qb.update({ name: 'test 123', type: PublisherType.GLOBAL }).where({ id: 123, type: PublisherType.LOCAL });
    
    console.log(qb.getQuery());
    // update `publisher2` set `name` = ?, `type` = ? where `id` = ? and `type` = ?
    
    console.log(qb.getParams());
    // ['test 123', PublisherType.GLOBAL, 123, PublisherType.LOCAL]
    
    // run the query
    const res1 = await qb.execute();
    

Under the hood, MikroORM’s query builder uses Knex.js, which you can get access to via the `qb.getKnexQuery()` function. This means all the complex and raw SQL queries you want to construct and run can be performed. Hence, you get the flexibility and performance benefits of choosing MikroORM in your tech stack. The [documentation](https://mikro-orm.io/docs/query-builder) on its Query Builder has many examples of query building — including different types of joins — which are too many to list here. You’ll be pleased to learn that the Query Builder provides a function for displaying its SQL output during development without enabling a debug option. Here’s an example:

    const qb = orm.em.createQueryBuilder(BookTag, 't');
    qb.select(['b.*', 't.*'])
      .leftJoin('t.books', 'b')
      .where('b.title = ? or b.title = ?', ['test 123', 'lol 321'])
      .andWhere('1 = 1')
      .orWhere('1 = 2')
      .limit(2, 1);
    
    console.log(qb.getQuery());
    // select `b`.*, `t`.*, `e1`.`book_tag_id`, `e1`.`book_uuid_pk` from `book_tag` as `t`
    // left join `book_to_book_tag` as `e1` ON `t`.`id` = `e1`.`book_tag_id`
    // left join `book` as `b` ON `e1`.`book_uuid_pk` = `b`.`uuid_pk`
    // where (((b.title = ? or b.title = ?) and (1 = 1)) or (1 = 2))
    // limit ? offset ?
    

One issue of concern is that the library is quite young and the number of users are quite low. However, the library’s founder has enabled the [GitHub sponsor](https://github.com/sponsors) feature, which allows them to raise funds so that they can work full-time on the project. I believe this is a better approach to open-source development than having to work part-time on a different project. By having full-time developers working on an open-source project, they can focus on maintaining the quality of the library and ensuring the backlog is kept to a minimum. I do hope that they get a major sponsor soon.

### Prisma

*   **Launch**: April 2019
*   [Website](https://www.prisma.io/)
*   [GitHub](https://github.com/prisma/prisma): Used by 5.7k
*   **Databases** : PostgreSQL, MySQL, SQLite, SQL Server

Prisma is the most recent TypeScript ORM in this article. It describes itself as a “next-generation ORM” that makes working with databases easy for application developers. It provides the following tools:

*   **[Prisma Client](https://www.prisma.io/docs/concepts/components/prisma-client/)**: a client library that provides type-safe access to the database
*   **[Prisma Migrate](https://www.prisma.io/docs/concepts/components/prisma-migrate/)** ([preview](https://www.prisma.io/docs/about/releases#preview)): a migration tool that autogenerates when you make changes to the schema file
*   **[Prisma Studio](https://www.prisma.io/docs/concepts/components/prisma-studio/)**: a modern GUI for browsing and managing data in your database

Prisma is very different from all the other ORMs we’ve looked at. It doesn’t use object models (entity classes), but rather a schema file to map all the tables and columns. This file is used by the migration tool to generate an SQL migration file and the client library to generate type definitions. All generated type definitions are stored in a `.prisma/client/index.d.ts` folder. Here’s an example of the generated representation for `User` type:

    export declare type User = {
      id: string
      email: string
      name: string | null
    }
    

You may have noticed that the `posts` reference in the model isn’t present in the TypeScript definition. The recommended solution is to create a variation of the `User` type like this:

    import { Prisma } from '@prisma/client'
    // Define a type that includes the relation to `Post`
    type UserWithPosts = Prisma.UserGetPayload<{
      include: { posts: true }
    }>
    

When you write a query, your code will be checked to ensure you don’t reference a property that doesn’t exist and that you assign the correct data type for each property. When you execute the query, all results will be returned in plain JavaScript objects.

Traditional ORMs provide an object-oriented way for working with relational databases by mapping tables to _model classes_ in your programming language. This approach leads to many problems that are caused by the [object-relational impedance mismatch](https://en.wikipedia.org/wiki/object%E2%80%93relational_impedance_mismatch).

Setting up a Prisma project is a bit of a process, which you can find the full instructions [here](https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch-typescript-postgres). For now, we’re simply just evaluating. Here are the basic installation steps:

    npm install prisma typescript ts-node @types/node --save-dev
    

You’ll need to update `tsconfig.json` as follows:

    {
      "compilerOptions": {
        "sourceMap": true,
        "outDir": "dist",
        "strict": true,
        "lib": ["esnext"],
        "esModuleInterop": true
      }
    }
    

Start by creating your application’s data model in the schema file located at `prisma/schema.prisma`:

    datasource db {
      provider = "postgresql"
      url      = env("DATABASE_UR
    }
    
    model Post {
      id        Int      @default(autoincrement()) @id
      createdAt DateTime @default(now())
      updatedAt DateTime @updatedAt
      title     String   @db.VarChar(255)
      content   String?
      published Boolean  @default(false)
      author    User     @relation(fields: [authorId], references: [id])
      authorId  Int
    }
    
    model Profile {
      id     Int     @default(autoincrement()) @id
      bio    String?
      user   User    @relation(fields: [userId], references: [id])
      userId Int     @unique
    }
    
    model User {
      id      Int      @default(autoincrement()) @id
      email   String   @unique
      name    String?
      posts   Post[]
      profile Profile?
    }
    

Next, you’ll need to map your data model to the database schema using `prisma migrate` CLI tool:

    npx prisma migrate dev --name init --preview-feature
    

We’ll skip ahead the installation process and look at our setup code in `index.ts`:

    import { PrismaClient } from '@prisma/client'
    
    const prisma = new PrismaClient()
    
    async function main() {
      const allUsers = await prisma.user.findMany()
      console.log(allUsers)
    }
    
    main()
      .catch(e => {
        throw e
      })
      .finally(async () => {
        await prisma.$disconnect()
      })
    

Below is a sample demonstrating how to persist data and query records:

    async function main() {
      await prisma.user.create({
        data: {
          name: 'Alice',
          email: 'alice@prisma.io',
          posts: {
            create: { title: 'Hello World' },
          },
          profile: {
            create: { bio: 'I like turtles' },
          },
        },
      })
    
      const allUsers = await prisma.user.findMany({
        include: {
          posts: true,
          profile: true,
        },
      })
      console.dir(allUsers, { depth: null })
    }
    

When you run the above code, the results will be returned as JavaScript objects like this:

    [
      {
        email: 'alice@prisma.io',
        id: 1,
        name: 'Alice',
        posts: [
          {
            content: null,
            createdAt: 2020-03-21T16:45:01.246Z,
            id: 1,
            published: false,
            title: 'Hello World',
            authorId: 1,
          }
        ],
        profile: {
          bio: 'I like turtles',
          id: 1,
          userId: 1,
        }
      }
    ]
    

Prisma’s documentation looks pretty, and it appears to have a lot of content. Unfortunately, I’ve found it difficult finding the information you need. Either it’s due to an over-complicated navigation system, or that specific content is missing. Information is spread over multiple sections, including:

*   concepts
*   guides
*   reference
*   support/help articles

Prisma is a newer library that follows a different philosophy on data layer building. It also appears to be growing faster than MikroORM, especially since it was launched a year later.

Conclusion
----------

As we conclude, I’d like to briefly discuss the case against using ORM libraries in your project. The main arguments include:

*   bulky, inefficient queries
*   frustrations using a library
*   migration issues: keeping entity classes and the database scheme in sync
*   loss of type safety when using the raw SQL option

You can read all the arguments against using ORM libraries [here](https://blog.logrocket.com/why-you-should-avoid-orms-with-examples-in-node-js-e0baab73fa5) and [here](https://hackernoon.com/migrating-from-query-builders-and-orms-in-javascript-or-typescript-gc113uh0).

Having looked at all current JavaScript and TypeScript ORM libraries, you should be aware that each one differs in its implementation. Most of the arguments against ORM libraries have been resolved by the newer ones, such as Object.js and Prisma. If you decide not to use an ORM library, you’ll have to decide the individual tools and libraries that make up your data layer stack.

The way I see it, choosing an ORM for your project is the best solution because of this one reason: **documentation**.

As developers, we’re pretty bad at documenting our own code. If we were to implement a custom solution, or implement a library that’s not well known, future maintainers would have a hard time keeping your application up to date with its business needs.

However, if you use a well-documented ORM library, it becomes much easier for them to work on your application long after you’ve left the project. This is because ORMs instill good code practices, such as architecture and patterns such as Data Mapper. And while that may introduce a learning curve, it’s better in the long run.

I hope I’ve provided useful information that can help you evaluate an ORM library for your project. If you’d like a recommendation, choose a TypeScript ORM library that’s is most suited for an enterprise-class project.

Share This Article
------------------


[](#top-go-orms--)Top Go ORMs [![Go Report Card](https://camo.githubusercontent.com/e6353334a03f1dbdb1be1e4a73756df4623888580958626840de8dc50ebab3c4/68747470733a2f2f676f7265706f7274636172642e636f6d2f62616467652f6769746875622e636f6d2f642d7473756a692f617765736f6d652d676f2d6f726d73)](https://goreportcard.com/report/github.com/d-tsuji/awesome-go-orms) [![Actions Status](https://github.com/d-tsuji/awesome-go-orms/workflows/CI/badge.svg)](https://github.com/d-tsuji/awesome-go-orms/actions)
========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

A list of popular github projects related to Go ORM(Object-Relational Mapping) (ranked by stars automatically) Please update **list.txt** (via Pull Request)

Project Name

Stars

Forks

Open Issues

Description

Last Update

[beego](https://github.com/beego/beego)

27570

5392

28

beego is an open-source, high-performance web framework for the Go programming language.

2022-01-15 15:59:01

[gorm](https://github.com/go-gorm/gorm)

26518

3007

52

The fantastic ORM library for Golang, aims to be developer friendly

2022-01-15 15:49:44

[sqlx](https://github.com/jmoiron/sqlx)

11307

876

290

general purpose extensions to golang's database/sql

2022-01-15 22:43:44

[ent](https://github.com/ent/ent)

9635

539

207

An entity framework for Go

2022-01-15 23:01:48

[xorm](https://github.com/go-xorm/xorm)

6479

796

308

Simple and Powerful ORM for Go, support mysql,postgres,tidb,sqlite3,mssql,oracle, Moved to [https://gitea.com/xorm/xorm](https://gitea.com/xorm/xorm)

2022-01-14 15:32:52

[pg](https://github.com/go-pg/pg)

4959

363

107

Golang ORM with focus on PostgreSQL features and performance

2022-01-14 23:16:16

[sqlboiler](https://github.com/volatiletech/sqlboiler)

4563

415

98

Generate a Go ORM tailored to your database schema.

2022-01-15 19:21:38

[gorp](https://github.com/go-gorp/gorp)

3546

377

136

Go Relational Persistence - an ORM-ish library for Go

2022-01-13 16:51:46

[db](https://github.com/upper/db)

2872

203

129

Data access layer for PostgreSQL, CockroachDB, MySQL, SQLite and MongoDB with ORM-like features.

2022-01-15 10:22:14

[gormt](https://github.com/xxjwxc/gormt)

1638

269

39

database to golang struct

2022-01-15 06:33:43

[reform](https://github.com/go-reform/reform)

1218

56

72

A better ORM for Go, based on non-empty interfaces and code generation.

2022-01-13 12:14:04

[pop](https://github.com/gobuffalo/pop)

1158

224

123

A Tasty Treat For All Your Database Needs

2022-01-12 23:26:41

[prisma-client-go](https://github.com/prisma/prisma-client-go)

1101

53

90

Prisma Client Go is an auto-generated and fully type-safe database client

2022-01-14 18:23:01

[go-sqlbuilder](https://github.com/huandu/go-sqlbuilder)

690

64

1

A flexible and powerful SQL string builder library plus a zero-config ORM.

2022-01-15 10:20:50

[go-queryset](https://github.com/jirfag/go-queryset)

646

62

18

100% type-safe ORM for Go (Golang) with code generation and MySQL, PostgreSQL, Sqlite3, SQL Server support. GORM under the hood.

2022-01-11 09:33:24

[jet](https://github.com/go-jet/jet)

598

42

14

Type safe SQL builder with code generation and automatic query result data mapping

2022-01-15 08:53:23

[qbs](https://github.com/coocood/qbs)

548

103

10

QBS stands for Query By Struct. A Go ORM.

2021-09-18 08:26:02

[rel](https://github.com/go-rel/rel)

468

44

17

💎 Modern ORM for Golang - Testable, Extendable and Crafted Into a Clean and Elegant API

2022-01-15 07:42:07

[zoom](https://github.com/albrow/zoom)

284

25

2

A blazing-fast datastore and querying engine for Go built on Redis.

2022-01-11 19:28:53

[grimoire](https://github.com/Fs02/grimoire)

156

16

0

Database access layer for golang

2021-11-30 19:23:23

[go-store](https://github.com/gosuri/go-store)

106

8

1

A simple and fast Redis backed key-value store library for Go

2021-12-13 20:34:50

[GoBatis](https://github.com/runner-mei/GoBatis)

106

17

2

An easy ORM tool for Golang, support MyBatis-Like XML template SQL

2022-01-09 05:13:48

[marlow](https://github.com/dadleyy/marlow)

82

7

2

golang generator for type-safe sql api constructs

2021-09-29 00:13:39

[go-firestorm](https://github.com/jschoedt/go-firestorm)

26

7

0

Simple Go ORM for Google/Firebase Cloud Firestore

2021-12-13 23:52:09

[lore](https://github.com/abrahambotros/lore)

10

2

0

Light Object-Relational Environment (LORE) provides a simple and lightweight pseudo-ORM/pseudo-struct-mapping environment for Go

2021-10-12 08:51:16

_Last Automatic Update: 2022-01-16T01:01:10Z_