source "https://rubygems.org"

# Mirrors what GitHub Pages runs. The `jekyll-theme-minimal` theme and
# `jekyll-seo-tag` both come in via this gem, so the site carries no copy
# of the theme itself.
gem "github-pages", group: :jekyll_plugins
gem "webrick"

# Ruby 3.4+ dropped these from the default gems, but the Jekyll version
# github-pages pins still requires them. Needed for local preview only;
# GitHub Pages builds with its own older Ruby and ignores this file.
gem "base64"
gem "bigdecimal"
gem "csv"
gem "logger"

group :test do
  gem "html-proofer", "~> 5.0"
end
