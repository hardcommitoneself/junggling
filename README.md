[![NPM Version][npm-image]][npm-url]
[![NPM Downloads][downloads-image]][downloads-url]
[![Build status][build-image]][build-url]
[![Test Coverage][coveralls-image]][coveralls-url]

## About

[JugglingDB](http://1602.github.io/jugglingdb/) is cross-db ORM for nodejs, providing
**common interface** to access most popular database formats.  Currently
supported are: mysql, sqlite3, postgres, mongodb, redis and
js-memory-storage (yep, self-written engine for test-usage only). You can add
your favorite database adapter, checkout one of the existing adapters to learn
how.

Jugglingdb also works on client-side (using WebService and Memory adapters),
which allows to write rich client-side apps talking to server using JSON API.

## Installation

    npm install jugglingdb

and you should install appropriate adapter, for example for redis:

    npm install jugglingdb-redis-hq

check following list of available adapters

## JugglingDB adapters

<table>
  <thead>
    <tr>
      <th>Database type</th>
      <th>Package name</th>
      <th>Maintainer</th>
      <th>Build status / coverage</th>
    </tr>
  </thead>
  <tbody>
    <!-- ArangoDB -->
    <tr>
      <td><a href="http://www.arangodb.org/"><img width="16" height="16" src="https://www.arangodb.com/wp-content/uploads/2016/03/small-1.png" style="vertical-align:middle" alt="ArangoDB" /></a> ArangoDB</td>
      <td><a href="https://github.com/m0ppers/jugglingdb-arango">jugglingdb-arango</a></td>
      <td><a href="https://github.com/m0ppers">Andreas Streichardt</a></td>
      <td><a href="https://travis-ci.org/m0ppers/jugglingdb-arango"><img src="https://travis-ci.org/m0ppers/jugglingdb-arango.svg?branch=master" alt="Build Status" /></a></td>
    </tr>
    <!-- Firebird -->
    <tr>
      <td><a href="http://firebirdsql.org"><img src="http://firebirdsql.org/favicon.ico" alt="Firebird"/></a> Firebird</td>
      <td><a href="http://github.com/hgourvest/jugglingdb-firebird">jugglingdb-firebird</a></td>
      <td><a href="http://github.com/hgourvest">Henri Gourvest</a></td>
    </tr>
    <!-- MongoDB -->
    <tr>
      <td><a href="http://www.mongodb.org"><img width="16" height="16" src="https://www.mongodb.com/assets/images/global/favicon.ico" alt="MongoDB" /></a> MongoDB</td>
      <td><a href="https://github.com/jugglingdb/mongodb-adapter">jugglingdb-mongodb</a></td>
      <td><a href="https://github.com/1602">Anatoliy Chakkaev</a></td>
      <td><a href="https://circleci.com/gh/jugglingdb/mongodb-adapter"><img src="https://circleci.com/gh/jugglingdb/mongodb-adapter.svg?&style=shield" alt="Build Status" /></a> <a href='https://coveralls.io/github/jugglingdb/mongodb-adapter?branch=master'><img src='https://coveralls.io/repos/github/jugglingdb/mongodb-adapter/badge.svg?branch=master' alt='Coverage Status' /></a></td>
    </tr>
    <!-- MySQL -->
    <tr>
      <td><a href="http://www.mysql.com/"><img width="16" height="16" src="http://www.mysql.com/common/themes/sakila/favicon.ico" style="vertical-align:middle"" alt="MySQL" /></a> MySQL</td>
      <td><a href="https://github.com/jugglingdb/mysql-adapter">jugglingdb-mysql</a></td>
      <td><a href="https://github.com/dgsan">dgsan</a></td>
      <td><a href="https://circleci.com/gh/jugglingdb/mysql-adapter"><img src="https://circleci.com/gh/jugglingdb/mysql-adapter.svg?style=shield" alt="Build Status" /></a> <a href='https://coveralls.io/github/jugglingdb/mysql-adapter?branch=master'><img src='https://coveralls.io/repos/github/jugglingdb/mysql-adapter/badge.svg?branch=master' alt='Coverage Status' /></a></td>
    </tr>
    <!-- CouchDB / nano -->
    <tr>
      <td><a href="http://couchdb.apache.org/"><img width="16" src="http://couchdb.apache.org/favicon.ico" style="vertical-align:middle"" alt="CouchDB" /></a> CouchDB / nano</td>
      <td><a href="https://github.com/jugglingdb/nano-adapter">jugglingdb-nano</a></td>
      <td><a href="https://github.com/nrw">Nicholas Westlake</a></td>
      <td><a href="https://travis-ci.org/jugglingdb/nano-adapter"><img src="https://travis-ci.org/jugglingdb/nano-adapter.svg?branch=master" alt="Build Status" /></a></td>
    </tr>
    <!-- PostgreSQL -->
    <tr>
      <td><a href="http://www.postgresql.org/"><img src="http://www.postgresql.org/favicon.ico" style="vertical-align:middle"" alt="PostgreSQL" /></a> PostgreSQL</td>
      <td><a href="https://github.com/jugglingdb/postgres-adapter">jugglingdb-postgres</a></td>
      <td><a href="https://github.com/1602">Anatoliy Chakkaev</a></td>
      <td><a href="https://circleci.com/gh/jugglingdb/postgres-adapter"><img src="https://circleci.com/gh/jugglingdb/postgres-adapter.svg?style=shield" alt="Build Status" /></a> <a href='https://coveralls.io/github/jugglingdb/postgres-adapter?branch=master'><img src='https://coveralls.io/repos/github/jugglingdb/postgres-adapter/badge.svg?branch=master' alt='Coverage Status' /></a></td>
    </tr>
    <!-- Redis -->
    <tr>
      <td><a href="http://redis.io/"><img src="http://redis.io/images/favicon.png" alt="Redis" /></a> Redis</td>
      <td><a href="https://github.com/jugglingdb/redis-hq-adapter">jugglingdb-redis-hq</a></td>
      <td><a href="https://github.com/1602">Anatoliy Chakkaev</a></td>
      <td><a href="https://circleci.com/gh/jugglingdb/redis-hq-adapter"><img src="https://circleci.com/gh/jugglingdb/redis-hq-adapter.svg?style=shield" alt="Build Status" /></a> <a href='https://coveralls.io/github/jugglingdb/redis-hq-adapter?branch=master'><img src='https://coveralls.io/repos/github/jugglingdb/redis-hq-adapter/badge.svg?branch=master' alt='Coverage Status' /></a></td>
    </tr>
    <!-- RethinkDB -->
    <tr>
      <td><a href="http://www.rethinkdb.com/"><img src="http://www.rethinkdb.com/favicon.ico" alt="RethinkDB" width="16" height="16" /></a> RethinkDB</td>
      <td><a href="https://github.com/fuwaneko/jugglingdb-rethink">jugglingdb-rethink</a></td>
      <td><a href="https://github.com/fuwaneko">Tewi Inaba</a></td>
      <td><a href="https://travis-ci.org/fuwaneko/jugglingdb-rethink"><img src="https://travis-ci.org/fuwaneko/jugglingdb-rethink.svg?branch=master" alt="Build Status" /></a></td>
    </tr>
    <!-- SQLite 3 -->
    <tr>
      <td><a href="http://www.sqlite.org/"><img width="16" src="https://www.sqlmaestro.com/data/181/1249905374-32x32.gif" style="vertical-align:middle" alt="SQLite" /></a> SQLite</td>
      <td><a href="https://github.com/jugglingdb/sqlite3-adapter">jugglingdb-sqlite3</a></td>
      <td><a href="https://github.com/anatoliychakkaev">Anatoliy Chakkaev</a></td>
      <td><a href="https://circleci.com/gh/jugglingdb/sqlite3-adapter"><img src="https://circleci.com/gh/jugglingdb/sqlite3-adapter.svg?style=shield" alt="Build Status" /></a> <a href='https://coveralls.io/github/jugglingdb/sqlite3-adapter?branch=master'><img src='https://coveralls.io/repos/github/jugglingdb/sqlite3-adapter/badge.svg?branch=master' alt='Coverage Status' /></a></td>
    </tr>
    <tr>
      <td>WebService</td>
      <td>built-in</td>
      <td><a href="https://github.com/1602">Anatoliy Chakkaev</a></td>
      <td>n/a</td>
    </tr>
    <tr>
      <td>Memory (bogus)</td>
      <td>built-in</td>
      <td><a href="https://github.com/1602">Anatoliy Chakkaev</a></td>
      <td>n/a</td>
    </tr>
    <!-- DynamoDB -->
    <tr>
      <td><a href="http://en.wikipedia.org/wiki/Amazon_DynamoDB"> DynamoDB </a></td>
      <td><a href="https://github.com/tmpaul/jugglingdb-dynamodb">jugglingdb-dynamodb</a></td>
      <td><a href="https://github.com/tmpaul">tmpaul</a></td>
      <td><a href="https://travis-ci.org/tmpaul/jugglingdb-dynamodb"><img src="https://travis-ci.org/tmpaul/jugglingdb-dynamodb.svg?branch=master" alt="Build Status" /></a></td>
    </tr>
    <tr>
      <td><a href="http://www.microsoft.com/en-ca/server-cloud/products/sql-server/">SQL Server<a></td>
      <td><a href="https://github.com/Quadrus/jugglingdb-mssql">jugglingdb-mssql</a></td>
      <td><a href="https://github.com/Quadrus">Quadrus</a></td>
      <td>n/a</td>
    </tr>
    <tr>
      <td><a href="https://msdn.microsoft.com/en-us/library/azure/jj553018.aspx">Azure Table Storage<a></td>
      <td><a href="https://github.com/yads/jugglingdb-azure-tablestorage">jugglingdb-azure-tablestorage</a></td>
      <td><a href="https://github.com/yads">Vadim Kazakov</a></td>
      <td>n/a</td>
    </tr>

  </tbody>
</table>

## Participation

- Check status of project on trello board: https://trello.com/board/jugglingdb/4f0a0b1e27d3103c64288388
- Make sure all tests pass (`npm test` command)
- Feel free to vote and comment on cards (tickets/issues), if you want to join team -- send me a message with your email.

If you want to create your own jugglingdb adapter, you should publish your
adapter package with name `jugglingdb-ADAPTERNAME`. Creating adapter is simple,
check [jugglingdb/redis-adapter](https://github.com/jugglingdb/redis-adapter) for example. JugglingDB core
exports common tests each adapter should pass, you could create your adapter in
TDD style, check that adapter pass all tests defined in `test/common_test.js`.

## Usage

```javascript
var Schema = require('jugglingdb').Schema;
var schema = new Schema('redis', {port: 6379}); //port number depends on your configuration
// define models
var Post = schema.define('Post', {
    title:     { type: String, length: 255 },
    content:   { type: Schema.Text },
    date:      { type: Date,    default: function () { return new Date;} },
    timestamp: { type: Number,  default: Date.now },
    published: { type: Boolean, default: false, index: true }
});

// simplier way to describe model
var User = schema.define('User', {
    name:         String,
    bio:          Schema.Text,
    approved:     Boolean,
    joinedAt:     Date,
    age:          Number
}, {
    restPath: '/users' // tell WebService adapter which path use as API endpoint
});

var Group = schema.define('Group', {name: String});

// define any custom method
User.prototype.getNameAndAge = function () {
    return this.name + ', ' + this.age;
};

// models also accessible in schema:
schema.models.User;
schema.models.Post;
```

SEE [schema(3)](http://1602.github.io/jugglingdb/schema.3.html) for details schema usage.

```javascript
// setup relationships
User.hasMany(Post,   {as: 'posts',  foreignKey: 'userId'});
// creates instance methods:
// user.posts(conds)
// user.posts.build(data) // like new Post({userId: user.id});
// user.posts.create(data) // build and save

Post.belongsTo(User, {as: 'author', foreignKey: 'userId'});
// creates instance methods:
// post.author(callback) -- getter when called with function
// post.author() -- sync getter when called without params
// post.author(user) -- setter when called with object

User.hasAndBelongsToMany('groups');
// user.groups(callback) - get groups of user
// user.groups.create(data, callback) - create new group and connect with user
// user.groups.add(group, callback) - connect existing group with user
// user.groups.remove(group, callback) - remove connection between group and user

schema.automigrate(); // required only for mysql and postgres NOTE: it will drop User and Post tables

// work with models:
var user = new User;
user.save(function (err) {
    var post = user.posts.build({title: 'Hello world'});
    post.save(console.log);
});

// or just call it as function (with the same result):
var user = User();
user.save(...);

// Common API methods
// each method returns promise, or may accept callback as last param

// just instantiate model
new Post({ published: 0, userId: 1 });

// save model (of course async)
Post.create();

// all posts
Post.all();

// all posts by user
Post.all({ where: { userId: user.id }, order: 'id', limit: 10, skip: 20 });

// the same as prev
user.posts(cb)

// get one latest post
Post.findOne({ where: { published: true }, order: 'date DESC' });

// same as new Post({userId: user.id});
user.posts.build({ published: 1 });

// save as Post.create({userId: user.id});
user.posts.create();

// find instance by id
User.find(1);

// find instance by id and reject promise when not found
User.fetch(1)
    .then(user => console.log('found user', user))
    .catch(err => console.error('can not fetch user with id 1:', err));

// count instances
User.count([conditions])

// destroy instance
user.destroy();

// destroy all instances
User.destroyAll();

// update multiple instances (currently only on the sql adapters)
Post.bulkUpdate({ update: { published: 0 }, where: { id: [1, 2, 3] }});

// update single instance
Post.update(1, { published: 1 });
```

SEE [model(3)](http://1602.github.com/jugglingdb/model.3.html) for more information about
jugglingdb Model API. Or `man jugglingdb-model` in terminal.

```javascript

// Setup validations
User.validatesPresenceOf('name', 'email')
User.validatesLengthOf('password', {min: 5, message: {min: 'Password is too short'}});
User.validatesInclusionOf('gender', {in: ['male', 'female']});
User.validatesExclusionOf('domain', {in: ['www', 'billing', 'admin']});
User.validatesNumericalityOf('age', {int: true});
User.validatesUniquenessOf('email', {message: 'email is not unique'});

user.isValid(function (valid) {
    if (!valid) {
        user.errors // hash of errors {attr: [errmessage, errmessage, ...], attr: ...}    
    }
})

```

SEE ALSO [jugglingdb-validations(3)](http://1602.github.com/jugglingdb/validations.3.html) or
`man jugglingdb-validations` in terminal. Validation tests: ./test/validations.test.js

## Hooks

The following hooks supported:

    - afterInitialize
    - beforeCreate
    - afterCreate
    - beforeSave
    - afterSave
    - beforeUpdate
    - afterUpdate
    - beforeDestroy
    - afterDestroy
    - beforeValidate
    - afterValidate

Each callback is class method of the model, it should accept single argument: `next`, this is callback which should be called after end of the hook. Except `afterInitialize` because this method is syncronous (called after `new Model`).

During beforehooks the `next` callback accepts one argument, which is used to terminate flow. The argument passed on as the `err` parameter to the API method callback.

## Object lifecycle:

```javascript
var user = new User;
// afterInitialize
user.save(callback); // If Model.id isn't set, save will invoke Model.create() instead
// beforeValidate
// afterValidate
// beforeSave
// beforeUpdate
// afterUpdate
// afterSave
// callback
user.updateAttribute('email', 'email@example.com', callback);
// beforeValidate
// afterValidate
// beforeSave
// beforeUpdate
// afterUpdate
// afterSave
// callback
user.destroy(callback);
// beforeDestroy
// afterDestroy
// callback
User.create(data, callback);
// beforeValidate
// afterValidate
// beforeCreate
// beforeSave
// afterSave
// afterCreate
// callback
```

SEE [jugglingdb-hooks](http://1602.github.com/jugglingdb/hooks.3.html) or type this command
in your fav terminal: `man jugglingdb-hooks`. Also check tests for usage
examples: ./test/hooks.test.js

## Your own database adapter

To use custom adapter, pass it's package name as first argument to `Schema` constructor:

    var mySchema = new Schema('mycouch', {host:.., port:...});

In that case your adapter should be named as 'jugglingdb-mycouch' npm package.

## Testing [outdated]

TODO: upd this section

Core of jugglingdb tests only basic features (database-agnostic) like
validations, hooks and runs db-specific tests using memory storage. It also
exports complete bucket of tests for external running. Each adapter should run
this bucket (example from `jugglingdb-redis`):

    var jdb = require('jugglingdb'),
    Schema = jdb.Schema,
    test = jdb.test;

    var schema = new Schema(__dirname + '/..', {host: 'localhost', database: 1});

    test(module.exports, schema);

Each adapter could add specific tests to standart bucket:

    test.it('should do something special', function (test) {
        test.done();
    });

Or it could tell core to skip some test from bucket:

    test.skip('name of test case');

To run tests use this command:

    npm test

Before running make sure you've installed package (`npm install`) and if you
running some specific adapter tests, ensure you've configured database
correctly (host, port, username, password).

## Contributing

If you have found a bug please try to write unit test before reporting. Before
submit pull request make sure all tests still passed. Check
[roadmap](http://1602.github.com/jugglingdb/roadmap.3.html), github issues if you want to
help. Contribution to docs highly appreciated. Contents of man pages and
http://1602.github.com/jugglingdb/ generated from md files stored in this repo at ./docs repo

## MIT License

    Copyright (C) 2011 by Anatoliy Chakkaev <mail [??t] anatoliy [d??t] in>

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/1602/jugglingdb/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

[coveralls-url]: https://coveralls.io/github/1602/jugglingdb
[coveralls-image]: https://coveralls.io/repos/github/1602/jugglingdb/badge.svg?branch=master
[build-url]: https://circleci.com/gh/1602/jugglingdb
[build-image]: https://circleci.com/gh/1602/jugglingdb.svg?style=shield
[npm-image]: https://img.shields.io/npm/v/jugglingdb.svg
[npm-url]: https://npmjs.org/package/jugglingdb
[downloads-image]: https://img.shields.io/npm/dm/jugglingdb.svg
[downloads-url]: https://npmjs.org/package/jugglingdb
