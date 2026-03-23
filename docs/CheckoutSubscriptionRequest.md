# PostBoost::CheckoutSubscriptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **plan_id** | **Integer** |  |  |
| **cycle** | **String** |  |  |
| **coupon** | **String** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::CheckoutSubscriptionRequest.new(
  plan_id: null,
  cycle: null,
  coupon: null
)
```

