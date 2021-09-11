# What kind of data is a good fit for an SQL database?

For complex queries: SQL databases are good fit for the complex query intensive environment

# Give a real world example.?

## 1. MySQL Community Edition

`MySQL database` is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js. The following are some of MySQL benefits and strengths:

- Replication: By replicating MySQL database across multiple nodes the work load can be reduced heavily increasing the scalability and availability of business application
- Sharding: MySQL sharding os useful when there is large no of write operations in a high traffic website. By sharding MySQL servers, the application is partitioned into multiple servers dividing the database into small chunks. As low cost servers can be deployed for this purpose, this is cost effective.
- Memcached as a NoSQL API to MySQL: Memcached can be used to increase the performance of the data retrieval operations giving an advantage of NoSQL api to MySQL server.
- Maturity: This database has been around for a long time and tremendous community input and testing has gone into this database making it very stable.
- Wide range of Platforms and Languages: MySql is available for all major platforms like Linux, Windows, Mac, BSD and Solaris. It also has connectors to languages like Node.js, Ruby, C#, C++, C, Java, Perl, PHP and Python.
- Cost effectiveness: It is open source and free.

## 2. MS-SQL Server Express Edition

It is a powerful and user friendly database which has good stability, reliability and scalability with support from Microsoft. The following are some of MS-SQL benefits and strengths:

- Integrated Development Environment: Microsoft visual studio, Sql Server Management Studio and Visual Developer tools provide a very helpful way for development and increase the developers productivity.
- Disaster Recovery: It has good disaster recovery mechanism including database mirroring, fail over clustering and RAID partitioning.
- Cloud back-up: Microsoft also provides cloud storage when you perform a cloud-backup of your database

## 3. Oracle Express Edition

It is a limited edition of Oracle Enterprise Edition server with certain limitations. This database is free for development and deployment. The following are some of Oracle benefits and strengths:

- Easy to Upgrade: Can be easily upgraded to newer version, or to an enterprise edition.

- Wide platform support: It supports a wide range of platforms including Linux and Windows

- Scalability: Although the scalability of this database is not cost effective as MySQL server, but the solution is very reliable, secure, easily manageable and productive.

# What kind of data is a good fit a NoSQL database?

NoSQL databases are not good fit for complex queries. On a high-level, NoSQL don’t have standard interfaces to perform complex queries, and the queries themselves in NoSQL are not as powerful as SQL query language.

# Give a real world example.

## 1. MongoDB

`Mongodb` is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema. It has been developed by the founders of DoubleClick, written in C++ and is currently being used by some big companies like The New York Times, Craigslist, MTV Networks. The following are some of MongoDB benefits and strengths:

- Speed: For simple queries, it gives good performance, as all the related data are in single document which eliminates the join operations.
- Scalability: It is horizontally scalable i.e. you can reduce the workload by increasing the number of servers in your resource pool instead of relying on a stand alone resource.
- Manageable: It is easy to use for both developers and administrators. This also gives the ability to shard database
- Dynamic Schema: Its gives you the flexibility to evolve your data schema without modifying the existing data

## 2. CouchDB

`CouchDB` is also a document based NoSQL database. It stores data in form of JSON documents. The following are some of CouchDB benefits and strengths:

- Schema-less: As a member of NoSQL family, it also have dynamic schema which makes it more flexible, having a form of JSON documents for storing data.
- HTTP query: You can access your database documents using your web browser.
- Conflict Resolution: It has automatic conflict detection which is useful while in a distributed database.
- Easy Replication: Implementing replication is fairly straight forward

## 3. Redis

`Redis` is another Open Source NoSQL database which is mainly used because of its lightening speed. It is written in ANSI C language. The following are some of Redis benefits and strengths:

- Data structures: Redis provides efficient data structures to an extend that it is sometimes called as data structure server. The keys stored in database can be - hashes, lists, strings, sorted or unsorted sets.
  Redis as Cache: You can use Redis as a cache by implementing keys with limited time to live to improve the performance.
- Very fast: It is consider as one of the fastest NoSQL server as it works with the in-memory dataset.

# Which type of database is best for hierarchical data storage?

For the type of data to be stored: SQL databases are not best fit for hierarchical data storage. But, NoSQL database fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.

# Which type of database is best for scalability?

For scalability: In most typical situations, SQL databases are vertically scalable. You can manage increasing load by increasing the CPU, RAM, SSD, etc, on a single server. On the other hand, NoSQL databases are horizontally scalable. You can just add few more servers easily in your NoSQL database infrastructure to handle the large traffic.
![](https://cdn-cgiac.nitrocdn.com/wPseOUIDKwfwoBwNunqSiZZPVVauXeiJ/assets/static/optimized/rev-a6ed3a0/wp-content/uploads/2021/04/encyclopedia-%D9%85%D8%A7-%D9%87%D9%8A-%D9%84%D8%BA%D8%A9-%D8%A5%D8%B3-%D9%83%D9%8A%D9%88-%D8%A5%D9%84-SQL.jpg)

# What does SQL stand for?

`SQL` (pronounced "ess-que-el") stands for Structured Query Language. SQL is used to communicate with a database. According to ANSI (American National Standards Institute), it is the standard language for relational database management systems.

# What is a realational database?

A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables. In a relational database, each row in the table is a record with a unique ID called the key. The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish the relationships among data points.

# What type of structure does a relational database work with?

The relational model means that the logical data structures—the data tables, views, and indexes—are separate from the physical storage structures. This separation means that database administrators can manage physical data storage without affecting access to that data as a logical structure.

# What is a ‘schema’?

A SQL database contains multiple objects such as tables, views, stored procedures, functions, indexes, triggers. We define SQL Schema as a logical collection of database objects. A user owns that owns the schema is known as schema owner. It is a useful mechanism to segregate database objects for different applications, access rights, managing the security administration of databases. We do not have any restrictions on the number of objects in a schema.

# What is a NoSQL database?

When people use the term “NoSQL database”, they typically use it to refer to any non-relational database. Some say the term “NoSQL” stands for “non SQL” while others say it stands for “not only SQL.” Either way, most agree that NoSQL databases are databases that store data in a format other than relational tables.

A common misconception is that NoSQL databases or non-relational databases don’t store relationship data well. NoSQL databases can store relationship data—they just store it differently than relational databases do. In fact, when compared with SQL databases, many find modeling relationship data in NoSQL databases to be easier than in SQL databases, because related data doesn’t have to be split between tables.

NoSQL data models allow related data to be nested within a single data structure.

# Howo does it work?

NoSQL databases emerged in the late 2000s as the cost of storage dramatically decreased. Gone were the days of needing to create a complex, difficult-to-manage data model simply for the purposes of reducing data duplication. Developers (rather than storage) were becoming the primary cost of software development, so NoSQL databases optimized for developer productivity.
As storage costs rapidly decreased, the amount of data applications needed to store and query increased. This data came in all shapes and sizes—structured, semistructured, and polymorphic—and defining the schema in advance became nearly impossible. NoSQL databases allow developers to store huge amounts of unstructured data, giving them a lot of flexibility.

Additionally, the Agile Manifesto was rising in popularity, and software engineers were rethinking the way they developed software. They were recognizing the need to rapidly adapt to changing requirements. They needed the ability to iterate quickly and make changes throughout their software stack—all the way down to the database model. NoSQL databases gave them this flexibility.

Cloud computing also rose in popularity, and developers began using public clouds to host their applications and data. They wanted the ability to distribute data across multiple servers and regions to make their applications resilient, to scale-out instead of scale-up, and to intelligent geo-place their data. Some NoSQL databases like MongoDB provided these capabilities.

# What is inside of a Mongo database?

MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.

# Which is more flexible - SQL or MongoDB? and why.

Data in MongoDB has a flexible schema. Collections do not enforce document structure by default. This flexibility gives you data-modeling choices to match your application and its performance requirements. ... MongoDB provides the capability for schema validation during updates and insertions.
MongoDB is almost 100 times faster than traditional database system like RDBMS, which is slower in comparison with the NoSQL databases. ... MongoDB supports deep query-ability i.e we can perform dynamic queries on documents using the document-based query language that's nearly as powerful as SQL

# What is the disadvantage of a NoSQL database?

- NoSQL databases don’t have the reliability functions which Relational Databases have (basically don’t support ACID).
- This also means that NoSQL databases offer consistency in performance and scalability.
- In order to support ACID developers will have to implement their own code, making their systems more complex.
- This may reduce the number of safe applications that commit transactions, for example bank systems.
- NoSQL is not compatible (at all) with SQL.
  - Note: Some NoSQL management systems do use a Structured Query Language.
  - his means that you will need a manual query language, making things slower and more complex.

* NoSQL are very new compared to Relational Databases, which means that are far less stable and may have a lot less functionalities.
![](https://blog.couchbase.com/wp-content/uploads/2017/04/nosql-vs-sql-overview-1.png)