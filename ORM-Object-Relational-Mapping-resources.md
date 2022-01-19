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
