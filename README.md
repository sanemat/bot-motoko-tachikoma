bot-motoko-tachikoma
====================

Sample for tachikoma

Use tachikoma as gem
----

```
 /Gemfile
source "https://rubygems.org"
gem 'tachikoma'
```

```
 /.gitignore
/repos/*
!/repos/.gitkeep
```

```
 /Rakefile
require 'bundler/setup'
require 'tachikoma/tasks'
```

```
# Add your yaml file to data/YOUR.yaml
```

Then,

```
$ BUILD_FOR=foo \
  TOKEN_FOO=foo \
  bundle exec rake tachikoma:load tachikoma:fetch tachikoma:bundle tachikoma:pull_request
```

It works!
