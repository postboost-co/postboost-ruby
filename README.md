# PostBoost Ruby SDK

Official Ruby client for the [PostBoost API](https://postboost.co/docs/api).

## Install

```bash
gem install postboost
```

| | |
|---|---|
| **RubyGems** | [rubygems.org/gems/postboost](https://rubygems.org/gems/postboost) |
| **GitHub** | [postboost-co/postboost-ruby](https://github.com/postboost-co/postboost-ruby) |
| **Docs** | [postboost.co/docs/api](https://postboost.co/docs/api) |
| **Version** | v1.0.0 |

## Quick start

```ruby
require 'postboost'

PostBoost.configure { |c| c.access_token = ENV['POSTBOOST_API_TOKEN'] }

api = PostBoost::PostsApi.new
posts = api.list_posts('YOUR_WORKSPACE_UUID')
posts.each { |p| puts p.uuid }
```

## License

MIT
