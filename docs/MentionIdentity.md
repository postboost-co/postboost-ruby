# PostBoost::MentionIdentity

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **provider** | **String** | Mention provider key (network family). |  |
| **provider_id** | **String** | The profile&#39;s network ID, when resolved. Never accepted from clients. | [optional] |
| **handle** | **String** |  |  |
| **label** | **String** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::MentionIdentity.new(
  provider: linkedin,
  provider_id: null,
  handle: janedoe,
  label: null
)
```

