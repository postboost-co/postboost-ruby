# PostBoost::ConnectLink

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Single-use link for the signed-in user who created it. Valid 15 minutes. |  |
| **expires_at** | **Time** |  |  |
| **provider** | **String** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ConnectLink.new(
  url: null,
  expires_at: null,
  provider: null
)
```

