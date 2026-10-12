# PostBoost::WebhookSubscriptionInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **callback_url** | **String** | Public &#x60;https://&#x60; URL that receives the deliveries. |  |
| **events** | [**Array&lt;WebhookEventName&gt;**](WebhookEventName.md) |  |  |
| **name** | **String** | Label shown in Settings → Webhooks. Defaults to \&quot;&lt;Source&gt; trigger\&quot;. | [optional] |
| **source** | **String** | The tool creating the subscription. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::WebhookSubscriptionInput.new(
  callback_url: null,
  events: null,
  name: null,
  source: null
)
```

