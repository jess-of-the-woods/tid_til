[deployment](deployment.md)

### heroku

Keep your git origin master & heroku & local copy in sync

Can have a separate 'staging' branch on heroku for testing

Sort out deployment rhythm early.

Use PostgreSQL on heroku production.

Heroku doesn't like nodemon. Use `node server.js` instead in start script. Can have `"start-dev": "nodemon server.js"` in package.json.

Add bundle.js to .gitignore and add: `"postinstall": "npm run build"` to package.json. Heroku should run this and build client side bundle after deployment.

Make sure modules needed to run are in Dependencies in package.json (not DevDependencies), including any modules needed for building (browserify etc.)

---

### heroku CLI ([toolbelt](https://toolbelt.heroku.com/))

`heroku login`: login to heroku

`heroku create`: create a new app (with randomly generated name), optionally: `heroku create appName`

`heroku git:remote --app tandem-nz`: add remote to existing repo

#### pushing
`git push heroku master`

`git push heroku master:master`

`git push heroku branchName:branchName`: push branch to heroku branch

#### Other
`heroku open`: open app in browser

`heroku run bash`: access BASH on remote server (type `exit` to exit)

`heroku releases`: shows all deployments

`heroku rollback v19`: rollback to version 19 deployed

`heroku restart`: restart crashed app.

### logs
`heroku logs`: shows any error messages from deployment

`heroku logs --tail`: watch logs


### database / postgreSQL
provision free version of PostgreSQL on heroku (through website)

`connection: process.env.DATABASE_URL`

`heroku pg:psql`: connect to remote postgres terminal (run outside of heroku bash)

`heroku pg:reset DATABASE`: drop and recreate your database

`heroku run knex migrate:latest`

`createdb stuff`

`psql stuff`

`dropdb stuff`

### port number
```javascript
var port = process.env.PORT || 3000;

app.listen(port, function () {
  console.log('listening on port' + port)
});
```

see also [postgreSQL](../databases/postgreSQL.md)
