# PostBoost::AnalyticsSummaryData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total_followers** | **Integer** |  | [optional] |
| **follower_growth** | **Hash&lt;String, Object&gt;** | Growth in the period with the change against the previous period. | [optional] |
| **total_posts** | **Hash&lt;String, Object&gt;** | Posts in the period with the change against the previous period. | [optional] |
| **best_account** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **needs_attention** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **audience_chart** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **leaderboard** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **most_active** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **least_active** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **follower_distribution** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **posting_streak** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::AnalyticsSummaryData.new(
  total_followers: null,
  follower_growth: null,
  total_posts: null,
  best_account: null,
  needs_attention: null,
  audience_chart: null,
  leaderboard: null,
  most_active: null,
  least_active: null,
  follower_distribution: null,
  posting_streak: null
)
```

