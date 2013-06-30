bot-motoko-tachikoma
====================

Sample for tachikoma

Use tachikoma as gem
----

```
 /Gemfile
source "https://rubygems.org"
gem 'tachikoma', github: 'sanemat/tachikoma'
```

```
 /.gitignore
/repos/*
!/repos/.gitkeep
```

```
 /Rakefile
require 'bundler/setup'
require 'tachikoma'
require 'tachikoma/tasks'
```

```
$ mkdir -p data
$ mkdir -p repos
$ touch repos/.gitkeep
# Add your yaml file
```

Then,

```
$ BUILD_FOR=foo \
  TOKEN_FOO=foo \
  bundle exec rake tachikoma:load tachikoma:fetch tachikoma:bundle tachikoma:pull_request
```

It works!

Configure example
----


```ruby
# /Rakefile
Tachikoma.root_path = File.expand_path(__FILE__) # reset `root_path`

namespace :tachikoma do
  @default_timestamp_format = '%Y-%m-%d-%H-%M-%S%z'
end
```
