# PostBoost::PostingTimes

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_data** | **Boolean** |  |  |
| **timezone** | **String** |  |  |
| **offset_hours** | **Integer** |  |  |
| **accounts** | **Integer** | Accounts that contributed scores. |  |
| **samples** | **Integer** |  |  |
| **days** | [**Array&lt;PostingTimesDaysInner&gt;**](PostingTimesDaysInner.md) | One entry per weekday (&#x60;day&#x60; 0 &#x3D; Sunday). |  |
| **day_intervals** | **Array&lt;Array&lt;PostingTimesDayIntervalsInnerInner&gt;&gt;** | Per weekday, 2-hour intervals. |  |
| **best** | [**Array&lt;PostingTimesBestInner&gt;**](PostingTimesBestInner.md) | Up to three recommended slots, at most one per weekday. |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::PostingTimes.new(
  has_data: null,
  timezone: Europe/Istanbul,
  offset_hours: null,
  accounts: null,
  samples: null,
  days: null,
  day_intervals: null,
  best: null
)
```

