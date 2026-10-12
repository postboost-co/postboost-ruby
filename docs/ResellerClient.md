# PostBoost::ResellerClient

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** | The client workspace UUID; use it as &#x60;workspaceUuid&#x60; for the client&#39;s own endpoints. |  |
| **name** | **String** |  |  |
| **status** | **String** |  |  |
| **accounts** | **Integer** |  |  |
| **accounts_needing_reconnect** | **Integer** |  |  |
| **members** | **Integer** |  |  |
| **created_at** | **Time** |  |  |
| **archived_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ResellerClient.new(
  uuid: null,
  name: null,
  status: null,
  accounts: null,
  accounts_needing_reconnect: null,
  members: null,
  created_at: null,
  archived_at: null
)
```

