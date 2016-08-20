[notes](notes.md) | [security](security.md) | [backend](backend.md) | [server-side](server-side.md)

## Authentication/Login/Encryption

### Authentication
- Sessions
- Cookies
- Passwords

### Sessions
- Servers have amnesia, authentication is a way to solve that problem by using sessions
- Uses cookie. text file that sits on your client. has session id & has expiry date
- core part of session technology.
- Server has a sessions data store.. unique id with empty object
- can use `req.session` and pass in data in express
- never trust data in cookies.. user can edit cookies. set expiry date etc in server data store..
- When using HTTP, its possible to steal cookies & impersonate others
- `req.session.theme`/ `req.session.userId`

#### User stories
As an authenticated user,
- I can: edit my own profile details
- so that: I can keep them up to date

#### Social Login
- need user table in database
- User Flow
- Login Flow

Will there be server routes which don't require authentication? Think about the flow between those routes.

### OAuth/OAuth2 ( Omni Auth )
Third party authentication, sign in with 3rd party ( facebook/ google / twitter / github etc. )

1. users table
2. `<a>` link in hbs to auth/github route ( defined in server file )
3. instantiate github strategy
4. setup passport & database interface




See also [express.js](javascript/express.md)
