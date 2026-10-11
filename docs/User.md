# PostBoost::User

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **name** | **String** |  |  |
| **email** | **String** |  |  |
| **avatar** | **String** | URL of the user&#39;s avatar, or null when none is set. | [optional] |
| **is_admin** | **Boolean** |  |  |
| **email_verified_at** | **Time** |  | [optional] |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::User.new(
  id: null,
  name: null,
  email: null,
  avatar: null,
  is_admin: null,
  email_verified_at: null,
  created_at: null
)
```

