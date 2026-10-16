# PostBoost::FreeToolPlanContentCalendarRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_date** | **String** | First day of the calendar (YYYY-MM-DD). Each week starts on this weekday. |  |
| **weeks** | **Integer** |  | [optional][default to 4] |
| **posts_per_week** | [**FreeToolPlanContentCalendarRequestPostsPerWeek**](FreeToolPlanContentCalendarRequestPostsPerWeek.md) |  |  |
| **times** | [**FreeToolPlanContentCalendarRequestTimes**](FreeToolPlanContentCalendarRequestTimes.md) |  | [optional] |
| **pillars** | **Array&lt;String&gt;** | Content themes, rotated over the posts in date order. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPlanContentCalendarRequest.new(
  start_date: null,
  weeks: null,
  posts_per_week: null,
  times: null,
  pillars: null
)
```

