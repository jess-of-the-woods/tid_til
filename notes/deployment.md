[notes](notes.md) | [backend](backend.md)

## Deployment

### options
- Heroku
- AWS ( amazon )
- Digital Ocean

`heroku git:remote --app tandem-nz` ( add remote to existing repo )

`heroku login`

`heroku create`

`heroku logs`: shows any error messages from deployment

`heroku logs --tail`

`heroku releases`: shows all deployments

`heroku rollback v19`: rollback to version 19 deployed

provision free version of postgres on heroku
`git push heroku master:master`
`git push heroku branchName:branchName` ( push branch to heroku branch )

`heroku open`

connection: process.env.DATABASE_URL

`heroku restart`

`heroku pg:psql` ( connect to remote postgres terminal ) ( run outside of heroku bash )
`heroku pg:reset DATABASE`  ( drop and recreate your database )

heroku doesn't like nodemon
use '`node server.js`' instead in start script
can do npm 'start-dev': 'nodemon server.js'

make sure modules needed to run are in Dependencies in package.json ( not DevDependencies )
```javascript
var port = process.env.PORT || 3000;

app.listen(port, function () {
  console.log('listening on port' + port)
});
```

`heroku run knex migrate:latest`


`createdb stuff`

`psql stuff`

`dropdb stuff`

__

`heroku run bash`

`git push heroku master`

keep your git origin master & heroku & local copy in sync

can have a separate 'staging' branch on heroku for testing

sort out deployment rhythm early

use postgres on heroku production


instructions: https://github.com/hihi-2016/meow-heroku
