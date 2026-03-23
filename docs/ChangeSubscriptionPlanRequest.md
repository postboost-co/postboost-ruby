# PostBoost::ChangeSubscriptionPlanRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **plan_id** | **Integer** |  |  |
| **cycle** | **String** |  |  |
| **prorate** | **Boolean** |  |  |
| **billing_immediately** | **Boolean** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ChangeSubscriptionPlanRequest.new(
  plan_id: null,
  cycle: null,
  prorate: null,
  billing_immediately: null
)
```

