#Databases:

* [SQL](#sql)
* [PostgreSQL](#postgresql)
* [NoSQL](#nosql)
* [Knex](#knex)
* [Database in an App](#database in an app)
* [Database testing](#database testing)

##Persistence:
- Data persists after program execution.. long term storage. On a hard drive somewhere
- File System vs Memory

##Databases vs a File
- Access large quantity of data quickly, easily & efficiently ( refill pad vs file cabinet )
- Simultaneous multi-user access, multiple requests ( collisions, race conditions )
- Structured Data vs unstructured ( e.g. spreadsheet vs text file )
- Permissions

__________________

####SQL:

statement always end in `;`

```sql
CREATE TABLE table_name (
    column_1 data_type,
    column_2 data_type,
    column_3 data_type
  );

INSERT INTO celebs (id, name, age) VALUES (4, 'Taylor Swift', 26);
SELECT name FROM celebs;

UPDATE celebs
SET age = 22
WHERE id = 1;
```
####SQL Joins & relationships:

relationships between data, modelling data

#####People table:
 id, email, password (id is primary key)

#####Shoes table:
 size, color, owner_id (foreign id)

one to many relationship. one person, many shoes

`LEFT INNER JOIN` (most commonly used join)

```sql
SELECT * FROM shoes INNER JOIN people ON people.id = shoes.owner_id
```

####Many to many relationship:
- Shoe-sharing household
- Many people wear the shoes, the shoes are worn by many
- wear event table in middle.. ( join tables )

twitter project.. one person can follow many people, a person can be followed by many people.

[tutorialspoint](http://www.tutorialspoint.com/sql/)

```sql
SELECT * FROM MassiveTable
LIMIT 10 ( return 10 items )
OFFSET 20 ( start at 20th )
```
______________

##PostgreSQL :
- handles multi-threading
- Needs to be installed and configured correctly
- `npm i pg --save`
- i knexfile.js client: pg, database: twitter_clone_dev
- `psql` ( enters pg repl ) `psql database name`
- set up pg so you don't need a username & password

`createdb databaseName`
`dropdb databaseName`
`psql databaseName`

`knex migrate:latest --env test` => migrates test db ( test is referenced from config file, knexfile.js )

`psql databaseName` - enters interactive terminal

####PostgreSQL interactive terminal:
`\l` lists all databases
`\d` ( describe ( lists all tables )
`\d`  tableName
`\q` to exit
`SELECT * FROM tableName;`
sql queries end with  `;`

___________________

####NoSQL:
- approach to building DB's
- described as non-relational (as opposed to SQL which is relational)
- good for rapid expansion of db (millions of records)

__________________

###Knex:
- lets us access data from within programs
- knex translates javascript into SQL
- knexfile.js ( config details, says which file to use ), so that knex command in CLI knows where to look for config info.

####Migrations:
- `knex migrate:make CreateCarsTable` - throws up error that we need to install sqlite3 (if  not installed)
creates new migration file in new folder with timestamp as part of filename
- open new migration file, look at knexjs documentation, create table, add stuff to exports.up & exports.down
- `knex migrate:latest`
- name migrations well so they describe what they do.
- migrate current data from DB to a new ..form, changes structure of db, schema are instructions on how to migrate to new state ( add fields, remove fields )
- migration up is forward, migration down is back ( rollback migration )
- install knex globally = `npm i -g knex`

varchar = variable character. basically a string. any character up to max 255 long

#####Seeds
seed data is test data, good for testing environment, or development
- `knex seed:make seedName` - creates new seed file..
- add data to seed file
- `knex seed:run` - runs seed file, inserts seed data into tables

####Knex vs Knex.raw..
#####Knex syntax :

```sql
  knex.select()
  .table('cats')
```

#####Raw SQL syntax:
```sql
  var allTheCats = 'SELECT * FROM cats'
```
can use either way.. Knex or raw. When queries get really big, raw becomes a bit unwieldy & ugly

`DROP` means delete/destroy. E.g. `drop table` etc

____

####Database testing :

different connections to different databases.. in testing file and in server.js
one for testing. one for development

knex is outside of config file.. we pass knex to app and then get back a app object w/ a particular database

---

###15 April 2016 - Database in an app

`git init`

`npm init`

`npm i -g express-generator` (install globally)

`express /path/to/folder` or just type `express`
`npm install` ( installs dependencies )

if git add all node modules.. `git rm  -r --cached node_modules/`
`touch .gitignore`, add node_modules

`npm i knex --save` - needed in package.json even if installed globally

`npm i knex -g` - makes it available to use as a command

`knex init`
look at knexfile.js (should point to a file)
`npm i sqlite3 --save`
