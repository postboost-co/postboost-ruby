# PostBoost::PostingScheduleDay

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | Weekday, 1 (Monday) to 6 (Saturday), 0 (Sunday). |  |
| **status** | **Boolean** | Whether the queue posts on this day. |  |
| **times** | [**Array&lt;PostingScheduleDayTimesInner&gt;**](PostingScheduleDayTimesInner.md) |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostingScheduleDay.new(
  id: null,
  status: null,
  times: null
)
```

