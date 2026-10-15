# PostBoost::AccountConnectionHealth

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | &#x60;expired&#x60;: must be reconnected now. &#x60;expiring&#x60;: the connection hits its hard expiry within 7 days. &#x60;failing&#x60;: the latest publish attempt failed. &#x60;healthy&#x60;: none of these.  |  |
| **expiry_kind** | **String** | What limits the connection: &#x60;access&#x60; (the access token), &#x60;refresh&#x60; (the refresh token), &#x60;expired&#x60;, &#x60;unknown&#x60; (refreshed automatically, no known hard limit) or &#x60;none&#x60; (the network&#39;s connections do not expire on a schedule).  |  |
| **expires_at** | **Time** | When the connection stops working unless reconnected; null without a hard expiry. |  |
| **days_left** | **Integer** | Whole days until &#x60;expires_at&#x60; (0 &#x3D; less than a day). |  |
| **refreshable** | **Boolean** | PostBoost refreshes the token automatically until the hard expiry. |  |
| **note** | **String** | Plain-language explanation of the prediction. |  |
| **reconnect_reason** | [**AccountConnectionHealthReconnectReason**](AccountConnectionHealthReconnectReason.md) |  |  |
| **last_success_at** | **Time** | When the account last published successfully. |  |
| **last_error** | **String** | The error of the account&#39;s latest failed publish, shortened to 300 characters. |  |
| **reconnect_url** | **String** | Where a workspace member reconnects the account. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AccountConnectionHealth.new(
  status: null,
  expiry_kind: null,
  expires_at: null,
  days_left: null,
  refreshable: null,
  note: null,
  reconnect_reason: null,
  last_success_at: null,
  last_error: null,
  reconnect_url: null
)
```

