# PostBoost::XUsage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **period_start** | **Time** |  |  |
| **period_end** | **Time** |  |  |
| **enforced** | **Boolean** | Whether an allowance applies to this workspace. |  |
| **posts** | [**XUsageCounter**](XUsageCounter.md) |  |  |
| **link_posts** | [**XUsageCounter**](XUsageCounter.md) |  |  |
| **estimated_cost_usd** | **Float** | PostBoost&#39;s estimate of what X charged for these posts. Informational; you are not billed per post. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::XUsage.new(
  period_start: null,
  period_end: null,
  enforced: null,
  posts: null,
  link_posts: null,
  estimated_cost_usd: null
)
```

