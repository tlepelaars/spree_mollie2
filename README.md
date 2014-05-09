SpreeMollie
===========

Integration of [Mollie](http://mollie.nl) payment service in Spree using the official ruby gem, [mollie-api-ruby](http://https://github.com/mollie/mollie-api-ruby).

Please note that this extension overrides the default `payment` partial. Other payment methods will not be available as a result of this.

Installation
------------

Add spree_mollie to your Gemfile:

```ruby
gem 'spree_mollie', :git => 'https://github.com/javereec/spree_mollie.git', :branch => '2-2-stable'
```

Bundle your dependencies and run the installation generator:

```shell
bundle
bundle exec rails g spree_mollie:install
```

Testing
-------

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'spree_mollie/factories'
```

Copyright (c) 2014 Jan Vereecken, released under the New BSD License
