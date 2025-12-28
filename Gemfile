source "https://rubygems.org"

gem "base64", "~> 0.3.0"
gem "csv", "~> 3.3"
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
gem "jekyll", "~> 4.3.2"
gem "logger", "~> 1.7"
gem "minima", github: "jekyll/minima", ref: "bf9ef98"
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
