# PostBoost::FreeToolPlanPostingFrequencyRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **networks** | **Array&lt;String&gt;** | The networks you post on. Bluesky and Mastodon are not offered: no published frequency we could verify. |  |
| **posts_per_week_capacity** | **Integer** | How many posts your team can make in a week, across all networks. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPlanPostingFrequencyRequest.new(
  networks: null,
  posts_per_week_capacity: null
)
```

