# PostBoost::ScheduleResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **success** | **Boolean** |  |  |
| **scheduled_at** | **Time** |  | [optional] |
| **needs_approval** | **Boolean** | True when the post now waits for approval instead of being scheduled (not returned by approve). | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::ScheduleResult.new(
  success: null,
  scheduled_at: 2025-06-01T10:00:00Z,
  needs_approval: null
)
```

