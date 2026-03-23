# PostBoost::SubscriptionInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform_subscription_id** | **String** |  |  |
| **platform_plan_id** | **String** |  |  |
| **status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  |  |
| **trial_ends_at** | **Time** | Required when status is &#x60;trialing&#x60;. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::SubscriptionInput.new(
  platform_subscription_id: null,
  platform_plan_id: null,
  status: null,
  trial_ends_at: null
)
```

