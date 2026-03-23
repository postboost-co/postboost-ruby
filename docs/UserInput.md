# PostBoost::UserInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **email** | **String** |  |  |
| **password** | **String** |  |  |
| **password_confirmation** | **String** |  |  |
| **is_admin** | **Boolean** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::UserInput.new(
  name: null,
  email: null,
  password: null,
  password_confirmation: null,
  is_admin: null
)
```

