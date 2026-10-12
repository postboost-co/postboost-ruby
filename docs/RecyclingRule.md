# PostBoost::RecyclingRule

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **uuid** | **String** |  |  |
| **type** | **String** |  |  |
| **post_uuid** | **String** |  |  |
| **tag_uuid** | **String** |  |  |
| **account_ids** | **Array&lt;Integer&gt;** |  |  |
| **interval_days** | **Integer** |  |  |
| **max_runs** | **Integer** |  |  |
| **runs_done** | **Integer** | Copies created so far. |  |
| **placement** | **String** |  |  |
| **active** | **Boolean** |  |  |
| **next_run_at** | **Time** |  |  |
| **last_run_at** | **Time** |  |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'postboost'

instance = PostBoost::RecyclingRule.new(
  uuid: null,
  type: null,
  post_uuid: null,
  tag_uuid: null,
  account_ids: null,
  interval_days: null,
  max_runs: null,
  runs_done: null,
  placement: null,
  active: null,
  next_run_at: null,
  last_run_at: null,
  created_at: null
)
```

