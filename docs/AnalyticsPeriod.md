# PostBoost::AnalyticsPeriod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_date** | **Date** |  |  |
| **end_date** | **Date** |  |  |
| **previous_start_date** | **Date** | Start of the equally long range before this one, used for comparisons. |  |
| **previous_end_date** | **Date** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::AnalyticsPeriod.new(
  start_date: null,
  end_date: null,
  previous_start_date: null,
  previous_end_date: null
)
```

