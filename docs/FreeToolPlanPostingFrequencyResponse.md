# PostBoost::FreeToolPlanPostingFrequencyResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posts_per_week_capacity** | **Integer** |  | [optional] |
| **sum_of_minimums** | **Integer** | The recommended minimums of the chosen networks added up. | [optional] |
| **networks** | [**Array&lt;FreeToolPlanPostingFrequencyResponseNetworksInner&gt;**](FreeToolPlanPostingFrequencyResponseNetworksInner.md) | One row per chosen network, in a fixed network order. | [optional] |
| **slots** | [**Array&lt;FreeToolPlanPostingFrequencyResponseSlotsInner&gt;**](FreeToolPlanPostingFrequencyResponseSlotsInner.md) | The weekly grid: each network&#39;s posts spread evenly from Monday, sorted by day. | [optional] |
| **warnings** | **Array&lt;String&gt;** |  | [optional] |
| **last_verified** | **Date** | When the ranges were last checked against their sources. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPlanPostingFrequencyResponse.new(
  posts_per_week_capacity: null,
  sum_of_minimums: null,
  networks: null,
  slots: null,
  warnings: null,
  last_verified: null
)
```

