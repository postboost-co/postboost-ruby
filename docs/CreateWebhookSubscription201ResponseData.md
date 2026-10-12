# PostBoost::CreateWebhookSubscription201ResponseData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **callback_url** | **String** |  |  |
| **events** | **Array&lt;String&gt;** |  |  |
| **active** | **Boolean** |  |  |
| **created_at** | **Time** |  | [optional] |
| **secret** | **String** | Signing secret for &#x60;X-Signature&#x60;. Returned once. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::CreateWebhookSubscription201ResponseData.new(
  uuid: null,
  name: null,
  callback_url: null,
  events: null,
  active: null,
  created_at: null,
  secret: null
)
```

