# PostBoost::WebhookEventPayload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event** | [**WebhookEventName**](WebhookEventName.md) |  |  |
| **data** | **Hash&lt;String, Object&gt;** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::WebhookEventPayload.new(
  event: null,
  data: null
)
```

