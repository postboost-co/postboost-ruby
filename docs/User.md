# PostBoost::User

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **name** | **String** |  |  |
| **email** | **String** |  |  |
| **avatar** | **String** | URL of the user&#39;s avatar, or null when none is set. | [optional] |
| **is_admin** | **Boolean** |  |  |
| **email_verified_at** | **String** | Display string in the configured timezone and clock: &#x60;M j, H:i&#x60; this year, &#x60;M j, Y, H:i&#x60; otherwise (12-hour setting: &#x60;h:ia&#x60;), not RFC 3339. | [optional] |
| **created_at** | **String** | Display string in the configured timezone and clock: &#x60;M j, H:i&#x60; this year, &#x60;M j, Y, H:i&#x60; otherwise (12-hour setting: &#x60;h:ia&#x60;), not RFC 3339. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::User.new(
  id: null,
  name: null,
  email: null,
  avatar: null,
  is_admin: null,
  email_verified_at: Oct 16, 14:05,
  created_at: Mar 3, 2025, 09:12
)
```

