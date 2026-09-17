source "https://rubygems.org"

# GitHub Pages builds this site using the `github-pages` gem, which pins
# Jekyll and every plugin to the exact versions GitHub's build servers run.
# Building locally against this same gem keeps `bundle exec jekyll serve`
# honest about what will actually happen on Pages.
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
  gem "jekyll-include-cache"
end

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data
# gem and associated library.
install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", install_if: Gem.win_platform?
