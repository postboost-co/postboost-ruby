# PostBoost::WebhookEnvelope

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **event** | **String** |  |  |
| **id** | **String** | Delivery ID, one per event. Retries and manual resends repeat it. |  |
| **occurred_at** | **Time** | When the event happened (ISO 8601, UTC). |  |
| **workspace_uuid** | **String** | The workspace the event belongs to (null only on instance-wide system webhooks). Also sent as the &#x60;X-PostBoost-Workspace&#x60; header. |  |
| **data** | **Hash&lt;String, Object&gt;** | The post (&#x60;post.*&#x60;, as &#x60;getPost&#x60; returns it, plus &#x60;account&#x60; on per-account events), the account (&#x60;account.*&#x60;) or the reply draft (&#x60;inbox.*&#x60;). |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::WebhookEnvelope.new(
  event: null,
  id: null,
  occurred_at: 2026-10-12T10:00:03+00:00,
  workspace_uuid: null,
  data: null
)
```

