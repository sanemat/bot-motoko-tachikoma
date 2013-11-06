bot-motoko-tachikoma
====================

Sample for [tachikoma](https://rubygems.org/gems/tachikoma)

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

Important! task name does not have backword compatible!

Then, _above v4.0.0.beta_

```bash
$ BUILD_FOR=foo \
  TOKEN_FOO=foo \
  bundle exec rake tachikoma:run_bundle
```

If you use carton,

```bash
$ BUILD_FOR=cpanmetadb-perl \
TOKEN_CPANMETADB_PERL=github-access-token \
bundle exec rake tachikoma:run_carton
```

It works!

----
Below _v3.1_ (Too Old API):

```
$ BUILD_FOR=foo \
  TOKEN_FOO=foo \
  bundle exec rake tachikoma:load tachikoma:fetch tachikoma:bundle tachikoma:pull_request
```

carton feature(>= 3.0.9)

```bash
$ BUILD_FOR=cpanmetadb-perl \
TOKEN_CPANMETADB_PERL=github-access-token \
bundle exec rake tachikoma:load tachikoma:fetch tachikoma:carton tachikoma:pull_request
```
