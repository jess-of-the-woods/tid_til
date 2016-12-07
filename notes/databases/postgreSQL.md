[databases](index.md) | [SQL](SQL.md)

## PostgreSQL
- handles multi-threading
- Needs to be installed and configured correctly
- `npm i pg --save`
- i knexfile.js client: pg, database: twitter_clone_dev
- `psql` ( enters pg repl ) `psql database name`
- set up pg so you don't need a username & password

`createdb databaseName`: creates new database

`dropdb databaseName`: drops database

`knex migrate:latest --env test`: migrates test database (test is referenced from config file, knexfile.js)

### PostgreSQL interactive terminal
- `psql` - enters interactive terminal
- `psql databaseName` - enters terminal w/ a particular database
- `\?` - lists all available commands
- `\l` - lists all databases
- `\d` - describe (lists all tables)
- `\d tableName` - describe tableName (schema)
- `\q` - exit
- `SELECT * FROM tableName;`

SQL queries end with  `;`

see also [heroku](../devOps/heroku.md)
