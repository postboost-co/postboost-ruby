# PostBoost::PostWarning

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |
| **account_id** | **Integer** | The account the warning is about; null when it is about the whole post. |  |
| **message** | **String** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostWarning.new(
  code: null,
  account_id: null,
  message: null
)
```

