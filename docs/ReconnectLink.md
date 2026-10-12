# PostBoost::ReconnectLink

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** | Single-use link to forward to the account owner. |  |
| **expires_at** | **Time** |  |  |
| **account_uuid** | **String** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ReconnectLink.new(
  url: null,
  expires_at: null,
  account_uuid: null
)
```

