# PostBoost::AccountConnectionHealthReconnectReason

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** |  |  |
| **message** | **String** | The reason in plain language. |  |
| **found_at** | **Time** | When the check first found the token dead. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AccountConnectionHealthReconnectReason.new(
  code: linkedin_revoked,
  message: null,
  found_at: null
)
```

