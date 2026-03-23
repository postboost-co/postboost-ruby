# PostBoost::SubscriptionUpdateInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **platform_plan_id** | **String** |  |  |
| **status** | [**SubscriptionStatus**](SubscriptionStatus.md) |  |  |
| **trial_ends_at** | **Time** | Required when status is &#x60;trialing&#x60;. | [optional] |
| **paused_from** | **Time** | Required when status is &#x60;paused&#x60;. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::SubscriptionUpdateInput.new(
  platform_plan_id: null,
  status: null,
  trial_ends_at: null,
  paused_from: null
)
```

