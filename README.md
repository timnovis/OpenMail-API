# OpenMail API

## Get Started

### Prerequisites

* Have MySQL running locally
* Have Redis running locally `brew install redis` and `brew services start redis`
* Node.js 8.6.0 or later
* npm or yarn

### Get the project running

1. Replace `.env.example` with `.env` with your db config settings
2. Replace `src/config/local.js` with your database settings (don't commit your changes to this file)
3. Run `yarn` or `npm install`
4. Run `npm run migrate:latest` to set up the database schema
5. Run `yarn dev` to start the dev server

## TODO

* Allow subscribers to be members of multiple lists
* ~~Set up the AWS SDK and implement sending batch emails (the core feature of this whole project, which I haven't done yet)~~
* Allow users to schedule emails
* Update and delete users endpoints
* Update and delete individual subscribers endpoints
* Update list name endpoint
* Campaign reporting stats
* ~~Import subscibers CSV to list~~
* Export subscribers CSV from list
* User defined list columns in addition to the default firstName and lastName
* Public endpoint to add a subscriber to a list, e.g. for an API integration/signup form
* Request payload validation, maybe with something like this https://github.com/ctavan/express-validator


## Knex seeds and migrations
### Seeds
#### Create
```
npm run seed the_name_of_seed

# By default this runs on development, but can be overwritten:
npm run seed the_name_of_seed NODE_ENV=development

# Alternatively, for test seeds (the most common):
npm run seed:test the_name_of_seed
```

#### Run
```
# Environment rules apply as above:
npm run seed:run
```

### Migrations
#### Create
```
npm run migrate the_name_of_migration
```

#### Run
```
npm run migrate:latest
```

#### Rollback
```
npm run migrate:rollback
```
