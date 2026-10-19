# PostBoost::FreeToolSummarizeReportResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **posts** | **Integer** |  | [optional] |
| **date_range** | [**FreeToolSummarizeReportResponseDateRange**](FreeToolSummarizeReportResponseDateRange.md) |  | [optional] |
| **views** | **Integer** |  | [optional] |
| **engagements** | **Integer** |  | [optional] |
| **engagement_rate** | **Float** | Percent, 2 decimals; null without views. | [optional] |
| **engagements_from** | **Array&lt;String&gt;** | The counts added up as engagements. | [optional] |
| **networks** | [**Array&lt;FreeToolSummarizeReportResponseNetworksInner&gt;**](FreeToolSummarizeReportResponseNetworksInner.md) |  | [optional] |
| **top_posts** | [**Array&lt;FreeToolSummarizeReportResponseTopPostsInner&gt;**](FreeToolSummarizeReportResponseTopPostsInner.md) |  | [optional] |
| **weekdays** | [**Array&lt;FreeToolSummarizeReportResponseWeekdaysInner&gt;**](FreeToolSummarizeReportResponseWeekdaysInner.md) |  | [optional] |
| **best_weekday** | **String** | The weekday with the highest average engagements per post. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolSummarizeReportResponse.new(
  posts: null,
  date_range: null,
  views: null,
  engagements: null,
  engagement_rate: null,
  engagements_from: null,
  networks: null,
  top_posts: null,
  weekdays: null,
  best_weekday: null
)
```

