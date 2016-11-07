## CatFacts API

Welcome to the CatFacts API.  The world's premier API for finding facts about cats!

Sadly this API is not secure yet.  

### Details

All requests should include the following query parameters:

* `t` - the timestamp as an Unix Timestamp Integer
* `client` - the public key
* `token` - SHA256 hash of the user's secret key and the timestamp they generated the request

Any timestamp older than 2 minutes should be refused.

### Client Details

Let's say your boss told you there's a client with these details:

* **Public Key:** `charlie_kelly`
* **Secret Key:** `k1tten_m1tt3ns`


### To run the app

```
bundle exec rake db:create:all
bundle exec rake db:migrate
bundle exec rake db:seed
```

### To run the tests

```
bundle exec rake db:migrate RAILS_ENV=test
bundle exec rake:test
```
To run a specific test file:
```
ruby -Itest test/controllers/api/v1/facts_controller_test.rb
```

replacing the path as necessary
