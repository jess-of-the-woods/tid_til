[npm](npm.md) | [SQL](../SQL.md)

## Knex.js

<a href="http://knexjs.org/"><img src="http://knexjs.org/docs/images/knex.png" width="300"></a>


- Node module
- Lets us access data from within programs
- knex translates javascript into SQL
- knexfile.js ( config details, says which file to use ), so that knex command in CLI knows where to look for config info.

### Migrations
- `knex migrate:make CreateCarsTable`: Throws up error that we need to install sqlite3 (if  not installed). If sqlite3 is installed, creates new migration file in new folder with timestamp as part of filename.
- Open new migration file, look at knexjs documentation, create table, add stuff to exports.up & exports.down
- `knex migrate:latest`: Runs all migrations.
- Name migrations well so they describe what they do.
- Migrate current data from DB to a new ..form, changes structure of db, schema are instructions on how to migrate to new state (add fields, remove fields)
- Migration up is forward, migration down is back ( rollback migration )
- Install knex globally = `npm i -g knex`

varchar = variable character. basically a string. any character up to max 255 long

### Seeds
seed data is test data, good for testing environment, or development
- `knex seed:make seedName` - creates new seed file..
- add data to seed file
- `knex seed:run` - runs seed file, inserts seed data into tables

### Knex vs Knex.raw..

##### Knex syntax

```sql
  knex.select()
  .table('cats')
```

##### Raw SQL syntax
```javascript
  var allTheCats = 'SELECT * FROM cats'
```
can use either way.. Knex or raw. When queries get really big, raw becomes a bit unwieldy & ugly

`DROP` means delete/destroy. E.g. `drop table`
