bot-motoko-tachikoma
====================

Sample for tachikoma

Use tachikoma as gem
----

```
 /Gemfile
source 'https://rubygems.org'
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

### Example for carton

Tachikoma gets ability for carton on v3.0.9.

```bash
$ BUILD_FOR=cpanmetadb-perl \
TOKEN_CPANMETADB_PERL=github-access-token \
bundle exec rake tachikoma:load tachikoma:fetch tachikoma:carton tachikoma:pull_request
```
