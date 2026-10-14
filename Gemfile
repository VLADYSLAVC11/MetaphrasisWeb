# For a local preview only. GitHub Pages builds the site itself and ignores
# this file:
#   bundle install
#   bundle exec jekyll serve      # http://localhost:4000/MetaphrasisWeb/
#
# The Jekyll and markdown parser GitHub Pages runs (github-pages 232). Not the
# github-pages gem itself: its commonmarker dependency refuses Ruby 4, and the
# site uses none of the extra plugins it brings.
source "https://rubygems.org"

gem "jekyll", "~> 3.10.0"
gem "kramdown-parser-gfm", "~> 1.1"

# Standard libraries Ruby 3.4+ no longer ships by default, which this Jekyll
# still loads. Harmless on an older Ruby.
gem "base64"
gem "bigdecimal"
gem "csv"
gem "logger"
gem "ostruct"
gem "webrick"
