# PostBoost::CompetitorInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | Your Instagram account &#x60;id&#x60; (connected through a Facebook Page) used to look the competitor up. |  |
| **username** | **String** | Instagram username, with or without &#x60;@&#x60;. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::CompetitorInput.new(
  account_id: null,
  username: natgeo
)
```

