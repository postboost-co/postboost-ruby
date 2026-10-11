# PostBoost::MentionInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **avatar** | **String** |  | [optional] |
| **identities** | [**Array&lt;MentionIdentityInput&gt;**](MentionIdentityInput.md) |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::MentionInput.new(
  name: null,
  avatar: null,
  identities: null
)
```

