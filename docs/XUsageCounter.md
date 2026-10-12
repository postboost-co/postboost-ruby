# PostBoost::XUsageCounter

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **used** | **Integer** |  |  |
| **limit** | **Integer** | Monthly allowance; null &#x3D; unlimited. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::XUsageCounter.new(
  used: null,
  limit: null
)
```

