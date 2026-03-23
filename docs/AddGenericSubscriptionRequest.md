# PostBoost::AddGenericSubscriptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **plan_id** | **Integer** |  |  |
| **trial_days** | **Integer** |  | [optional] |
| **keep_prev_trial_ends_at** | **Boolean** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AddGenericSubscriptionRequest.new(
  plan_id: null,
  trial_days: null,
  keep_prev_trial_ends_at: null
)
```

