[notes](notes.md) | [backend](backend.md)

## Deployment (Heroku)

Keep your git origin master & heroku & local copy in sync

Can have a separate 'staging' branch on heroku for testing

Sort out deployment rhythm early

Use PostgreSQL on heroku production

Heroku doesn't like nodemon. Use `node server.js` instead in start script. Can have `"start-dev": "nodemon server.js"` in package.json.

Add bundle.js to .gitignore and add: `"postinstall": "npm run build"` to package.json. Heroku should run this and build client side bundle after deployment.

Make sure modules needed to run are in Dependencies in package.json (not DevDependencies), including any modules needed for building (browserify etc.)

---

### Heroku CLI ([toolbelt](https://toolbelt.heroku.com/))

`heroku login`: Login to Heroku

`heroku create`: Create a new app (with randomly generated name), optionally: `heroku create appName`

`heroku git:remote --app tandem-nz`: Add remote to existing repo

`git push heroku master`

`heroku run bash`: Access BASH on remote server (type `exit` to exit)

`heroku releases`: shows all deployments

`heroku rollback v19`: rollback to version 19 deployed

`git push heroku master:master`

`git push heroku branchName:branchName`: Push branch to heroku branch

`heroku open`

`heroku restart`: Restart crashed app.

### Logs
`heroku logs`: Shows any error messages from deployment

`heroku logs --tail`: Watch logs


### Database / PostgreSQL
provision free version of PostgreSQL on Heroku (through website)

`connection: process.env.DATABASE_URL`

`heroku pg:psql`: Connect to remote postgres terminal (run outside of heroku bash)

`heroku pg:reset DATABASE`: Drop and recreate your database

`heroku run knex migrate:latest`

`createdb stuff`

`psql stuff`

`dropdb stuff`

### Port number
```javascript
var port = process.env.PORT || 3000;

app.listen(port, function () {
  console.log('listening on port' + port)
});
```

### Deployment Platforms
- Heroku
- AWS (Amazon Web Services)
- Digital Ocean
- Github pages?

---

See also [databases](databases.md)


### Links

- [Meow-Heroku](https://github.com/hihi-2016/meow-heroku) - instructions (EDA Repo)
- [Node.js support](https://devcenter.heroku.com/articles/nodejs-support) - inc. specifying node version number.
