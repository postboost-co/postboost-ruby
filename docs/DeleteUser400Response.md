# PostBoost::DeleteUser400Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  | [optional] |
| **message** | **String** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::DeleteUser400Response.new(
  success: false,
  message: You cannot delete yourself.
)
```

