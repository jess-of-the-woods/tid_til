[notes](notes.md) | [backend](backend.md) | [server-side](server-side.md)

## databases
- **[Knex](javascript/knex.md)**
- **[SQL](SQL.md)**
* [PostgreSQL](#postgresql)
* [NoSQL](#nosql)
* [Database in an App](#database in an app)
* [Database testing](#database testing)

## Persistence
- Data persists after program execution.. long term storage. On a hard drive somewhere
- File System vs Memory

## Databases vs a File
- Access large quantity of data quickly, easily & efficiently ( refill pad vs file cabinet )
- Simultaneous multi-user access, multiple requests ( collisions, race conditions )
- Structured Data vs unstructured ( e.g. spreadsheet vs text file )
- Permissions

---

### PostgreSQL
- handles multi-threading
- Needs to be installed and configured correctly
- `npm i pg --save`
- i knexfile.js client: pg, database: twitter_clone_dev
- `psql` ( enters pg repl ) `psql database name`
- set up pg so you don't need a username & password

`createdb databaseName`: creates new database

`dropdb databaseName`: drops database

`knex migrate:latest --env test`: migrates test database (test is referenced from config file, knexfile.js)

#### PostgreSQL interactive terminal
- `psql` - enters interactive terminal
- `psql databaseName` - enters terminal w/ a particular database
- `\?` - lists all available commands
- `\l` - lists all databases
- `\d` - describe (lists all tables)
- `\d tableName` - describe tableName (schema)
- `\q` - exit
- `SELECT * FROM tableName;`

SQL queries end with  `;`

---

## NoSQL
- approach to building databases
- described as non-relational (as opposed to SQL which is relational)
- good for rapid expansion of database (millions of records)

---

## Database testing
different connections to different databases.. in testing file and in server.js
one for testing. one for development

knex is outside of config file.. we pass knex to app and then get back a app object with a particular database

---

### 15 April 2016 - Database in an App
`git init`:  Initialises new git repository in project.

`npm init`: Initialises folder as a node project.

`npm i -g express-generator`: Installs express-generator globally

`express /path/to/folder` or just type `express` / ( `express .` ? )

`npm install`: Installs dependencies

if you accidentally 'git add' node modules.. `git rm  -r --cached node_modules/`

`touch .gitignore` then add node_modules to gitignore file.

`npm i knex --save`: knex module needed in package.json even if installed globally.

`npm i knex -g`: Installs knex, makes it available to use as a command in terminal.

`knex init`: Creates knex config file. look at knexfile.js (should point to a file)

`npm i sqlite3 --save`

---

([ontology](https://en.wikipedia.org/wiki/Ontology_(information_science)) - wikipedia

See Also [data visualisation](dataVisualisation.md) | [node](javascript/node.md) | ontology | info science
