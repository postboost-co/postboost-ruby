# PostBoost::ScheduleResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  |  |
| **scheduled_at** | **String** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). | [optional] |
| **needs_approval** | **Boolean** | True when the post now waits for approval instead of being scheduled (not returned by approve). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ScheduleResult.new(
  success: null,
  scheduled_at: 2026-10-16 10:00:00,
  needs_approval: null
)
```

