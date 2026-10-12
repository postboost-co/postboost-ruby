# PostBoost::RecyclingRuleUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **interval_days** | **Integer** |  | [optional] |
| **max_runs** | **Integer** |  | [optional] |
| **placement** | **String** |  | [optional] |
| **account_ids** | **Array&lt;Integer&gt;** |  | [optional] |
| **start_at** | **Time** | Next run. | [optional] |
| **active** | **Boolean** |  | [optional] |

## Example

```ruby
require 'postboost'

instance = PostBoost::RecyclingRuleUpdate.new(
  interval_days: null,
  max_runs: null,
  placement: null,
  account_ids: null,
  start_at: null,
  active: null
)
```

