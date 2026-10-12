# PostBoost::ImageCreditBalance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **enabled** | **Boolean** | &#x60;false&#x60; when images are charged to text credits instead (the pool is switched off). |  |
| **used** | **Integer** |  |  |
| **limit** | **Integer** | Image credits this month; &#x60;null&#x60; &#x3D; no limit. |  |
| **remaining** | **Integer** |  |  |
| **period_start** | **Time** |  |  |
| **period_end** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::ImageCreditBalance.new(
  enabled: null,
  used: null,
  limit: null,
  remaining: null,
  period_start: null,
  period_end: null
)
```

