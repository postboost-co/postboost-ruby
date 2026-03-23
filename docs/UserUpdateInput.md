# PostBoost::UserUpdateInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **email** | **String** |  |  |
| **password** | **String** | Omit or set to null to keep the current password. | [optional] |
| **password_confirmation** | **String** |  | [optional] |
| **is_admin** | **Boolean** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::UserUpdateInput.new(
  name: null,
  email: null,
  password: null,
  password_confirmation: null,
  is_admin: null
)
```

