# PostBoost::RecommendedPostingTimes

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_data** | **Boolean** |  |  |
| **timezone** | **String** |  | [optional] |
| **slots_per_day** | **Integer** |  |  |
| **samples** | **Integer** | Number of past posts the recommendation is based on. |  |
| **times** | **Array&lt;Hash&lt;String, Object&gt;&gt;** | Recommended times per weekday. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::RecommendedPostingTimes.new(
  has_data: null,
  timezone: null,
  slots_per_day: null,
  samples: null,
  times: null
)
```

