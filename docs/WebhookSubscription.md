# PostBoost::WebhookSubscription

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **name** | **String** |  |  |
| **callback_url** | **String** |  |  |
| **events** | **Array&lt;String&gt;** |  |  |
| **active** | **Boolean** |  |  |
| **created_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::WebhookSubscription.new(
  uuid: null,
  name: null,
  callback_url: null,
  events: null,
  active: null,
  created_at: null
)
```

