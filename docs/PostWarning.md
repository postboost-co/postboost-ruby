# PostBoost::PostWarning

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | One of the codes above. The list grows over time (&#x60;x-extensible-enum&#x60;), so accept unknown values. |  |
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

