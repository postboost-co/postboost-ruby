# PostBoost::CreateApiKey201ResponseData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **name** | **String** |  |  |
| **abilities** | [**Array&lt;ApiKeyAbility&gt;**](ApiKeyAbility.md) |  |  |
| **account_ids** | **Array&lt;Integer&gt;** |  | [optional] |
| **created_by** | **String** | Name of the user the key acts as. | [optional] |
| **last_used_at** | **Time** |  | [optional] |
| **expires_at** | **Date** |  | [optional] |
| **created_at** | **Time** |  | [optional] |
| **token** | **String** | The plain API key. Shown only in this response. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::CreateApiKey201ResponseData.new(
  id: null,
  name: null,
  abilities: null,
  account_ids: null,
  created_by: null,
  last_used_at: null,
  expires_at: null,
  created_at: null,
  token: null
)
```

