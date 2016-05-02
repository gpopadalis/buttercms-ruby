# ButterCMS API Ruby Client

## Setup

To setup your project, follow these steps:

1. Install using `gem install buttercms-ruby` or by adding to your `Gemfile`:

  ```ruby
  gem 'buttercms-ruby', '~>1.0.1'
  ```

2. Set your API token.

  ```ruby
  require 'buttercms-ruby'

  ButterCMS::api_token = "YourToken"
  ```

## Quick Start

```ruby
posts = ButterCMS::Post.all(page: 1, page_size: 10)
puts posts.first.title
puts posts.meta.next_page

post = ButterCMS::Post.find("post-slug")
puts post.title

author = ButterCMS::Author.find("author-slug")
puts author.first_name

category = ButterCMS::Category.find("category-slug")
puts category.name

rss_feed = ButterCMS::Feed.find(:rss)
puts rss_feed.data
```
