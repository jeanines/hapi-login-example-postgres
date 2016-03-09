# hapi-login-example-postgres-postgres
A login form using hapi-auth-register, hapi-auth-login &amp; hapi-auth-jwt2 with a PostgreSQL DB

[![Build Status](https://travis-ci.org/dwyl/hapi-login-example-postgres-postgres.svg?branch=master)](https://travis-ci.org/dwyl/hapi-login-example-postgres-postgres)
[![codecov.io](http://codecov.io/github/dwyl/hapi-login-example-postgres/coverage.svg?branch=master)](http://codecov.io/github/dwyl/hapi-login-example-postgres?branch=master)
[![Code Climate](https://codeclimate.com/github/dwyl/hapi-login-example-postgres/badges/gpa.svg)](https://codeclimate.com/github/dwyl/hapi-login-example-postgres)
[![Dependency Status](https://david-dm.org/dwyl/hapi-login-example-postgres.svg)](https://david-dm.org/dwyl/hapi-login-example-postgres)
[![devDependency Status](https://david-dm.org/dwyl/hapi-login-example-postgres/dev-status.svg)](https://david-dm.org/dwyl/hapi-login-example-postgres#info=devDependencies)
[![HitCount](https://hitt.herokuapp.com/dwyl/hapi-login-example-postgres.svg)](https://github.com/dwyl/hapi-login-example-postgres)

## Why?

> "*For the things we have to learn before we can do them, we learn by doing them.*" ~ [Aristotle](https://www.goodreads.com/quotes/tag/learning-by-doing)

We did not *find* an ***end-to-end*** solution/tutorial
for ***login*** (*using email & password*) in Hapi.js apps,
so we *wrote* it.

If ***anything*** is ***unclear*** in this (*or any of our other repos*),
***please tell us***:
[![Join the chat at https://gitter.im/dwyl/chat](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/dwyl/chat/)  



## What?

This repo is a *showcase* for how to use the
[**hapi-login**](https://github.com/nelsonic/hapi-login) plugin
for a *simple* (*yet complete*) web/app login process.


## Try it: https://hapi-login.herokuapp.com/

![login form](https://cloud.githubusercontent.com/assets/194400/10523082/6e7fab3c-7370-11e5-91e2-639fc725b3e6.png)

## How?

The best way to get started is to run this example *locally*.

#### 1. Clone the repo:

```sh
git clone git@github.com:dwyl/hapi-login-example-postgres.git
cd hapi-login-example-postgres
```
#### 2. Install *Dependencies* from NPM

```sh
npm install
```

#### 3. Ensure you have the Required Environment Variables

create an `config.env` file in your `hapi-login-example-postgres` directory.
add a line for your `DATABASE_URL` variable:
e.g:
```sh
export DATABASE_URL=postgres:password//postgres:@localhost/test
```
> default on mac is: export DATABASE_URL=postgres://postgres:@localhost/test  
> if you don't *already* have a database called `test` on your system,  
> create it now by running this command in your psql/pgadmin: `CREATE DATABASE test;`

#### 4. Run the Tests

```sh
npm test
```

#### 5. Run the Server

```sh
npm start
```

That's it.  
Now, ~~hack~~ *customise* it to your heart's content!

When you visit http://localhost:8000/ you will see a login form, you can login with any valid email address:
![hapi-login-01](https://cloud.githubusercontent.com/assets/194400/10522464/312648ca-736d-11e5-9f9f-36e39755b186.png)

Make sure the email address is valid:
![hapi-login-03](https://cloud.githubusercontent.com/assets/194400/10522488/47a24568-736d-11e5-8f3b-47a08699b09a.png)

Your password needs to be more than 6 characters long:
![hapi-login-05](https://cloud.githubusercontent.com/assets/194400/10522520/78b44052-736d-11e5-919f-903270075795.png)

We also use https://github.com/chriso/validator.js
to mitigate [Cross Site Scripting](https://en.wikipedia.org/wiki/Cross-site_scripting)
vulnerability:

Avoids Cross Site Scripting:
![hapi login avoids XSS](https://cloud.githubusercontent.com/assets/194400/10522594/db57b45a-736d-11e5-969a-844d186db80b.png)


## Want *More*?

If you would like to see this example *expanded*,
please either [***create an issue***](https://github.com/dwyl/hapi-login-example-postgres/issues)
with a *specific request* or [![Join the chat at https://gitter.im/dwyl/chat](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/dwyl/chat/)
