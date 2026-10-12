# PostBoost::ApiKeyInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **abilities** | [**Array&lt;ApiKeyAbility&gt;**](ApiKeyAbility.md) |  |  |
| **account_ids** | **Array&lt;Integer&gt;** | Limit the key to these account ids of the workspace. Omit or null for every account. A limited key must send &#x60;account_ids&#x60; on recycling rules, report exports and AI drafts, and its lists show only its accounts. | [optional] |
| **expires_at** | **Date** | Last day the key works. Must be after today. Omit for no expiry. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ApiKeyInput.new(
  name: null,
  abilities: null,
  account_ids: null,
  expires_at: null
)
```

