# PostBoost::FreeToolPlanContentCalendarResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **end_date** | **String** | Last day of the calendar (YYYY-MM-DD). | [optional] |
| **total** | **Integer** | Number of posts planned. | [optional] |
| **slots** | [**Array&lt;FreeToolPlanContentCalendarResponseSlotsInner&gt;**](FreeToolPlanContentCalendarResponseSlotsInner.md) |  | [optional] |
| **csv** | **String** | The calendar as CSV (UTF-8 with BOM): Date, Day, Time, Network, Pillar, Idea. | [optional] |
| **ics** | **String** | The calendar as an iCalendar file: one 15-minute event per post, in floating local time. | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::FreeToolPlanContentCalendarResponse.new(
  end_date: null,
  total: null,
  slots: null,
  csv: null,
  ics: null
)
```

