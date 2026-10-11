# PostBoost::PostAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **summary** | **Hash&lt;String, Object&gt;** | Totals (views, likes, comments, shares), trends, engagement rate, breakdown, funnel and peak day across the post&#39;s accounts. Empty when nothing is published yet. |  |
| **winner** | **Object** |  | [optional] |
| **accounts** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostAnalytics.new(
  summary: null,
  winner: null,
  accounts: null
)
```

