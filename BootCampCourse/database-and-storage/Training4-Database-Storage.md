# Training: 4 Database and Storage

This time the simple concept of Relation-database (sqlite) and Document-database (Mongodb) are introduce and practised in Python environment.

## 1 SQLite

there are some great sources to learn:

- [CN-Python-SQLite](http://www.cnblogs.com/yuxc/archive/2011/08/18/2143606.html)
- [CN 2](http://www.cnblogs.com/hongten/p/hongten_python_sqlite3.html)
- [EN-Step by Step](http://www.blog.pythonlibrary.org/2012/07/18/python-a-simple-step-by-step-sqlite-tutorial/)

facts about sqlite:

- it stores database in a file or memory.
- it use 'SQL' language to describe data model.
- it stores many tables, each table has its scheme, which defines the column and each record is a row like a EXCEL table.
- it has simples dependency and least concerns, but not suitable for very large data.

## 2 SQL

SQL sources:

- [W3School: SQL cn](http://www.w3school.com.cn/sql/sql_intro.asp)
- [SQL course cn](http://www.1keydata.com/cn/sql/)
- [SQL course en](http://www.sqlcourse.com/intro.html)
- [W3School: SQL en](https://www.w3schools.com/sql/)

you at lease should know:

- create table
- insert data
- query condition: Where, And Or Not..
- update data
- delete data
- Min/Max, Count, Avg, Sum
- Wildcards

## 3 MongoDB

MongoDB is a document, scheme free database, support JSON direct save. it can store flexible and not limited to table like datas. sources:

- [concept db/collection](https://docs.mongodb.com/manual/core/databases-and-collections/)
- [concept db/documents](https://docs.mongodb.com/manual/core/document/)
- [Official Python](https://docs.mongodb.com/getting-started/python/)
- [Official Pymongo client](https://docs.mongodb.com/getting-started/python/client/)
- [CN python+mongodb](http://www.oschina.net/question/54100_27233)
- [CN mongodb for blog](https://serholiu.com/python-mongodb)

you should know:

- use python's client(pymongo) connect db and dataset
- CRUD operations [official en](https://docs.mongodb.com/manual/crud/)
- Query Documents
- Query Array
- Statistic of current db/collections
- optional but recommended:[complext query](https://docs.mongodb.com/manual/tutorial/query-embedded-documents/)


## 4 Exercise

- use python, define a table, insert the data row by row
- import a EXCEL data into a SQLite database.
- export SQLite data to CSV files.
- find statistics of this database (Count, Min, Max, Avg, Sum)
- the ubuntu server has installed mongodb (see /etc/mongodb.conf), check its status
- use pymongo or alike lib to connect this db
- use mongo to store you current project's data
- find the statistics of your data collection
