## Description
Slides for a presentation on Git and Github

## Prerequisites
- Ruby 2.0.0 or greater (host machine)
  - For Windows, use http://rubyinstaller.org (check "add Ruby executables to your PATH")
  - In cmd.exe, `ruby -v` should show the Ruby version

## Install Dependencies
```
$ gem install bundler
$ bundle install
```

## Run
```
$ bundle exec rackup
```

## Potential Problems
- If you get an error that looks like:

  ```
  ERROR:  Could not find a valid gem 'bundler' (>= 0), here is why:
            Unable to download data from https://rubygems.org/ - SSL_connect retur
  ned=1 errno=0 state=SSLv3 read server certificate B: certificate verify failed (
  https://api.rubygems.org/latest_specs.4.8.gz)
  ```

  then you'll need to configure RubyGems to use http instead of https:

  ```
  $ gem sources --add http://rubygems.org/
  $ gem sources --remove https://rubygems.org/
  ```
