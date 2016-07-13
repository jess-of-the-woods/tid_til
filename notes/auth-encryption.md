[notes](notes.md) | [backend](backend.md) | [server-side](server-side.md)

## Authentication/Login/Encryption

18 April 2016

In express, `app.use` allows you to use middleware.. i.e. hbs, body-parser, express-sessions etc. You can also write your own middleware.

### Authentication
- Sessions
- Cookies
- Authentication
- Passwords


- Servers have amnesia, authentication is a way to solve that problem by using sessions
- Uses cookie. text file that sits on your client. has session id & has expiry date
- core part of session technology.
- Server has a sessions data store.. unique id with empty object
- can use `req.session` and pass in data in express
- never trust data in cookies.. user can edit cookies. set expiry date etc in server data store..
- When using HTTP, its possible to steal cookies & impersonate others


### Encryption

#### Symmetric
key works for locking & unlocking

Algorithm which is cheap to use..

#### Asymmetric
- public & private keys
- SSH
- HTTPS

**Bob**
- private: spaghetti
- public: ravioli

**Alice**
- private: bananas
- public: apples


### Hashing
- Protects server databases from break in.., being hacked.
- transforms text ( to cyphertext ) by applying  algorithm, one-way process ( 1 way function )
- hard to predict
- bcrypt ( blowfish is publicly available hashing algorithm )
- hashes kinda work like maps, deterministic.. same input & algorithm will always return same output/hash
- on each login, hash is applied

### Review

**encryption**
- symmetric/asymmetric,
- HTTPS, ( salt )

**authentication**
- sessions
  - `req.session.theme`/ `req.session.userId`


- cookie


### OAuth ( Omni Auth )
-3rd party auth, sign in with 3rd party ( facebook/ google/ twitter/ github.. )

#### User stories
- As an authenticated user:
- I can: edit my own profile details
- so that: I can keep them up to date

#### Social Login
- need user table in database
- User Flow
- Login Flow

will there be routes which don't require authentication? think about the flow between those routes

1. users table
2. `<a>` link in hbs to auth/github route ( defined in server file )
3. instantiate github strategy
4. setup passport & database interface


checkout password maker (chrome)

See also [express.js](javascript/express.md)
