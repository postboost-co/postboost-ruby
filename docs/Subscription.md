# PostBoost::Subscription

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **platform_subscription_id** | **String** |  |  |
| **platform_plan_id** | **String** |  |  |
| **status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  |  |
| **recurring** | **Boolean** |  |  |
| **trial_ends_at** | **String** | Display date in the configured timezone, &#x60;M j, Y&#x60; (not RFC 3339). | [optional] |
| **paused_from** | **String** | Display date in the configured timezone, &#x60;M j, Y&#x60; (not RFC 3339). | [optional] |
| **ends_at** | **String** | Display date in the configured timezone, &#x60;M j, Y&#x60; (not RFC 3339). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::Subscription.new(
  name: null,
  platform_subscription_id: null,
  platform_plan_id: null,
  status: null,
  recurring: null,
  trial_ends_at: Oct 30, 2026,
  paused_from: Oct 30, 2026,
  ends_at: Oct 30, 2026
)
```

