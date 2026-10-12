# PostBoost::AccountHealth

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **provider** | **String** |  |  |
| **authorized** | **Boolean** | False when the account must be reconnected. |  |
| **has_token** | **Boolean** | Whether an access token is stored for the account. |  |
| **healthy** | **Boolean** | &#x60;authorized&#x60; and &#x60;has_token&#x60;: the account can publish. |  |
| **daily_cap** | [**AccountHealthDailyCap**](AccountHealthDailyCap.md) |  |  |
| **connection** | [**AccountConnectionHealth**](AccountConnectionHealth.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AccountHealth.new(
  id: null,
  uuid: null,
  name: null,
  provider: null,
  authorized: null,
  has_token: null,
  healthy: null,
  daily_cap: null,
  connection: null
)
```

