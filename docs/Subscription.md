# PostBoost::Subscription

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **platform_subscription_id** | **String** |  |  |
| **platform_plan_id** | **String** |  |  |
| **status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  |  |
| **recurring** | **Boolean** |  |  |
| **trial_ends_at** | **Time** |  | [optional] |
| **paused_from** | **Time** |  | [optional] |
| **ends_at** | **Time** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::Subscription.new(
  name: null,
  platform_subscription_id: null,
  platform_plan_id: null,
  status: null,
  recurring: null,
  trial_ends_at: null,
  paused_from: null,
  ends_at: null
)
```

